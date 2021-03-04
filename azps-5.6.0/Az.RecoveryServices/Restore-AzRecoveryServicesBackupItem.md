---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 3d3cbb196a287e24837c0e7b0e61b16eaa06ce95
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942307"
---
# <span data-ttu-id="544bf-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="544bf-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="544bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="544bf-102">SYNOPSIS</span></span>

<span data-ttu-id="544bf-103">Stellt die Daten und die Konfiguration für ein Sicherungselement auf dem angegebenen Wiederherstellungspunkt wieder her.</span><span class="sxs-lookup"><span data-stu-id="544bf-103">Restores the data and configuration for a Backup item to the specified recovery point.</span></span> <span data-ttu-id="544bf-104">Die erforderlichen Parameter variieren je nach Sicherungselementtyp.</span><span class="sxs-lookup"><span data-stu-id="544bf-104">The required parameters vary with the backup item type.</span></span>
<span data-ttu-id="544bf-105">Derselbe Befehl wird auch verwendet, um virtuelle Azure-Computer, Datenbanken, die auf virtuellen Azure-Computern ausgeführt werden, und Azure-Dateifreigaben wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="544bf-105">The same command is used to restore Azure Virtual machines, databases running within Azure Virtual machines and Azure file shares as well.</span></span>

## <span data-ttu-id="544bf-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="544bf-106">SYNTAX</span></span>

### <span data-ttu-id="544bf-107">AzureVMParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="544bf-107">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-DiskEncryptionSetId <string>] [-RestoreToSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="544bf-108">AzureVMManagedDiskParameterSet</span><span class="sxs-lookup"><span data-stu-id="544bf-108">AzureVMManagedDiskParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-TargetResourceGroupName] <String>
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-DiskEncryptionSetId <string>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="544bf-109">AzureVMRestoreManagedAsUnmanaged</span><span class="sxs-lookup"><span data-stu-id="544bf-109">AzureVMRestoreManagedAsUnmanaged</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="544bf-110">AzureVMUnManagedDiskParameterSet</span><span class="sxs-lookup"><span data-stu-id="544bf-110">AzureVMUnManagedDiskParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="544bf-111">AzureFileShareParameterSet</span><span class="sxs-lookup"><span data-stu-id="544bf-111">AzureFileShareParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-RestoreToSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="544bf-112">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="544bf-112">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase> [-RestoreToSecondaryRegion]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="544bf-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="544bf-113">DESCRIPTION</span></span>

<span data-ttu-id="544bf-114">Das **Cmdlet Restore-AzRecoveryServicesBackupItem** stellt die Daten und die Konfiguration für ein Azure Backup-Element auf einem angegebenen Wiederherstellungspunkt wieder her.</span><span class="sxs-lookup"><span data-stu-id="544bf-114">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>

<span data-ttu-id="544bf-115">**Für azure vm backup**</span><span class="sxs-lookup"><span data-stu-id="544bf-115">**For Azure VM  backup**</span></span>

