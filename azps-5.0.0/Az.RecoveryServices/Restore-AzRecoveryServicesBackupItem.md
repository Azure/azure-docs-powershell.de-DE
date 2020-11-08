---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 52e4a9b76adc8c8980ab20951278435894a303bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177418"
---
# <span data-ttu-id="f1a74-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="f1a74-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="f1a74-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f1a74-102">SYNOPSIS</span></span>

<span data-ttu-id="f1a74-103">Wiederherstellen der Daten und der Konfiguration für ein Sicherungselement an einem Wiederherstellungspunkt</span><span class="sxs-lookup"><span data-stu-id="f1a74-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="f1a74-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1a74-104">SYNTAX</span></span>

### <span data-ttu-id="f1a74-105">AzureVMParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f1a74-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1a74-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1a74-106">AzureFileParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1a74-107">AzureVMRestoreAsUnmanaged</span><span class="sxs-lookup"><span data-stu-id="f1a74-107">AzureVMRestoreAsUnmanaged</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1a74-108">AzureVMTargetRGParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1a74-108">AzureVMTargetRGParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-TargetResourceGroupName] <String>
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1a74-109">AzureVMUseOSAParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1a74-109">AzureVMUseOSAParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1a74-110">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1a74-110">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1a74-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1a74-111">DESCRIPTION</span></span>

<span data-ttu-id="f1a74-112">Das Cmdlet **Restore-AzRecoveryServicesBackupItem** stellt die Daten und die Konfiguration für ein Azure Backup-Element an einem angegebenen Wiederherstellungspunkt wieder her.</span><span class="sxs-lookup"><span data-stu-id="f1a74-112">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="f1a74-113">Mit diesem Cmdlet wird die Wiederherstellung aus dem Vault für Wiederherstellungsdienste auf dem Speicherkonto des Kunden gestartet.</span><span class="sxs-lookup"><span data-stu-id="f1a74-113">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="f1a74-114">Beim Wiederherstellungsvorgang wird der vollständige virtuelle Computer nicht wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="f1a74-114">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="f1a74-115">Nachdem der Wiederherstellungsvorgang fertig ist, müssen Sie die verwalteten Datenträger für eine Ziel Ressourcengruppe und die Konfigurationsinformationen für das Kunden Speicherkonto wiederherstellen, indem Sie den virtuellen Computer erstellen und starten.</span><span class="sxs-lookup"><span data-stu-id="f1a74-115">It restores the managed disks to a target resource group and configuration information to customer storage account After the restore operation is finished, you must create the virtual machine and start it.</span></span> <span data-ttu-id="f1a74-116">Bitte refter Sie verschiedene mögliche Parametersätze und Parameter Text, um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f1a74-116">Please refter to different possible parameter sets and parameter text for more information.</span></span>
<span data-ttu-id="f1a74-117">Setzen Sie den Vault-Kontext mithilfe des-Vault-Parameters.</span><span class="sxs-lookup"><span data-stu-id="f1a74-117">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="f1a74-118">Hinweis: zum erfolgreichen Ausführen dieses Cmdlets zusätzlich zu-Vault-VaultLocation-Parameter sollte ebenfalls verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1a74-118">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="f1a74-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1a74-119">EXAMPLES</span></span>

### <span data-ttu-id="f1a74-120">Beispiel 1: Wiederherstellen eines Elements in einem Wiederherstellungspunkt</span><span class="sxs-lookup"><span data-stu-id="f1a74-120">Example 1: Restore an item to a recovery point</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $restoreDiskLUNs = ("0", "1")
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -RestoreDiskList $restoreDiskLUNs -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="f1a74-121">Der erste Befehl ruft den RecoveryServices-Tresor ab und speichert ihn in $Vault Variablen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-121">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="f1a74-122">Der zweite Befehl ruft die Sicherungselemente ab und speichert Sie dann in der $BackupItem Variablen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-122">The second command gets the Backup items and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="f1a74-123">Der dritte Befehl ruft das Datum ab sieben Tage zuvor ab und speichert es dann in der $StartDate Variablen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-123">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="f1a74-124">Der vierte Befehl ruft das aktuelle Datum ab und speichert es dann in der $EndDate Variablen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-124">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="f1a74-125">Der fünfte Befehl ruft eine Liste der Wiederherstellungspunkte für das jeweilige Sicherungselement ab, das nach $StartDate und $EndDate gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="f1a74-125">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="f1a74-126">Der sechste Befehl gibt an, welche Datenträger vom Wiederherstellungspunkt wiederhergestellt werden sollen, und speichert Sie in $restoreDiskLUNs Variablen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-126">The sixth command specifies which disks to restore from the recovery point and stores it in $restoreDiskLUNs variable.</span></span>
<span data-ttu-id="f1a74-127">Mit dem letzten Befehl werden die Datenträger auf dem Zielspeicher Konto DestAccount in der DestRG-Ressourcengruppe wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="f1a74-127">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="f1a74-128">Beispiel 2: Wiederherstellen mehrerer Dateien eines AzureFileShare-Elements</span><span class="sxs-lookup"><span data-stu-id="f1a74-128">Example 2: Restore Multiple files of an AzureFileShare item</span></span>

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

