---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 593603e212c2ebfd709e5f4c70797ea369877b76
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360729"
---
# Restore-AzRecoveryServicesBackupItem

## SYNOPSIS

Stellt die Daten und die Konfiguration für ein Sicherungselement auf dem angegebenen Wiederherstellungspunkt wieder her. Die erforderlichen Parameter variieren je nach Typ des Sicherungselements.
Derselbe Befehl wird zum Wiederherstellen virtueller Azure-Computer, von Datenbanken, die auf virtuellen Azure-Computern ausgeführt werden, und von Azure-Dateifreigaben verwendet.

## SYNTAX

### AzureVMParameterSet (Standard)
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### AzureVMManagedDiskParameterSet
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-TargetResourceGroupName] <String>
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureVMRestoreManagedAsUnmanaged
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureVMUnManagedDiskParameterSet
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureFileShareParameterSet
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

## BESCHREIBUNG

Das **Cmdlet "Restore-AzRecoveryServicesBackupItem"** stellt die Daten und die Konfiguration für ein Azure Backup-Element auf einem angegebenen Wiederherstellungspunkt wieder her.

**Für Azure VM Backup**

Mit diesem Befehl können Sie virtuelle Azure-Computer sichern und Datenträger (verwaltete und nicht verwaltete Datenträger) wiederherstellen. Der Wiederherstellungsvorgang stellt nicht den vollständigen virtuellen Computer wiederher.
Wenn es sich um eine verwaltete Datenträger-VM handelt, sollte eine Zielressourcengruppe angegeben werden, in der die wiederhergestellten Datenträger gespeichert werden. Wenn die Momentaufnahmen in der Ressourcengruppe vorhanden sind, die in der Sicherungsrichtlinie angegeben wurde, wird der Wiederherstellungsvorgang sofort ausgeführt, und die Datenträger werden aus lokalen Momentaufnahmen erstellt und in der Zielressourcengruppe gespeichert. Es gibt auch eine Option, um sie als nicht verwaltete Datenträger wiederherzustellen, aber dadurch werden die daten genutzt, die sich im Tresor der Azure-Wiederherstellungsdienste befinden, und daher viel langsamer sein. Die Konfiguration der VM und die Bereitstellungsvorlage, die zum Erstellen einer VM aus den wiederhergestellten Datenträgern verwendet werden kann, werden in das angegebene Speicherkonto heruntergeladen.
Wenn es sich um eine nicht verwaltete Datenträger-VM handelt, sind die Momentaufnahmen im ursprünglichen Speicherkonto des Datenträgers und/oder im Wiederherstellungsdiensttresor vorhanden. Wenn der Benutzer die Möglichkeit hat, das ursprüngliche Speicherkonto zum Wiederherstellen zu verwenden, kann eine sofortige Wiederherstellung bereitgestellt werden. Andernfalls werden Daten aus dem Azure Recovery Services-Tresor abgerufen, und Datenträger werden zusammen mit der Konfiguration der VM und der Bereitstellungsvorlage in einem angegebenen Speicherkonto erstellt.

> [!IMPORTANT]
> Standardmäßig werden mit der Azure VM-Sicherung alle Datenträger gesichert. Sie können relevante Datenträger selektiv mit den Parametern "exclusionList" oder "InclusionList" während "Enable-Backup" sichern. Die Option zum selektiven Wiederherstellen von Datenträgern ist nur verfügbar, wenn sie selektiv gesichert wurden.

Weitere Informationen finden Sie unter verschiedenen möglichen Parametersätzen und Parametertext.

> [!NOTE]
> Wenn der Parameter "-VaultId" verwendet wird, sollte auch der Parameter "-VaultLocation" verwendet werden.

**Für die Sicherung der Dateifreigabe in Azure**

Sie können eine gesamte Dateifreigabe oder bestimmte/mehrere Dateien/Ordner auf der Freigabe wiederherstellen. Sie können den ursprünglichen Speicherort oder einen anderen Speicherort wiederherstellen.

**Für Azure Workloads**

Sie können SQL DBs innerhalb von Azure VMs wiederherstellen


