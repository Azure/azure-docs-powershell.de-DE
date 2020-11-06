---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 331F32CB-7777-401C-A42A-23098944CFBE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
ms.openlocfilehash: cbdb60fb4ec139b1dae92b7dd8e2e54675ae1f90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482554"
---
# <span data-ttu-id="4973e-101">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="4973e-101">Get-AzureRmBackupJob</span></span>

## <span data-ttu-id="4973e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4973e-102">SYNOPSIS</span></span>
<span data-ttu-id="4973e-103">Ruft Backup-Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="4973e-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4973e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4973e-104">SYNTAX</span></span>

### <span data-ttu-id="4973e-105">Filterset (Standard)</span><span class="sxs-lookup"><span data-stu-id="4973e-105">FiltersSet (Default)</span></span>
```
Get-AzureRmBackupJob -Vault <AzureRMBackupVault> [-JobId <String>] [-From <DateTime>] [-To <DateTime>]
 [-Status <String>] [-Type <String>] [-Operation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4973e-106">JobsListFilter</span><span class="sxs-lookup"><span data-stu-id="4973e-106">JobsListFilter</span></span>
```
Get-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4973e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4973e-107">DESCRIPTION</span></span>
<span data-ttu-id="4973e-108">Das Cmdlet " **Get-AzureRmBackupJob** " ruft Azure Backup-Aufträge für einen bestimmten Tresor ab.</span><span class="sxs-lookup"><span data-stu-id="4973e-108">The **Get-AzureRmBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>

## <span data-ttu-id="4973e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4973e-109">EXAMPLES</span></span>

### <span data-ttu-id="4973e-110">Beispiel 1: Abrufen aller Aufträge in einem sicherungstresor</span><span class="sxs-lookup"><span data-stu-id="4973e-110">Example 1: Get all jobs in a Backup vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupJob -Vault $Vault
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
co03-vm         ConfigureBackup Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="4973e-111">Der erste Befehl ruft den Tresor mit dem Namen Vault03 mit dem Cmdlet **Get-AzureRmBackupVault** ab.</span><span class="sxs-lookup"><span data-stu-id="4973e-111">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="4973e-112">Der Befehl speichert das Objekt in der $Vault Variablen.</span><span class="sxs-lookup"><span data-stu-id="4973e-112">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="4973e-113">Der zweite Befehl ruft alle Aufträge für den Tresor in $Vault ab.</span><span class="sxs-lookup"><span data-stu-id="4973e-113">The second command gets all the jobs for the vault in $Vault.</span></span>

### <span data-ttu-id="4973e-114">Beispiel 2: Abrufen abgeschlossener Aufträge</span><span class="sxs-lookup"><span data-stu-id="4973e-114">Example 2: Get completed jobs</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Status Completed
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="4973e-115">Dieser Befehl ruft abgeschlossene Aufträge aus dem Tresor in $Vault ab.</span><span class="sxs-lookup"><span data-stu-id="4973e-115">This command gets completed jobs from the vault in $Vault.</span></span>

### <span data-ttu-id="4973e-116">Beispiel 3: Abrufen von fehlgeschlagenen Aufträgen für die letzte Woche</span><span class="sxs-lookup"><span data-stu-id="4973e-116">Example 3: Get failed jobs for the last week</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -From (Get-Date).AddDays(-7) -Status Failed
```

<span data-ttu-id="4973e-117">Dieser Befehl ruft fehlerhafte Aufträge aus der letzten Woche aus dem Tresor in $Vault ab.</span><span class="sxs-lookup"><span data-stu-id="4973e-117">This command gets failed jobs from the last week from the vault in $Vault.</span></span>
<span data-ttu-id="4973e-118">Der Parameter from gibt eine Uhrzeit *von* sieben Tagen in der Vergangenheit an.</span><span class="sxs-lookup"><span data-stu-id="4973e-118">The *From* parameter specifies a time seven days in the past.</span></span>
<span data-ttu-id="4973e-119">Der Befehl gibt keinen Wert für den Parameter " *to" an* .</span><span class="sxs-lookup"><span data-stu-id="4973e-119">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="4973e-120">Daher wird der Standardwert für die aktuelle Uhrzeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="4973e-120">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="4973e-121">Beispiel 4: Abrufen der Sicherung für einen in Bearbeitung befindlichen Auftrag, der abgeschlossen ist</span><span class="sxs-lookup"><span data-stu-id="4973e-121">Example 4: Poll Backup for an in progress job that finishes</span></span>
```
PS C:\>$Jobs = Get-AzureRmBackupJob -Vault $Vault -Status InProgress
$Job = $Jobs[0] 
while ( $Job.Status -ne Completed ) 
{
   Write-Host "Waiting for completion..." 
   Start-Sleep -Seconds 10
   $job = Get-AzureRmBackupJob -Vault $Vault -Job $Job
}
Write-Host "Done!"
Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

