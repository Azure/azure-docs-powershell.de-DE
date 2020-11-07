---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientPackage.md
ms.openlocfilehash: d08f91029940d60440d50be406dbdfe3652934a7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841475"
---
# Get-AzVpnClientPackage

## Synopsis
Ruft Informationen zu einem VPN-Clientpaket ab.

## Syntax

```
Get-AzVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzVpnClientPackage** " Ruft Informationen zu den VPN-Client Paketen ab, die von einem virtuellen Netzwerkgateway zur Verfügung stehen.
Clientpakete enthalten Konfigurationsdaten, die es einem Clientcomputer ermöglichen, eine VPN-Verbindung mit einem virtuellen Azure-Netzwerk herzustellen. auf Clientcomputern muss das richtige Konfigurationspaket installiert sein, um eine VPN-Verbindung herzustellen.
Unterschiedliche Konfigurationspakete sind basierend auf der Windows-Version des Clientcomputers (beispielsweise Windows 7 oder Windows 10) und auf der Prozessorarchitektur des Clientcomputers verfügbar (amd64 oder x86).
Sie müssen den Architekturtyp angeben, wenn Sie **Get-AzVpnClientPackage** ausführen.

## Beispiele

### Beispiel 1: Abrufen von Informationen zu einem VPN-Clientpaket für die Prozessorarchitektur
```
PS C:\>Get-AzVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Zeichenfolge
Der Parameter "ResourceGroupName" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.

### Zeichenfolge
Der Parameter "VirtualNetworkGatewayName" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.

## Ausgaben

###  
**Get-AzVpnClientPackage** gibt Instanzen des System. String-Objekts zurück.

## Notizen

## Verwandte Links

[Größe ändern – AzVirtualNetworkGateway](./Resize-AzVirtualNetworkGateway.md)

[Satz-AzVirtualNetworkGatewayVpnClientConfig](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)


