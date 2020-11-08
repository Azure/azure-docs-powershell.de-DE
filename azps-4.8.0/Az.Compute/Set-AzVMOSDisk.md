---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
ms.openlocfilehash: 66bcaab66f6385bdc9f59233054d90932ac6fa33
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010214"
---
# Set-AzVMOSDisk

## Synopsis
Legt die Datenträgereigenschaften des Betriebssystems auf einem virtuellen Computer fest.

## Syntax

### DefaultParamSet (Standard)
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsParamSet
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsDiskEncryptionParameterSet
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### LinuxParamSet
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### LinuxDiskEncryptionParameterSet
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Set-AzVMOSDisk** " legt die Datenträgereigenschaften des Betriebssystems auf einem virtuellen Computer fest.

## Beispiele

### Beispiel 1: Einrichten von Eigenschaften auf einem virtuellen Computer vom Platt Form Abbild
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

Der erste Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailabilitySet13 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt dann in der $AvailabilitySet Variablen.
Der zweite Befehl erstellt ein Objekt eines virtuellen Computers und speichert es dann in der $VirtualMachine-Variablen.
Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.
Der virtuelle Computer gehört zum verfügbaren Verfügbarkeits Satz, der in $AvailabilitySet gespeichert ist.
Der endgültige Befehl legt die Eigenschaften auf dem virtuellen Computer in $VirtualMachine fest.

### Beispiel 2: Festlegen von Eigenschaften auf einem virtuellen Computer vom generalisierten Benutzerbild
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

Der erste Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailabilitySet13 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt in der $AvailabilitySet Variablen.
Der zweite Befehl erstellt ein Objekt eines virtuellen Computers und speichert es in der $VirtualMachine-Variablen.
Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.
Der virtuelle Computer gehört zum verfügbaren Verfügbarkeits Satz, der in $AvailabilitySet gespeichert ist.
Der endgültige Befehl legt die Eigenschaften auf dem virtuellen Computer in $VirtualMachine fest.

### Beispiel 3: Festlegen von Eigenschaften auf einem virtuellen Computer aus einem speziellen Benutzerbild
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

Der erste Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailabilitySet13 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt in der $AvailabilitySet Variablen.
Der zweite Befehl erstellt ein Objekt eines virtuellen Computers und speichert es in der $VirtualMachine-Variablen.
Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.
Der virtuelle Computer gehört zum verfügbaren Verfügbarkeits Satz, der in $AvailabilitySet gespeichert ist.
Der endgültige Befehl legt die Eigenschaften auf dem virtuellen Computer in $VirtualMachine fest.

### Beispiel 4: Festlegen der Datenträger Verschlüsselungseinstellungen auf einem virtuellen Computer-Betriebssystemdatenträger
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

In diesem Beispiel werden die Datenträger Verschlüsselungseinstellungen auf einem virtuellen Computer-Betriebssystemdatenträger festgelegt.

## Parameter

### -Caching
Gibt den Zwischenspeichermodus des Betriebssystemdatenträgers an.
Gültige Werte sind: 
- ReadOnly
- ReadWrite der Standardwert ist ReadWrite.
Durch Ändern des Caching-Werts wird der virtuelle Computer neu gestartet.
Diese Einstellung wirkt sich auf die Leistung des Datenträgers aus.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Createoption
Gibt an, ob dieses Cmdlet einen Datenträger auf dem virtuellen Computer von einer Plattform oder einem Benutzerbild erstellt oder einen vorhandenen Datenträger anfügt.
Gültige Werte sind: 
- Anfügen.
Geben Sie diese Option an, um einen virtuellen Computer von einem spezialisierten Datenträger zu erstellen.
Wenn Sie diese Option angeben, geben Sie den *SourceImageUri* -Parameter nicht an.
Verwenden Sie stattdessen das Set-AzVMSourceImage-Cmdlet.
Sie müssen auch die *Windows* -oder *Linux* -Parameter verwenden, um der Azure-Plattform den Typ des Betriebssystems auf der virtuellen Festplatte mitzuteilen.
Der *VhdUri* -Parameter genügt, um der Azure-Plattform den Speicherort des anzufügenden Datenträgers mitzuteilen. 
- FromImage.
Geben Sie diese Option an, um einen virtuellen Computer aus einem Platt Form Bild oder einem generalisierten Benutzerbild zu erstellen.
Im Fall eines generalisierten Benutzerbilds müssen Sie auch den *SourceImageUri* -Parameter und entweder die *Windows* -oder *Linux* -Parameter angeben, um der Azure-Plattform den Speicherort und den Typ der VHD des Betriebssystems festzulegen, anstatt das Cmdlet " **AzVMSourceImage** " zu verwenden.
Im Fall eines Platt Form Bilds genügt der *VhdUri* -Parameter. 
- Leer.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
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

### -DiffDiskSetting
Gibt die differenzierenden Datenträgereinstellungen für den Betriebssystemdatenträger an.

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

### -DiskEncryptionKeyUrl
Gibt den Speicherort des Datenträger Verschlüsselungsschlüssels an.

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: True
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskEncryptionKeyVaultId
Gibt die Ressourcen-ID des Schlüsseldepots mit dem Datenträgerverschlüsselungsschlüssel an.

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: True
Position: 8
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
Gibt die Größe des Betriebssystemdatenträgers in GB an.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyEncryptionKeyUrl
Gibt den Speicherort des Schlüssel Verschlüsselungsschlüssels an.

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyEncryptionKeyVaultId
Gibt die Ressourcen-ID des Schlüsseldepots mit dem Schlüssel Verschlüsselungsschlüssel an.

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Linux
Gibt an, dass das Betriebssystem des Benutzer Abbilds Linux ist.
Geben Sie diesen Parameter für die Bereitstellung von auf dem Bild basierenden Benutzern an.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LinuxParamSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedDiskId
Gibt die ID eines verwalteten Datenträgers an.

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

### -Name
Gibt den Namen des Betriebssystemdatenträgers an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OSDiskName, DiskName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceImageUri
Gibt den URI der VHD für Benutzerbild Szenarien an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountType
Gibt den Speicher Kontotyp des verwalteten Datenträgers an.

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

### -VhdUri
Gibt den Uniform Resource Identifier (URI) einer virtuellen Festplatte (VHD) an.
Bei einem bildbasierten virtuellen Computer gibt dieser Parameter die VHD-Datei an, die erstellt werden soll, wenn ein Platt Form Bild oder Benutzerbild angegeben wird.
Hierbei handelt es sich um den Speicherort, an dem das BLOB (Image Binary Large Object) kopiert wird, um den virtuellen Computer zu starten.
Bei einem Startszenario für einen datenträgerbasierten virtuellen Computer gibt dieser Parameter die VHD-Datei an, die vom virtuellen Computer zum Starten direkt verwendet wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OSDiskVhdUri, DiskVhdUri

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Gibt das Objekt des lokalen virtuellen Computers an, auf dem die Datenträgereigenschaften des Betriebssystems festgelegt werden sollen.
Verwenden Sie das Get-AzVM-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Windows
Gibt an, dass das Betriebssystem des Benutzer Abbilds Windows ist.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsParamSet, WindowsDiskEncryptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WriteAccelerator
Gibt an, ob WriteAccelerator auf dem Betriebssystemdatenträger aktiviert oder deaktiviert werden soll.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine

### System. String

## Ausgaben

### Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine

## Notizen

## Verwandte Links

[Get-AzVM](./Get-AzVM.md)

[Get-AzAvailabilitySet](./Get-AzAvailabilitySet.md)

[Neu – AzVMConfig](./New-AzVMConfig.md)


