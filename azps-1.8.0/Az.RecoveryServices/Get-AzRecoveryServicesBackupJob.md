---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 21498e13490b22b58621e2100dcc885442db7607
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659912"
---
# <span data-ttu-id="588e0-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="588e0-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="588e0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="588e0-102">SYNOPSIS</span></span>
<span data-ttu-id="588e0-103">Ruft Backup-Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="588e0-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="588e0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="588e0-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="588e0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="588e0-105">DESCRIPTION</span></span>
<span data-ttu-id="588e0-106">Das Cmdlet " **Get-AzRecoveryServicesBackupJob** " ruft Azure Backup-Aufträge für einen bestimmten Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="588e0-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="588e0-107">Setzen Sie den Vault-Kontext mithilfe des Set-AzRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="588e0-107">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="588e0-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="588e0-108">EXAMPLES</span></span>

### <span data-ttu-id="588e0-109">Beispiel 1: Abrufen aller in Bearbeitung befindlichen Aufträge</span><span class="sxs-lookup"><span data-stu-id="588e0-109">Example 1: Get all in-progress jobs</span></span>
```
PS C:\>$Joblist = Get-AzRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="588e0-110">Der erste Befehl ruft den Status eines in Bearbeitung befindlichen Auftrags als Array ab und speichert ihn dann in der $jobList Variablen.</span><span class="sxs-lookup"><span data-stu-id="588e0-110">The first command gets status of an in-progress job as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="588e0-111">Der zweite Befehl zeigt das erste Element im $jobList-Array an.</span><span class="sxs-lookup"><span data-stu-id="588e0-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="588e0-112">Beispiel 2: Abrufen aller fehlgeschlagenen Aufträge in den letzten 7 Tagen</span><span class="sxs-lookup"><span data-stu-id="588e0-112">Example 2: Get all failed jobs in the last 7 days</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

<span data-ttu-id="588e0-113">Dieser Befehl ruft fehlerhafte Aufträge aus der letzten Woche im Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="588e0-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="588e0-114">Der Parameter " *from* " gibt an, welche Uhrzeit sieben Tage in der Vergangenheit in UTC angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="588e0-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="588e0-115">Der Befehl gibt keinen Wert für den Parameter " *to" an* .</span><span class="sxs-lookup"><span data-stu-id="588e0-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="588e0-116">Daher wird der Standardwert für die aktuelle Uhrzeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="588e0-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="588e0-117">Beispiel 3: Abrufen eines in Bearbeitung befindlichen Auftrags und warten auf den Abschluss</span><span class="sxs-lookup"><span data-stu-id="588e0-117">Example 3: Get an in-progress job and wait for completion</span></span>
```
PS C:\> 
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress
$Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $job = Get-AzBackAzureRmRecoveryServicesBackupJob  -Job $Job
    }
    Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="588e0-118">Dieses Skript ruft den ersten Job ab, der gerade ausgeführt wird, bis der Auftrag abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="588e0-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="588e0-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="588e0-119">PARAMETERS</span></span>

### <span data-ttu-id="588e0-120">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="588e0-120">-BackupManagementType</span></span>
<span data-ttu-id="588e0-121">Gibt den Sicherungs Verwaltungstyp an.</span><span class="sxs-lookup"><span data-stu-id="588e0-121">Specifies the Backup management type.</span></span>
<span data-ttu-id="588e0-122">Derzeit wird nur AzureVM, AzureStorage unterstützt.</span><span class="sxs-lookup"><span data-stu-id="588e0-122">Currently, only AzureVM, AzureStorage is supported.</span></span>

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

### <span data-ttu-id="588e0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="588e0-123">-DefaultProfile</span></span>
<span data-ttu-id="588e0-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="588e0-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="588e0-125">-Ab</span><span class="sxs-lookup"><span data-stu-id="588e0-125">-From</span></span>
<span data-ttu-id="588e0-126">Gibt den Anfang als **DateTime** -Objekt eines Zeitbereichs für die Aufträge an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="588e0-126">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="588e0-127">Verwenden Sie das Get-Date-Cmdlet, um ein **DateTime** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="588e0-127">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="588e0-128">Wenn Sie weitere Informationen zu **DateTime** -Objekten wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="588e0-128">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="588e0-129">Verwenden des UTC-Formats für Datumsangaben</span><span class="sxs-lookup"><span data-stu-id="588e0-129">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="588e0-130">-Job</span><span class="sxs-lookup"><span data-stu-id="588e0-130">-Job</span></span>
<span data-ttu-id="588e0-131">Gibt den Namen des abzurufenden Sicherungsauftrags an.</span><span class="sxs-lookup"><span data-stu-id="588e0-131">Specifies the name of the Backup job to get.</span></span>

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

