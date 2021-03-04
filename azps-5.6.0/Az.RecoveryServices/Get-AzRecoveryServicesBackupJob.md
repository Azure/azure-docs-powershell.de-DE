---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 011b27cfff166173d485636a1e8890d917484651
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934736"
---
# <span data-ttu-id="ab599-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="ab599-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="ab599-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab599-102">SYNOPSIS</span></span>

<span data-ttu-id="ab599-103">Ruft Sicherungsaufträge ab.</span><span class="sxs-lookup"><span data-stu-id="ab599-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="ab599-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab599-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
  [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab599-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ab599-105">DESCRIPTION</span></span>

<span data-ttu-id="ab599-106">Das **Get-AzRecoveryServicesBackupJob-Cmdlet** ruft Azure-Sicherungsaufträge für einen bestimmten Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="ab599-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="ab599-107">Legen Sie den Tresorkontext mithilfe des -VaultId-Parameters ein.</span><span class="sxs-lookup"><span data-stu-id="ab599-107">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="ab599-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ab599-108">EXAMPLES</span></span>

### <span data-ttu-id="ab599-109">Beispiel 1: Alle in Bearbeitung ausgeführten Aufträge erhalten</span><span class="sxs-lookup"><span data-stu-id="ab599-109">Example 1: Get all in-progress jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="ab599-110">Der erste Befehl ruft den Status eines aktuellen Jobs als Array ab und speichert ihn dann in der $Joblist Variablen.</span><span class="sxs-lookup"><span data-stu-id="ab599-110">The first command gets status of an in-progress jobs as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="ab599-111">Mit dem zweiten Befehl wird das erste Element im array $Joblist angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ab599-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="ab599-112">Beispiel 2: Alle fehlgeschlagenen Aufträge in den letzten 7 Tagen erhalten</span><span class="sxs-lookup"><span data-stu-id="ab599-112">Example 2: Get all failed jobs in the last 7 days</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

<span data-ttu-id="ab599-113">Dieser Befehl ruft fehlgeschlagene Aufträge aus der letzten Woche im Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="ab599-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="ab599-114">Der *Parameter Von* gibt eine in UTC angegebene Zeit von sieben Tagen in der Vergangenheit an.</span><span class="sxs-lookup"><span data-stu-id="ab599-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="ab599-115">Der Befehl gibt keinen Wert für den Parameter *An* an an.</span><span class="sxs-lookup"><span data-stu-id="ab599-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="ab599-116">Daher wird der Standardwert der aktuellen Uhrzeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="ab599-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="ab599-117">Beispiel 3: Erhalten eines in Bearbeitung ausgeführten Auftrags und Warten auf den Abschluss</span><span class="sxs-lookup"><span data-stu-id="ab599-117">Example 3: Get an in-progress job and wait for completion</span></span>

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

<span data-ttu-id="ab599-118">Dieses Skript abruft den ersten Auftrag, der zurzeit ausgeführt wird, bis der Auftrag abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="ab599-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="ab599-119">Hinweis: Sie können das **Cmdlet Wait-AzRecoveryServicesBackupJob** verwenden, um auf den Abschluss eines Azure-Sicherungsauftrags statt auf die While-Schleife zu warten.</span><span class="sxs-lookup"><span data-stu-id="ab599-119">Note: You can use **Wait-AzRecoveryServicesBackupJob** cmdlet to wait for an Azure Backup job to finish instead of While loop.</span></span>

### <span data-ttu-id="ab599-120">Beispiel 4: Alle AzureVM-Aufträge in den letzten 2 Tagen erhalten, die erfolgreich abgeschlossen wurden</span><span class="sxs-lookup"><span data-stu-id="ab599-120">Example 4: Get all AzureVM jobs in last 2 days which finished successfully</span></span>

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob  -VaultId $vault.ID  -Status Completed -From (Get-Date).AddDays(-2).ToUniversalTime() -BackupManagementType AzureVM
```
<span data-ttu-id="ab599-121">Das erste Cmdlet ruft das Tresorobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="ab599-121">First cmdlet fetches the vault object.</span></span> <span data-ttu-id="ab599-122">Das zweite Cmdlet speichert alle AzureVM-Aufträge im angegebenen Tresor, der in den letzten 2 Tagen abgeschlossen wurde, um $jobs.</span><span class="sxs-lookup"><span data-stu-id="ab599-122">Second cmdlet stores all the AzureVM jobs in the given vault which completed in last 2 days to $jobs.</span></span> <span data-ttu-id="ab599-123">Ändern Sie den Wert des Parameters BackupManagementType in MAB, um MAB-Agentaufträge abrufen zu können.</span><span class="sxs-lookup"><span data-stu-id="ab599-123">Change the value of BackupManagementType parameter to MAB in order to fetch MAB agent jobs.</span></span>

## <span data-ttu-id="ab599-124">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ab599-124">PARAMETERS</span></span>

### <span data-ttu-id="ab599-125">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="ab599-125">-BackupManagementType</span></span>

<span data-ttu-id="ab599-126">Die Klasse der zu schützenden Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="ab599-126">The class of resources being protected.</span></span> <span data-ttu-id="ab599-127">Derzeit werden für dieses Cmdlet AzureVM, AzureStorage, AzureWorkload und MAB unterstützte Werte unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ab599-127">Currently the values supported for this cmdlet are AzureVM, AzureStorage, AzureWorkload, MAB.</span></span>

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

### <span data-ttu-id="ab599-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab599-128">-DefaultProfile</span></span>

<span data-ttu-id="ab599-129">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab599-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab599-130">-Von</span><span class="sxs-lookup"><span data-stu-id="ab599-130">-From</span></span>

<span data-ttu-id="ab599-131">Gibt den Anfang als **DateTime-Objekt** eines Zeitbereichs für die Aufträge an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="ab599-131">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="ab599-132">Verwenden Sie zum Abrufen eines **DateTime-Objekts** **das Get-Date-Cmdlet.**</span><span class="sxs-lookup"><span data-stu-id="ab599-132">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="ab599-133">Weitere Informationen zu **DateTime-Objekten** finden Sie unter `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="ab599-133">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="ab599-134">Verwenden Sie das UTC-Format für Datumsangaben.</span><span class="sxs-lookup"><span data-stu-id="ab599-134">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="ab599-135">-Job</span><span class="sxs-lookup"><span data-stu-id="ab599-135">-Job</span></span>

<span data-ttu-id="ab599-136">Gibt den zu erhaltenden Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="ab599-136">Specifies the job to get.</span></span>

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

### <span data-ttu-id="ab599-137">-JobId</span><span class="sxs-lookup"><span data-stu-id="ab599-137">-JobId</span></span>

<span data-ttu-id="ab599-138">Gibt die ID eines Auftrags an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="ab599-138">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="ab599-139">Die ID ist die JobId-Eigenschaft eines **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase-Objekts.**</span><span class="sxs-lookup"><span data-stu-id="ab599-139">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="ab599-140">-Operation</span><span class="sxs-lookup"><span data-stu-id="ab599-140">-Operation</span></span>

<span data-ttu-id="ab599-141">Gibt einen Vorgang der Aufträge an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="ab599-141">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="ab599-142">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="ab599-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ab599-143">Sicherung</span><span class="sxs-lookup"><span data-stu-id="ab599-143">Backup</span></span>
- <span data-ttu-id="ab599-144">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="ab599-144">ConfigureBackup</span></span>
- <span data-ttu-id="ab599-145">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="ab599-145">DeleteBackupData</span></span>
- <span data-ttu-id="ab599-146">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="ab599-146">DisableBackup</span></span>
- <span data-ttu-id="ab599-147">Wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="ab599-147">Restore</span></span>
- <span data-ttu-id="ab599-148">BackupDataMove</span><span class="sxs-lookup"><span data-stu-id="ab599-148">BackupDataMove</span></span>

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

### <span data-ttu-id="ab599-149">-Status</span><span class="sxs-lookup"><span data-stu-id="ab599-149">-Status</span></span>

<span data-ttu-id="ab599-150">Gibt einen Status der Aufträge an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="ab599-150">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="ab599-151">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="ab599-151">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ab599-152">InProgress</span><span class="sxs-lookup"><span data-stu-id="ab599-152">InProgress</span></span>
- <span data-ttu-id="ab599-153">Fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="ab599-153">Failed</span></span>
- <span data-ttu-id="ab599-154">Storniert</span><span class="sxs-lookup"><span data-stu-id="ab599-154">Cancelled</span></span>
- <span data-ttu-id="ab599-155">Abbrechen</span><span class="sxs-lookup"><span data-stu-id="ab599-155">Cancelling</span></span>
- <span data-ttu-id="ab599-156">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="ab599-156">Completed</span></span>
- <span data-ttu-id="ab599-157">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="ab599-157">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="ab599-158">-To</span><span class="sxs-lookup"><span data-stu-id="ab599-158">-To</span></span>

<span data-ttu-id="ab599-159">Gibt das Ende eines Zeitbereichs als **DateTime-Objekt** für die Aufträge an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="ab599-159">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="ab599-160">Der Standardwert ist die aktuelle Systemzeit.</span><span class="sxs-lookup"><span data-stu-id="ab599-160">The default value is the current system time.</span></span>
<span data-ttu-id="ab599-161">Wenn Sie diesen Parameter angeben, müssen Sie auch den **-From-Parameter** angeben.</span><span class="sxs-lookup"><span data-stu-id="ab599-161">If you specify this parameter, you must also specify the **-From** parameter.</span></span>
<span data-ttu-id="ab599-162">Verwenden Sie das UTC-Format für Datumsangaben.</span><span class="sxs-lookup"><span data-stu-id="ab599-162">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="ab599-163">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ab599-163">-VaultId</span></span>

<span data-ttu-id="ab599-164">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="ab599-164">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ab599-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab599-165">CommonParameters</span></span>
<span data-ttu-id="ab599-166">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab599-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab599-167">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab599-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab599-168">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ab599-168">INPUTS</span></span>

### <span data-ttu-id="ab599-169">System.String</span><span class="sxs-lookup"><span data-stu-id="ab599-169">System.String</span></span>

## <span data-ttu-id="ab599-170">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ab599-170">OUTPUTS</span></span>

### <span data-ttu-id="ab599-171">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="ab599-171">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="ab599-172">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ab599-172">NOTES</span></span>

## <span data-ttu-id="ab599-173">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ab599-173">RELATED LINKS</span></span>

[<span data-ttu-id="ab599-174">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="ab599-174">Get-AzRecoveryServicesBackupJobDetail</span></span>](./Get-AzRecoveryServicesBackupJobDetail.md)

[<span data-ttu-id="ab599-175">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="ab599-175">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="ab599-176">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="ab599-176">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)