<span data-ttu-id="f1a74-129">Der erste Befehl ruft den Sicherungs Container des Typs AzureVM ab und speichert ihn dann in der $Container Variablen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-129">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="f1a74-130">Der zweite Befehl ruft das Sicherungselement mit dem Namen fileshareitem ab und speichert es dann in der $BackupItem-Variablen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-130">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="f1a74-131">Der dritte Befehl ruft eine Liste der Wiederherstellungspunkte für das jeweilige Sicherungselement ab.</span><span class="sxs-lookup"><span data-stu-id="f1a74-131">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="f1a74-132">Der vierte Befehl spceifies die Dateien, die wiederhergestellt werden sollen, und speichert Sie in $Files Variablen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-132">The fourth command spceifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="f1a74-133">Mit dem letzten Befehl werden die angegebenen Dateien an Ihrem ursprünglichen Speicherort wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="f1a74-133">The last command restores the specified files to its original location.</span></span>

### <span data-ttu-id="f1a74-134">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="f1a74-134">Example 3</span></span>

<span data-ttu-id="f1a74-135">Wiederherstellen der Daten und der Konfiguration für ein Sicherungselement an einem Wiederherstellungspunkt</span><span class="sxs-lookup"><span data-stu-id="f1a74-135">Restores the data and configuration for a Backup item to a recovery point.</span></span> <span data-ttu-id="f1a74-136">automatisch</span><span class="sxs-lookup"><span data-stu-id="f1a74-136">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Restore-AzRecoveryServicesBackupItem -VaultId $vault.ID -WLRecoveryConfig <RecoveryConfigBase>
```
### <span data-ttu-id="f1a74-137">Beispiel 4: Wiederherstellen einer verwalteten VM als verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="f1a74-137">Example 4: Restore a managed VM as managed Disks</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -TargetResourceGroupName "Target_RG" -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="f1a74-138">Der erste Befehl ruft den RecoveryServices-Tresor ab und speichert ihn in $Vault Variablen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-138">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="f1a74-139">Der zweite Befehl ruft das Sicherungselement ab und speichert es dann in der $BackupItem-Variablen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-139">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="f1a74-140">Der dritte Befehl ruft das Datum ab sieben Tage zuvor ab und speichert es dann in der $StartDate Variablen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-140">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="f1a74-141">Der vierte Befehl ruft das aktuelle Datum ab und speichert es dann in der $EndDate Variablen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-141">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="f1a74-142">Der fünfte Befehl ruft eine Liste der Wiederherstellungspunkte für das jeweilige Sicherungselement ab, das nach $StartDate und $EndDate gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="f1a74-142">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="f1a74-143">Der sechste Befehl stellt die Datenträger als verwaltete Datenträger mit der angegebenen Ziel Ressourcengruppe wieder her.</span><span class="sxs-lookup"><span data-stu-id="f1a74-143">The sixth command restores the disks as managed disks with the given target resource group.</span></span>

### <span data-ttu-id="f1a74-144">Beispiel 5: Wiederherstellen einer verwalteten VM als nicht verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="f1a74-144">Example 5: Restore a managed VM as unmanaged Disks</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -RestoreAsUnmanagedDisks -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="f1a74-145">Der erste Befehl ruft den RecoveryServices-Tresor ab und speichert ihn in $Vault Variablen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-145">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="f1a74-146">Der zweite Befehl ruft das Sicherungselement ab und speichert es dann in der $BackupItem-Variablen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-146">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="f1a74-147">Der dritte Befehl ruft das Datum ab sieben Tage zuvor ab und speichert es dann in der $StartDate Variablen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-147">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="f1a74-148">Der vierte Befehl ruft das aktuelle Datum ab und speichert es dann in der $EndDate Variablen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-148">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="f1a74-149">Der fünfte Befehl ruft eine Liste der Wiederherstellungspunkte für das jeweilige Sicherungselement ab, das nach $StartDate und $EndDate gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="f1a74-149">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="f1a74-150">Der sechste Befehl stellt die Datenträger als nicht verwaltete Datenträger wieder her.</span><span class="sxs-lookup"><span data-stu-id="f1a74-150">The sixth command restores the disks as unmanaged disks.</span></span>

### <span data-ttu-id="f1a74-151">Beispiel 6: Wiederherstellen einer nicht verwalteten VM als nicht verwaltete Datenträger unter Verwendung des ursprünglichen speicherkontos</span><span class="sxs-lookup"><span data-stu-id="f1a74-151">Example 6: Restore an unmanaged VM as unmanaged Disks using original storage account.</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -BackupManagementType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem[0] -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -UseOriginalStorageAccount -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="f1a74-152">Der erste Befehl ruft den RecoveryServices-Tresor ab und speichert ihn in $Vault Variablen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-152">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="f1a74-153">Der zweite Befehl ruft das Sicherungselement ab und speichert es dann in der $BackupItem-Variablen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-153">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="f1a74-154">Der dritte Befehl ruft das Datum ab sieben Tage zuvor ab und speichert es dann in der $StartDate Variablen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-154">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="f1a74-155">Der vierte Befehl ruft das aktuelle Datum ab und speichert es dann in der $EndDate Variablen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-155">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="f1a74-156">Der fünfte Befehl ruft eine Liste der Wiederherstellungspunkte für das jeweilige Sicherungselement ab, das nach $StartDate und $EndDate gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="f1a74-156">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="f1a74-157">Der sechste Befehl stellt die Datenträger als nicht verwaltete Datenträger unter Verwendung des ursprünglichen speicherkontos des virtuellen Computers wieder her.</span><span class="sxs-lookup"><span data-stu-id="f1a74-157">The sixth command restores the disks as unmanaged disks using the original storage account of the VM.</span></span>

## <span data-ttu-id="f1a74-158">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1a74-158">PARAMETERS</span></span>

### <span data-ttu-id="f1a74-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1a74-159">-DefaultProfile</span></span>

<span data-ttu-id="f1a74-160">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f1a74-160">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1a74-161">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="f1a74-161">-MultipleSourceFilePath</span></span>
<span data-ttu-id="f1a74-162">Wird für die Wiederherstellung mehrerer Dateien aus einer Dateifreigabe verwendet.</span><span class="sxs-lookup"><span data-stu-id="f1a74-162">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="f1a74-163">Die Pfade der Elemente, die in der Dateifreigabe wiederhergestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-163">The paths of the items to be restored within the file share.</span></span>

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

### <span data-ttu-id="f1a74-164">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="f1a74-164">-RecoveryPoint</span></span>

<span data-ttu-id="f1a74-165">Gibt den Wiederherstellungspunkt an, für den das Sicherungselement wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1a74-165">Specifies the recovery point to which to restore the backup item.</span></span>
<span data-ttu-id="f1a74-166">Verwenden Sie das Cmdlet **Get-AzRecoveryServicesBackupRecoveryPoint** , um ein **AzureRmRecoveryServicesBackupRecoveryPoint** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-166">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

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

### <span data-ttu-id="f1a74-167">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="f1a74-167">-ResolveConflict</span></span>

<span data-ttu-id="f1a74-168">Wenn das wiederhergestellte Element auch im Ziel vorhanden ist, verwenden Sie diese Option, um anzugeben, ob Sie überschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-168">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="f1a74-169">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f1a74-169">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f1a74-170">Überschreiben</span><span class="sxs-lookup"><span data-stu-id="f1a74-170">Overwrite</span></span>
- <span data-ttu-id="f1a74-171">Skip</span><span class="sxs-lookup"><span data-stu-id="f1a74-171">Skip</span></span>

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

### <span data-ttu-id="f1a74-172">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="f1a74-172">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="f1a74-173">Verwenden Sie diese Option, um anzugeben, dass Sie als nicht verwaltete Datenträger wiederhergestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-173">Use this switch to specify to restore as unmanaged disks</span></span>

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

### <span data-ttu-id="f1a74-174">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="f1a74-174">-RestoreDiskList</span></span>
<span data-ttu-id="f1a74-175">Angeben, welche Datenträger von der gesicherten VM wiederhergestellt werden sollen</span><span class="sxs-lookup"><span data-stu-id="f1a74-175">Specify which disks to recover of the backed up VM</span></span>

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

### <span data-ttu-id="f1a74-176">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="f1a74-176">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="f1a74-177">Verwenden Sie diese Option, um nur Betriebssystemdatenträger einer gesicherten VM wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-177">Use this switch to restore only OS disks of a backed up VM</span></span>

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

### <span data-ttu-id="f1a74-178">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="f1a74-178">-SourceFilePath</span></span>

<span data-ttu-id="f1a74-179">Wird für eine bestimmte Elementwiederherstellung aus einer Dateifreigabe verwendet.</span><span class="sxs-lookup"><span data-stu-id="f1a74-179">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="f1a74-180">Der Pfad des Elements, das innerhalb der Dateifreigabe wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1a74-180">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="f1a74-181">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="f1a74-181">-SourceFileType</span></span>

<span data-ttu-id="f1a74-182">Wird für eine bestimmte Elementwiederherstellung aus einer Dateifreigabe verwendet.</span><span class="sxs-lookup"><span data-stu-id="f1a74-182">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="f1a74-183">Der Typ des Elements, das innerhalb der Dateifreigabe wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1a74-183">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="f1a74-184">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f1a74-184">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f1a74-185">Datei</span><span class="sxs-lookup"><span data-stu-id="f1a74-185">File</span></span>
- <span data-ttu-id="f1a74-186">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="f1a74-186">Directory</span></span>

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

### <span data-ttu-id="f1a74-187">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f1a74-187">-StorageAccountName</span></span>

<span data-ttu-id="f1a74-188">Gibt den Namen des Zielspeicher Kontos in Ihrem Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="f1a74-188">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="f1a74-189">Im Rahmen des Wiederherstellungsvorgangs speichert dieses Cmdlet die Datenträger und die Konfigurationsinformationen in diesem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="f1a74-189">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="f1a74-190">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1a74-190">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="f1a74-191">Gibt den Namen der Ressourcengruppe an, die das Zielspeicher Konto in Ihrem Abonnement enthält.</span><span class="sxs-lookup"><span data-stu-id="f1a74-191">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="f1a74-192">Im Rahmen des Wiederherstellungsvorgangs speichert dieses Cmdlet die Datenträger und die Konfigurationsinformationen in diesem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="f1a74-192">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="f1a74-193">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="f1a74-193">-TargetFileShareName</span></span>

<span data-ttu-id="f1a74-194">Die Dateifreigabe, in der die Dateifreigabe wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1a74-194">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="f1a74-195">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="f1a74-195">-TargetFolder</span></span>

<span data-ttu-id="f1a74-196">Der Ordner, in dem die Dateifreigabe innerhalb des TargetFileShareName wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1a74-196">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="f1a74-197">Wenn der gesicherte Inhalt in einem Stammordner wiederhergestellt werden soll, geben Sie die Werte für den Zielordner als leere Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="f1a74-197">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="f1a74-198">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1a74-198">-TargetResourceGroupName</span></span>

<span data-ttu-id="f1a74-199">Die Ressourcengruppe, in der die verwalteten Datenträger wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f1a74-199">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="f1a74-200">Anwendbar auf eine Sicherung von VM mit verwalteten Datenträgern</span><span class="sxs-lookup"><span data-stu-id="f1a74-200">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="f1a74-201">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f1a74-201">-TargetStorageAccountName</span></span>

<span data-ttu-id="f1a74-202">Das Speicherkonto, in dem die Dateifreigabe wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1a74-202">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="f1a74-203">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1a74-203">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="f1a74-204">Verwenden Sie diese Option, wenn die Datenträger des Wiederherstellungspunkts auf ihren ursprünglichen Speicherkonten wiederhergestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-204">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="f1a74-205">-Tresor</span><span class="sxs-lookup"><span data-stu-id="f1a74-205">-VaultId</span></span>

<span data-ttu-id="f1a74-206">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="f1a74-206">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="f1a74-207">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="f1a74-207">-VaultLocation</span></span>

<span data-ttu-id="f1a74-208">Der Speicherort des Speichers für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="f1a74-208">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="f1a74-209">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="f1a74-209">-WLRecoveryConfig</span></span>

<span data-ttu-id="f1a74-210">Wiederherstellungskonfiguration</span><span class="sxs-lookup"><span data-stu-id="f1a74-210">Recovery config</span></span>

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

### <span data-ttu-id="f1a74-211">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f1a74-211">-Confirm</span></span>

<span data-ttu-id="f1a74-212">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-212">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1a74-213">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1a74-213">-WhatIf</span></span>

<span data-ttu-id="f1a74-214">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1a74-214">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="f1a74-215">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1a74-215">CommonParameters</span></span>
<span data-ttu-id="f1a74-216">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1a74-216">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1a74-217">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1a74-217">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1a74-218">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f1a74-218">INPUTS</span></span>

### <span data-ttu-id="f1a74-219">System. String</span><span class="sxs-lookup"><span data-stu-id="f1a74-219">System.String</span></span>

### <span data-ttu-id="f1a74-220">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="f1a74-220">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="f1a74-221">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f1a74-221">OUTPUTS</span></span>

### <span data-ttu-id="f1a74-222">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="f1a74-222">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="f1a74-223">Notizen</span><span class="sxs-lookup"><span data-stu-id="f1a74-223">NOTES</span></span>

## <span data-ttu-id="f1a74-224">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f1a74-224">RELATED LINKS</span></span>

[<span data-ttu-id="f1a74-225">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="f1a74-225">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="f1a74-226">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="f1a74-226">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="f1a74-227">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="f1a74-227">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
