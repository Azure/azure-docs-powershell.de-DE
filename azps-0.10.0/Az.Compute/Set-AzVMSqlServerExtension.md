---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 4093e236f84d7587586ba30c8bd4653c4ba7358f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844195"
---
# Set-AzVMSqlServerExtension

## Synopsis
Legt die Azure SQL Server-Erweiterung auf einem virtuellen Computer fest.

## Syntax

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Set-AzVMSqlServerExtension** " legt die AzureSQL-Server Erweiterung auf einem virtuellen Computer fest.

## Beispiele

### Beispiel 1: Festlegen der Einstellungen für automatische Patches auf einem virtuellen Computer
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

Mit dem ersten Befehl wird mithilfe des Cmdlets **New-AzureVMSqlServerAutoPatchingConfig** ein Configuration-Objekt erstellt.
Der Befehl speichert die Konfiguration in der $AutoPatchingConfig-Variablen.

Der zweite Befehl ruft den virtuellen Computer mit dem Namen "VirtualMachine11" auf dem Dienst mit dem Namen Service02 mithilfe des Get-AzVM-Cmdlets ab.
Der Befehl übergibt dieses Objekt mithilfe des Pipelineoperators an das aktuelle Cmdlet.

Das aktuelle Cmdlet legt die Einstellungen für das automatische Patchen in $AutoPatchingConfig für den virtuellen Computer fest.
Der Befehl übergibt den virtuellen Computer an das Update-AzVM-Cmdlet.

### Beispiel 2: Festlegen automatischer Sicherungseinstellungen auf einem virtuellen Computer
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

Mit dem ersten Befehl wird mithilfe des Cmdlets **New-AzureVMSqlServerAutoBackupConfig** ein Configuration-Objekt erstellt.
Der Befehl speichert die Konfiguration in der $AutoBackupConfig-Variablen.

Der zweite Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine11 auf dem Dienst mit dem Namen Service02 ab und übergibt ihn dann an das aktuelle Cmdlet.

Das aktuelle Cmdlet legt die Einstellungen für automatische Sicherungskopien in $AutoBackupConfig für den virtuellen Computer fest.
Der Befehl übergibt den virtuellen Computer an das Update-AzVM-Cmdlet.

### Beispiel 3: Deaktivieren einer SQL Server-Erweiterung auf einem virtuellen Computer
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

Dieser Befehl ruft einen virtuellen Computer mit dem Namen VirtualMachine08 in Service03 ab und übergibt ihn dann an das aktuelle Cmdlet.
Der Befehl deaktiviert die Erweiterung SQL Server Virtual Machine auf diesem virtuellen Computer.

### Beispiel 4: Deinstallieren einer SQL Server-Erweiterung auf einem bestimmten virtuellen Computer
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

Dieser Befehl ruft einen virtuellen Computer mit dem Namen VirtualMachine08 in Service03 ab und übergibt ihn dann an das aktuelle Cmdlet.
Der Befehl deinstalliert eine SQL Server Virtual Machine-Erweiterung auf diesem virtuellen Computer.

## Parameter

### -AutoBackupSettings
Gibt die automatischen SQL Server-Sicherungseinstellungen an.
Verwenden Sie das New-AzureVMSqlServerAutoBackupConfig-Cmdlet, um ein **AutoBackupSettings** -Objekt zu erstellen.

```yaml
Type: AutoBackupSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutoPatchingSettings
Gibt die automatischen Updateeinstellungen für SQL Server an.
Verwenden Sie das New-AzureVMSqlServerAutoPatchingConfig-Cmdlet, um ein **AutoPatchingSettings** -Objekt zu erstellen.

```yaml
Type: AutoPatchingSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
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

### -KeyVaultCredentialSettings
```yaml
Type: KeyVaultCredentialSettings
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Standort
Gibt den Speicherort der virtuellen Maschine an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen der SQL Server-Erweiterung an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
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
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Gibt die Version der SQL Server-Erweiterung an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Gibt den Namen des virtuellen Computers an, auf dem dieses Cmdlet die SQL Server-Erweiterung festlegt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse

## Notizen

## Verwandte Links

[Get-AzVM](./Get-AzVM.md)

[Get-AzVMSqlServerExtension](./Get-AzVMSqlServerExtension.md)

[Neu – AzureVMSqlServerAutoPatchingConfig](./New-AzureVMSqlServerAutoPatchingConfig.md)

[Neu – AzureVMSqlServerAutoBackupConfig](./New-AzureVMSqlServerAutoBackupConfig.md)

[Remove-AzVMSqlServerExtension](./Remove-AzVMSqlServerExtension.md)

[Update-AzVM](./Update-AzVM.md)


