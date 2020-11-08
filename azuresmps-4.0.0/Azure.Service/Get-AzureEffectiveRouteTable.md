---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 82CF6E71-FFE2-4B2C-8AAD-04C137AD5706
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49f9cce74cb2621d6c9ff51485b7c4bce4a302bf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006559"
---
# Get-AzureEffectiveRouteTable

## Synopsis
Ruft die Route ab, die auf einem virtuellen Computer angewendet wurde.

## Syntax

### IaaSGetEffectiveRouteTableParamSet
```
Get-AzureEffectiveRouteTable -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### SlotGetEffectiveRouteTableParamSet
```
Get-AzureEffectiveRouteTable -ServiceName <String> [-Slot <String>] -RoleInstanceName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureEffectiveRouteTable** " Ruft die Route ab, die auf einem virtuellen Computer angewendet wurde.
Dieser Vorgang kann einige Sekunden dauern.

## Beispiele

### Beispiel 1: Abrufen der effektiven Route, auf die ein virtueller Computer angewendet wurde
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureEffectiveRouteTable
```

Dieser Befehl ruft einen virtuellen Computer mit dem Namen ContosoVM06 für den Dienst mit dem Namen ContosoService ab und übergibt das Objekt des virtuellen Computers an das aktuelle Cmdlet.
Das aktuelle Cmdlet ruft die Route ab, die auf diesen virtuellen Computer angewendet wurde.

## Parameter

### -NetworkInterfaceName
Gibt den Namen des Netzwerkadapters an, für den dieses Cmdlet effektive Routen erhält.

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

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest. Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleInstanceName
Gibt den Namen einer PaaS-Rolle an, für die dieses Cmdlet effektive Routen erhält.

```yaml
Type: String
Parameter Sets: SlotGetEffectiveRouteTableParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
Gibt den Namen eines Cloud-Diensts an.
Die PaaS-Rolle, für die dieses Cmdlet effektive Routen erhält, gehört zu dem Dienst, den dieser Parameter angibt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Slot
Gibt einen PaaS-Steckplatz an.
Die PaaS-Rolle, für die dieses Cmdlet effektive Routen erhält, weist den Slot auf, den dieser Parameter angibt.
Gültige Werte sind: 

- Produktions
- Inszenierung 

Der Standardwert ist Production.

```yaml
Type: String
Parameter Sets: SlotGetEffectiveRouteTableParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Gibt das Objekt des virtuellen Computers an, für das dieses Cmdlet effektive Routen erhält.

```yaml
Type: PersistentVMRoleContext
Parameter Sets: IaaSGetEffectiveRouteTableParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### System. Collections. Generic. IEnumerable<Microsoft. WindowsAzure. Management. Network. Models. EffectiveRouteTable, Microsoft. WindowsAzure. Management. Network>

## Notizen

## Verwandte Links

[Get-AzureRouteTable](./Get-AzureRouteTable.md)

[Neu – AzureRouteTable](./New-AzureRouteTable.md)

[Remove-AzureRouteTable](./Remove-AzureRouteTable.md)

[Remove-AzureSubnetRouteTable](./Remove-AzureSubnetRouteTable.md)

[Satz-AzureSubnetRouteTable](./Set-AzureSubnetRouteTable.md)


