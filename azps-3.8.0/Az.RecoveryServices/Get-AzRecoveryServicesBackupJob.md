---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 4d5ec07e7a068e1ab96f485ee67db0c1dd43f388
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995590"
---
# <span data-ttu-id="d3291-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="d3291-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="d3291-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d3291-102">SYNOPSIS</span></span>

<span data-ttu-id="d3291-103">Ruft Backup-Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="d3291-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="d3291-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3291-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3291-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d3291-105">DESCRIPTION</span></span>

<span data-ttu-id="d3291-106">Das Cmdlet " **Get-AzRecoveryServicesBackupJob** " ruft Azure Backup-Aufträge für einen bestimmten Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="d3291-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="d3291-107">Setzen Sie den Vault-Kontext mithilfe des-Vault-Parameters.</span><span class="sxs-lookup"><span data-stu-id="d3291-107">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="d3291-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d3291-108">EXAMPLES</span></span>

### <span data-ttu-id="d3291-109">Beispiel 1: Abrufen aller in Bearbeitung befindlichen Aufträge</span><span class="sxs-lookup"><span data-stu-id="d3291-109">Example 1: Get all in-progress jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="d3291-110">Der erste Befehl ruft den Status eines ausgeführten Auftrags als Array ab und speichert ihn dann in der $jobList Variablen.</span><span class="sxs-lookup"><span data-stu-id="d3291-110">The first command gets status of an in-progress jobs as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="d3291-111">Der zweite Befehl zeigt das erste Element im $jobList-Array an.</span><span class="sxs-lookup"><span data-stu-id="d3291-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="d3291-112">Beispiel 2: Abrufen aller fehlgeschlagenen Aufträge in den letzten 7 Tagen</span><span class="sxs-lookup"><span data-stu-id="d3291-112">Example 2: Get all failed jobs in the last 7 days</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

<span data-ttu-id="d3291-113">Dieser Befehl ruft fehlerhafte Aufträge aus der letzten Woche im Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="d3291-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="d3291-114">Der Parameter " *from* " gibt an, welche Uhrzeit sieben Tage in der Vergangenheit in UTC angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="d3291-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="d3291-115">Der Befehl gibt keinen Wert für den Parameter " *to" an* .</span><span class="sxs-lookup"><span data-stu-id="d3291-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="d3291-116">Daher wird der Standardwert für die aktuelle Uhrzeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="d3291-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="d3291-117">Beispiel 3: Abrufen eines in Bearbeitung befindlichen Auftrags und warten auf den Abschluss</span><span class="sxs-lookup"><span data-stu-id="d3291-117">Example 3: Get an in-progress job and wait for completion</span></span>

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

<span data-ttu-id="d3291-118">Dieses Skript ruft den ersten Job ab, der gerade ausgeführt wird, bis der Auftrag abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="d3291-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="d3291-119">Hinweis: Sie können das Cmdlet **Wait-AzRecoveryServicesBackupJob** verwenden, um auf den Abschluss eines Azure Backup-Auftrags anstatt auf while-Schleife zu warten.</span><span class="sxs-lookup"><span data-stu-id="d3291-119">Note: You can use **Wait-AzRecoveryServicesBackupJob** cmdlet to wait for an Azure Backup job to finish instead of While loop.</span></span>

## <span data-ttu-id="d3291-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3291-120">PARAMETERS</span></span>

### <span data-ttu-id="d3291-121">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="d3291-121">-BackupManagementType</span></span>

<span data-ttu-id="d3291-122">Gibt den Sicherungs Verwaltungstyp an.</span><span class="sxs-lookup"><span data-stu-id="d3291-122">Specifies the Backup management type.</span></span>
<span data-ttu-id="d3291-123">Derzeit wird nur AzureVM, AzureStorage unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d3291-123">Currently, only AzureVM, AzureStorage is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3291-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3291-124">-DefaultProfile</span></span>

<span data-ttu-id="d3291-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d3291-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3291-126">-Ab</span><span class="sxs-lookup"><span data-stu-id="d3291-126">-From</span></span>

<span data-ttu-id="d3291-127">Gibt den Anfang als **DateTime** -Objekt eines Zeitbereichs für die Aufträge an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="d3291-127">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="d3291-128">Verwenden Sie das Cmdlet " **Get-Date** ", um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d3291-128">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="d3291-129">Wenn Sie weitere Informationen zu **DateTime** -Objekten wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="d3291-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="d3291-130">Verwenden des UTC-Formats für Datumsangaben</span><span class="sxs-lookup"><span data-stu-id="d3291-130">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="d3291-131">-Job</span><span class="sxs-lookup"><span data-stu-id="d3291-131">-Job</span></span>

