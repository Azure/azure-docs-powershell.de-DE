---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: 8171a87ea744eb708e65c71a1d25b13190b6f0fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665361"
---
# Get-AzureRmVpnClientRevokedCertificate

## Synopsis
Ruft Informationen zu VPN-Client Sperrungs Zertifikaten ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmVpnClientRevokedCertificate** " gibt Informationen zu den Client Sperr Zertifikaten zurück, die einem virtuellen Netzwerkgateway zugewiesen sind.
Client Sperr Zertifikate verhindern, dass Clientcomputer das angegebene Zertifikat für die Authentifizierung verwenden.
Mit **Get-AzureRmVpnClientRevokedCertificate** können Sie Informationen zu allen Client Sperr Zertifikaten auf dem Gateway zurückgeben oder mithilfe des *VpnClientRevokedCertificateName* -Parameters Informationen zu einem einzelnen Zertifikat abrufen.

## Beispiele

### Beispiel 1: Abrufen von Informationen zu allen Client Sperr Zertifikaten
```
PS C:\>Get-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

Dieser Befehl ruft Informationen zu allen Client Sperr Zertifikaten ab, die dem virtuellen Netzwerkgateway mit dem Namen ContosoVirtualNetworkGateway zugeordnet sind.

### Beispiel 2: Abrufen von Informationen zu bestimmten Client Sperr Zertifikaten
```
PS C:\>Get-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

Dieser Befehl ist eine Variation des Befehls, der in Beispiel 1 gezeigt wird.
In diesem Fall wird jedoch der *VpnClientRevokedCertificateName* -Parameter verwendet, um die zurückgegebenen Daten auf ein bestimmtes vom Client gesperrtes Zertifikat zu begrenzen: das Zertifikat mit dem Namen ContosoRevokedClientCertificate.

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

### -VirtualNetworkGatewayName
Gibt den Namen des virtuellen Netzwerkgateways an, in dem die gesperrten Zertifikatinformationen zugewiesen sind.

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
Gibt den Namen des VPN-Clientzertifikats an, das dieses Cmdlet erhält.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
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

###  
**Get-AzureRmVpnClientRevokedCertificate** gibt Instanzen des **Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate** -Objekts zurück.

## Notizen

## Verwandte Links

[Add-AzureRmVpnClientRevokedCertificate](./Add-AzureRmVpnClientRevokedCertificate.md)

[Neu – AzureRmVpnClientRevokedCertificate](./New-AzureRmVpnClientRevokedCertificate.md)

[Remove-AzureRmVpnClientRevokedCertificate](./Remove-AzureRmVpnClientRevokedCertificate.md)


