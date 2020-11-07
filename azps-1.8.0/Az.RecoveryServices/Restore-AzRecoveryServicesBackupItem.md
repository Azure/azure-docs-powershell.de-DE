---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: eb54d22f74216dc883726d34df204ce80c711a22
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659827"
---
# <span data-ttu-id="71662-101">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="71662-101">Restore-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="71662-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="71662-102">SYNOPSIS</span></span>
<span data-ttu-id="71662-103">Wiederherstellen der Daten und der Konfiguration für ein Sicherungselement an einem Wiederherstellungspunkt</span><span class="sxs-lookup"><span data-stu-id="71662-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

## <span data-ttu-id="71662-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="71662-104">SYNTAX</span></span>

### <span data-ttu-id="71662-105">AzureVMParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="71662-105">AzureVMParameterSet (Default)</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71662-106">AzureFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="71662-106">AzureFileParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71662-107">AzureWorkloadParameterSet</span><span class="sxs-lookup"><span data-stu-id="71662-107">AzureWorkloadParameterSet</span></span>
```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71662-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71662-108">DESCRIPTION</span></span>
<span data-ttu-id="71662-109">Das Cmdlet **Restore-AzRecoveryServicesBackupItem** stellt die Daten und die Konfiguration für ein Azure Backup-Element an einem angegebenen Wiederherstellungspunkt wieder her.</span><span class="sxs-lookup"><span data-stu-id="71662-109">The **Restore-AzRecoveryServicesBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="71662-110">Mit diesem Cmdlet wird die Wiederherstellung aus dem Vault für Wiederherstellungsdienste auf dem Speicherkonto des Kunden gestartet.</span><span class="sxs-lookup"><span data-stu-id="71662-110">This cmdlet starts the restore from the Recovery Services vault to customer's storage account.</span></span>
<span data-ttu-id="71662-111">Beim Wiederherstellungsvorgang wird der vollständige virtuelle Computer nicht wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="71662-111">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="71662-112">Die Datenträgerdaten und Konfigurationsinformationen werden wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="71662-112">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="71662-113">Nach Abschluss des Wiederherstellungsvorgangs müssen Sie den virtuellen Computer erstellen und starten.</span><span class="sxs-lookup"><span data-stu-id="71662-113">After the restore operation is finished, you must create the virtual machine and start it.</span></span>
<span data-ttu-id="71662-114">Setzen Sie den Vault-Kontext mithilfe des Set-AzRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="71662-114">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="71662-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="71662-115">EXAMPLES</span></span>

### <span data-ttu-id="71662-116">Beispiel 1: Wiederherstellen eines Elements in einem Wiederherstellungspunkt</span><span class="sxs-lookup"><span data-stu-id="71662-116">Example 1: Restore an item to a recovery point</span></span>
```
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() 
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG"
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="71662-117">Der erste Befehl ruft den Sicherungs Container des Typs AzureVM ab und speichert ihn dann in der $Container Variablen.</span><span class="sxs-lookup"><span data-stu-id="71662-117">The first command gets the Backup container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="71662-118">Der zweite Befehl ruft das Sicherungselement mit dem Namen V2VM aus $Container ab und speichert es dann in der $BackupItem-Variablen.</span><span class="sxs-lookup"><span data-stu-id="71662-118">The second command gets the Backup item named V2VM from $Container, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="71662-119">Der dritte Befehl ruft das Datum ab sieben Tage zuvor ab und speichert es dann in der $StartDate Variablen.</span><span class="sxs-lookup"><span data-stu-id="71662-119">The third command gets the date from seven days earlier, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="71662-120">Der vierte Befehl ruft das aktuelle Datum ab und speichert es dann in der $EndDate Variablen.</span><span class="sxs-lookup"><span data-stu-id="71662-120">The fourth command gets the current date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="71662-121">Der fünfte Befehl ruft eine Liste der Wiederherstellungspunkte für das jeweilige Sicherungselement ab, das nach $StartDate und $EndDate gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="71662-121">The fifth command gets a list of recovery points for the specific backup item filtered by $StartDate and $EndDate.</span></span>
<span data-ttu-id="71662-122">Der angegebene Datumsbereich ist die letzten 7 Tage.</span><span class="sxs-lookup"><span data-stu-id="71662-122">The date range specified is the last 7 days.</span></span>
<span data-ttu-id="71662-123">Mit dem letzten Befehl werden die Datenträger auf dem Zielspeicher Konto DestAccount in der DestRG-Ressourcengruppe wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="71662-123">The last command restores the disks to the target storage account DestAccount in the DestRG resource group.</span></span>

