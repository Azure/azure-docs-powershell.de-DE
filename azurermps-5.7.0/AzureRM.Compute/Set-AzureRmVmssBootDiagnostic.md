---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssBootDiagnostic.md
ms.openlocfilehash: 868bf95ca2f54105143f122665ffa89732ada167
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497697"
---
# Set-AzureRmVmssBootDiagnostic

## Synopsis
Legt das Start Diagnose Profil für den virtuellen Computer fest.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Set-AzureRmVmssBootDiagnostic [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Legt das Start Diagnose Profil für den virtuellen Computer fest.

## Beispiele

### Beispiel 1: Festlegen der Boot Diagnostics-Profileigenschaft für eine VMSS
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzureRmVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzureRmVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

Mit diesem Befehl wird die Start Diagnose-Profileigenschaft für die VMSS mit dem Namen ContosoVMSS festgelegt.

## Parameter

### -Aktiviert
Gibt an, ob die Start Diagnose für den Skalierungs Satz der virtuellen Maschine aktiviert werden soll.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageUri
Der URI des speicherkontos, das für die Platzierung der Konsolenausgabe und des Screenshots verwendet werden soll.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Gibt das VMSS-Objekt an.
Sie können das New-AzureRmVmssConfig-Cmdlet verwenden, um das Objekt zu erstellen.

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
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
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

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

### Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet
System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. String

## Ausgaben

### Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet

## Notizen

## Verwandte Links

