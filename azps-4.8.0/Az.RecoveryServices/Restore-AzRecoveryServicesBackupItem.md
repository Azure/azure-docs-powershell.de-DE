---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 7dbafdececffe1a5e96c2c39dfb6d63f05961622
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009578"
---
# Restore-AzRecoveryServicesBackupItem

## Synopsis

Wiederherstellen der Daten und der Konfiguration für ein Sicherungselement an einem Wiederherstellungspunkt

## Syntax

### AzureVMParameterSet (Standard)
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureFileParameterSet
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureWorkloadParameterSet
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung

Das Cmdlet **Restore-AzRecoveryServicesBackupItem** stellt die Daten und die Konfiguration für ein Azure Backup-Element an einem angegebenen Wiederherstellungspunkt wieder her.
Mit diesem Cmdlet wird die Wiederherstellung aus dem Vault für Wiederherstellungsdienste auf dem Speicherkonto des Kunden gestartet.
Beim Wiederherstellungsvorgang wird der vollständige virtuelle Computer nicht wiederhergestellt.
Nachdem der Wiederherstellungsvorgang fertig ist, müssen Sie die verwalteten Datenträger für eine Ziel Ressourcengruppe und die Konfigurationsinformationen für das Kunden Speicherkonto wiederherstellen, indem Sie den virtuellen Computer erstellen und starten. Bitte refter Sie verschiedene mögliche Parametersätze und Parameter Text, um weitere Informationen zu erhalten.
Setzen Sie den Vault-Kontext mithilfe des-Vault-Parameters.

Hinweis: zum erfolgreichen Ausführen dieses Cmdlets zusätzlich zu-Vault-VaultLocation-Parameter sollte ebenfalls verwendet werden.

## Beispiele

### Beispiel 1: Wiederherstellen eines Elements in einem Wiederherstellungspunkt

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $restoreDiskLUNs = ("0", "1")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetRG $ManagedDiskRG -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -RestoreDiskList $restoreDiskLUNs -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

Der erste Befehl ruft den Sicherungs Container des Typs AzureVM ab und speichert ihn dann in der $Container Variablen.
Der zweite Befehl ruft das Sicherungselement mit dem Namen V2VM aus $Container ab und speichert es dann in der $BackupItem-Variablen.
Der dritte Befehl ruft das Datum ab sieben Tage zuvor ab und speichert es dann in der $StartDate Variablen.
Der vierte Befehl ruft das aktuelle Datum ab und speichert es dann in der $EndDate Variablen.
Der fünfte Befehl ruft eine Liste der Wiederherstellungspunkte für das jeweilige Sicherungselement ab, das nach $StartDate und $EndDate gefiltert wird.
Der angegebene Datumsbereich ist die letzten 7 Tage.
Der siebte Befehl gibt an, welche Datenträger vom Wiederherstellungspunkt wiederhergestellt werden sollen, und speichert Sie in $restoreDiskLUNs Variablen.
Mit dem letzten Befehl werden die Datenträger auf dem Zielspeicher Konto DestAccount in der DestRG-Ressourcengruppe wiederhergestellt.

### Beispiel 2: Wiederherstellen mehrerer Dateien eines AzureFileShare-Elements

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureStorage -WorkloadType AzureVM -VaultId $vault.ID -Name "fileshareitem"
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -VaultId $vault.ID
PS C:\> $files = ("file1.txt", "file2.txt")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -MultipleSourceFilePath $files -SourceFileType File -ResolveConflict Overwrite -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    fileshareitem            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

Der erste Befehl ruft den Sicherungs Container des Typs AzureVM ab und speichert ihn dann in der $Container Variablen.
Der zweite Befehl ruft das Sicherungselement mit dem Namen fileshareitem ab und speichert es dann in der $BackupItem-Variablen.
Der dritte Befehl ruft eine Liste der Wiederherstellungspunkte für das jeweilige Sicherungselement ab.
Der vierte Befehl spceifies die Dateien, die wiederhergestellt werden sollen, und speichert Sie in $Files Variablen.
Mit dem letzten Befehl werden die angegebenen Dateien an Ihrem ursprünglichen Speicherort wiederhergestellt.

### Beispiel 3

Wiederherstellen der Daten und der Konfiguration für ein Sicherungselement an einem Wiederherstellungspunkt automatisch

