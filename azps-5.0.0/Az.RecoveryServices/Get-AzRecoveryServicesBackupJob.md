---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 623acc7d96fc6c3dc4f1496f42a53bf276f8e778
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301228"
---
# <span data-ttu-id="5313a-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="5313a-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="5313a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5313a-102">SYNOPSIS</span></span>

<span data-ttu-id="5313a-103">Ruft Backup-Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="5313a-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="5313a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5313a-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5313a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5313a-105">DESCRIPTION</span></span>

<span data-ttu-id="5313a-106">Das Cmdlet " **Get-AzRecoveryServicesBackupJob** " ruft Azure Backup-Aufträge für einen bestimmten Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="5313a-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="5313a-107">Setzen Sie den Vault-Kontext mithilfe des-Vault-Parameters.</span><span class="sxs-lookup"><span data-stu-id="5313a-107">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="5313a-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5313a-108">EXAMPLES</span></span>

### <span data-ttu-id="5313a-109">Beispiel 1: Abrufen aller in Bearbeitung befindlichen Aufträge</span><span class="sxs-lookup"><span data-stu-id="5313a-109">Example 1: Get all in-progress jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="5313a-110">Der erste Befehl ruft den Status eines ausgeführten Auftrags als Array ab und speichert ihn dann in der $jobList Variablen.</span><span class="sxs-lookup"><span data-stu-id="5313a-110">The first command gets status of an in-progress jobs as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="5313a-111">Der zweite Befehl zeigt das erste Element im $jobList-Array an.</span><span class="sxs-lookup"><span data-stu-id="5313a-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="5313a-112">Beispiel 2: Abrufen aller fehlgeschlagenen Aufträge in den letzten 7 Tagen</span><span class="sxs-lookup"><span data-stu-id="5313a-112">Example 2: Get all failed jobs in the last 7 days</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

<span data-ttu-id="5313a-113">Dieser Befehl ruft fehlerhafte Aufträge aus der letzten Woche im Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="5313a-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="5313a-114">Der Parameter " *from* " gibt an, welche Uhrzeit sieben Tage in der Vergangenheit in UTC angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="5313a-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="5313a-115">Der Befehl gibt keinen Wert für den Parameter " *to" an* .</span><span class="sxs-lookup"><span data-stu-id="5313a-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="5313a-116">Daher wird der Standardwert für die aktuelle Uhrzeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="5313a-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="5313a-117">Beispiel 3: Abrufen eines in Bearbeitung befindlichen Auftrags und warten auf den Abschluss</span><span class="sxs-lookup"><span data-stu-id="5313a-117">Example 3: Get an in-progress job and wait for completion</span></span>

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
$Job = $Jobs[0]
While ( $Job.Status -ne Completed ) {
    Write-Host -Object "Waiting for completion..."
    Start-Sleep -Seconds 10
    $Job = Get-AzRecoveryServicesBackupJob -Job $Job -VaultId $vault.ID
}
Write-Host -Object "Done!"

Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

<span data-ttu-id="5313a-118">Dieses Skript ruft den ersten Job ab, der gerade ausgeführt wird, bis der Auftrag abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="5313a-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="5313a-119">Hinweis: Sie können das Cmdlet **Wait-AzRecoveryServicesBackupJob** verwenden, um auf den Abschluss eines Azure Backup-Auftrags anstatt auf while-Schleife zu warten.</span><span class="sxs-lookup"><span data-stu-id="5313a-119">Note: You can use **Wait-AzRecoveryServicesBackupJob** cmdlet to wait for an Azure Backup job to finish instead of While loop.</span></span>