<span data-ttu-id="d3291-132">Gibt den abzurufenden Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="d3291-132">Specifies the job to get.</span></span>

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

### <span data-ttu-id="d3291-133">-JobId</span><span class="sxs-lookup"><span data-stu-id="d3291-133">-JobId</span></span>

<span data-ttu-id="d3291-134">Gibt die ID eines Auftrags an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="d3291-134">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="d3291-135">Die ID ist die JobId-Eigenschaft eines **Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="d3291-135">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="d3291-136">-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d3291-136">-Operation</span></span>

<span data-ttu-id="d3291-137">Gibt einen Vorgang der Aufträge an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="d3291-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="d3291-138">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d3291-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d3291-139">Backup</span><span class="sxs-lookup"><span data-stu-id="d3291-139">Backup</span></span>
- <span data-ttu-id="d3291-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="d3291-140">ConfigureBackup</span></span>
- <span data-ttu-id="d3291-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="d3291-141">DeleteBackupData</span></span>
- <span data-ttu-id="d3291-142">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="d3291-142">DisableBackup</span></span>
- <span data-ttu-id="d3291-143">Wiederherstellungs</span><span class="sxs-lookup"><span data-stu-id="d3291-143">Restore</span></span>

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

### <span data-ttu-id="d3291-144">-Status</span><span class="sxs-lookup"><span data-stu-id="d3291-144">-Status</span></span>

<span data-ttu-id="d3291-145">Gibt den Status der Aufträge an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="d3291-145">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="d3291-146">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d3291-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d3291-147">InProgress</span><span class="sxs-lookup"><span data-stu-id="d3291-147">InProgress</span></span>
- <span data-ttu-id="d3291-148">Fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="d3291-148">Failed</span></span>
- <span data-ttu-id="d3291-149">Storniert</span><span class="sxs-lookup"><span data-stu-id="d3291-149">Cancelled</span></span>
- <span data-ttu-id="d3291-150">Abbrechen</span><span class="sxs-lookup"><span data-stu-id="d3291-150">Cancelling</span></span>
- <span data-ttu-id="d3291-151">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="d3291-151">Completed</span></span>
- <span data-ttu-id="d3291-152">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="d3291-152">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="d3291-153">-To</span><span class="sxs-lookup"><span data-stu-id="d3291-153">-To</span></span>

<span data-ttu-id="d3291-154">Gibt das Ende als **DateTime** -Objekt eines Zeitbereichs für die Aufträge an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="d3291-154">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="d3291-155">Der Standardwert ist die aktuelle Systemzeit.</span><span class="sxs-lookup"><span data-stu-id="d3291-155">The default value is the current system time.</span></span>
<span data-ttu-id="d3291-156">Wenn Sie diesen Parameter angeben, müssen Sie auch den **-from-** Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="d3291-156">If you specify this parameter, you must also specify the **-From** parameter.</span></span>
<span data-ttu-id="d3291-157">Verwenden des UTC-Formats für Datumsangaben</span><span class="sxs-lookup"><span data-stu-id="d3291-157">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="d3291-158">-Tresor</span><span class="sxs-lookup"><span data-stu-id="d3291-158">-VaultId</span></span>

<span data-ttu-id="d3291-159">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="d3291-159">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="d3291-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3291-160">CommonParameters</span></span>
<span data-ttu-id="d3291-161">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3291-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3291-162">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3291-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3291-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d3291-163">INPUTS</span></span>

### <span data-ttu-id="d3291-164">System. String</span><span class="sxs-lookup"><span data-stu-id="d3291-164">System.String</span></span>

## <span data-ttu-id="d3291-165">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d3291-165">OUTPUTS</span></span>

### <span data-ttu-id="d3291-166">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="d3291-166">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="d3291-167">Notizen</span><span class="sxs-lookup"><span data-stu-id="d3291-167">NOTES</span></span>

## <span data-ttu-id="d3291-168">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d3291-168">RELATED LINKS</span></span>

[<span data-ttu-id="d3291-169">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="d3291-169">Get-AzRecoveryServicesBackupJobDetail</span></span>](./Get-AzRecoveryServicesBackupJobDetail.md)

[<span data-ttu-id="d3291-170">Stopp-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="d3291-170">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="d3291-171">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="d3291-171">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)