<span data-ttu-id="4973e-122">Dieses Skript ruft den ersten Job ab, der gerade ausgeführt wird, bis der Auftrag abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="4973e-122">This script polls the first job that is currently in progress until the job has completed.</span></span>
<span data-ttu-id="4973e-123">Die erste Zeile des Skripts Ruft alle Aufträge in $Vault ab, die in Bearbeitung sind, und speichert diese Aufträge dann in der $Jobs-Arrayvariablen.</span><span class="sxs-lookup"><span data-stu-id="4973e-123">The first line of the script gets all the jobs in $Vault that are in progress, and then stores those jobs in the $Jobs array variable.</span></span>
<span data-ttu-id="4973e-124">In der zweiten Zeile wird der erste Auftrag aus dem $Jobs-Array in der $Job Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4973e-124">The second line stores the first job from the $Jobs array in the $Job variable.</span></span>
<span data-ttu-id="4973e-125">In der dritten Zeile wird eine **while** -Schleife gestartet, die den aktuellen Status des Auftrags überprüft, bis der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="4973e-125">The third line starts a **while** loop that checks the current status of the job until the job is completed.</span></span>
<span data-ttu-id="4973e-126">Für Informationen zum Schlüsselwort **while** geben Sie `Get-Help about_While` .</span><span class="sxs-lookup"><span data-stu-id="4973e-126">For information about the **while** keyword, type `Get-Help about_While`.</span></span>
<span data-ttu-id="4973e-127">Die **while** -Schleife schreibt eine Nachricht in die Konsole, schläft zehn Sekunden lang und aktualisiert dann die $Job-Variable.</span><span class="sxs-lookup"><span data-stu-id="4973e-127">The **while** loop writes a message to the console, sleeps for ten seconds, and then updates the $Job variable.</span></span>
<span data-ttu-id="4973e-128">Das Skript aktualisiert die $Job-Variable unter Verwendung des vorhandenen Werts von $Job und des aktuellen Cmdlets, um den aktuellen Status des Auftrags abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4973e-128">The script updates the $Job variable by using existing value of $Job and the current cmdlet to get the current status of the job.</span></span>
<span data-ttu-id="4973e-129">Wenn Sie Informationen zu den Windows PowerShell-Cmdlets erhalten, geben Sie `Get-Help Write-Host` und ein `Get-Help Start-Sleep` .</span><span class="sxs-lookup"><span data-stu-id="4973e-129">For information about the Windows PowerShell cmdlets, type `Get-Help Write-Host` and `Get-Help Start-Sleep`.</span></span>
<span data-ttu-id="4973e-130">In der letzten Zeile des Skripts wird Ihnen mitgeteilt, dass das Skript beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="4973e-130">The final line of the script tells you that the script has finished.</span></span>

## <span data-ttu-id="4973e-131">Parameter</span><span class="sxs-lookup"><span data-stu-id="4973e-131">PARAMETERS</span></span>

