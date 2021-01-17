---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 32ecad0d89725d4fa01d76ebfe9a319dfece6b80
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459704"
---
# <span data-ttu-id="5a430-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="5a430-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="5a430-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a430-102">SYNOPSIS</span></span>

<span data-ttu-id="5a430-103">Stellt die Daten und die Konfiguration für ein Sicherungselement auf dem angegebenen Wiederherstellungspunkt wieder her.</span><span class="sxs-lookup"><span data-stu-id="5a430-103">Restores the data and configuration for a Backup item to the specified recovery point.</span></span> <span data-ttu-id="5a430-104">Die erforderlichen Parameter variieren je nach Typ des Sicherungselements.</span><span class="sxs-lookup"><span data-stu-id="5a430-104">The required parameters vary with the backup item type.</span></span>
<span data-ttu-id="5a430-105">Derselbe Befehl wird zum Wiederherstellen virtueller Azure-Computer, von Datenbanken, die auf virtuellen Azure-Computern ausgeführt werden, und von Azure-Dateifreigaben verwendet.</span><span class="sxs-lookup"><span data-stu-id="5a430-105">The same command is used to restore Azure Virtual machines, databases running within Azure Virtual machines and Azure file shares as well.</span></span>

## <span data-ttu-id="5a430-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5a430-106">SYNTAX</span></span>