<span data-ttu-id="544bf-116">Mit diesem Befehl können Sie virtuelle Azure-Computer sichern und Datenträger (sowohl verwaltet als auch nicht verwaltet) wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="544bf-116">You can backup Azure virtual machines and restore disks (both managed and un-managed) using this command.</span></span> <span data-ttu-id="544bf-117">Der Wiederherstellungsvorgang stellt nicht den vollständigen virtuellen Computer wiederher.</span><span class="sxs-lookup"><span data-stu-id="544bf-117">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="544bf-118">Wenn es sich um eine verwaltete Datenträger-VM handelt, sollte eine Zielressourcengruppe angegeben werden, in der die wiederhergestellten Datenträger aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="544bf-118">If this is a managed disk VM, a target Resource group should be specified where the restored disks are kept.</span></span> <span data-ttu-id="544bf-119">Wenn die Zielressourcengruppe angegeben wird, wenn die Momentaufnahmen in der Ressourcengruppe vorhanden sind, die in der Sicherungsrichtlinie angegeben wurde, wird der Wiederherstellungsvorgang sofort ausgeführt, und die Datenträger werden aus lokalen Momentaufnahmen erstellt und in der Zielressourcengruppe gespeichert.</span><span class="sxs-lookup"><span data-stu-id="544bf-119">When target resource group is specified, if the snapshots are present in the resource group that was specified in backup policy, the restore operation will be instant and the disks are created from local snapshots and kept in target-resource group.</span></span> <span data-ttu-id="544bf-120">Es gibt auch eine Option, um sie als nicht verwaltete Datenträger wiederherzustellen, dies nutzt jedoch die im Azure Recovery Services-Tresor vorhandenen Daten und wird daher viel langsamer sein.</span><span class="sxs-lookup"><span data-stu-id="544bf-120">There is also an option to restore them as un-managed disks but this will leverage the data present in Azure recovery services vault and hence will be lot slower.</span></span> <span data-ttu-id="544bf-121">Die Konfiguration der VM und die Bereitstellungsvorlage, mit der vm aus den wiederhergestellten Datenträgern erstellt werden kann, werden in das angegebene Speicherkonto heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="544bf-121">The configuration of the VM and the deployment template which can be used to create VM out of the restored disks will be downloaded to the specified storage account.</span></span>
<span data-ttu-id="544bf-122">Wenn es sich um eine nicht verwaltete Datenträger-VM handelt, sind die Momentaufnahmen im ursprünglichen Speicherkonto des Datenträgers und/oder im Wiederherstellungsdienste-Tresor vorhanden.</span><span class="sxs-lookup"><span data-stu-id="544bf-122">If this is an un-managed disk VM, then the snapshots are present in disk's original storage account and/or in the recovery services vault.</span></span> <span data-ttu-id="544bf-123">Wenn der Benutzer eine Option zum Wiederherstellen des ursprünglichen Speicherkontos bietet, kann die sofortige Wiederherstellung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="544bf-123">If user gives an option to use Original storage account to restore, then instant restore can be provided.</span></span> <span data-ttu-id="544bf-124">Andernfalls werden Daten aus dem Azure Recovery Services-Tresor abgerufen, und Datenträger werden zusammen mit der Konfiguration der VM und der Bereitstellungsvorlage in einem angegebenen Speicherkonto erstellt.</span><span class="sxs-lookup"><span data-stu-id="544bf-124">Otherwise, data is fetched from Azure Recovery services vault and disks are created in specified storage account along with the configuration of the VM and the deployment template.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="544bf-125">Standardmäßig werden mit der Azure VM-Sicherung alle Datenträger gesichert.</span><span class="sxs-lookup"><span data-stu-id="544bf-125">By default, Azure VM backup backs up all disks.</span></span> <span data-ttu-id="544bf-126">Sie können relevante Datenträger selektiv sichern, indem Sie die Parameter exclusionList oder InclusionList während der Enable-Backup-Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="544bf-126">You can selectively backup relevant disks using the exclusionList or InclusionList parameters during Enable-Backup.</span></span> <span data-ttu-id="544bf-127">Die Option zum selektiven Wiederherstellen von Datenträgern ist nur verfügbar, wenn sie selektiv gesichert wurden.</span><span class="sxs-lookup"><span data-stu-id="544bf-127">The option to selectively restore disks is available only if one has selectively backed them up.</span></span>

<span data-ttu-id="544bf-128">Weitere Informationen finden Sie unter verschiedenen möglichen Parametersätzen und Parametertext.</span><span class="sxs-lookup"><span data-stu-id="544bf-128">Please refer to different possible parameter sets and parameter text for more information.</span></span>

> [!NOTE]
> <span data-ttu-id="544bf-129">Wenn der Parameter -VaultId verwendet wird, sollte auch der Parameter -VaultLocation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="544bf-129">If -VaultId parameter is used then -VaultLocation parameter should be used as well.</span></span>