## <span data-ttu-id="71662-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="71662-124">PARAMETERS</span></span>

### <span data-ttu-id="71662-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71662-125">-DefaultProfile</span></span>
<span data-ttu-id="71662-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="71662-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71662-127">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="71662-127">-RecoveryPoint</span></span>
<span data-ttu-id="71662-128">Gibt den Wiederherstellungspunkt an, auf den der virtuelle Computer wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="71662-128">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="71662-129">Verwenden Sie das Get-AzRecoveryServicesBackupRecoveryPoint-Cmdlet, um ein **AzureRmRecoveryServicesBackupRecoveryPoint** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="71662-129">To obtain an **AzureRmRecoveryServicesBackupRecoveryPoint** object, use the Get-AzRecoveryServicesBackupRecoveryPoint cmdlet.</span></span>

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

### <span data-ttu-id="71662-130">-ResolveConflict</span><span class="sxs-lookup"><span data-stu-id="71662-130">-ResolveConflict</span></span>
<span data-ttu-id="71662-131">Wenn das wiederhergestellte Element auch im Ziel vorhanden ist, verwenden Sie diese Option, um anzugeben, ob Sie überschrieben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="71662-131">In case the restored item also exists in the destination, use this to indicate whether to overwrite or not.</span></span>

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

### <span data-ttu-id="71662-132">-SourceFilePath</span><span class="sxs-lookup"><span data-stu-id="71662-132">-SourceFilePath</span></span>
<span data-ttu-id="71662-133">Wird für eine bestimmte Elementwiederherstellung aus einer Dateifreigabe verwendet.</span><span class="sxs-lookup"><span data-stu-id="71662-133">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="71662-134">Der Pfad des Elements, das innerhalb der Dateifreigabe wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="71662-134">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="71662-135">-SourceFileType</span><span class="sxs-lookup"><span data-stu-id="71662-135">-SourceFileType</span></span>
<span data-ttu-id="71662-136">Wird für eine bestimmte Elementwiederherstellung aus einer Dateifreigabe verwendet.</span><span class="sxs-lookup"><span data-stu-id="71662-136">Used for a particular item restore from a file share.</span></span> <span data-ttu-id="71662-137">Der Pfad des Elements, das innerhalb der Dateifreigabe wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="71662-137">The path of the item to be restored within the file share.</span></span>

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

### <span data-ttu-id="71662-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="71662-138">-StorageAccountName</span></span>
<span data-ttu-id="71662-139">Gibt den Namen des Zielspeicher Kontos in Ihrem Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="71662-139">Specifies the name of the target Storage account in your subscription.</span></span>
<span data-ttu-id="71662-140">Im Rahmen des Wiederherstellungsvorgangs speichert dieses Cmdlet die Datenträger und die Konfigurationsinformationen in diesem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="71662-140">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="71662-141">-StorageAccountResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71662-141">-StorageAccountResourceGroupName</span></span>
<span data-ttu-id="71662-142">Gibt den Namen der Ressourcengruppe an, die das Zielspeicher Konto in Ihrem Abonnement enthält.</span><span class="sxs-lookup"><span data-stu-id="71662-142">Specifies the name of the resource group that contains the target Storage account in your subscription.</span></span>
<span data-ttu-id="71662-143">Im Rahmen des Wiederherstellungsvorgangs speichert dieses Cmdlet die Datenträger und die Konfigurationsinformationen in diesem Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="71662-143">As a part of the restore process, this cmdlet stores the disks and the configuration information in this Storage account.</span></span>

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

