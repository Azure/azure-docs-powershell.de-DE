---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: cc23d8535e7aaca656379811121ed09bad2f64bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824359"
---
# <span data-ttu-id="f750c-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="f750c-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="f750c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f750c-102">SYNOPSIS</span></span>

<span data-ttu-id="f750c-103">Ruft Backup-Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="f750c-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="f750c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f750c-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f750c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f750c-105">DESCRIPTION</span></span>

<span data-ttu-id="f750c-106">Das Cmdlet " **Get-AzRecoveryServicesBackupJob** " ruft Azure Backup-Aufträge für einen bestimmten Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="f750c-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="f750c-107">Setzen Sie den Vault-Kontext mithilfe des-Vault-Parameters.</span><span class="sxs-lookup"><span data-stu-id="f750c-107">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="f750c-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f750c-108">EXAMPLES</span></span>

### <span data-ttu-id="f750c-109">Beispiel 1: Abrufen aller in Bearbeitung befindlichen Aufträge</span><span class="sxs-lookup"><span data-stu-id="f750c-109">Example 1: Get all in-progress jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="f750c-110">Der erste Befehl ruft den Status eines ausgeführten Auftrags als Array ab und speichert ihn dann in der $jobList Variablen.</span><span class="sxs-lookup"><span data-stu-id="f750c-110">The first command gets status of an in-progress jobs as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="f750c-111">Der zweite Befehl zeigt das erste Element im $jobList-Array an.</span><span class="sxs-lookup"><span data-stu-id="f750c-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="f750c-112">Beispiel 2: Abrufen aller fehlgeschlagenen Aufträge in den letzten 7 Tagen</span><span class="sxs-lookup"><span data-stu-id="f750c-112">Example 2: Get all failed jobs in the last 7 days</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

<span data-ttu-id="f750c-113">Dieser Befehl ruft fehlerhafte Aufträge aus der letzten Woche im Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="f750c-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="f750c-114">Der Parameter " *from* " gibt an, welche Uhrzeit sieben Tage in der Vergangenheit in UTC angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="f750c-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="f750c-115">Der Befehl gibt keinen Wert für den Parameter " *to" an* .</span><span class="sxs-lookup"><span data-stu-id="f750c-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="f750c-116">Daher wird der Standardwert für die aktuelle Uhrzeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="f750c-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="f750c-117">Beispiel 3: Abrufen eines in Bearbeitung befindlichen Auftrags und warten auf den Abschluss</span><span class="sxs-lookup"><span data-stu-id="f750c-117">Example 3: Get an in-progress job and wait for completion</span></span>

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

<span data-ttu-id="f750c-118">Dieses Skript ruft den ersten Job ab, der gerade ausgeführt wird, bis der Auftrag abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="f750c-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="f750c-119">Hinweis: Sie können das Cmdlet **Wait-AzRecoveryServicesBackupJob** verwenden, um auf den Abschluss eines Azure Backup-Auftrags anstatt auf while-Schleife zu warten.</span><span class="sxs-lookup"><span data-stu-id="f750c-119">Note: You can use **Wait-AzRecoveryServicesBackupJob** cmdlet to wait for an Azure Backup job to finish instead of While loop.</span></span>

## <span data-ttu-id="f750c-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="f750c-120">PARAMETERS</span></span>

### <span data-ttu-id="f750c-121">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="f750c-121">-BackupManagementType</span></span>

<span data-ttu-id="f750c-122">Gibt den Sicherungs Verwaltungstyp an.</span><span class="sxs-lookup"><span data-stu-id="f750c-122">Specifies the Backup management type.</span></span>
<span data-ttu-id="f750c-123">Derzeit wird nur AzureVM, AzureStorage unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f750c-123">Currently, only AzureVM, AzureStorage is supported.</span></span>

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

### <span data-ttu-id="f750c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f750c-124">-DefaultProfile</span></span>

<span data-ttu-id="f750c-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f750c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f750c-126">-Ab</span><span class="sxs-lookup"><span data-stu-id="f750c-126">-From</span></span>

<span data-ttu-id="f750c-127">Gibt den Anfang als **DateTime** -Objekt eines Zeitbereichs für die Aufträge an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="f750c-127">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="f750c-128">Verwenden Sie das Cmdlet " **Get-Date** ", um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f750c-128">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="f750c-129">Wenn Sie weitere Informationen zu **DateTime** -Objekten wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="f750c-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="f750c-130">Verwenden des UTC-Formats für Datumsangaben</span><span class="sxs-lookup"><span data-stu-id="f750c-130">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="f750c-131">-Job</span><span class="sxs-lookup"><span data-stu-id="f750c-131">-Job</span></span>