<span data-ttu-id="544bf-130">**Für azure file share backup**</span><span class="sxs-lookup"><span data-stu-id="544bf-130">**For Azure File share backup**</span></span>

<span data-ttu-id="544bf-131">Sie können eine gesamte Dateifreigabe oder bestimmte/mehrere Dateien/Ordner für die Freigabe wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="544bf-131">You can restore an entire file share or specific/multiple files/folders on the share.</span></span> <span data-ttu-id="544bf-132">Sie können den ursprünglichen Speicherort oder einen anderen Speicherort wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="544bf-132">You can restore to the original location or to an alternate location.</span></span>

<span data-ttu-id="544bf-133">**Für Azure Workloads**</span><span class="sxs-lookup"><span data-stu-id="544bf-133">**For Azure Workloads**</span></span>

<span data-ttu-id="544bf-134">Sie können SQL in Azure VMs wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="544bf-134">You can restore SQL DBs within Azure VMs</span></span>


## <span data-ttu-id="544bf-135">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="544bf-135">EXAMPLES</span></span>

### <span data-ttu-id="544bf-136">Beispiel 1: Wiederherstellen der Datenträger eines gesicherten verwalteten Datenträgers Azure VM von einem bestimmten Wiederherstellungspunkt</span><span class="sxs-lookup"><span data-stu-id="544bf-136">Example 1: Restore the disks of a backed up Managed disk Azure VM from a given recovery point</span></span>

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

<span data-ttu-id="544bf-137">Der erste Befehl ruft den Recovery Services-Tresor ab und speichert ihn in $vault Variablen.</span><span class="sxs-lookup"><span data-stu-id="544bf-137">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="544bf-138">Der zweite Befehl ruft das Sicherungselement vom Typ AzureVM des Namens "V2VM" ab und speichert es in der $BackupItem Variablen.</span><span class="sxs-lookup"><span data-stu-id="544bf-138">The second command gets the Backup item of type AzureVM, of the name "V2VM", and stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="544bf-139">Der dritte Befehl ruft das Datum aus sieben Tagen früher ab und speichert es dann in der $StartDate Variablen.</span><span class="sxs-lookup"><span data-stu-id="544bf-139">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="544bf-140">Der vierte Befehl ruft das aktuelle Datum ab und speichert es dann in der $EndDate Variablen.</span><span class="sxs-lookup"><span data-stu-id="544bf-140">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="544bf-141">Der fünfte Befehl ruft eine Liste der Wiederherstellungspunkte für das bestimmte Sicherungselement ab, das nach $StartDate und $EndDate.</span><span class="sxs-lookup"><span data-stu-id="544bf-141">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="544bf-142">Mit dem letzten Befehl werden alle Datenträger in der Zielressourcengruppe Target_RG wiederhergestellt und dann die VM-Konfigurationsinformationen und die Bereitstellungsvorlage im Speicherkonto DestAccount in der Ressourcengruppe DestRG bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="544bf-142">The last command restores all the disks to the target Resource group Target_RG, and then provides the VM configuration information and the deployment template in the storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="544bf-143">Beispiel 2: Wiederherstellen angegebener Datenträger eines gesicherten verwalteten Datenträgers Azure VM von einem bestimmten Wiederherstellungspunkt</span><span class="sxs-lookup"><span data-stu-id="544bf-143">Example 2: Restore specified disks of a backed up Managed disk Azure VM from a given recovery point</span></span>

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