## BEISPIELE

### Beispiel 1: Wiederherstellen der Datenträger eines gesicherten verwalteten Datenträgers der Azure VM von einem bestimmten Wiederherstellungspunkt

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

Der erste Befehl ruft den Wiederherstellungsdiensttresor ab und speichert ihn in $vault Variable.
Der zweite Befehl ruft das Sicherungselement vom Typ "AzureVM" mit dem Namen "V2VM" ab und speichert es in der $BackupItem Variable.
Der dritte Befehl ruft das Datum aus sieben Tagen früher ab und speichert es dann in $StartDate Variable.
Der vierte Befehl ruft das aktuelle Datum ab und speichert es dann in der $EndDate Variable.
Der fünfte Befehl ruft eine Liste mit Wiederherstellungspunkten für das spezifische Sicherungselement ab, nach $StartDate und $EndDate.
Mit dem letzten Befehl werden alle Datenträger in der Zielressourcengruppe Target_RG wiederhergestellt. Anschließend werden die Informationen zur VM-Konfiguration und die Bereitstellungsvorlage im Speicherkonto "DestAccount" in der Ressourcengruppe "DestRG" bereitgestellt.

### Beispiel 2: Wiederherstellen angegebener Datenträger eines gesicherten verwalteten Datenträgers der Azure VM von einem bestimmten Wiederherstellungspunkt

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $restoreDiskLUNs = ("0", "1")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -RestoreDiskList $restoreDiskLUNs -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

Der erste Befehl ruft den Wiederherstellungsdiensttresor ab und speichert ihn in $vault Variable.
Der zweite Befehl ruft das Sicherungselement vom Typ "AzureVM" mit dem Namen "V2VM" ab und speichert es in der $BackupItem Variable.
Der dritte Befehl ruft das Datum aus sieben Tagen früher ab und speichert es dann in $StartDate Variable.
Der vierte Befehl ruft das aktuelle Datum ab und speichert es dann in der $EndDate Variable.
Der fünfte Befehl ruft eine Liste mit Wiederherstellungspunkten für das spezifische Sicherungselement ab, nach $StartDate und $EndDate.
Der sechste Befehl speichert die Liste der Datenträger, die in der WiederherstellungsvariablenDiskLUN wiederhergestellt werden sollen.
Der letzte Befehl stellt die angegebenen Datenträger (der angegebenen LUNs) in der Zielressourcengruppe Target_RG wieder dar und stellt dann die Informationen zur VM-Konfiguration und die Bereitstellungsvorlage im Speicherkonto "DestAccount" in der Ressourcengruppe "DestRG" zur Verfügung.

### Beispiel 3: Wiederherstellen von Datenträgern einer verwalteten VM als nicht verwaltete Datenträger

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType "AzureVM" -WorkloadType "AzureVM" -Name "V2VM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -RestoreAsUnmanagedDisks -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

Der erste Befehl ruft den RecoveryServices-Tresor ab und speichert ihn in $vault Variable.
Der zweite Befehl ruft das Sicherungselement ab und speichert es dann in $BackupItem Variable.
Der dritte Befehl ruft das Datum aus sieben Tagen früher ab und speichert es dann in $StartDate Variable.
Der vierte Befehl ruft das aktuelle Datum ab und speichert es dann in der $EndDate Variable.
Der fünfte Befehl ruft eine Liste mit Wiederherstellungspunkten für das spezifische Sicherungselement ab, nach $StartDate und $EndDate.
Mit dem sechsten Befehl werden die Datenträger als nicht verwaltete Datenträger wiederhergestellt.

### Beispiel 4: Wiederherstellen einer nicht verwalteten VM als nicht verwaltete Datenträger mithilfe des ursprünglichen Speicherkontos

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -Name "UnManagedVM" -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -UseOriginalStorageAccount -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

