---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
ms.openlocfilehash: 16095113dcc0604bfb7b739b1227db337a0cf6f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483089"
---
# Remove-AzureRmVMAccessExtension

## Synopsis
Entfernt die VMAccess-Erweiterung von einem virtuellen Computer.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Remove-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureRmVMAccessExtension** entfernt die Virtual Machine Access-Erweiterung (Virtual Machine Access, VMAccess) von einem virtuellen Computer.

## Beispiele

## Parameter

### -Force
Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen der Erweiterung an, die vom Cmdlet entfernt wird.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe des virtuellen Computers an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Gibt den Namen einer virtuellen Maschine an.
Dieses Cmdlet entfernt VMAccess für den virtuellen Computer, den dieser Parameter angibt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.

Das Cmdlet wird nicht ausgeführt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
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

[Get-AzureRmVMAccessExtension](./Get-AzureRmVMAccessExtension.md)

[Satz-AzureRmVMAccessExtension](./Set-AzureRmVMAccessExtension.md)

[Remove-AzureRmVMExtension](./Remove-AzureRmVMExtension.md)