<span data-ttu-id="544bf-144">Der erste Befehl ruft den Recovery Services-Tresor ab und speichert ihn in $vault Variablen.</span><span class="sxs-lookup"><span data-stu-id="544bf-144">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="544bf-145">Der zweite Befehl ruft das Sicherungselement vom Typ AzureVM des Namens "V2VM" ab und speichert es in der $BackupItem Variablen.</span><span class="sxs-lookup"><span data-stu-id="544bf-145">The second command gets the Backup item of type AzureVM, of the name "V2VM", and stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="544bf-146">Der dritte Befehl ruft das Datum aus sieben Tagen früher ab und speichert es dann in der $StartDate Variablen.</span><span class="sxs-lookup"><span data-stu-id="544bf-146">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="544bf-147">Der vierte Befehl ruft das aktuelle Datum ab und speichert es dann in der $EndDate Variablen.</span><span class="sxs-lookup"><span data-stu-id="544bf-147">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="544bf-148">Der fünfte Befehl ruft eine Liste der Wiederherstellungspunkte für das bestimmte Sicherungselement ab, das nach $StartDate und $EndDate.</span><span class="sxs-lookup"><span data-stu-id="544bf-148">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="544bf-149">Der sechste Befehl speichert die Liste der Datenträger, die in der Variablen RestoreDiskLUN wiederhergestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="544bf-149">The sixth command stores the list of disks to be restored in the restoreDiskLUN variable.</span></span>
<span data-ttu-id="544bf-150">Mit dem letzten Befehl werden die angegebenen Datenträger der angegebenen LUNs in der Zielressourcengruppe Target_RG wiederhergestellt und dann die VM-Konfigurationsinformationen und die Bereitstellungsvorlage im Speicherkonto DestAccount in der Ressourcengruppe DestRG bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="544bf-150">The last command restores the given disks, of the specified LUNs, to the target Resource group Target_RG, and then provides the VM configuration information and the deployment template in the storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="544bf-151">Beispiel 3: Wiederherstellen von Datenträgern einer verwalteten VM als nicht verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="544bf-151">Example 3: Restore disks of a managed VM as unmanaged Disks</span></span>

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

<span data-ttu-id="544bf-152">Der erste Befehl ruft den RecoveryServices-Tresor ab und speichert ihn in $vault Variablen.</span><span class="sxs-lookup"><span data-stu-id="544bf-152">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="544bf-153">Der zweite Befehl ruft das Sicherungselement ab und speichert es dann in der $BackupItem Variablen.</span><span class="sxs-lookup"><span data-stu-id="544bf-153">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="544bf-154">Der dritte Befehl ruft das Datum aus sieben Tagen früher ab und speichert es dann in der $StartDate Variablen.</span><span class="sxs-lookup"><span data-stu-id="544bf-154">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="544bf-155">Der vierte Befehl ruft das aktuelle Datum ab und speichert es dann in der $EndDate Variablen.</span><span class="sxs-lookup"><span data-stu-id="544bf-155">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="544bf-156">Der fünfte Befehl ruft eine Liste der Wiederherstellungspunkte für das bestimmte Sicherungselement ab, das nach $StartDate und $EndDate.</span><span class="sxs-lookup"><span data-stu-id="544bf-156">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="544bf-157">Mit dem sechsten Befehl werden die Datenträger als nicht verwaltete Datenträger wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="544bf-157">The sixth command restores the disks as unmanaged disks.</span></span>

### <span data-ttu-id="544bf-158">Beispiel 4: Wiederherstellen einer nicht verwalteten VM als nicht verwaltete Datenträger mithilfe des ursprünglichen Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="544bf-158">Example 4: Restore an unmanaged VM as unmanaged Disks using original storage account</span></span>

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

<span data-ttu-id="544bf-159">Der erste Befehl ruft den RecoveryServices-Tresor ab und speichert ihn in $vault Variablen.</span><span class="sxs-lookup"><span data-stu-id="544bf-159">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="544bf-160">Der zweite Befehl ruft das Sicherungselement ab und speichert es dann in der $BackupItem Variablen.</span><span class="sxs-lookup"><span data-stu-id="544bf-160">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="544bf-161">Der dritte Befehl ruft das Datum aus sieben Tagen früher ab und speichert es dann in der $StartDate Variablen.</span><span class="sxs-lookup"><span data-stu-id="544bf-161">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="544bf-162">Der vierte Befehl ruft das aktuelle Datum ab und speichert es dann in der $EndDate Variablen.</span><span class="sxs-lookup"><span data-stu-id="544bf-162">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="544bf-163">Der fünfte Befehl ruft eine Liste der Wiederherstellungspunkte für das bestimmte Sicherungselement ab, das nach $StartDate und $EndDate.</span><span class="sxs-lookup"><span data-stu-id="544bf-163">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="544bf-164">Mit dem sechsten Befehl werden die Datenträger als nicht verwaltete Datenträger in ihren ursprünglichen Speicherkonten wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="544bf-164">The sixth command restores the disks as unmanaged disks to their original storage accounts</span></span>