```powershell <!-- Aladdin Generated Example --> 
Restore-AzRecoveryServicesBackupItem -VaultId $vault.ID -WLRecoveryConfig <RecoveryConfigBase>
```

## Parameter

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

### -MultipleSourceFilePath
Wird für die Wiederherstellung mehrerer Dateien aus einer Dateifreigabe verwendet. Die Pfade der Elemente, die in der Dateifreigabe wiederhergestellt werden sollen.

```yaml
Type: System.String[]
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryPoint

Gibt den Wiederherstellungspunkt an, für den das Sicherungselement wiederhergestellt werden soll.
Verwenden Sie das Cmdlet **Get-AzRecoveryServicesBackupRecoveryPoint** , um ein **AzureRmRecoveryServicesBackupRecoveryPoint** -Objekt abzurufen.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: AzureVMParameterSet, AzureFileParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResolveConflict

Wenn das wiederhergestellte Element auch im Ziel vorhanden ist, verwenden Sie diese Option, um anzugeben, ob Sie überschrieben werden sollen.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Überschreiben
- Skip

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RestoreFSResolveConflictOption
Parameter Sets: AzureFileParameterSet
Aliases:
Accepted values: Overwrite, Skip

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestoreAsUnmanagedDisks
Verwenden Sie diese Option, um anzugeben, dass Sie als nicht verwaltete Datenträger wiederhergestellt werden sollen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestoreDiskList
Angeben, welche Datenträger von der gesicherten VM wiederhergestellt werden sollen

```yaml
Type: System.String[]
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestoreOnlyOSDisk
Verwenden Sie diese Option, um nur Betriebssystemdatenträger einer gesicherten VM wiederherzustellen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceFilePath

Wird für eine bestimmte Elementwiederherstellung aus einer Dateifreigabe verwendet. Der Pfad des Elements, das innerhalb der Dateifreigabe wiederhergestellt werden soll.

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceFileType

Wird für eine bestimmte Elementwiederherstellung aus einer Dateifreigabe verwendet. Der Typ des Elements, das innerhalb der Dateifreigabe wiederhergestellt werden soll.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Datei
- Verzeichnis

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SourceFileType]
Parameter Sets: AzureFileParameterSet
Aliases:
Accepted values: File, Directory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName

Gibt den Namen des Zielspeicher Kontos in Ihrem Abonnement an.
Im Rahmen des Wiederherstellungsvorgangs speichert dieses Cmdlet die Datenträger und die Konfigurationsinformationen in diesem Speicherkonto.

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountResourceGroupName

Gibt den Namen der Ressourcengruppe an, die das Zielspeicher Konto in Ihrem Abonnement enthält.
Im Rahmen des Wiederherstellungsvorgangs speichert dieses Cmdlet die Datenträger und die Konfigurationsinformationen in diesem Speicherkonto.

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetFileShareName

Die Dateifreigabe, in der die Dateifreigabe wiederhergestellt werden soll.

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetFolder

Der Ordner, in dem die Dateifreigabe innerhalb des TargetFileShareName wiederhergestellt werden soll. Wenn der gesicherte Inhalt in einem Stammordner wiederhergestellt werden soll, geben Sie die Werte für den Zielordner als leere Zeichenfolge an.

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetResourceGroupName

Die Ressourcengruppe, in der die verwalteten Datenträger wiederhergestellt werden. Anwendbar auf eine Sicherung von VM mit verwalteten Datenträgern

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetStorageAccountName

Das Speicherkonto, in dem die Dateifreigabe wiederhergestellt werden soll.

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseOriginalStorageAccount

Verwenden Sie diese Option, wenn die Datenträger des Wiederherstellungspunkts auf ihren ursprünglichen Speicherkonten wiederhergestellt werden sollen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tresor

Arm-ID des Speichers für Wiederherstellungsdienste

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VaultLocation

Der Speicherort des Speichers für Wiederherstellungsdienste.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WLRecoveryConfig

Wiederherstellungskonfiguration

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase
Parameter Sets: AzureWorkloadParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Bestätigen

Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
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

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

### Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. RecoveryPointBase

## Ausgaben

### Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase

## Notizen

## Verwandte Links

[Backup-AzRecoveryServicesBackupItem](./Backup-AzRecoveryServicesBackupItem.md)

[Get-AzRecoveryServicesBackupItem](./Get-AzRecoveryServicesBackupItem.md)

[Get-AzRecoveryServicesBackupRecoveryPoint](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