### <span data-ttu-id="5313a-120">Beispiel 4: Abrufen aller AzureVM-Aufträge in den letzten 2 Tagen, die erfolgreich abgeschlossen wurden</span><span class="sxs-lookup"><span data-stu-id="5313a-120">Example 4: Get all AzureVM jobs in last 2 days which finished successfully</span></span>

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob  -VaultId $vault.ID  -Status Completed -From (Get-Date).AddDays(-2).ToUniversalTime() -BackupManagementType AzureVM
```
<span data-ttu-id="5313a-121">Das erste Cmdlet ruft das Vault-Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="5313a-121">First cmdlet fetches the vault object.</span></span> <span data-ttu-id="5313a-122">Das zweite Cmdlet speichert alle AzureVM-Aufträge im angegebenen Tresor, die in den letzten 2 Tagen in $Jobs abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="5313a-122">Second cmdlet stores all the AzureVM jobs in the given vault which completed in last 2 days to $jobs.</span></span> <span data-ttu-id="5313a-123">Ändern Sie den Wert des BackupManagementType-Parameters in MAB, um MAB-Agent-Aufträge abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5313a-123">Change the value of BackupManagementType parameter to MAB in order to fetch MAB agent jobs.</span></span>

## <span data-ttu-id="5313a-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="5313a-124">PARAMETERS</span></span>

### <span data-ttu-id="5313a-125">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="5313a-125">-BackupManagementType</span></span>

<span data-ttu-id="5313a-126">Die Klasse der Ressourcen, die geschützt werden.</span><span class="sxs-lookup"><span data-stu-id="5313a-126">The class of resources being protected.</span></span> <span data-ttu-id="5313a-127">Derzeit sind die für dieses Cmdlet unterstützten Werte AzureVM, AzureStorage, AzureWorkload, MAB.</span><span class="sxs-lookup"><span data-stu-id="5313a-127">Currently the values supported for this cmdlet are AzureVM, AzureStorage, AzureWorkload, MAB.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload, MAB

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5313a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5313a-128">-DefaultProfile</span></span>

<span data-ttu-id="5313a-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5313a-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5313a-130">-Ab</span><span class="sxs-lookup"><span data-stu-id="5313a-130">-From</span></span>

<span data-ttu-id="5313a-131">Gibt den Anfang als **DateTime** -Objekt eines Zeitbereichs für die Aufträge an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5313a-131">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="5313a-132">Verwenden Sie das Cmdlet " **Get-Date** ", um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5313a-132">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="5313a-133">Wenn Sie weitere Informationen zu **DateTime** -Objekten wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="5313a-133">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="5313a-134">Verwenden des UTC-Formats für Datumsangaben</span><span class="sxs-lookup"><span data-stu-id="5313a-134">Use UTC format for dates.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5313a-135">-Job</span><span class="sxs-lookup"><span data-stu-id="5313a-135">-Job</span></span>

<span data-ttu-id="5313a-136">Gibt den abzurufenden Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="5313a-136">Specifies the job to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5313a-137">-JobId</span><span class="sxs-lookup"><span data-stu-id="5313a-137">-JobId</span></span>

<span data-ttu-id="5313a-138">Gibt die ID eines Auftrags an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5313a-138">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="5313a-139">Die ID ist die JobId-Eigenschaft eines **Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="5313a-139">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="5313a-140">-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5313a-140">-Operation</span></span>

<span data-ttu-id="5313a-141">Gibt einen Vorgang der Aufträge an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5313a-141">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="5313a-142">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5313a-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5313a-143">Backup</span><span class="sxs-lookup"><span data-stu-id="5313a-143">Backup</span></span>
- <span data-ttu-id="5313a-144">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="5313a-144">ConfigureBackup</span></span>
- <span data-ttu-id="5313a-145">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="5313a-145">DeleteBackupData</span></span>
- <span data-ttu-id="5313a-146">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="5313a-146">DisableBackup</span></span>
- <span data-ttu-id="5313a-147">Wiederherstellungs</span><span class="sxs-lookup"><span data-stu-id="5313a-147">Restore</span></span>
- <span data-ttu-id="5313a-148">BackupDataMove</span><span class="sxs-lookup"><span data-stu-id="5313a-148">BackupDataMove</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobOperation]
Parameter Sets: (All)
Aliases:
Accepted values: Backup, Restore, ConfigureBackup, DisableBackup, DeleteBackupData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5313a-149">-Status</span><span class="sxs-lookup"><span data-stu-id="5313a-149">-Status</span></span>

<span data-ttu-id="5313a-150">Gibt den Status der Aufträge an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5313a-150">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="5313a-151">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5313a-151">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5313a-152">InProgress</span><span class="sxs-lookup"><span data-stu-id="5313a-152">InProgress</span></span>
- <span data-ttu-id="5313a-153">Fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="5313a-153">Failed</span></span>
- <span data-ttu-id="5313a-154">Storniert</span><span class="sxs-lookup"><span data-stu-id="5313a-154">Cancelled</span></span>
- <span data-ttu-id="5313a-155">Abbrechen</span><span class="sxs-lookup"><span data-stu-id="5313a-155">Cancelling</span></span>
- <span data-ttu-id="5313a-156">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="5313a-156">Completed</span></span>
- <span data-ttu-id="5313a-157">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="5313a-157">CompletedWithWarnings</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobStatus]
Parameter Sets: (All)
Aliases:
Accepted values: InProgress, Cancelling, Cancelled, Completed, CompletedWithWarnings, Failed

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5313a-158">-To</span><span class="sxs-lookup"><span data-stu-id="5313a-158">-To</span></span>

<span data-ttu-id="5313a-159">Gibt das Ende als **DateTime** -Objekt eines Zeitbereichs für die Aufträge an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5313a-159">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="5313a-160">Der Standardwert ist die aktuelle Systemzeit.</span><span class="sxs-lookup"><span data-stu-id="5313a-160">The default value is the current system time.</span></span>
<span data-ttu-id="5313a-161">Wenn Sie diesen Parameter angeben, müssen Sie auch den **-from-** Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="5313a-161">If you specify this parameter, you must also specify the **-From** parameter.</span></span>
<span data-ttu-id="5313a-162">Verwenden des UTC-Formats für Datumsangaben</span><span class="sxs-lookup"><span data-stu-id="5313a-162">Use UTC format for dates.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5313a-163">-Tresor</span><span class="sxs-lookup"><span data-stu-id="5313a-163">-VaultId</span></span>

<span data-ttu-id="5313a-164">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="5313a-164">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="5313a-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5313a-165">CommonParameters</span></span>
<span data-ttu-id="5313a-166">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5313a-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5313a-167">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5313a-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5313a-168">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5313a-168">INPUTS</span></span>

### <span data-ttu-id="5313a-169">System. String</span><span class="sxs-lookup"><span data-stu-id="5313a-169">System.String</span></span>

## <span data-ttu-id="5313a-170">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5313a-170">OUTPUTS</span></span>

### <span data-ttu-id="5313a-171">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="5313a-171">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="5313a-172">Notizen</span><span class="sxs-lookup"><span data-stu-id="5313a-172">NOTES</span></span>

## <span data-ttu-id="5313a-173">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5313a-173">RELATED LINKS</span></span>

[<span data-ttu-id="5313a-174">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="5313a-174">Get-AzRecoveryServicesBackupJobDetail</span></span>](./Get-AzRecoveryServicesBackupJobDetail.md)

[<span data-ttu-id="5313a-175">Stopp-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="5313a-175">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="5313a-176">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="5313a-176">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)
