---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 29233b0bdce273205acffcb87dbf3a8adb1d4a52
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305864"
---
# Add-AzVMDataDisk

## SYNOPSIS
Fügt einem virtuellen Computer einen Datenträger hinzu.

## SYNTAX

### VmNormalDiskParameterSetName (Standard)
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-SourceImageUri] <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### VmManagedDiskParameterSetName
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Add-AzVMDataDisk"** fügt einem virtuellen Computer einen Datenträger hinzu.
Sie können einen Datenträger hinzufügen, wenn Sie einen virtuellen Computer erstellen, oder Sie können einen Datenträger zu einem vorhandenen virtuellen Computer hinzufügen.

## BEISPIELE

### Beispiel 1: Hinzufügen von Datenträgern zu einem neuen virtuellen Computer
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

Der erste Befehl erstellt ein Objekt des virtuellen Computers und speichert es dann in der $VirtualMachine Variable.
Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.
Mit den nächsten drei Befehlen werden den Variablen $DataDiskVhdUri 01, $DataDiskVhdUri 02 und $DataDiskVhdUri 03 Pfade von drei Datenträgern zugewiesen.
Dieser Ansatz ist nur zur Lesbarkeit der folgenden Befehle.
Mit den letzten drei Befehlen wird dem virtuellen Computer, der auf dem Computer gespeichert ist, jeweils ein Datenträger $VirtualMachine.
Der Befehl gibt den Namen und Speicherort des Datenträgers sowie weitere Eigenschaften des Datenträgers an.
Der URI der einzelnen Datenträger wird in $DataDiskVhdUri 01, $DataDiskVhdUri 02 und $DataDiskVhdUri 03 gespeichert.

### Beispiel 2: Hinzufügen eines Datenträgers zu einem vorhandenen virtuellen Computer
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

Der erste Befehl ruft den virtuellen Computer "VirtualMachine07" mithilfe des [Get-AzVM-Cmdlets](./Get-AzVM.md) ab.
Der Befehl speichert den virtuellen Computer in der $VirtualMachine Variable.
Der zweite Befehl fügt dem virtuellen Computer, der auf der Festplatte gespeichert ist, einen $VirtualMachine.
Der letzte Befehl aktualisiert den Zustand des virtuellen Computers, der in $VirtualMachine ResourceGroup11 gespeichert ist.

### Beispiel 3: Hinzufügen eines Datenträgers zu einem neuen virtuellen Computer aus einem generalisierten Benutzerbild
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

Der erste Befehl erstellt ein Objekt des virtuellen Computers und speichert es in der $VirtualMachine Variable.
Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.
Mit den nächsten beiden Befehlen werden Pfade für das Datenbild und die Datenträger den $DataImageUri und $DataDiskUri Zuzuordnen.
Dieser Ansatz wird verwendet, um die Lesbarkeit der folgenden Befehle zu verbessern.
Mit den endgültigen Befehlen wird dem virtuellen Computer, der auf dem Computer gespeichert ist, ein Datenträger $VirtualMachine.
Der Befehl gibt den Namen und Speicherort für den Datenträger und andere Eigenschaften des Datenträgers an.

### Beispiel 4: Hinzufügen von Datenträgern zu einem neuen virtuellen Computer aus einem speziellen Benutzerbild
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

Der erste Befehl erstellt ein Objekt des virtuellen Computers und speichert es in der $VirtualMachine Variable.
Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.
Mit den nächsten Befehlen werden pfade des Datenträgers der variablen $DataDiskUri.
Dieser Ansatz wird verwendet, um die Lesbarkeit der folgenden Befehle zu verbessern.
Mit dem letzten Befehl wird dem virtuellen Computer, der auf dem Computer gespeichert ist, ein $VirtualMachine.
Der Befehl gibt den Namen und Speicherort des Datenträgers sowie weitere Eigenschaften des Datenträgers an.

## PARAMETERS

### -Zwischenspeichern
Gibt den Zwischenspeicherungsmodus des Datenträgers an.
Die zulässigen Werte für diesen Parameter sind:
- ReadOnly
- ReadWrite
- Keine Der Standardwert ist "ReadWrite".
Wenn Sie diesen Wert ändern, wird der virtuelle Computer neu gestartet.
Diese Einstellung wirkt sich auf die Konsistenz und Leistung des Datenträgers aus.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CreateOption
Gibt an, ob mit diesem Cmdlet ein Datenträger auf dem virtuellen Computer über eine Plattform oder ein Benutzerabbild erstellt, ein leerer Datenträger erstellt oder ein vorhandener Datenträger anfügen wird.
Die zulässigen Werte für diesen Parameter sind:
- Anfügen.
Geben Sie diese Option an, um einen virtuellen Computer von einem speziellen Datenträger zu erstellen.
Wenn Sie diese Option angeben, geben Sie nicht den *Parameter "SourceImageUri"* an.
Der *VhdUri* ist alles, was benötigt wird, um der Azure-Plattform den Speicherort der virtuellen Festplatte (VHD) zu mitteilen, die als Datenträger an den virtuellen Computer anfügen soll.
- Leer.
Geben Sie dies an, um einen leeren Datenträger zu erstellen.
- FromImage.
Geben Sie diese Option an, um einen virtuellen Computer aus einem generalisierten Bild oder Datenträger zu erstellen.
Wenn Sie diese Option angeben, müssen Sie auch den *Parameter "SourceImageUri"* angeben, um der Azure-Plattform den Speicherort der VHD anzugeben, die als Datenträger anfügen werden soll.
Der *Parameter "VhdUri"* wird als Speicherort verwendet, an dem die Festplatte VHD gespeichert wird, wenn sie vom virtuellen Computer verwendet wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
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
Gibt die Ressourcen-ID des vom Kunden verwalteten Datenträgerverschlüsselungssatz an.  Dies kann nur für verwalteten Datenträger angegeben werden.

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
Gibt die Größe (in Gigabyte) eines leeren Datenträgers an, der an einen virtuellen Computer anfügen wird.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Lun
Gibt die Wahrheitsnummer einer Einheit (LUN) für einen Datenträger an.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagedDiskId
Gibt die ID eines verwalteten Datenträgers an.

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen des hinzuzufügenden Datenträgers an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SourceImageUri
Gibt den Quell-URI des Datenträgers an, den dieses Cmdlet anfügen soll.

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountType
Gibt den Speicherkontotyp des verwalteten Datenträgers an.

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VhdUri
Gibt den URI (Uniform Resource Identifier) für die virtuelle Festplattendatei (VHD) an, die erstellt wird, wenn ein Plattformbild oder ein Benutzerbild verwendet wird.
Dieses Cmdlet kopiert das große Binärobjekt (BLOB) des Bilds an diesen Speicherort.
Dies ist der Ort, an dem der virtuelle Computer gestartet wird.

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Gibt das Objekt des lokalen virtuellen Computers an, dem ein Datenträger hinzugefügt werden soll.
Sie können das **Get-AzVM-Cmdlet** verwenden, um ein Objekt des virtuellen Computers zu erhalten.
Sie können das **Cmdlet "New-AzVMConfig"** verwenden, um ein Objekt für einen virtuellen Computer zu erstellen.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WriteAccelerator
Gibt an, ob WriteAccelerator auf einem verwalteten Datenträger aktiviert oder deaktiviert werden soll.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.String

### Microsoft.Azure.Management.Compute.Models.CachingTypes

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## AUSGABEN

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Remove-AzVMDataDisk](./Remove-AzVMDataDisk.md)

[Get-AzVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)
