---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 31d9c5d5c627f4d3451c47584b09760655e77342
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306056"
---
# New-AzApplicationGatewaySslCertificate

## SYNOPSIS
Erstellt ein SSL-Zertifikat für ein Azure-Anwendungsgateway.

## SYNTAX

```
New-AzApplicationGatewaySslCertificate -Name <String> [-CertificateFile <String>] [-Password <SecureString>]
 [-KeyVaultSecretId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "New-AzApplicationGatewaySslCertificate"** erstellt ein SSL-Zertifikat für ein Azure-Anwendungsgateway.

## BEISPIELE

### Beispiel 1: Erstellen eines SSL-Zertifikats für ein Azure-Anwendungsgateway.
```
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

Dieser Befehl erstellt ein #A0 namens Cert01 für das Standardanwendungsgateway und speichert das Ergebnis in der Variablen namens $Cert.

### Beispiel 2: Erstellen sie ein SSL-Zertifikat mit dem geheimen Schlüsselvault Secret (version-less secretId), und fügen Sie es einem Anwendungsgateway hinzu.
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

Machen Sie sich das Geheimnis, und erstellen Sie ein SSL-Zertifikat mithilfe `New-AzApplicationGatewaySslCertificate` von .
Hinweis: Da hier die Datei "Version-less secretId" bereitgestellt wird, synchronisiert das Anwendungsgateway das Zertifikat in regelmäßigen Abständen mit KeyVault.

### Beispiel 3: Erstellen Sie ein SSL-Zertifikat, indem Sie den geheimen Schlüssel "KeyVault Secret" verwenden, und fügen Sie es einem Anwendungsgateway hinzu.
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

Machen Sie sich das Geheimnis, und erstellen Sie ein SSL-Zertifikat mithilfe `New-AzApplicationGatewaySslCertificate` von .
Hinweis: Wenn anwendungsgateway das Zertifikat mit KeyVault synchronisiert, geben Sie die version-less secretId an.

## PARAMETERS

### -CertificateFile
Gibt den Pfad der Datei "PFX" des von diesem Cmdlet erstellten SSL-Zertifikats an.

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
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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
SecretId (URI) des geheimen Schlüsselvaultschlüssels. Verwenden Sie diese Option, wenn eine bestimmte Version des geheimen Schlüssels verwendet werden muss.

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
Gibt den Namen des von diesem Cmdlet erstellten SSL-Zertifikats an.

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

### -Password
Gibt das Kennwort für ssl an, das von diesem Cmdlet erstellt wird.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Add-AzApplicationGatewaySslCertificate](./Add-AzApplicationGatewaySslCertificate.md)

[Get-AzApplicationGatewaySslCertificate](./Get-AzApplicationGatewaySslCertificate.md)

[Remove-AzApplicationGatewaySslCertificate](./Remove-AzApplicationGatewaySslCertificate.md)

[Set-AzApplicationGatewaySslCertificate](./Set-AzApplicationGatewaySslCertificate.md)


