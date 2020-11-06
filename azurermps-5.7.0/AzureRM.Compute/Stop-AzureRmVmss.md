---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
ms.openlocfilehash: 3798590f3b4df738bc38231018adabf99ba39237
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503826"
---
# Stop-AzureRmVmss

## Synopsis
Beendet die VMSS oder einen Satz virtueller Computer innerhalb des VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Defaultparameter (Standard)
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### FriendMethod
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Stop-AzureRmVmss** beendet alle virtuellen Maschinen innerhalb des Scale-Sets (Virtual Machine Scale) (VMSS) oder einer Gruppe virtueller Computer.
Sie können den *InstanceId* -Parameter verwenden, um einen Satz virtueller Computer auszuwählen.

## Beispiele

### Beispiel 1: Beenden aller virtuellen Computer innerhalb des VMSS
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

Dieser Befehl beendet alle virtuellen Computer, die zum VMSS mit dem Namen ContosoVMSS gehören.

### Beispiel 2: Beenden einer bestimmten Gruppe von virtuellen Computern innerhalb des VMSS
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

Mit diesem Befehl wird eine bestimmte Gruppe von virtuellen Computern beendet, die durch das Array der Instanz-ID-Zeichenfolge angegeben werden, die zum VMSS mit dem Namen ContosoVMSS gehören.

## Parameter

### -Force
Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceId
Gibt als Zeichenfolgenarray die ID oder IDs der Instanzen des virtuellen Computers an, die von diesem Cmdlet angehalten werden.
Beispiel: `-InstanceId "0", "3"` .

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe des VMSS an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StayProvisioned
Wenn angegeben, wird der virtuelle Computer in den Zustand beendet gesetzt. Wenn keine Angabe erfolgt, gibt der virtuelle Computer den Status "Stopped-dereserviert" ein. Der Benutzer wird weiterhin für VMS im Zustand "beendet", jedoch nicht für VMS im Status "nicht mehr zugewiesen" berechnet.


```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMScaleSetName
Gibt den Namen der VMSS an, für die dieses Cmdlet die virtuellen Computer beendet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureRmVmss](./Get-AzureRmVmss.md)

[Neu – AzureRmVmss](./New-AzureRmVmss.md)

[Remove-AzureRmVmss](./Remove-AzureRmVmss.md)

[Neustart-AzureRmVmss](./Restart-AzureRmVmss.md)

[Satz-AzureRmVmss](./Set-AzureRmVmss.md)

[Anfang-AzureRmVmss](./Start-AzureRmVmss.md)

[Update-AzureRmVmss](./Update-AzureRmVmss.md)