Der erste Befehl ruft den RecoveryServices-Tresor ab und speichert ihn in $vault Variable.
Der zweite Befehl ruft das Sicherungselement ab und speichert es dann in $BackupItem Variable.
Der dritte Befehl ruft das Datum aus sieben Tagen früher ab und speichert es dann in der $StartDate Variable.
Der vierte Befehl ruft das aktuelle Datum ab und speichert es dann in der $EndDate Variable.
Der fünfte Befehl ruft eine Liste mit Wiederherstellungspunkten für das spezifische Sicherungselement ab, nach $StartDate und $EndDate.
Mit dem sechsten Befehl werden die Datenträger als nicht verwaltete Datenträger auf ihren ursprünglichen Speicherkonten wiederhergestellt.

### Beispiel 5: Wiederherstellen mehrerer Dateien eines AzureFileShare-Elements

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureStorage -WorkloadType AzureVM -VaultId $vault.ID -Name "fileshareitem"
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -VaultId $vault.ID
PS C:\> $files = ("file1.txt", "file2.txt")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -MultipleSourceFilePath $files -SourceFileType File -ResolveConflict Overwrite -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    fileshareitem   Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

Der erste Befehl ruft den Wiederherstellungsdiensttresor ab und speichert ihn in $vault Variable.
Der zweite Befehl ruft das Sicherungselement mit dem Namen "fileshareitem" ab und speichert es dann in $BackupItem Variable.
Der dritte Befehl ruft eine Liste mit Wiederherstellungspunkten für das spezifische Sicherungselement ab.
Der vierte Befehl gibt an, welche Dateien wiederhergestellt werden müssen, und speichert sie in $files Variable.
Mit dem letzten Befehl werden die angegebenen Dateien an ihrem ursprünglichen Speicherort wiederhergestellt.

### Beispiel 6: Wiederherstellen eines SQL DB innerhalb einer Azure VM auf eine andere Ziel-VM für einen eindeutigen vollständigen Wiederherstellungspunkt

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureWorkload -WorkloadType MSSQL -VaultId $vault.ID -Name "MSSQLSERVER;model"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $FullRP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $TargetInstance = Get-AzRecoveryServicesBackupProtectableItem -WorkloadType MSSQL -ItemType SQLInstance -Name "<SQLInstance Name>" -ServerName "<SQL VM name>" -VaultId $vault.ID
PS C:\> $AnotherInstanceWithFullConfig = Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -RecoveryPoint $FullRP -TargetItem $TargetInstance -AlternateWorkloadRestore -VaultId $vault.ID
PS C:\> Restore-AzRecoveryServicesBackupItem -WLRecoveryConfig $AnotherInstanceWithLogConfig -VaultId $vault.ID
    WorkloadName       Operation        Status            StartTime                 EndTime          JobID
    ------------       ---------        ------            ---------                 -------          -----
    MSSQLSERVER/m...   Restore          InProgress        3/17/2019 10:02:45 AM                      3274xg2b-e4fg-5952-89b4-8cb566gc1748

```

### Beispiel 7: Wiederherstellen einer SQL-DB innerhalb einer Azure VM auf eine andere Ziel-VM für einen Protokollwiederherstellungspunkt

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureWorkload -WorkloadType MSSQL -VaultId $vault.ID -Name "MSSQLSERVER;model"
PS C:\> $PointInTime = Get-Date -Date "2019-03-20 01:00:00Z"
PS C:\> $TargetInstance = Get-AzRecoveryServicesBackupProtectableItem -WorkloadType MSSQL -ItemType SQLInstance -Name "<SQLInstance Name>" -ServerName "<SQL VM name>" -VaultId $vault.ID
PS C:\> $AnotherInstanceWithLogConfig = Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -PointInTime $PointInTime -Item $BackupItem -AlternateWorkloadRestore -VaultId $vault.ID
PS C:\> Restore-AzRecoveryServicesBackupItem -WLRecoveryConfig $AnotherInstanceWithLogConfig -VaultId $vault.ID
    WorkloadName     Operation      Status           StartTime                 EndTime           JobID
    ------------     ---------      ------           ---------                 -------           -----
    MSSQLSERVER/m... Restore        InProgress       3/17/2019 10:02:45 AM                       3274xg2b-e4fg-5952-89b4-8cb566gc1748

```