### <span data-ttu-id="544bf-165">Beispiel 5: Wiederherstellen mehrerer Dateien eines AzureFileShare-Elements</span><span class="sxs-lookup"><span data-stu-id="544bf-165">Example 5: Restore Multiple files of an AzureFileShare item</span></span>

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

<span data-ttu-id="544bf-166">Der erste Befehl ruft den Recovery Services-Tresor ab und speichert ihn in $vault Variablen.</span><span class="sxs-lookup"><span data-stu-id="544bf-166">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="544bf-167">Der zweite Befehl ruft das Sicherungselement mit dem Namen fileshareitem ab und speichert es dann in der $BackupItem Variablen.</span><span class="sxs-lookup"><span data-stu-id="544bf-167">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="544bf-168">Der dritte Befehl ruft eine Liste der Wiederherstellungspunkte für das bestimmte Sicherungselement ab.</span><span class="sxs-lookup"><span data-stu-id="544bf-168">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="544bf-169">Der vierte Befehl gibt an, welche Dateien wiederhergestellt und in $files gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="544bf-169">The fourth command specifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="544bf-170">Mit dem letzten Befehl werden die angegebenen Dateien an ihrem ursprünglichen Speicherort wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="544bf-170">The last command restores the specified files to its original location.</span></span>

### <span data-ttu-id="544bf-171">Beispiel 6: Wiederherstellen eines SQL DB innerhalb einer Azure-VM auf einer anderen Ziel-VM für einen eindeutig vollständigen Wiederherstellungspunkt</span><span class="sxs-lookup"><span data-stu-id="544bf-171">Example 6: Restore a SQL DB within an Azure VM to another target VM for a distinct full recovery point</span></span>

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

### <span data-ttu-id="544bf-172">Beispiel 7: Wiederherstellen eines SQL-DB innerhalb einer Azure-VM auf einer anderen Ziel-VM für einen Protokollwiederherstellungspunkt</span><span class="sxs-lookup"><span data-stu-id="544bf-172">Example 7: Restore a SQL DB within an Azure VM to another target VM for a log recovery point</span></span>

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

## <span data-ttu-id="544bf-173">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="544bf-173">PARAMETERS</span></span>

### <span data-ttu-id="544bf-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="544bf-174">-DefaultProfile</span></span>

<span data-ttu-id="544bf-175">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="544bf-175">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="544bf-176">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="544bf-176">-MultipleSourceFilePath</span></span>
<span data-ttu-id="544bf-177">Wird für mehrere Dateien verwendet, die aus einer Dateifreigabe wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="544bf-177">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="544bf-178">Die Pfade der Elemente, die innerhalb der Dateifreigabe wiederhergestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="544bf-178">The paths of the items to be restored within the file share.</span></span>

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

### <span data-ttu-id="544bf-179">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="544bf-179">-RecoveryPoint</span></span>

<span data-ttu-id="544bf-180">Gibt den Wiederherstellungspunkt an, an dem das Sicherungselement wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="544bf-180">Specifies the recovery point to which to restore the backup item.</span></span>
<span data-ttu-id="544bf-181">Zum Abrufen eines **AzureRmRecoveryServicesBackupRecoveryPoint-Objekts** verwenden Sie das **Get-AzRecoveryServicesBackupRecoveryPoint-Cmdlet.**</span><span class="sxs-lookup"><span data-stu-id="544bf-181">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

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

