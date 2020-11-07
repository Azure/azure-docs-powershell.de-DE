---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: c73f65866b2a23527540319744854e50f6639268
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663897"
---
# Add-AzureRmVpnClientRevokedCertificate

## Synopsis
Fügt ein VPN-Client Sperrungs Zertifikat hinzu.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Add-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Add-AzureRmVpnClientRevokedCertificate** weist einem virtuellen Netzwerkgateway ein Client Sperr Zertifikat zu.
Client Sperr Zertifikate verhindern, dass Clientcomputer das angegebene Zertifikat für die Authentifizierung verwenden.
Sie müssen sowohl den Zertifikatnamen als auch den Fingerabdruck des Zertifikats angeben, um dieses Cmdlet verwenden zu können.

## Beispiele

### Beispiel 1: Hinzufügen eines neuen Client Sperr Zertifikats zu einem virtuellen Netzwerkgateway
```
PS C:\>Add-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

Mit diesem Befehl wird dem virtuellen Netzwerkgateway mit dem Namen ContosoVirtualNetwork ein neues Client Sperr Zertifikat hinzugefügt.
Um das Zertifikat hinzuzufügen, müssen Sie sowohl den Zertifikatnamen als auch den Fingerabdruck des Zertifikats angeben.

## Parameter

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, der das virtuelle Netzwerkgateway zugewiesen ist.

Ressourcengruppen kategorisieren Elemente, um die Bestandsverwaltung und die allgemeine Azure-Verwaltung zu vereinfachen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Fingerabdruck
Gibt den eindeutigen Bezeichner des hinzuzufügenden Zertifikats an.
Zum Beispiel:

-Daumenabdruck "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"

Sie können Fingerabdruckinformationen für Ihre Zertifikate abrufen, indem Sie einen Windows PowerShell-Befehl wie den folgenden verwenden: `Get-ChildItem -Path Cert:\LocalMachine\Root`

Der vorhergehende Befehl ruft Informationen für alle lokalen Computerzertifikate ab, die im Stammzertifikatspeicher gefunden wurden.

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

### -VirtualNetworkGatewayName
Gibt den Namen des virtuellen Netzwerkgateways an, in dem das Zertifikat hinzugefügt werden soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VpnClientRevokedCertificateName
Gibt den Namen des VPN-Clientzertifikats an, das hinzugefügt werden soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate

## Notizen

## Verwandte Links

[Get-AzureRmVpnClientRevokedCertificate](./Get-AzureRmVpnClientRevokedCertificate.md)

[Neu – AzureRmVpnClientRevokedCertificate](./New-AzureRmVpnClientRevokedCertificate.md)

[Remove-AzureRmVpnClientRevokedCertificate](./Remove-AzureRmVpnClientRevokedCertificate.md)