## PARAMETERS

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

### -MultipleSourceFilePath
Wird für mehrere Dateien verwendet, die aus einer Dateifreigabe wiederhergestellt werden. Die Pfade der Elemente, die in der Dateifreigabe wiederhergestellt werden sollen.

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

Gibt den Wiederherstellungspunkt an, an dem das Sicherungselement wiederhergestellt werden soll.
Zum Abrufen eines **AzureRmRecoveryServicesBackupRecoveryPoint-Objekts** verwenden Sie das **Cmdlet "Get-AzRecoveryServicesBackupRecoveryPoint".**

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: AzureVMParameterSet, AzureFileParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResolveConflict

Falls das wiederhergestellte Element auch am Ziel vorhanden ist, verwenden Sie diese Option, um anzugeben, ob das Element überschrieben werden soll oder nicht.
Die zulässigen Werte für diesen Parameter sind:

- Überschreiben
- Überspringen

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
Verwenden Sie diesen Schalter, um anzugeben, dass sie als nicht verwaltete Datenträger wiederhergestellt werden

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMRestoreAsUnmanaged
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestoreDiskList
Angeben, welche Datenträger von der gesicherten VM wiederhergestellt werden

```yaml
Type: System.String[]
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestoreOnlyOSDisk
Verwenden Sie diesen Schalter, um nur Betriebssystemdatenträger einer gesicherten VM wiederherzustellen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceFilePath

Wird für die Wiederherstellung eines bestimmten Elements aus einer Dateifreigabe verwendet. Der Pfad des Elements, das in der Dateifreigabe wiederhergestellt werden soll.

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

Wird für die Wiederherstellung eines bestimmten Elements aus einer Dateifreigabe verwendet. Der Typ des Elements, das in der Dateifreigabe wiederhergestellt werden soll.
Die zulässigen Werte für diesen Parameter sind:

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

Gibt den Namen des Zielspeicherkontos in Ihrem Abonnement an.
Im Rahmen des Wiederherstellungsvorgangs speichert dieses Cmdlet die Datenträger und die Konfigurationsinformationen in diesem Speicherkonto.

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountResourceGroupName

Gibt den Namen der Ressourcengruppe an, die das Zielspeicherkonto in Ihrem Abonnement enthält.
Im Rahmen des Wiederherstellungsvorgangs speichert dieses Cmdlet die Datenträger und die Konfigurationsinformationen in diesem Speicherkonto.

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMRestoreAsUnmanaged, AzureVMTargetRGParameterSet, AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetFileShareName

Die Dateifreigabe, auf der die Dateifreigabe wiederhergestellt werden muss.

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

Der Ordner, in dem die Dateifreigabe im TargetFileShareName wiederhergestellt werden muss. Wenn der gesicherte Inhalt in einem Stammordner wiederhergestellt werden soll, geben Sie die Werte für den Zielordner als leere Zeichenfolge an.

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

Die Ressourcengruppe, in die die verwalteten Datenträger wiederhergestellt werden. Gilt für die Sicherung von VM mit verwalteten Datenträgern

```yaml
Type: System.String
Parameter Sets: AzureVMTargetRGParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetStorageAccountName

Das Speicherkonto, auf dem die Dateifreigabe wiederhergestellt werden muss.

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

### -UseAccountStorageAccount

Verwenden Sie diesen Schalter, wenn die Datenträger aus dem Wiederherstellungspunkt auf ihre ursprünglichen Speicherkonten wiederhergestellt werden sollen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMUseOSAParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultId

ARM-ID des Wiederherstellungsdienste-Tresors.

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

Speicherort des Wiederherstellungsdienste-Tresors.

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

### -Confirm

Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

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

### -Waswenn

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase

## AUSGABEN

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Backup-AzRecoveryServicesBackupItem](./Backup-AzRecoveryServicesBackupItem.md)

[Get-AzRecoveryServicesBackupItem](./Get-AzRecoveryServicesBackupItem.md)

[Get-AzRecoveryServicesBackupRecoveryPoint](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