### <span data-ttu-id="588e0-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="588e0-132">-JobId</span></span>
<span data-ttu-id="588e0-133">Gibt die ID eines Auftrags an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="588e0-133">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="588e0-134">Die ID ist die InstanceId-Eigenschaft eines **AzureRmRecoveryServicesBackupJob** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="588e0-134">The ID is the InstanceId property of an **AzureRmRecoveryServicesBackupJob** object.</span></span>
<span data-ttu-id="588e0-135">Verwenden Sie Get-AzRecoveryServicesBackupJob, um ein **AzureRmRecoveryServicesBackupJob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="588e0-135">To obtain an **AzureRmRecoveryServicesBackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="588e0-136">-Vorgang</span><span class="sxs-lookup"><span data-stu-id="588e0-136">-Operation</span></span>
<span data-ttu-id="588e0-137">Gibt einen Vorgang der Aufträge an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="588e0-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="588e0-138">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="588e0-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="588e0-139">Backup</span><span class="sxs-lookup"><span data-stu-id="588e0-139">Backup</span></span>
- <span data-ttu-id="588e0-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="588e0-140">ConfigureBackup</span></span>
- <span data-ttu-id="588e0-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="588e0-141">DeleteBackupData</span></span>
- <span data-ttu-id="588e0-142">Registrieren</span><span class="sxs-lookup"><span data-stu-id="588e0-142">Register</span></span>
- <span data-ttu-id="588e0-143">Wiederherstellungs</span><span class="sxs-lookup"><span data-stu-id="588e0-143">Restore</span></span>
- <span data-ttu-id="588e0-144">Schutz aufheben</span><span class="sxs-lookup"><span data-stu-id="588e0-144">UnProtect</span></span>
- <span data-ttu-id="588e0-145">Registrierung</span><span class="sxs-lookup"><span data-stu-id="588e0-145">Unregister</span></span>

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

### <span data-ttu-id="588e0-146">-Status</span><span class="sxs-lookup"><span data-stu-id="588e0-146">-Status</span></span>
<span data-ttu-id="588e0-147">Gibt den Status der Aufträge an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="588e0-147">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="588e0-148">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="588e0-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="588e0-149">InProgress</span><span class="sxs-lookup"><span data-stu-id="588e0-149">InProgress</span></span>
- <span data-ttu-id="588e0-150">Fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="588e0-150">Failed</span></span>
- <span data-ttu-id="588e0-151">Storniert</span><span class="sxs-lookup"><span data-stu-id="588e0-151">Cancelled</span></span>
- <span data-ttu-id="588e0-152">Abbrechen</span><span class="sxs-lookup"><span data-stu-id="588e0-152">Cancelling</span></span>
- <span data-ttu-id="588e0-153">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="588e0-153">Completed</span></span>
- <span data-ttu-id="588e0-154">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="588e0-154">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="588e0-155">-To</span><span class="sxs-lookup"><span data-stu-id="588e0-155">-To</span></span>
<span data-ttu-id="588e0-156">Gibt das Ende als **DateTime** -Objekt eines Zeitbereichs für die Aufträge an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="588e0-156">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="588e0-157">Der Standardwert ist die aktuelle Systemzeit.</span><span class="sxs-lookup"><span data-stu-id="588e0-157">The default value is the current system time.</span></span>
<span data-ttu-id="588e0-158">Wenn Sie diesen Parameter angeben, müssen Sie auch den *from* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="588e0-158">If you specify this parameter, you must also specify the *From* parameter.</span></span>
<span data-ttu-id="588e0-159">Verwenden des UTC-Formats für Datumsangaben</span><span class="sxs-lookup"><span data-stu-id="588e0-159">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="588e0-160">-Tresor</span><span class="sxs-lookup"><span data-stu-id="588e0-160">-VaultId</span></span>
<span data-ttu-id="588e0-161">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="588e0-161">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="588e0-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="588e0-162">CommonParameters</span></span>
<span data-ttu-id="588e0-163">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="588e0-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="588e0-164">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="588e0-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="588e0-165">Eingaben</span><span class="sxs-lookup"><span data-stu-id="588e0-165">INPUTS</span></span>

### <span data-ttu-id="588e0-166">System. String</span><span class="sxs-lookup"><span data-stu-id="588e0-166">System.String</span></span>

## <span data-ttu-id="588e0-167">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="588e0-167">OUTPUTS</span></span>

### <span data-ttu-id="588e0-168">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="588e0-168">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="588e0-169">Notizen</span><span class="sxs-lookup"><span data-stu-id="588e0-169">NOTES</span></span>

## <span data-ttu-id="588e0-170">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="588e0-170">RELATED LINKS</span></span>

[<span data-ttu-id="588e0-171">Get-AzRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="588e0-171">Get-AzRecoveryServicesBackupJobDetails</span></span>](./Get-AzRecoveryServicesBackupJobDetails.md)

[<span data-ttu-id="588e0-172">Stopp-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="588e0-172">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="588e0-173">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="588e0-173">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)