### <span data-ttu-id="544bf-182">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="544bf-182">-ResolveConflict</span></span>

<span data-ttu-id="544bf-183">Falls das wiederhergestellte Element auch im Ziel vorhanden ist, verwenden Sie diese Option, um anzugeben, ob überschrieben werden soll oder nicht.</span><span class="sxs-lookup"><span data-stu-id="544bf-183">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="544bf-184">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="544bf-184">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="544bf-185">Überschreiben</span><span class="sxs-lookup"><span data-stu-id="544bf-185">Overwrite</span></span>
- <span data-ttu-id="544bf-186">Überspringen</span><span class="sxs-lookup"><span data-stu-id="544bf-186">Skip</span></span>

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

### <span data-ttu-id="544bf-187">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="544bf-187">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="544bf-188">Verwenden Sie diesen Schalter, um anzugeben, wie nicht verwaltete Datenträger wiederhergestellt werden</span><span class="sxs-lookup"><span data-stu-id="544bf-188">Use this switch to specify to restore as unmanaged disks</span></span>

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

### <span data-ttu-id="544bf-189">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="544bf-189">-RestoreDiskList</span></span>
<span data-ttu-id="544bf-190">Angeben der Datenträger, die von der gesicherten VM wiederhergestellt werden müssen</span><span class="sxs-lookup"><span data-stu-id="544bf-190">Specify which disks to recover of the backed up VM</span></span>

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

### <span data-ttu-id="544bf-191">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="544bf-191">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="544bf-192">Verwenden sie diesen Schalter, um nur Betriebssystemdatenträger einer gesicherten VM wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="544bf-192">Use this switch to restore only OS disks of a backed up VM</span></span>

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

### <span data-ttu-id="544bf-193">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="544bf-193">-SourceFilePath</span></span>

<span data-ttu-id="544bf-194">Wird für die Wiederherstellung eines bestimmten Elements aus einer Dateifreigabe verwendet.</span><span class="sxs-lookup"><span data-stu-id="544bf-194">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="544bf-195">Der Pfad des Elements, das innerhalb der Dateifreigabe wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="544bf-195">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="544bf-196">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="544bf-196">-SourceFileType</span></span>

<span data-ttu-id="544bf-197">Wird für die Wiederherstellung eines bestimmten Elements aus einer Dateifreigabe verwendet.</span><span class="sxs-lookup"><span data-stu-id="544bf-197">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="544bf-198">Der Typ des Elements, das innerhalb der Dateifreigabe wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="544bf-198">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="544bf-199">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="544bf-199">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="544bf-200">Datei</span><span class="sxs-lookup"><span data-stu-id="544bf-200">File</span></span>
- <span data-ttu-id="544bf-201">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="544bf-201">Directory</span></span>

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

### <span data-ttu-id="544bf-202">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="544bf-202">-StorageAccountName</span></span>

<span data-ttu-id="544bf-203">Gibt den Namen des Zielspeicherkontos in Ihrem Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="544bf-203">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="544bf-204">Im Rahmen des Wiederherstellungsvorgangs werden in diesem Cmdlet die Datenträger und die Konfigurationsinformationen in diesem Speicherkonto gespeichert.</span><span class="sxs-lookup"><span data-stu-id="544bf-204">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="544bf-205">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="544bf-205">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="544bf-206">Gibt den Namen der Ressourcengruppe an, die das Zielspeicherkonto in Ihrem Abonnement enthält.</span><span class="sxs-lookup"><span data-stu-id="544bf-206">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="544bf-207">Im Rahmen des Wiederherstellungsvorgangs werden in diesem Cmdlet die Datenträger und die Konfigurationsinformationen in diesem Speicherkonto gespeichert.</span><span class="sxs-lookup"><span data-stu-id="544bf-207">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="544bf-208">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="544bf-208">-TargetFileShareName</span></span>

<span data-ttu-id="544bf-209">Die Dateifreigabe, auf die die Dateifreigabe wiederhergestellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="544bf-209">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="544bf-210">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="544bf-210">-TargetFolder</span></span>

