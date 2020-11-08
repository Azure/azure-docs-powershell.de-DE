---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 47c2f4dcb3e18c969c57d037d9e4f0104b1980f3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177255"
---
# Add-AzApplicationGatewaySslCertificate

## Synopsis
Fügt ein SSL-Zertifikat zu einem Anwendungsgateway hinzu.

## Syntax

```
Add-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Add-AzApplicationGatewaySslCertificate** wird ein SSL-Zertifikat zu einem Anwendungsgateway hinzugefügt.

## Beispiele

### Beispiel 1: Hinzufügen eines SSL-Zertifikats mit PFX zu einem Anwendungsgateway
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

Dieser Befehl ruft ein Anwendungsgateway mit dem Namen ApplicationGateway01 ab und fügt dann ein SSL-Zertifikat mit dem Namen Cert01 hinzu.

### Beispiel 2: Fügen Sie ein SSL-Zertifikat unter Verwendung von keyvault Secret (Version-less Secret-Code) zu einem Anwendungsgateway hinzu.
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultCertificate -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.SecretId.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

Rufen Sie das Geheimnis ab, und verweisen Sie es in der `Add-AzApplicationGatewaySslCertificate` , um es dem Anwendungs Gateway mit dem Namen hinzuzufügen `Cert01` .
Hinweis: Da Version-less-geheim-Nr hier bereitgestellt wird, synchronisiert Application Gateway das Zertifikat in regelmäßigen Abständen mit dem keyvault.

### Beispiel 3: Hinzufügen eines SSL-Zertifikats unter Verwendung von keyvault Secret (Versionsverwaltung) zu einem Anwendungsgateway
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultCertificate -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

Rufen Sie das Geheimnis ab, und verweisen Sie es in der `Add-AzApplicationGatewaySslCertificate` , um es dem Anwendungs Gateway mit dem Namen hinzuzufügen `Cert01` .
Hinweis: Wenn es erforderlich ist, dass Application Gateway das Zertifikat mit dem keyvault synchronisiert, geben Sie bitte den versionslosen Geheimdienst an.

## Parameter

### -ApplicationGateway
Gibt den Namen des Anwendungs Gateways an, dem dieses Cmdlet ein SSL-Zertifikat hinzufügt.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Certificatedatei
Gibt die PFX-Datei eines SSL-Zertifikats an, das von diesem Cmdlet hinzugefügt wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVaultSecretId
Geheim-URL (URI) des keyvault-Geheimnisses. Verwenden Sie diese Option, wenn eine bestimmte Version von Secret verwendet werden muss.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen des SSL-Zertifikats an, das von diesem Cmdlet hinzugefügt wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kennwort
Gibt das Kennwort des SSL-Zertifikats an, das von diesem Cmdlet hinzugefügt wird.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. Network. Models. PSApplicationGateway

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSApplicationGateway

## Notizen

## Verwandte Links

[Get-AzApplicationGatewaySslCertificate](./Get-AzApplicationGatewaySslCertificate.md)

[Neu – AzApplicationGatewaySslCertificate](./New-AzApplicationGatewaySslCertificate.md)

[Remove-AzApplicationGatewaySslCertificate](./Remove-AzApplicationGatewaySslCertificate.md)

[Satz-AzApplicationGatewaySslCertificate](./Set-AzApplicationGatewaySslCertificate.md)


