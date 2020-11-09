---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 29233b0bdce273205acffcb87dbf3a8adb1d4a52
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300363"
---
# Add-AzVMDataDisk

## Synopsis
Fügt einen Daten Datenträger zu einem virtuellen Computer hinzu.

## Syntax

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

## Beschreibung
Mit dem Cmdlet **Add-AzVMDataDisk** wird ein Daten Datenträger zu einem virtuellen Computer hinzugefügt.
Sie können einen Datenträger hinzufügen, wenn Sie einen virtuellen Computer erstellen, oder Sie können einen Daten Datenträger zu einem vorhandenen virtuellen Computer hinzufügen.

## Beispiele

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

Der erste Befehl erstellt ein Objekt eines virtuellen Computers und speichert es dann in der $VirtualMachine-Variablen.
Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.
Die nächsten drei Befehle weisen den $DataDiskVhdUri 01-, $DataDiskVhdUri 02-und $DataDiskVhdUri 03-Variablen Pfade mit drei Datenträgern zu.
Dieser Ansatz dient nur zur Lesbarkeit der folgenden Befehle.
Die letzten drei Befehle fügen jeweils einen Datenträger zum virtuellen Computer hinzu, der in $VirtualMachine gespeichert ist.
Der Befehl gibt den Namen und den Speicherort für den Datenträger sowie weitere Eigenschaften des Datenträgers an.
Der URI jedes Datenträgers wird in $DataDiskVhdUri 01, $DataDiskVhdUri 02 und $DataDiskVhdUri 03 gespeichert.

### Beispiel 2: Hinzufügen eines Datenlaufwerks zu einem vorhandenen virtuellen Computer
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

Der erste Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine07 mit dem Cmdlet [Get-AzVM](./Get-AzVM.md) ab.
Der Befehl speichert den virtuellen Computer in der $VirtualMachine-Variablen.
Der zweite Befehl fügt dem virtuellen Computer, der in $VirtualMachine gespeichert ist, einen Daten Datenträger hinzu.
Der endgültige Befehl aktualisiert den Zustand des virtuellen Computers, der in $VirtualMachine in ResourceGroup11 gespeichert ist.

### Beispiel 3: Hinzufügen eines Datenlaufwerks zu einem neuen virtuellen Computer aus einem generalisierten Benutzerbild
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

Der erste Befehl erstellt ein Objekt eines virtuellen Computers und speichert es in der $VirtualMachine-Variablen.
Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.
In den nächsten beiden Befehlen werden den $DataImageUri-und $DataDiskUri Variablen Pfade für das Daten Bild und die Datenlaufwerke zugewiesen.
Dieser Ansatz wird verwendet, um die Lesbarkeit der folgenden Befehle zu verbessern.
Mit den letzten Befehlen wird dem virtuellen Computer, der in $VirtualMachine gespeichert ist, ein Daten Datenträger hinzugefügt.
Der Befehl gibt den Namen und den Speicherort für den Datenträger und andere Eigenschaften des Datenträgers an.

### Beispiel 4: Hinzufügen von Datenträgern zu einem neuen virtuellen Computer aus einem speziellen Benutzerbild
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

Der erste Befehl erstellt ein Objekt eines virtuellen Computers und speichert es in der $VirtualMachine-Variablen.
Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.
Die nächsten Befehle weisen der $DataDiskUri-Variablen Pfade des Daten Datenträgers zu.
Dieser Ansatz wird verwendet, um die Lesbarkeit der folgenden Befehle zu verbessern.
Der letzte Befehl fügt dem virtuellen Computer, der in $VirtualMachine gespeichert ist, einen Daten Datenträger hinzu.
Der Befehl gibt den Namen und den Speicherort für den Datenträger sowie weitere Eigenschaften des Datenträgers an.

## Parameter

### -Caching
Gibt den Zwischenspeichermodus des Datenträgers an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- ReadOnly
- ReadWrite
- None der Standardwert ist ReadWrite.
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

### -Createoption
Gibt an, ob dieses Cmdlet einen Datenträger auf dem virtuellen Computer von einer Plattform oder einem Benutzerbild erstellt, einen leeren Datenträger erstellt oder einen vorhandenen Datenträger anfügt.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- Anfügen.
Geben Sie diese Option an, um einen virtuellen Computer von einem spezialisierten Datenträger zu erstellen.
Wenn Sie diese Option angeben, geben Sie den *SourceImageUri* -Parameter nicht an.
Die *VhdUri* ist alles, was erforderlich ist, um der Azure-Plattform den Speicherort der virtuellen Festplatte (VHD) mitzuteilen, die als Datenträger an den virtuellen Computer angefügt werden soll.
- Leer.
Geben Sie dies an, um einen leeren Datenträger zu erstellen.
- FromImage.
Geben Sie diese Option an, um einen virtuellen Computer aus einem generalisierten Bild oder Datenträger zu erstellen.
Wenn Sie diese Option angeben, müssen Sie auch den *SourceImageUri* -Parameter angeben, um der Azure-Plattform den Speicherort der VHD mitzuteilen, die als Daten Datenträger angefügt werden soll.
Der *VhdUri* -Parameter wird als Speicherort verwendet, der angibt, wo die VHD des Daten Datenträgers gespeichert wird, wenn Sie vom virtuellen Computer verwendet wird.

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
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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
Gibt die Ressourcen-ID des vom Kunden verwalteten Datenträger Verschlüsselungs Satzes an.  Dies kann nur für verwalteten Datenträger angegeben werden.

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
Gibt die Größe eines leeren Datenträgers an, der an einen virtuellen Computer angefügt werden soll.

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

### -LUN
Gibt die logische Einheitsnummer (LUN) für einen Datenträger an.

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
Gibt den Namen des hinzuzufügenden Daten Datenträgers an.

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
Gibt den Quell-URI des Datenträgers an, der von diesem Cmdlet angefügt wird.

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
Gibt den Speicher Kontotyp des verwalteten Datenträgers an.

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
Gibt den Uniform Resource Identifier (URI) für die VHD-Datei (Virtual Hard Disk) an, die beim Verwenden eines Platt Form Bilds oder eines Benutzerbilds erstellt werden soll.
Dieses Cmdlet kopiert das BLOB-Objekt (Binary Large Object) an diesen Speicherort.
Dies ist der Speicherort, an dem der virtuelle Computer gestartet werden soll.

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
Sie können das Cmdlet **Get-AzVM** verwenden, um ein Objekt eines virtuellen Computers abzurufen.
Sie können das Cmdlet **New-AzVMConfig** verwenden, um ein Objekt eines virtuellen Computers zu erstellen.

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
Gibt an, ob WriteAccelerator auf einem verwalteten Daten Datenträger aktiviert oder deaktiviert werden soll.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine

### System. String

### Microsoft. Azure. Management. Compute. Models. CachingTypes

### System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

## Ausgaben

### Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine

### Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM

## Notizen

## Verwandte Links

[Remove-AzVMDataDisk](./Remove-AzVMDataDisk.md)

[Get-AzVM](./Get-AzVM.md)

[Neu – AzVMConfig](./New-AzVMConfig.md)