<span data-ttu-id="544bf-211">Der Ordner, in dem die Dateifreigabe im TargetFileShareName wiederhergestellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="544bf-211">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="544bf-212">Wenn der gesicherte Inhalt in einem Stammordner wiederhergestellt werden soll, geben Sie den Zielordnerwerten eine leere Zeichenfolge zu.</span><span class="sxs-lookup"><span data-stu-id="544bf-212">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="544bf-213">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="544bf-213">-TargetResourceGroupName</span></span>

<span data-ttu-id="544bf-214">Die Ressourcengruppe, in der die verwalteten Datenträger wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="544bf-214">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="544bf-215">Anwendbar auf die Sicherung von VM mit verwalteten Datenträgern</span><span class="sxs-lookup"><span data-stu-id="544bf-215">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="544bf-216">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="544bf-216">-TargetStorageAccountName</span></span>

<span data-ttu-id="544bf-217">Das Speicherkonto, auf dem die Dateifreigabe wiederhergestellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="544bf-217">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="544bf-218">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="544bf-218">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="544bf-219">Verwenden Sie diesen Schalter, wenn die Datenträger vom Wiederherstellungspunkt in ihren ursprünglichen Speicherkonten wiederhergestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="544bf-219">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="544bf-220">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="544bf-220">-DiskEncryptionSetId</span></span> 

<span data-ttu-id="544bf-221">Die DES-ID zum Verschlüsseln der wiederhergestellten Datenträger.</span><span class="sxs-lookup"><span data-stu-id="544bf-221">The DES ID to encrypt the restored disks.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet, AzureVMManagedDiskParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="544bf-222">-RestoreToSecondaryRegion</span><span class="sxs-lookup"><span data-stu-id="544bf-222">-RestoreToSecondaryRegion</span></span>

<span data-ttu-id="544bf-223">Verwenden Sie diesen Schalter, um die Wiederherstellen des Kreuzbereichs in den sekundären Bereich auszulösen.</span><span class="sxs-lookup"><span data-stu-id="544bf-223">Use this switch to trigger the Cross region restore to secondary region.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureIaasVM
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="544bf-224">-VaultId</span><span class="sxs-lookup"><span data-stu-id="544bf-224">-VaultId</span></span>

<span data-ttu-id="544bf-225">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="544bf-225">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="544bf-226">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="544bf-226">-VaultLocation</span></span>

<span data-ttu-id="544bf-227">Speicherort des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="544bf-227">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="544bf-228">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="544bf-228">-WLRecoveryConfig</span></span>

<span data-ttu-id="544bf-229">Wiederherstellungskonfiguration</span><span class="sxs-lookup"><span data-stu-id="544bf-229">Recovery config</span></span>

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

### <span data-ttu-id="544bf-230">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="544bf-230">-Confirm</span></span>

<span data-ttu-id="544bf-231">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="544bf-231">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="544bf-232">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="544bf-232">-WhatIf</span></span>

<span data-ttu-id="544bf-233">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="544bf-233">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="544bf-234">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="544bf-234">CommonParameters</span></span>
<span data-ttu-id="544bf-235">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="544bf-235">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="544bf-236">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="544bf-236">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="544bf-237">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="544bf-237">INPUTS</span></span>

### <span data-ttu-id="544bf-238">System.String</span><span class="sxs-lookup"><span data-stu-id="544bf-238">System.String</span></span>

### <span data-ttu-id="544bf-239">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="544bf-239">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="544bf-240">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="544bf-240">OUTPUTS</span></span>

### <span data-ttu-id="544bf-241">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="544bf-241">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="544bf-242">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="544bf-242">NOTES</span></span>

## <span data-ttu-id="544bf-243">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="544bf-243">RELATED LINKS</span></span>

[<span data-ttu-id="544bf-244">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="544bf-244">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="544bf-245">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="544bf-245">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="544bf-246">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="544bf-246">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