<span data-ttu-id="f750c-132">Gibt den abzurufenden Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="f750c-132">Specifies the job to get.</span></span>

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

### <span data-ttu-id="f750c-133">-JobId</span><span class="sxs-lookup"><span data-stu-id="f750c-133">-JobId</span></span>

<span data-ttu-id="f750c-134">Gibt die ID eines Auftrags an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="f750c-134">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="f750c-135">Die ID ist die JobId-Eigenschaft eines **Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="f750c-135">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="f750c-136">-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f750c-136">-Operation</span></span>

<span data-ttu-id="f750c-137">Gibt einen Vorgang der Aufträge an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="f750c-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="f750c-138">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f750c-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f750c-139">Backup</span><span class="sxs-lookup"><span data-stu-id="f750c-139">Backup</span></span>
- <span data-ttu-id="f750c-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="f750c-140">ConfigureBackup</span></span>
- <span data-ttu-id="f750c-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="f750c-141">DeleteBackupData</span></span>
- <span data-ttu-id="f750c-142">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="f750c-142">DisableBackup</span></span>
- <span data-ttu-id="f750c-143">Wiederherstellungs</span><span class="sxs-lookup"><span data-stu-id="f750c-143">Restore</span></span>

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

### <span data-ttu-id="f750c-144">-Status</span><span class="sxs-lookup"><span data-stu-id="f750c-144">-Status</span></span>

<span data-ttu-id="f750c-145">Gibt den Status der Aufträge an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="f750c-145">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="f750c-146">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f750c-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f750c-147">InProgress</span><span class="sxs-lookup"><span data-stu-id="f750c-147">InProgress</span></span>
- <span data-ttu-id="f750c-148">Fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="f750c-148">Failed</span></span>
- <span data-ttu-id="f750c-149">Storniert</span><span class="sxs-lookup"><span data-stu-id="f750c-149">Cancelled</span></span>
- <span data-ttu-id="f750c-150">Abbrechen</span><span class="sxs-lookup"><span data-stu-id="f750c-150">Cancelling</span></span>
- <span data-ttu-id="f750c-151">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="f750c-151">Completed</span></span>
- <span data-ttu-id="f750c-152">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="f750c-152">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="f750c-153">-To</span><span class="sxs-lookup"><span data-stu-id="f750c-153">-To</span></span>

<span data-ttu-id="f750c-154">Gibt das Ende als **DateTime** -Objekt eines Zeitbereichs für die Aufträge an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="f750c-154">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="f750c-155">Der Standardwert ist die aktuelle Systemzeit.</span><span class="sxs-lookup"><span data-stu-id="f750c-155">The default value is the current system time.</span></span>
<span data-ttu-id="f750c-156">Wenn Sie diesen Parameter angeben, müssen Sie auch den **-from-** Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="f750c-156">If you specify this parameter, you must also specify the **-From** parameter.</span></span>
<span data-ttu-id="f750c-157">Verwenden des UTC-Formats für Datumsangaben</span><span class="sxs-lookup"><span data-stu-id="f750c-157">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="f750c-158">-Tresor</span><span class="sxs-lookup"><span data-stu-id="f750c-158">-VaultId</span></span>

<span data-ttu-id="f750c-159">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="f750c-159">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="f750c-160">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f750c-160">-CommonParameters</span></span>

<span data-ttu-id="f750c-161">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f750c-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f750c-162">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f750c-162">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f750c-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f750c-163">INPUTS</span></span>

### <span data-ttu-id="f750c-164">System. String</span><span class="sxs-lookup"><span data-stu-id="f750c-164">System.String</span></span>

## <span data-ttu-id="f750c-165">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f750c-165">OUTPUTS</span></span>

### <span data-ttu-id="f750c-166">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="f750c-166">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="f750c-167">Notizen</span><span class="sxs-lookup"><span data-stu-id="f750c-167">NOTES</span></span>

## <span data-ttu-id="f750c-168">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f750c-168">RELATED LINKS</span></span>

[<span data-ttu-id="f750c-169">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="f750c-169">Get-AzRecoveryServicesBackupJobDetail</span></span>](./Get-AzRecoveryServicesBackupJobDetail.md)

[<span data-ttu-id="f750c-170">Stopp-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="f750c-170">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="f750c-171">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="f750c-171">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)
