---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Disable-AzureRmVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Disable-AzureRmVMDiskEncryption.md
ms.openlocfilehash: 087ae12961d6bd9faf844221772b92c79362d13d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496645"
---
# Disable-AzureRmVMDiskEncryption

## Synopsis
Deaktiviert die Verschlüsselung auf einem virtuellen IaaS-Computer.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Disable-AzureRmVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Disable-AzureRmVMDiskEncryption** deaktiviert die Verschlüsselung auf einem virtuellen Computer mit einem Dienst (Infrastructure as a Service, IaaS).
Dieses Cmdlet wird nur auf virtuellen Windows-Computern und nicht auf virtuellen Linux-Computern unterstützt.
Dieses Cmdlet installiert eine Erweiterung auf dem virtuellen Computer, um die Verschlüsselung zu deaktivieren.
Wenn der Parameter *Name* nicht angegeben ist, wird eine Erweiterung mit dem Standardnamen "AzureDiskEncryption für Windows VMS" erstellt.
Vorsicht: Dieses Cmdlet startet den virtuellen Computer neu.

## Beispiele

### Beispiel 1: Deaktivieren der Verschlüsselung für alle Volumes auf einem virtuellen Windows-Computer
```
PS C:\> Disable-AzureRMVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

Mit diesem Befehl wird die Verschlüsselung für Volumes des Typs alle für den virtuellen Computer mit dem Namen VM002 deaktiviert, der zur Ressourcengruppe mit dem Namen Group001 gehört.
Da der Parameter *volumetype* nicht angegeben ist, legt das Cmdlet den Wert auf alle fest.

### Beispiel 2: Deaktivieren der Verschlüsselung für Daten-Volumes auf einem virtuellen Windows-Computer
```
PS C:\> $ResourceGroup = "Group002";
PS C:\> $VMName = "VM004";
PS C:\> Disable-AzureRMVMDiskEncryption -ResourceGroupName "Group002" -VMName "VM004" -VolumeType "Data"
```

Mit diesem Befehl wird die Verschlüsselung für Volumes vom Typ Data für den virtuellen Computer mit dem Namen VM004 deaktiviert, der zur Ressourcengruppe mit dem Namen Group002 gehört.

## Parameter

### -DisableAutoUpgradeMinorVersion
Gibt an, dass dieses Cmdlet die automatische Aktualisierung der Nebenversion der Erweiterung deaktiviert.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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
Gibt an der Name der Azure Resource Manager (Arm)-Ressource, die die Erweiterung darstellt.
Wenn dieser Parameter nicht angegeben wird, ist dieses Cmdlet standardmäßig auf "AzureDiskEncryption für Windows-VMS" festgelegt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Ressourcengruppennamen der virtuellen Maschine an.

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

### -TypeHandlerVersion
Gibt die Version der Verschlüsselungs Erweiterung an.
Wenn Sie keinen Wert für diesen Parameter angeben, wird die neueste Version der Erweiterung verwendet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Gibt den Namen des virtuellen Computers an, auf dem dieses Cmdlet die Verschlüsselung deaktiviert.

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

### -Volumetype
Gibt den Typ der virtuellen Maschinen-Volumes an, um den Verschlüsselungsvorgang auszuführen.
Bei Windows-virtuellen Computern sind gültige Werte: 

- Alle
- OS
- Daten.
Wenn Sie keinen Wert für diesen Parameter angeben, lautet der Standardwert alle.
Die Option "Verschlüsselung deaktivieren" wird derzeit für Linux nicht unterstützt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
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

### Dieses Cmdlet generiert keine Ausgabe.

## Notizen

## Verwandte Links

[Get-AzureRmVMDiskEncryptionStatus](./Get-AzureRmVMDiskEncryptionStatus.md)

[Remove-AzureRmVMDiskEncryptionExtension](./Remove-AzureRmVMDiskEncryptionExtension.md)

[Satz-AzureRmVMDiskEncryptionExtension](./Set-AzureRmVMDiskEncryptionExtension.md)