### <span data-ttu-id="71662-144">-TargetFileShareName</span><span class="sxs-lookup"><span data-stu-id="71662-144">-TargetFileShareName</span></span>
<span data-ttu-id="71662-145">Die Dateifreigabe, in der die Dateifreigabe wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="71662-145">The File Share to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="71662-146">-TargetFolder</span><span class="sxs-lookup"><span data-stu-id="71662-146">-TargetFolder</span></span>
<span data-ttu-id="71662-147">Der Ordner, in dem die Dateifreigabe innerhalb des targetFileShareName wiederhergestellt werden soll. lassen Sie die Variable leer, um Unterstamm Ordner wiederhergestellt zu werden.</span><span class="sxs-lookup"><span data-stu-id="71662-147">The folder under which the file share has to be restored to within the targetFileShareName.Leave the variable empty to restore under root folder.</span></span>

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

### <span data-ttu-id="71662-148">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71662-148">-TargetResourceGroupName</span></span>
<span data-ttu-id="71662-149">Die Ressourcengruppe, in der die verwalteten Datenträger wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="71662-149">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="71662-150">Anwendbar auf eine Sicherung von VM mit verwalteten Datenträgern</span><span class="sxs-lookup"><span data-stu-id="71662-150">Applicable to backup of VM with managed disks</span></span>

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

### <span data-ttu-id="71662-151">-TargetStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="71662-151">-TargetStorageAccountName</span></span>
<span data-ttu-id="71662-152">Das Speicherkonto, in dem die Dateifreigabe wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="71662-152">The storage account to which the file share has to be restored to.</span></span>

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

### <span data-ttu-id="71662-153">-UseOriginalStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71662-153">-UseOriginalStorageAccount</span></span>
<span data-ttu-id="71662-154">Verwenden Sie diese Option, wenn die Datenträger des Wiederherstellungspunkts auf ihren ursprünglichen Speicherkonten wiederhergestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="71662-154">Use this switch if the disks from the recovery point are to be restored to their original storage accounts.</span></span>

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

### <span data-ttu-id="71662-155">-Tresor</span><span class="sxs-lookup"><span data-stu-id="71662-155">-VaultId</span></span>
<span data-ttu-id="71662-156">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="71662-156">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="71662-157">-VaultLocation</span><span class="sxs-lookup"><span data-stu-id="71662-157">-VaultLocation</span></span>
<span data-ttu-id="71662-158">Der Speicherort des Speichers für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="71662-158">Location of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="71662-159">-WLRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="71662-159">-WLRecoveryConfig</span></span>
<span data-ttu-id="71662-160">Wiederherstellungskonfiguration</span><span class="sxs-lookup"><span data-stu-id="71662-160">Recovery config</span></span>

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

### <span data-ttu-id="71662-161">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="71662-161">-Confirm</span></span>
<span data-ttu-id="71662-162">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="71662-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71662-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71662-163">-WhatIf</span></span>
<span data-ttu-id="71662-164">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="71662-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71662-165">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="71662-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71662-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71662-166">CommonParameters</span></span>
<span data-ttu-id="71662-167">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71662-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71662-168">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71662-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71662-169">Eingaben</span><span class="sxs-lookup"><span data-stu-id="71662-169">INPUTS</span></span>

### <span data-ttu-id="71662-170">System. String</span><span class="sxs-lookup"><span data-stu-id="71662-170">System.String</span></span>

### <span data-ttu-id="71662-171">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="71662-171">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="71662-172">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="71662-172">OUTPUTS</span></span>

### <span data-ttu-id="71662-173">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="71662-173">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="71662-174">Notizen</span><span class="sxs-lookup"><span data-stu-id="71662-174">NOTES</span></span>

## <span data-ttu-id="71662-175">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="71662-175">RELATED LINKS</span></span>

[<span data-ttu-id="71662-176">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="71662-176">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="71662-177">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="71662-177">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="71662-178">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="71662-178">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)


