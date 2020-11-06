---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C868DFA4-8A9D-4108-B88B-ACD7F100A63C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteConfig.md
ms.openlocfilehash: ecd5df4728e963e8bcf4614a6acb554fdbf17788
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499793"
---
# Add-AzureRmRouteConfig

## Synopsis
Fügt eine Route zu einer Routentabelle hinzu.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Add-AzureRmRouteConfig -RouteTable <PSRouteTable> [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Add-AzureRmRouteConfig** wird eine Route zu einer Azure Route-Tabelle hinzugefügt.

## Beispiele

### Beispiel 1: Hinzufügen einer Route zu einer Routentabelle
```
PS C:\>$RouteTable = Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
PS C:\> Add-AzureRmRouteConfig -Name "Route13" -AddressPrefix 10.3.0.0/16 -NextHopType "VnetLocal" -RouteTable $RouteTable
```

Der erste Befehl ruft mithilfe des Get-AzureRmRouteTable-Cmdlets eine Routingtabelle mit dem Namen RouteTable01 ab.
Der Befehl speichert die Tabelle in der $RouteTable-Variablen.

Mit dem zweiten Befehl wird eine Route mit dem Namen Route13 zu der in $RouteTable gespeicherten Routentabelle hinzugefügt.
Diese Route leitet Pakete an das lokale virtuelle Netzwerk weiter.

### Beispiel 2: Hinzufügen einer Route zu einer Routentabelle mithilfe der Pipeline
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzureRmRouteConfig -Name "Route02" -AddressPrefix 10.2.0.0/16 -NextHopType VnetLocal | Set-AzureRmRouteTable
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable01
Etag              : W/"f13e1bc8-d41f-44d0-882d-b8b5a1134f59"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route02",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route02",
                        "AddressPrefix": "10.2.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route13",
                        "Etag": null, 
                        "Id": null, 
                        "AddressPrefix": "10.3.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": null
                      }
                    ] 
Subnets           : []
```

Dieser Befehl ruft die Routingtabelle mit dem Namen RouteTable01 mithilfe von **Get-AzureRmRouteTable**.
Der Befehl übergibt diese Tabelle mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Das aktuelle Cmdlet fügt die Route mit dem Namen "Route02" hinzu und übergibt dann das Ergebnis an das Cmdlet "AzureRmRouteTable", das die Tabelle so aktualisiert, dass die Änderungen wieder **gegeben** werden.

## Parameter

### -AddressPrefix
Gibt das Ziel im CIDR-Format (klassenlos InterDomain Routing) an, auf das die Route angewendet wird.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Name
Gibt den Namen der Route an, die der Route-Tabelle hinzugefügt werden soll.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NextHopIpAddress
Gibt die IP-Adresse einer virtuellen Appliance an, die Sie Ihrem virtuellen Azure-Netzwerk hinzufügen.
Diese Route leitet Pakete an diese Adresse weiter.
Geben Sie diesen Parameter nur an, wenn Sie einen Wert von VirtualAppliance für den *NextHopType* -Parameter angeben.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NextHopType
Gibt an, wie Pakete von dieser Route weitergeleitet werden.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Internet.
Das standardmäßige Internet Gateway, das von Azure bereitgestellt wird. 
- Keine.
Wenn Sie diesen Wert angeben, leitet die Route keine Pakete weiter. 
- VirtualAppliance.
Eine virtuelle Appliance, die Sie Ihrem virtuellen Azure-Netzwerk hinzufügen. 
- VirtualNetworkGateway.
Ein Azure Server-zu-Server-virtuelles privates Netzwerkgateway. 
- VnetLocal.
Lokales virtuelles Netzwerk.
Wenn Sie über zwei Subnetze (10.1.0.0/16 und 10.2.0.0/16) im gleichen virtuellen Netzwerk verfügen, wählen Sie den Wert VnetLocal für jedes Subnetz aus, um es an das andere Subnetz weiterzuleiten.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Routel
Gibt die Routingtabelle an, der das Cmdlet eine Route hinzufügt.

```yaml
Type: PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### PSRouteTable
Der Parameter "routeable" akzeptiert den Wert vom Typ "PSRouteTable" aus der Pipeline.

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSRouteTable

## Notizen

## Verwandte Links

[Get-AzureRmRouteConfig](./Get-AzureRmRouteConfig.md)

[Get-AzureRmRouteTable](./Get-AzureRmRouteTable.md)

[Neu – AzureRmRouteConfig](./New-AzureRmRouteConfig.md)

[Remove-AzureRmRouteConfig](./Remove-AzureRmRouteConfig.md)

[Satz-AzureRmRouteConfig](./Set-AzureRmRouteConfig.md)

[Satz-AzureRmRouteTable](./Set-AzureRmRouteTable.md)