### <span data-ttu-id="5a430-107">AzureVMParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5a430-107">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-DiskEncryptionSetId <string>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a430-108">AzureVMManagedDiskParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a430-108">AzureVMManagedDiskParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-TargetResourceGroupName] <String>
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-DiskEncryptionSetId <string>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a430-109">AzureVMRestoreManagedAsUnmanaged</span><span class="sxs-lookup"><span data-stu-id="5a430-109">AzureVMRestoreManagedAsUnmanaged</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a430-110">AzureVMUnManagedDiskParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a430-110">AzureVMUnManagedDiskParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String> [-UseOriginalStorageAccount]
 [-RestoreOnlyOSDisk] [-RestoreDiskList <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a430-111">AzureFileShareParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a430-111">AzureFileShareParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a430-112">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a430-112">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a430-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5a430-113">DESCRIPTION</span></span>

<span data-ttu-id="5a430-114">Das **Cmdlet "Restore-AzRecoveryServicesBackupItem"** stellt die Daten und die Konfiguration eines Azure -Sicherungselements auf einem angegebenen Wiederherstellungspunkt wieder her.</span><span class="sxs-lookup"><span data-stu-id="5a430-114">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>

<span data-ttu-id="5a430-115">**Für Azure VM Backup**</span><span class="sxs-lookup"><span data-stu-id="5a430-115">**For Azure VM  backup**</span></span>

<span data-ttu-id="5a430-116">Mit diesem Befehl können Sie virtuelle Azure-Computer sichern und Datenträger (verwaltete und nicht verwaltete Datenträger) wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="5a430-116">You can backup Azure virtual machines and restore disks (both managed and un-managed) using this command.</span></span> <span data-ttu-id="5a430-117">Der Wiederherstellungsvorgang stellt nicht den vollständigen virtuellen Computer wiederher.</span><span class="sxs-lookup"><span data-stu-id="5a430-117">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="5a430-118">Wenn es sich um eine verwaltete Datenträger-VM handelt, sollte eine Zielressourcengruppe angegeben werden, in der die wiederhergestellten Datenträger gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="5a430-118">If this is a managed disk VM, a target Resource group should be specified where the restored disks are kept.</span></span> <span data-ttu-id="5a430-119">Wenn die Momentaufnahmen in der Ressourcengruppe vorhanden sind, die in der Sicherungsrichtlinie angegeben wurde, wird der Wiederherstellungsvorgang sofort ausgeführt, und die Datenträger werden aus lokalen Momentaufnahmen erstellt und in der Zielressourcengruppe gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5a430-119">When target resource group is specified, if the snapshots are present in the resource group that was specified in backup policy, the restore operation will be instant and the disks are created from local snapshots and kept in target-resource group.</span></span> <span data-ttu-id="5a430-120">Es gibt auch eine Option, um sie als nicht verwaltete Datenträger wiederherzustellen, aber dadurch werden die daten genutzt, die sich im Tresor der Azure-Wiederherstellungsdienste befinden, und daher viel langsamer sein.</span><span class="sxs-lookup"><span data-stu-id="5a430-120">There is also an option to restore them as un-managed disks but this will leverage the data present in Azure recovery services vault and hence will be lot slower.</span></span> <span data-ttu-id="5a430-121">Die Konfiguration der VM und die Bereitstellungsvorlage, die zum Erstellen einer VM aus den wiederhergestellten Datenträgern verwendet werden kann, werden in das angegebene Speicherkonto heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="5a430-121">The configuration of the VM and the deployment template which can be used to create VM out of the restored disks will be downloaded to the specified storage account.</span></span>
<span data-ttu-id="5a430-122">Wenn es sich um eine nicht verwaltete Datenträger-VM handelt, sind die Momentaufnahmen im ursprünglichen Speicherkonto des Datenträgers und/oder im Wiederherstellungsdiensttresor vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5a430-122">If this is an un-managed disk VM, then the snapshots are present in disk's original storage account and/or in the recovery services vault.</span></span> <span data-ttu-id="5a430-123">Wenn der Benutzer eine Option zum Wiederherstellen des ursprünglichen Speicherkontos ausgibt, kann eine sofortige Wiederherstellung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5a430-123">If user gives an option to use Original storage account to restore, then instant restore can be provided.</span></span> <span data-ttu-id="5a430-124">Andernfalls werden Daten aus dem Azure Recovery Services-Tresor abgerufen, und Datenträger werden zusammen mit der Konfiguration der VM und der Bereitstellungsvorlage in einem angegebenen Speicherkonto erstellt.</span><span class="sxs-lookup"><span data-stu-id="5a430-124">Otherwise, data is fetched from Azure Recovery services vault and disks are created in specified storage account along with the configuration of the VM and the deployment template.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5a430-125">Standardmäßig werden mit der Azure VM-Sicherung alle Datenträger gesichert.</span><span class="sxs-lookup"><span data-stu-id="5a430-125">By default, Azure VM backup backs up all disks.</span></span> <span data-ttu-id="5a430-126">Sie können relevante Datenträger selektiv mit den Parametern "exclusionList" oder "InclusionList" während "Enable-Backup" sichern.</span><span class="sxs-lookup"><span data-stu-id="5a430-126">You can selectively backup relevant disks using the exclusionList or InclusionList parameters during Enable-Backup.</span></span> <span data-ttu-id="5a430-127">Die Option zum selektiven Wiederherstellen von Datenträgern ist nur verfügbar, wenn sie selektiv gesichert wurden.</span><span class="sxs-lookup"><span data-stu-id="5a430-127">The option to selectively restore disks is available only if one has selectively backed them up.</span></span>

<span data-ttu-id="5a430-128">Weitere Informationen finden Sie unter verschiedenen möglichen Parametersätzen und Parametertext.</span><span class="sxs-lookup"><span data-stu-id="5a430-128">Please refer to different possible parameter sets and parameter text for more information.</span></span>

> [!NOTE]
> <span data-ttu-id="5a430-129">Wenn der Parameter "-VaultId" verwendet wird, sollte auch der Parameter "-VaultLocation" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5a430-129">If -VaultId parameter is used then -VaultLocation parameter should be used as well.</span></span>

<span data-ttu-id="5a430-130">**Für die Sicherung der Dateifreigabe in Azure**</span><span class="sxs-lookup"><span data-stu-id="5a430-130">**For Azure File share backup**</span></span>

<span data-ttu-id="5a430-131">Sie können eine gesamte Dateifreigabe oder bestimmte/mehrere Dateien/Ordner auf der Freigabe wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="5a430-131">You can restore an entire file share or specific/multiple files/folders on the share.</span></span> <span data-ttu-id="5a430-132">Sie können den ursprünglichen Speicherort oder einen anderen Speicherort wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="5a430-132">You can restore to the original location or to an alternate location.</span></span>

<span data-ttu-id="5a430-133">**Für Azure Workloads**</span><span class="sxs-lookup"><span data-stu-id="5a430-133">**For Azure Workloads**</span></span>

<span data-ttu-id="5a430-134">Sie können die SQL in Azure VMs wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="5a430-134">You can restore SQL DBs within Azure VMs</span></span>


## <span data-ttu-id="5a430-135">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5a430-135">EXAMPLES</span></span>

### <span data-ttu-id="5a430-136">Beispiel 1: Wiederherstellen der Datenträger eines gesicherten verwalteten Datenträgers der Azure VM von einem bestimmten Wiederherstellungspunkt</span><span class="sxs-lookup"><span data-stu-id="5a430-136">Example 1: Restore the disks of a backed up Managed disk Azure VM from a given recovery point</span></span>

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

<span data-ttu-id="5a430-137">Der erste Befehl ruft den Wiederherstellungsdiensttresor ab und speichert ihn in $vault Variable.</span><span class="sxs-lookup"><span data-stu-id="5a430-137">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="5a430-138">Der zweite Befehl ruft das Sicherungselement vom Typ "AzureVM" mit dem Namen "V2VM" ab und speichert es in der $BackupItem Variable.</span><span class="sxs-lookup"><span data-stu-id="5a430-138">The second command gets the Backup item of type AzureVM, of the name "V2VM", and stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="5a430-139">Der dritte Befehl ruft das Datum aus sieben Tagen früher ab und speichert es dann in der $StartDate Variable.</span><span class="sxs-lookup"><span data-stu-id="5a430-139">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="5a430-140">Der vierte Befehl ruft das aktuelle Datum ab und speichert es dann in der $EndDate Variable.</span><span class="sxs-lookup"><span data-stu-id="5a430-140">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="5a430-141">Der fünfte Befehl ruft eine Liste mit Wiederherstellungspunkten für das spezifische Sicherungselement ab, nach $StartDate und $EndDate.</span><span class="sxs-lookup"><span data-stu-id="5a430-141">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="5a430-142">Mit dem letzten Befehl werden alle Datenträger in der Zielressourcengruppe Target_RG wiederhergestellt. Anschließend werden die Informationen zur VM-Konfiguration und die Bereitstellungsvorlage im Speicherkonto "DestAccount" in der Ressourcengruppe "DestRG" bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="5a430-142">The last command restores all the disks to the target Resource group Target_RG, and then provides the VM configuration information and the deployment template in the storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="5a430-143">Beispiel 2: Wiederherstellen angegebener Datenträger eines gesicherten verwalteten Datenträgers der Azure VM von einem bestimmten Wiederherstellungspunkt</span><span class="sxs-lookup"><span data-stu-id="5a430-143">Example 2: Restore specified disks of a backed up Managed disk Azure VM from a given recovery point</span></span>

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

<span data-ttu-id="5a430-144">Der erste Befehl ruft den Wiederherstellungsdiensttresor ab und speichert ihn in $vault Variable.</span><span class="sxs-lookup"><span data-stu-id="5a430-144">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="5a430-145">Der zweite Befehl ruft das Sicherungselement vom Typ "AzureVM" mit dem Namen "V2VM" ab und speichert es in der $BackupItem Variable.</span><span class="sxs-lookup"><span data-stu-id="5a430-145">The second command gets the Backup item of type AzureVM, of the name "V2VM", and stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="5a430-146">Der dritte Befehl ruft das Datum aus sieben Tagen früher ab und speichert es dann in der $StartDate Variable.</span><span class="sxs-lookup"><span data-stu-id="5a430-146">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="5a430-147">Der vierte Befehl ruft das aktuelle Datum ab und speichert es dann in der $EndDate Variable.</span><span class="sxs-lookup"><span data-stu-id="5a430-147">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="5a430-148">Der fünfte Befehl ruft eine Liste mit Wiederherstellungspunkten für das spezifische Sicherungselement ab, nach $StartDate und $EndDate.</span><span class="sxs-lookup"><span data-stu-id="5a430-148">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="5a430-149">Der sechste Befehl speichert die Liste der Datenträger, die in der WiederherstellungsvariablenDiskLUN wiederhergestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5a430-149">The sixth command stores the list of disks to be restored in the restoreDiskLUN variable.</span></span>
<span data-ttu-id="5a430-150">Der letzte Befehl stellt die angegebenen Datenträger (der angegebenen LUNs) in der Zielressourcengruppe Target_RG wieder dar und stellt dann die Informationen zur VM-Konfiguration und die Bereitstellungsvorlage im Speicherkonto "DestAccount" in der Ressourcengruppe "DestRG" zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="5a430-150">The last command restores the given disks, of the specified LUNs, to the target Resource group Target_RG, and then provides the VM configuration information and the deployment template in the storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="5a430-151">Beispiel 3: Wiederherstellen von Datenträgern einer verwalteten VM als nicht verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="5a430-151">Example 3: Restore disks of a managed VM as unmanaged Disks</span></span>

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

<span data-ttu-id="5a430-152">Der erste Befehl ruft den RecoveryServices-Tresor ab und speichert ihn in $vault Variable.</span><span class="sxs-lookup"><span data-stu-id="5a430-152">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="5a430-153">Der zweite Befehl ruft das Sicherungselement ab und speichert es dann in der $BackupItem Variable.</span><span class="sxs-lookup"><span data-stu-id="5a430-153">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="5a430-154">Der dritte Befehl ruft das Datum aus sieben Tagen früher ab und speichert es dann in der $StartDate Variable.</span><span class="sxs-lookup"><span data-stu-id="5a430-154">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="5a430-155">Der vierte Befehl ruft das aktuelle Datum ab und speichert es dann in der $EndDate Variable.</span><span class="sxs-lookup"><span data-stu-id="5a430-155">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="5a430-156">Der fünfte Befehl ruft eine Liste mit Wiederherstellungspunkten für das spezifische Sicherungselement ab, nach $StartDate und $EndDate.</span><span class="sxs-lookup"><span data-stu-id="5a430-156">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="5a430-157">Mit dem sechsten Befehl werden die Datenträger als nicht verwaltete Datenträger wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="5a430-157">The sixth command restores the disks as unmanaged disks.</span></span>

### <span data-ttu-id="5a430-158">Beispiel 4: Wiederherstellen einer nicht verwalteten VM als nicht verwaltete Datenträger mithilfe des ursprünglichen Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="5a430-158">Example 4: Restore an unmanaged VM as unmanaged Disks using original storage account</span></span>

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

<span data-ttu-id="5a430-159">Der erste Befehl ruft den RecoveryServices-Tresor ab und speichert ihn in $vault Variable.</span><span class="sxs-lookup"><span data-stu-id="5a430-159">The first command gets the RecoveryServices vault and stores it in $vault variable.</span></span>
<span data-ttu-id="5a430-160">Der zweite Befehl ruft das Sicherungselement ab und speichert es dann in der $BackupItem Variable.</span><span class="sxs-lookup"><span data-stu-id="5a430-160">The second command gets the Backup item and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="5a430-161">Der dritte Befehl ruft das Datum aus sieben Tagen früher ab und speichert es dann in der $StartDate Variable.</span><span class="sxs-lookup"><span data-stu-id="5a430-161">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="5a430-162">Der vierte Befehl ruft das aktuelle Datum ab und speichert es dann in der $EndDate Variable.</span><span class="sxs-lookup"><span data-stu-id="5a430-162">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="5a430-163">Der fünfte Befehl ruft eine Liste mit Wiederherstellungspunkten für das spezifische Sicherungselement ab, nach $StartDate und $EndDate.</span><span class="sxs-lookup"><span data-stu-id="5a430-163">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="5a430-164">Mit dem sechsten Befehl werden die Datenträger als nicht verwaltete Datenträger auf ihren ursprünglichen Speicherkonten wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="5a430-164">The sixth command restores the disks as unmanaged disks to their original storage accounts</span></span>

### <span data-ttu-id="5a430-165">Beispiel 5: Wiederherstellen mehrerer Dateien eines AzureFileShare-Elements</span><span class="sxs-lookup"><span data-stu-id="5a430-165">Example 5: Restore Multiple files of an AzureFileShare item</span></span>

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

<span data-ttu-id="5a430-166">Der erste Befehl ruft den Wiederherstellungsdiensttresor ab und speichert ihn in $vault Variable.</span><span class="sxs-lookup"><span data-stu-id="5a430-166">The first command gets the Recovery Services vault and stores it in $vault variable.</span></span>
<span data-ttu-id="5a430-167">Der zweite Befehl ruft das Sicherungselement mit dem Namen "fileshareitem" ab und speichert es dann in $BackupItem Variable.</span><span class="sxs-lookup"><span data-stu-id="5a430-167">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="5a430-168">Der dritte Befehl ruft eine Liste mit Wiederherstellungspunkten für das spezifische Sicherungselement ab.</span><span class="sxs-lookup"><span data-stu-id="5a430-168">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="5a430-169">Der vierte Befehl gibt an, welche Dateien wiederhergestellt werden müssen, und speichert sie in $files Variable.</span><span class="sxs-lookup"><span data-stu-id="5a430-169">The fourth command specifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="5a430-170">Mit dem letzten Befehl werden die angegebenen Dateien am ursprünglichen Speicherort wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="5a430-170">The last command restores the specified files to its original location.</span></span>

### <span data-ttu-id="5a430-171">Beispiel 6: Wiederherstellen einer SQL-DB innerhalb einer Azure VM auf eine andere Ziel-VM für einen eindeutigen vollständigen Wiederherstellungspunkt</span><span class="sxs-lookup"><span data-stu-id="5a430-171">Example 6: Restore a SQL DB within an Azure VM to another target VM for a distinct full recovery point</span></span>

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

### <span data-ttu-id="5a430-172">Beispiel 7: Wiederherstellen einer SQL-DB innerhalb einer Azure VM auf eine andere Ziel-VM für einen Protokollwiederherstellungspunkt</span><span class="sxs-lookup"><span data-stu-id="5a430-172">Example 7: Restore a SQL DB within an Azure VM to another target VM for a log recovery point</span></span>

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

## <span data-ttu-id="5a430-173">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a430-173">PARAMETERS</span></span>

### <span data-ttu-id="5a430-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a430-174">-DefaultProfile</span></span>

<span data-ttu-id="5a430-175">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5a430-175">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a430-176">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="5a430-176">-MultipleSourceFilePath</span></span>
<span data-ttu-id="5a430-177">Wird für mehrere Dateien verwendet, die aus einer Dateifreigabe wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5a430-177">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="5a430-178">Die Pfade der Elemente, die in der Dateifreigabe wiederhergestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5a430-178">The paths of the items to be restored within the file share.</span></span>

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

### <span data-ttu-id="5a430-179">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="5a430-179">-RecoveryPoint</span></span>

<span data-ttu-id="5a430-180">Gibt den Wiederherstellungspunkt an, an dem das Sicherungselement wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a430-180">Specifies the recovery point to which to restore the backup item.</span></span>
<span data-ttu-id="5a430-181">Zum Abrufen eines **AzureRmRecoveryServicesBackupRecoveryPoint-Objekts** verwenden Sie das **Cmdlet "Get-AzRecoveryServicesBackupRecoveryPoint".**</span><span class="sxs-lookup"><span data-stu-id="5a430-181">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

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

### <span data-ttu-id="5a430-182">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="5a430-182">-ResolveConflict</span></span>

<span data-ttu-id="5a430-183">Falls das wiederhergestellte Element auch am Ziel vorhanden ist, verwenden Sie diese Option, um anzugeben, ob das Element überschrieben werden soll oder nicht.</span><span class="sxs-lookup"><span data-stu-id="5a430-183">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="5a430-184">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="5a430-184">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5a430-185">Überschreiben</span><span class="sxs-lookup"><span data-stu-id="5a430-185">Overwrite</span></span>
- <span data-ttu-id="5a430-186">Überspringen</span><span class="sxs-lookup"><span data-stu-id="5a430-186">Skip</span></span>

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

### <span data-ttu-id="5a430-187">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="5a430-187">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="5a430-188">Verwenden Sie diesen Schalter, um anzugeben, dass sie als nicht verwaltete Datenträger wiederhergestellt werden</span><span class="sxs-lookup"><span data-stu-id="5a430-188">Use this switch to specify to restore as unmanaged disks</span></span>

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

### <span data-ttu-id="5a430-189">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="5a430-189">-RestoreDiskList</span></span>
<span data-ttu-id="5a430-190">Angeben der Datenträger, die von der gesicherten VM wiederhergestellt werden</span><span class="sxs-lookup"><span data-stu-id="5a430-190">Specify which disks to recover of the backed up VM</span></span>

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

### <span data-ttu-id="5a430-191">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="5a430-191">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="5a430-192">Verwenden Sie diesen Schalter, um nur Betriebssystemdatenträger einer gesicherten VM wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="5a430-192">Use this switch to restore only OS disks of a backed up VM</span></span>

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

### <span data-ttu-id="5a430-193">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="5a430-193">-SourceFilePath</span></span>

<span data-ttu-id="5a430-194">Wird für die Wiederherstellung eines bestimmten Elements aus einer Dateifreigabe verwendet.</span><span class="sxs-lookup"><span data-stu-id="5a430-194">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="5a430-195">Der Pfad des Elements, das in der Dateifreigabe wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a430-195">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="5a430-196">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="5a430-196">-SourceFileType</span></span>

<span data-ttu-id="5a430-197">Wird für die Wiederherstellung eines bestimmten Elements aus einer Dateifreigabe verwendet.</span><span class="sxs-lookup"><span data-stu-id="5a430-197">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="5a430-198">Der Typ des Elements, das in der Dateifreigabe wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a430-198">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="5a430-199">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="5a430-199">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5a430-200">Datei</span><span class="sxs-lookup"><span data-stu-id="5a430-200">File</span></span>
- <span data-ttu-id="5a430-201">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="5a430-201">Directory</span></span>

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

### <span data-ttu-id="5a430-202">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5a430-202">-StorageAccountName</span></span>

<span data-ttu-id="5a430-203">Gibt den Namen des Zielspeicherkontos in Ihrem Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="5a430-203">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="5a430-204">Im Rahmen des Wiederherstellungsvorgangs speichert dieses Cmdlet die Datenträger und die Konfigurationsinformationen in diesem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="5a430-204">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="5a430-205">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a430-205">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="5a430-206">Gibt den Namen der Ressourcengruppe an, die das Zielspeicherkonto in Ihrem Abonnement enthält.</span><span class="sxs-lookup"><span data-stu-id="5a430-206">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="5a430-207">Im Rahmen des Wiederherstellungsvorgangs speichert dieses Cmdlet die Datenträger und die Konfigurationsinformationen in diesem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="5a430-207">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="5a430-208">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="5a430-208">-TargetFileShareName</span></span>

<span data-ttu-id="5a430-209">Die Dateifreigabe, auf der die Dateifreigabe wiederhergestellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="5a430-209">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="5a430-210">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="5a430-210">-TargetFolder</span></span>

<span data-ttu-id="5a430-211">Der Ordner, in dem die Dateifreigabe im TargetFileShareName wiederhergestellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="5a430-211">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="5a430-212">Wenn der gesicherte Inhalt in einem Stammordner wiederhergestellt werden soll, geben Sie die Werte für den Zielordner als leere Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="5a430-212">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="5a430-213">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a430-213">-TargetResourceGroupName</span></span>

<span data-ttu-id="5a430-214">Die Ressourcengruppe, in die die verwalteten Datenträger wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5a430-214">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="5a430-215">Gilt für die Sicherung von VM mit verwalteten Datenträgern</span><span class="sxs-lookup"><span data-stu-id="5a430-215">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="5a430-216">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5a430-216">-TargetStorageAccountName</span></span>

<span data-ttu-id="5a430-217">Das Speicherkonto, auf dem die Dateifreigabe wiederhergestellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="5a430-217">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="5a430-218">-UseAccountStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5a430-218">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="5a430-219">Verwenden Sie diesen Schalter, wenn die Datenträger aus dem Wiederherstellungspunkt auf ihre ursprünglichen Speicherkonten wiederhergestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5a430-219">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="5a430-220">-VaultId</span><span class="sxs-lookup"><span data-stu-id="5a430-220">-VaultId</span></span>

<span data-ttu-id="5a430-221">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="5a430-221">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="5a430-222">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="5a430-222">-VaultLocation</span></span>

<span data-ttu-id="5a430-223">Speicherort des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="5a430-223">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="5a430-224">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="5a430-224">-WLRecoveryConfig</span></span>

<span data-ttu-id="5a430-225">Wiederherstellungskonfiguration</span><span class="sxs-lookup"><span data-stu-id="5a430-225">Recovery config</span></span>

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

### <span data-ttu-id="5a430-226">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a430-226">-Confirm</span></span>

<span data-ttu-id="5a430-227">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5a430-227">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a430-228">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5a430-228">-WhatIf</span></span>

<span data-ttu-id="5a430-229">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5a430-229">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="5a430-230">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a430-230">CommonParameters</span></span>
<span data-ttu-id="5a430-231">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a430-231">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a430-232">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a430-232">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a430-233">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5a430-233">INPUTS</span></span>

### <span data-ttu-id="5a430-234">System.String</span><span class="sxs-lookup"><span data-stu-id="5a430-234">System.String</span></span>

### <span data-ttu-id="5a430-235">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="5a430-235">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="5a430-236">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5a430-236">OUTPUTS</span></span>

### <span data-ttu-id="5a430-237">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="5a430-237">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="5a430-238">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5a430-238">NOTES</span></span>

## <span data-ttu-id="5a430-239">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5a430-239">RELATED LINKS</span></span>

[<span data-ttu-id="5a430-240">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="5a430-240">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="5a430-241">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="5a430-241">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="5a430-242">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="5a430-242">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
