---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 69b115fab623d1a951fa2f77632a33fb437a3555
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003739"
---
# <span data-ttu-id="94cea-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="94cea-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="94cea-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="94cea-102">SYNOPSIS</span></span>

<span data-ttu-id="94cea-103">Wiederherstellen der Daten und der Konfiguration für ein Sicherungselement an einem Wiederherstellungspunkt</span><span class="sxs-lookup"><span data-stu-id="94cea-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="94cea-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="94cea-104">SYNTAX</span></span>

### <span data-ttu-id="94cea-105">AzureVMParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="94cea-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-RestoreOnlyOSDisk]
 [-RestoreDiskList <String[]>] [-RestoreAsUnmanagedDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94cea-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="94cea-106">AzureFileParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-MultipleSourceFilePath <String[]>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94cea-107">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="94cea-107">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94cea-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="94cea-108">DESCRIPTION</span></span>

<span data-ttu-id="94cea-109">Das Cmdlet **Restore-AzRecoveryServicesBackupItem** stellt die Daten und die Konfiguration für ein Azure Backup-Element an einem angegebenen Wiederherstellungspunkt wieder her.</span><span class="sxs-lookup"><span data-stu-id="94cea-109">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="94cea-110">Mit diesem Cmdlet wird die Wiederherstellung aus dem Vault für Wiederherstellungsdienste auf dem Speicherkonto des Kunden gestartet.</span><span class="sxs-lookup"><span data-stu-id="94cea-110">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="94cea-111">Beim Wiederherstellungsvorgang wird der vollständige virtuelle Computer nicht wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="94cea-111">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="94cea-112">Nachdem der Wiederherstellungsvorgang fertig ist, müssen Sie die verwalteten Datenträger für eine Ziel Ressourcengruppe und die Konfigurationsinformationen für das Kunden Speicherkonto wiederherstellen, indem Sie den virtuellen Computer erstellen und starten.</span><span class="sxs-lookup"><span data-stu-id="94cea-112">It restores the managed disks to a target resource group and configuration information to customer storage account After the restore operation is finished, you must create the virtual machine and start it.</span></span>
<span data-ttu-id="94cea-113">Setzen Sie den Vault-Kontext mithilfe des-Vault-Parameters.</span><span class="sxs-lookup"><span data-stu-id="94cea-113">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="94cea-114">Hinweis: zum erfolgreichen Ausführen dieses Cmdlets zusätzlich zu-Vault-VaultLocation-Parameter sollte ebenfalls verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="94cea-114">Note: To successfully execute this cmdlet in addition to -VaultId parameter -VaultLocation parameter should be used as well.</span></span>

## <span data-ttu-id="94cea-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="94cea-115">EXAMPLES</span></span>

### <span data-ttu-id="94cea-116">Beispiel 1: Wiederherstellen eines Elements in einem Wiederherstellungspunkt</span><span class="sxs-lookup"><span data-stu-id="94cea-116">Example 1: Restore an item to a recovery point</span></span>

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

<span data-ttu-id="94cea-117">Der erste Befehl ruft den Sicherungs Container des Typs AzureVM ab und speichert ihn dann in der $Container Variablen.</span><span class="sxs-lookup"><span data-stu-id="94cea-117">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="94cea-118">Der zweite Befehl ruft das Sicherungselement mit dem Namen V2VM aus $Container ab und speichert es dann in der $BackupItem-Variablen.</span><span class="sxs-lookup"><span data-stu-id="94cea-118">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="94cea-119">Der dritte Befehl ruft das Datum ab sieben Tage zuvor ab und speichert es dann in der $StartDate Variablen.</span><span class="sxs-lookup"><span data-stu-id="94cea-119">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="94cea-120">Der vierte Befehl ruft das aktuelle Datum ab und speichert es dann in der $EndDate Variablen.</span><span class="sxs-lookup"><span data-stu-id="94cea-120">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="94cea-121">Der fünfte Befehl ruft eine Liste der Wiederherstellungspunkte für das jeweilige Sicherungselement ab, das nach $StartDate und $EndDate gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="94cea-121">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="94cea-122">Der angegebene Datumsbereich ist die letzten 7 Tage.</span><span class="sxs-lookup"><span data-stu-id="94cea-122">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="94cea-123">Der siebte Befehl gibt an, welche Datenträger vom Wiederherstellungspunkt wiederhergestellt werden sollen, und speichert Sie in $restoreDiskLUNs Variablen.</span><span class="sxs-lookup"><span data-stu-id="94cea-123">The seventh command specifies which disks to restore from the recovery point and stores it in $restoreDiskLUNs variable.</span></span>
<span data-ttu-id="94cea-124">Mit dem letzten Befehl werden die Datenträger auf dem Zielspeicher Konto DestAccount in der DestRG-Ressourcengruppe wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="94cea-124">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

### <span data-ttu-id="94cea-125">Beispiel 2: Wiederherstellen mehrerer Dateien eines AzureFileShare-Elements</span><span class="sxs-lookup"><span data-stu-id="94cea-125">Example 2: Restore Multiple files of an AzureFileShare item</span></span>

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

<span data-ttu-id="94cea-126">Der erste Befehl ruft den Sicherungs Container des Typs AzureVM ab und speichert ihn dann in der $Container Variablen.</span><span class="sxs-lookup"><span data-stu-id="94cea-126">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="94cea-127">Der zweite Befehl ruft das Sicherungselement mit dem Namen fileshareitem ab und speichert es dann in der $BackupItem-Variablen.</span><span class="sxs-lookup"><span data-stu-id="94cea-127">The second command gets the Backup item named fileshareitem and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="94cea-128">Der dritte Befehl ruft eine Liste der Wiederherstellungspunkte für das jeweilige Sicherungselement ab.</span><span class="sxs-lookup"><span data-stu-id="94cea-128">The third command gets a list of recovery points for the specific backup item.</span></span>
<span data-ttu-id="94cea-129">Der vierte Befehl spceifies die Dateien, die wiederhergestellt werden sollen, und speichert Sie in $Files Variablen.</span><span class="sxs-lookup"><span data-stu-id="94cea-129">The fourth command spceifies which files to restore and stores it in $files variable.</span></span>
<span data-ttu-id="94cea-130">Mit dem letzten Befehl werden die angegebenen Dateien an Ihrem ursprünglichen Speicherort wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="94cea-130">The last command restores the specified files to its original location.</span></span>

## <span data-ttu-id="94cea-131">Parameter</span><span class="sxs-lookup"><span data-stu-id="94cea-131">PARAMETERS</span></span>

### <span data-ttu-id="94cea-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94cea-132">-DefaultProfile</span></span>

<span data-ttu-id="94cea-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="94cea-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94cea-134">-MultipleSourceFilePath</span><span class="sxs-lookup"><span data-stu-id="94cea-134">-MultipleSourceFilePath</span></span>
<span data-ttu-id="94cea-135">Wird für die Wiederherstellung mehrerer Dateien aus einer Dateifreigabe verwendet.</span><span class="sxs-lookup"><span data-stu-id="94cea-135">Used for Multiple files restore from a file share.</span></span> <span data-ttu-id="94cea-136">Die Pfade der Elemente, die in der Dateifreigabe wiederhergestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="94cea-136">The paths of the items to be restored within the file share.</span></span>

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

### <span data-ttu-id="94cea-137">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="94cea-137">-RecoveryPoint</span></span>

<span data-ttu-id="94cea-138">Gibt den Wiederherstellungspunkt an, auf den der virtuelle Computer wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="94cea-138">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="94cea-139">Verwenden Sie das Cmdlet **Get-AzRecoveryServicesBackupRecoveryPoint** , um ein **AzureRmRecoveryServicesBackupRecoveryPoint** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="94cea-139">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet.</span></span>

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

### <span data-ttu-id="94cea-140">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="94cea-140">-ResolveConflict</span></span>

<span data-ttu-id="94cea-141">Wenn das wiederhergestellte Element auch im Ziel vorhanden ist, verwenden Sie diese Option, um anzugeben, ob Sie überschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="94cea-141">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>
<span data-ttu-id="94cea-142">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="94cea-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="94cea-143">Überschreiben</span><span class="sxs-lookup"><span data-stu-id="94cea-143">Overwrite</span></span>
- <span data-ttu-id="94cea-144">Skip</span><span class="sxs-lookup"><span data-stu-id="94cea-144">Skip</span></span>

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

### <span data-ttu-id="94cea-145">-RestoreAsUnmanagedDisks</span><span class="sxs-lookup"><span data-stu-id="94cea-145">-RestoreAsUnmanagedDisks</span></span>
<span data-ttu-id="94cea-146">Verwenden Sie diese Option, um anzugeben, dass Sie als nicht verwaltete Datenträger wiederhergestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="94cea-146">Use this switch to specify to restore as unmanaged disks</span></span>

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

### <span data-ttu-id="94cea-147">-RestoreDiskList</span><span class="sxs-lookup"><span data-stu-id="94cea-147">-RestoreDiskList</span></span>
<span data-ttu-id="94cea-148">Angeben, welche Datenträger von der gesicherten VM wiederhergestellt werden sollen</span><span class="sxs-lookup"><span data-stu-id="94cea-148">Specify which disks to recover of the backed up VM</span></span>

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

### <span data-ttu-id="94cea-149">-RestoreOnlyOSDisk</span><span class="sxs-lookup"><span data-stu-id="94cea-149">-RestoreOnlyOSDisk</span></span>
<span data-ttu-id="94cea-150">Verwenden Sie diese Option, um nur Betriebssystemdatenträger einer gesicherten VM wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="94cea-150">Use this switch to restore only OS disks of a backed up VM</span></span>

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

### <span data-ttu-id="94cea-151">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="94cea-151">-SourceFilePath</span></span>

<span data-ttu-id="94cea-152">Wird für eine bestimmte Elementwiederherstellung aus einer Dateifreigabe verwendet.</span><span class="sxs-lookup"><span data-stu-id="94cea-152">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="94cea-153">Der Pfad des Elements, das innerhalb der Dateifreigabe wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="94cea-153">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="94cea-154">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="94cea-154">-SourceFileType</span></span>

<span data-ttu-id="94cea-155">Wird für eine bestimmte Elementwiederherstellung aus einer Dateifreigabe verwendet.</span><span class="sxs-lookup"><span data-stu-id="94cea-155">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="94cea-156">Der Typ des Elements, das innerhalb der Dateifreigabe wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="94cea-156">The type of the item to be restored within the file share.</span></span>
<span data-ttu-id="94cea-157">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="94cea-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="94cea-158">Datei</span><span class="sxs-lookup"><span data-stu-id="94cea-158">File</span></span>
- <span data-ttu-id="94cea-159">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="94cea-159">Directory</span></span>

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

### <span data-ttu-id="94cea-160">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="94cea-160">-StorageAccountName</span></span>

<span data-ttu-id="94cea-161">Gibt den Namen des Zielspeicher Kontos in Ihrem Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="94cea-161">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="94cea-162">Im Rahmen des Wiederherstellungsvorgangs speichert dieses Cmdlet die Datenträger und die Konfigurationsinformationen in diesem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="94cea-162">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="94cea-163">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94cea-163">-StorageAccountResourceGroupName</span></span>

<span data-ttu-id="94cea-164">Gibt den Namen der Ressourcengruppe an, die das Zielspeicher Konto in Ihrem Abonnement enthält.</span><span class="sxs-lookup"><span data-stu-id="94cea-164">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="94cea-165">Im Rahmen des Wiederherstellungsvorgangs speichert dieses Cmdlet die Datenträger und die Konfigurationsinformationen in diesem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="94cea-165">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="94cea-166">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="94cea-166">-TargetFileShareName</span></span>

<span data-ttu-id="94cea-167">Die Dateifreigabe, in der die Dateifreigabe wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="94cea-167">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="94cea-168">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="94cea-168">-TargetFolder</span></span>

<span data-ttu-id="94cea-169">Der Ordner, in dem die Dateifreigabe innerhalb des TargetFileShareName wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="94cea-169">The folder under which the file share has to be restored to within the TargetFileShareName.</span></span> <span data-ttu-id="94cea-170">Wenn der gesicherte Inhalt in einem Stammordner wiederhergestellt werden soll, geben Sie die Werte für den Zielordner als leere Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="94cea-170">If the backed-up content is to be restored to a root folder, give the target folder values as an empty string.</span></span>

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

### <span data-ttu-id="94cea-171">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94cea-171">-TargetResourceGroupName</span></span>

<span data-ttu-id="94cea-172">Die Ressourcengruppe, in der die verwalteten Datenträger wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="94cea-172">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="94cea-173">Anwendbar auf eine Sicherung von VM mit verwalteten Datenträgern</span><span class="sxs-lookup"><span data-stu-id="94cea-173">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="94cea-174">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="94cea-174">-TargetStorageAccountName</span></span>

<span data-ttu-id="94cea-175">Das Speicherkonto, in dem die Dateifreigabe wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="94cea-175">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="94cea-176">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="94cea-176">-UseOriginalStorageAccount</span></span>

<span data-ttu-id="94cea-177">Verwenden Sie diese Option, wenn die Datenträger des Wiederherstellungspunkts auf ihren ursprünglichen Speicherkonten wiederhergestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="94cea-177">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="94cea-178">-Tresor</span><span class="sxs-lookup"><span data-stu-id="94cea-178">-VaultId</span></span>

<span data-ttu-id="94cea-179">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="94cea-179">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="94cea-180">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="94cea-180">-VaultLocation</span></span>

<span data-ttu-id="94cea-181">Der Speicherort des Speichers für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="94cea-181">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="94cea-182">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="94cea-182">-WLRecoveryConfig</span></span>

<span data-ttu-id="94cea-183">Wiederherstellungskonfiguration</span><span class="sxs-lookup"><span data-stu-id="94cea-183">Recovery config</span></span>

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

### <span data-ttu-id="94cea-184">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="94cea-184">-Confirm</span></span>

<span data-ttu-id="94cea-185">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="94cea-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94cea-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94cea-186">-WhatIf</span></span>

<span data-ttu-id="94cea-187">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="94cea-187">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94cea-188">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="94cea-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94cea-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94cea-189">CommonParameters</span></span>
<span data-ttu-id="94cea-190">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94cea-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94cea-191">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94cea-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94cea-192">Eingaben</span><span class="sxs-lookup"><span data-stu-id="94cea-192">INPUTS</span></span>

### <span data-ttu-id="94cea-193">System. String</span><span class="sxs-lookup"><span data-stu-id="94cea-193">System.String</span></span>

### <span data-ttu-id="94cea-194">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="94cea-194">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="94cea-195">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="94cea-195">OUTPUTS</span></span>

### <span data-ttu-id="94cea-196">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="94cea-196">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="94cea-197">Notizen</span><span class="sxs-lookup"><span data-stu-id="94cea-197">NOTES</span></span>

## <span data-ttu-id="94cea-198">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="94cea-198">RELATED LINKS</span></span>

[<span data-ttu-id="94cea-199">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="94cea-199">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="94cea-200">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="94cea-200">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="94cea-201">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="94cea-201">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