### <span data-ttu-id="4973e-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4973e-132">-DefaultProfile</span></span>
<span data-ttu-id="4973e-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4973e-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4973e-134">-Ab</span><span class="sxs-lookup"><span data-stu-id="4973e-134">-From</span></span>
<span data-ttu-id="4973e-135">Gibt den Anfang als **DateTime** -Objekt eines Zeitbereichs für die Aufträge an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="4973e-135">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="4973e-136">Verwenden Sie das Get-Date-Cmdlet, um ein **DateTime** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4973e-136">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="4973e-137">Wenn Sie weitere Informationen zu **DateTime** -Objekten wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="4973e-137">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: FiltersSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4973e-138">-Job</span><span class="sxs-lookup"><span data-stu-id="4973e-138">-Job</span></span>
<span data-ttu-id="4973e-139">Gibt einen Auftrag an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="4973e-139">Specifies a job that this cmdlet gets.</span></span>
<span data-ttu-id="4973e-140">Verwenden Sie das Get-AzureRmBackupJob-Cmdlet, um ein **AzureRmBackupJob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4973e-140">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobsListFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4973e-141">-JobId</span><span class="sxs-lookup"><span data-stu-id="4973e-141">-JobId</span></span>
<span data-ttu-id="4973e-142">Gibt die ID eines Auftrags an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="4973e-142">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="4973e-143">Die ID ist die **InstanceId** -Eigenschaft eines **AzureRmBackupJob** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="4973e-143">The ID is the **InstanceId** property of an **AzureRmBackupJob** object.</span></span>
<span data-ttu-id="4973e-144">Verwenden Sie Get-AzureRmBackupJob, um ein **AzureRmBackupJob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4973e-144">To obtain an **AzureRmBackupJob** object, use Get-AzureRmBackupJob.</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4973e-145">-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4973e-145">-Operation</span></span>
<span data-ttu-id="4973e-146">Gibt einen Vorgang der Aufträge an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="4973e-146">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="4973e-147">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4973e-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4973e-148">Backup</span><span class="sxs-lookup"><span data-stu-id="4973e-148">Backup</span></span> 
- <span data-ttu-id="4973e-149">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="4973e-149">ConfigureBackup</span></span> 
- <span data-ttu-id="4973e-150">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="4973e-150">DeleteBackupData</span></span> 
- <span data-ttu-id="4973e-151">Registrieren</span><span class="sxs-lookup"><span data-stu-id="4973e-151">Register</span></span> 
- <span data-ttu-id="4973e-152">Wiederherstellungs</span><span class="sxs-lookup"><span data-stu-id="4973e-152">Restore</span></span> 
- <span data-ttu-id="4973e-153">Schutz aufheben</span><span class="sxs-lookup"><span data-stu-id="4973e-153">UnProtect</span></span> 
- <span data-ttu-id="4973e-154">Registrierung</span><span class="sxs-lookup"><span data-stu-id="4973e-154">Unregister</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases:
Accepted values: Backup, ConfigureBackup, DeleteBackupData, Register, Restore, UnProtect, Unregister

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4973e-155">-Status</span><span class="sxs-lookup"><span data-stu-id="4973e-155">-Status</span></span>
<span data-ttu-id="4973e-156">Gibt den Status der Aufträge an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="4973e-156">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="4973e-157">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4973e-157">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4973e-158">InProgress</span><span class="sxs-lookup"><span data-stu-id="4973e-158">InProgress</span></span>
- <span data-ttu-id="4973e-159">Fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="4973e-159">Failed</span></span>
- <span data-ttu-id="4973e-160">Storniert</span><span class="sxs-lookup"><span data-stu-id="4973e-160">Cancelled</span></span>
- <span data-ttu-id="4973e-161">Abbrechen</span><span class="sxs-lookup"><span data-stu-id="4973e-161">Cancelling</span></span>
- <span data-ttu-id="4973e-162">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="4973e-162">Completed</span></span>
- <span data-ttu-id="4973e-163">CompletedWithWarnings Sie können diesen Parameter angeben, um alle in Bearbeitung befindlichen Aufträge oder alle fehlgeschlagenen Aufträge zu finden.</span><span class="sxs-lookup"><span data-stu-id="4973e-163">CompletedWithWarnings You can specify this parameter to find all in progress jobs or all failed jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases:
Accepted values: Cancelled, Cancelling, Completed, CompletedWithWarnings, Failed, InProgress

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4973e-164">-To</span><span class="sxs-lookup"><span data-stu-id="4973e-164">-To</span></span>
<span data-ttu-id="4973e-165">Gibt das Ende als **DateTime** -Objekt eines Zeitbereichs für die Aufträge an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="4973e-165">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="4973e-166">Der Standardwert ist die aktuelle Systemzeit.</span><span class="sxs-lookup"><span data-stu-id="4973e-166">The default value is the current system time.</span></span>
<span data-ttu-id="4973e-167">Wenn Sie diesen Parameter angeben, müssen Sie auch den *from* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="4973e-167">If you specify this parameter, you must also specify the *From* parameter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: FiltersSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4973e-168">-Typ</span><span class="sxs-lookup"><span data-stu-id="4973e-168">-Type</span></span>
<span data-ttu-id="4973e-169">Gibt den Typ des Containers an, für den das Cmdlet Sicherungsaufträge erhält.</span><span class="sxs-lookup"><span data-stu-id="4973e-169">Specifies the type of container for which this cmdlet gets backup jobs.</span></span>
<span data-ttu-id="4973e-170">Derzeit ist der einzige unterstützte Wert AzureVM.</span><span class="sxs-lookup"><span data-stu-id="4973e-170">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases:
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4973e-171">-Vault</span><span class="sxs-lookup"><span data-stu-id="4973e-171">-Vault</span></span>
<span data-ttu-id="4973e-172">Gibt den sicherungstresor an, für den dieses Cmdlet Aufträge erhält.</span><span class="sxs-lookup"><span data-stu-id="4973e-172">Specifies the Backup vault for which this cmdlet gets jobs.</span></span>
<span data-ttu-id="4973e-173">Verwenden Sie das Get-AzureRmBackupVault-Cmdlet, um ein **AzureRmBackupVault** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4973e-173">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: FiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4973e-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4973e-174">CommonParameters</span></span>
<span data-ttu-id="4973e-175">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4973e-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4973e-176">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4973e-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4973e-177">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4973e-177">INPUTS</span></span>

### <span data-ttu-id="4973e-178">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="4973e-178">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="4973e-179">Parameter: Vault (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4973e-179">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="4973e-180">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4973e-180">OUTPUTS</span></span>

### <span data-ttu-id="4973e-181">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="4973e-181">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="4973e-182">Notizen</span><span class="sxs-lookup"><span data-stu-id="4973e-182">NOTES</span></span>
* <span data-ttu-id="4973e-183">Keine</span><span class="sxs-lookup"><span data-stu-id="4973e-183">None</span></span>

## <span data-ttu-id="4973e-184">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4973e-184">RELATED LINKS</span></span>

[<span data-ttu-id="4973e-185">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="4973e-185">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="4973e-186">Stopp-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="4973e-186">Stop-AzureRmBackupJob</span></span>](./Stop-AzureRmBackupJob.md)

[<span data-ttu-id="4973e-187">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="4973e-187">Wait-AzureRmBackupJob</span></span>](./Wait-AzureRmBackupJob.md)


