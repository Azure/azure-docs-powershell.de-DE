---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
ms.openlocfilehash: 2f2a6fc8c7e04798e0f2fd3095c2111f12bec65b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927368"
---
# Add-AzVmssVMDataDisk

## SYNOPSIS
Fügt einer Vmss-VM einen Datendatenträger hinzu.

## SYNTAX

```
Add-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-Caching <CachingTypes>] [-DiskSizeInGB <Int32>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Add-AzVmssVMDataDisk** fügt einer Vmss-VM einen Datenträger hinzu.

## BEISPIELE

### Beispiel 1: Hinzufügen eines verwalteten Datenträgers zu einer Vmss VM.
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

Der erste Befehl ruft einen vorhandenen verwalteten Datenträger ab.
Der nächste Befehl ruft eine vorhandene Vmss-VM ab, die vom Ressourcengruppennamen, dem Vmss-Namen und der Instanz-ID angegeben wird.
Mit dem nächsten Befehl wird der verwalteten Festplatte der vmss VM, die lokal in der Datei gespeichert ist, $VmssVM.
Mit dem letzten Befehl wird die Vmss-VM mit dem hinzugefügten Datenträger aktualisiert.

## PARAMETER

### -Zwischenspeichern
Gibt den Zwischenspeichermodus des Datenträgers an.
Die zulässigen Werte für diesen Parameter sind:
- ReadOnly
- ReadWrite
- Keine Der Standardwert ist ReadWrite.
Wenn Sie diesen Wert ändern, wird der virtuelle Computer neu gestartet.
Diese Einstellung wirkt sich auf die Konsistenz und Leistung des Datenträgers aus.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CreateOption
Gibt an, ob mit diesem Cmdlet ein Datenträger auf dem virtuellen Computer auf einer Plattform oder einem Benutzerabbild erstellt, ein leerer Datenträger erstellt oder ein vorhandener Datenträger anfügen wird.
Die zulässigen Werte für diesen Parameter sind:
- Anfügen.
Geben Sie diese Option an, um einen virtuellen Computer auf einem speziellen Datenträger zu erstellen.
Wenn Sie diese Option angeben, geben Sie nicht den *SourceImageUri-Parameter* an.
Der *VhdUri* ist alles, was benötigt wird, um der Azure-Plattform den Speicherort der virtuellen Festplatte (VHD) zu mitteilen, die als Datenträger an den virtuellen Computer anfügen soll.
- Leer.
Geben Sie dies an, um einen leeren Datenträger zu erstellen.
- FromImage.
Geben Sie diese Option an, um einen virtuellen Computer auf einem generalisierten Bild oder Datenträger zu erstellen.
Wenn Sie diese Option angeben, müssen Sie auch den *Parameter SourceImageUri* angeben, um der Azure-Plattform den Speicherort der VHD anzugeben, die als Datenträger anfügen soll.
Der *Parameter VhdUri* wird als Speicherort verwendet, an dem der Datenträger VHD gespeichert wird, wenn er vom virtuellen Computer verwendet wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -DiskEncryptionSetId
Gibt die Ressourcen-ID des vom Kunden verwalteten Datenträgerverschlüsselungssatzs an.  Dies kann nur für verwaltete Datenträger angegeben werden.

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

### -DiskSizeInGB
Gibt die Größe (in Gigabyte) eines leeren Datenträgers an, der an einen virtuellen Computer anfügen soll.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Lun
Gibt die Logische Einheitennummer (LUN) für einen Datenträger an.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagedDiskId
Gibt die ID eines verwalteten Datenträgers an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountType
Gibt den Speicherkontotyp des verwalteten Datenträgers an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSetVM
Gibt das VM-Objekt des lokalen virtuellen Computermaßstabs an, dem ein Datenträger hinzugefügt werden soll.
Sie können das **Get-AzVmssVM-Cmdlet** verwenden, um ein VM-Objekt für den Virtuellen Computermaßstab zu erhalten.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WriteAccelerator
Gibt an, ob WriteAccelerator auf einem verwalteten Datenträger aktiviert oder deaktiviert werden soll.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM

### System.Int32

### System.String

### Microsoft.Azure.Management.Compute.Models.CachingTypes

## AUSGABEN

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM

## NOTIZEN

## VERWANDTE LINKS
