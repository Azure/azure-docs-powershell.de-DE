---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientPackage.md
ms.openlocfilehash: 1a75338b7c2b83f505c82ebc714ea583b3162eb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663467"
---
# Get-AzureRmVpnClientPackage

## Synopsis
Ruft Informationen zu einem VPN-Clientpaket ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmVpnClientPackage** " Ruft Informationen zu den VPN-Client Paketen ab, die von einem virtuellen Netzwerkgateway zur Verfügung stehen.
Clientpakete enthalten Konfigurationsdaten, die es einem Clientcomputer ermöglichen, eine VPN-Verbindung mit einem virtuellen Azure-Netzwerk herzustellen. auf Clientcomputern muss das richtige Konfigurationspaket installiert sein, um eine VPN-Verbindung herzustellen.
Unterschiedliche Konfigurationspakete sind basierend auf der Windows-Version des Clientcomputers (beispielsweise Windows 7 oder Windows 10) und auf der Prozessorarchitektur des Clientcomputers verfügbar (amd64 oder x86).
Sie müssen den Architekturtyp angeben, wenn Sie **Get-AzureRmVpnClientPackage** ausführen.

## Beispiele

### Beispiel 1: Abrufen von Informationen zu einem VPN-Clientpaket für die Prozessorarchitektur
```
PS C:\>Get-AzureRmVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

Dieser Befehl ruft Informationen zu den amd64-VPN-Client Paketen ab, die auf dem virtuellen Netzwerkgateway mit dem Namen ContosoVirtualNetworkGateway gespeichert sind.
Wenn Sie Informationen zu den x86-Client Paketen erhalten möchten, setzen Sie den Wert des *ProcessorArchitecture* -Parameters auf x86.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProcessorArchitecture
Gibt den Typ der CPU-Architektur an, für die das Clientpaket vorgesehen ist.
Gültige Werte sind amd64 und x86.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Amd64, X86

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, der das virtuelle Netzwerkgateway zugewiesen ist.

Ressourcengruppen kategorisieren Elemente, um die Bestandsverwaltung und die allgemeine Azure-Verwaltung zu vereinfachen.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualNetworkGatewayName
Gibt den Namen des virtuellen Netzwerkgateways an, in dem die Clientpaket Informationen gespeichert sind.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Zeichenfolge
Der Parameter "ResourceGroupName" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.

### Zeichenfolge
Der Parameter "VirtualNetworkGatewayName" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.

## Ausgaben

###  
**Get-AzureRmVpnClientPackage** gibt Instanzen des System. String-Objekts zurück.

## Notizen

## Verwandte Links

[Größe ändern – AzureRmVirtualNetworkGateway](./Resize-AzureRmVirtualNetworkGateway.md)

[Satz-AzureRmVirtualNetworkGatewayVpnClientConfig](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


