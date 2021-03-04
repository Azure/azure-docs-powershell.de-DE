---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 0078196d8b06ae791fa0855345eec02d1f2eb59c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930091"
---
# <span data-ttu-id="43f46-101">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="43f46-101">Get-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="43f46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43f46-102">SYNOPSIS</span></span>
<span data-ttu-id="43f46-103">Ruft einen Data Lake Analytics-Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="43f46-103">Gets a Data Lake Analytics job.</span></span>

## <span data-ttu-id="43f46-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43f46-104">SYNTAX</span></span>

### <span data-ttu-id="43f46-105">GetAllInResourceGroupAndAccount (Standard)</span><span class="sxs-lookup"><span data-stu-id="43f46-105">GetAllInResourceGroupAndAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43f46-106">GetBySpecificJobInformation</span><span class="sxs-lookup"><span data-stu-id="43f46-106">GetBySpecificJobInformation</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43f46-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43f46-107">DESCRIPTION</span></span>
<span data-ttu-id="43f46-108">Das **Cmdlet Get-AzDataLakeAnalyticsJob** erhält einen Azure Data Lake Analytics-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="43f46-108">The **Get-AzDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="43f46-109">Wenn Sie keinen Auftrag angeben, erhält dieses Cmdlet alle Aufträge.</span><span class="sxs-lookup"><span data-stu-id="43f46-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="43f46-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="43f46-110">EXAMPLES</span></span>

### <span data-ttu-id="43f46-111">Beispiel 1: Einen angegebenen Auftrag erhalten</span><span class="sxs-lookup"><span data-stu-id="43f46-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="43f46-112">Dieser Befehl ruft den Auftrag mit der angegebenen ID ab.</span><span class="sxs-lookup"><span data-stu-id="43f46-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="43f46-113">Beispiel 2: In der letzten Woche übermittelte Aufträge erhalten</span><span class="sxs-lookup"><span data-stu-id="43f46-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="43f46-114">Dieser Befehl ruft Aufträge ab, die in der letzten Woche übermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="43f46-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="43f46-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="43f46-115">PARAMETERS</span></span>

### <span data-ttu-id="43f46-116">-Konto</span><span class="sxs-lookup"><span data-stu-id="43f46-116">-Account</span></span>
<span data-ttu-id="43f46-117">Gibt den Namen eines Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="43f46-117">Specifies the name of a Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f46-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43f46-118">-DefaultProfile</span></span>
<span data-ttu-id="43f46-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="43f46-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43f46-120">-Include</span><span class="sxs-lookup"><span data-stu-id="43f46-120">-Include</span></span>
<span data-ttu-id="43f46-121">Gibt Optionen an, die den Typ der zusätzlichen Informationen angeben, die über den Auftrag abgerufen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="43f46-121">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="43f46-122">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="43f46-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="43f46-123">Keine</span><span class="sxs-lookup"><span data-stu-id="43f46-123">None</span></span>
- <span data-ttu-id="43f46-124">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="43f46-124">DebugInfo</span></span>
- <span data-ttu-id="43f46-125">Statistik</span><span class="sxs-lookup"><span data-stu-id="43f46-125">Statistics</span></span>
- <span data-ttu-id="43f46-126">Alle</span><span class="sxs-lookup"><span data-stu-id="43f46-126">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData
Parameter Sets: GetBySpecificJobInformation
Aliases:
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f46-127">-JobId</span><span class="sxs-lookup"><span data-stu-id="43f46-127">-JobId</span></span>
<span data-ttu-id="43f46-128">Gibt die ID des zu erhaltenden Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="43f46-128">Specifies the ID of the job to get.</span></span>

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobInformation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43f46-129">-Name</span><span class="sxs-lookup"><span data-stu-id="43f46-129">-Name</span></span>
<span data-ttu-id="43f46-130">Gibt einen Namen an, der zum Filtern der Auftragslistenergebnisse verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="43f46-130">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="43f46-131">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="43f46-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="43f46-132">Keine</span><span class="sxs-lookup"><span data-stu-id="43f46-132">None</span></span>
- <span data-ttu-id="43f46-133">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="43f46-133">DebugInfo</span></span>
- <span data-ttu-id="43f46-134">Statistik</span><span class="sxs-lookup"><span data-stu-id="43f46-134">Statistics</span></span>
- <span data-ttu-id="43f46-135">Alle</span><span class="sxs-lookup"><span data-stu-id="43f46-135">All</span></span>

```yaml
Type: System.String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f46-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="43f46-136">-PipelineId</span></span>
<span data-ttu-id="43f46-137">Eine optionale ID, die angibt, dass nur Aufträge teil der angegebenen Pipeline sind, sollte zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="43f46-137">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f46-138">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="43f46-138">-RecurrenceId</span></span>
<span data-ttu-id="43f46-139">Eine optionale ID, die angibt, dass nur Aufträge teil der angegebenen Serie sind, sollte zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="43f46-139">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f46-140">-Ergebnis</span><span class="sxs-lookup"><span data-stu-id="43f46-140">-Result</span></span>
<span data-ttu-id="43f46-141">Gibt einen Ergebnisfilter für die Auftragsergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="43f46-141">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="43f46-142">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="43f46-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="43f46-143">Keine</span><span class="sxs-lookup"><span data-stu-id="43f46-143">None</span></span>
- <span data-ttu-id="43f46-144">Storniert</span><span class="sxs-lookup"><span data-stu-id="43f46-144">Cancelled</span></span>
- <span data-ttu-id="43f46-145">Fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="43f46-145">Failed</span></span>
- <span data-ttu-id="43f46-146">Erfolgreich</span><span class="sxs-lookup"><span data-stu-id="43f46-146">Succeeded</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f46-147">-State</span><span class="sxs-lookup"><span data-stu-id="43f46-147">-State</span></span>
<span data-ttu-id="43f46-148">Gibt einen Zustandsfilter für die Auftragsergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="43f46-148">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="43f46-149">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="43f46-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="43f46-150">Akzeptiert</span><span class="sxs-lookup"><span data-stu-id="43f46-150">Accepted</span></span>
- <span data-ttu-id="43f46-151">Neu</span><span class="sxs-lookup"><span data-stu-id="43f46-151">New</span></span>
- <span data-ttu-id="43f46-152">Kompilieren</span><span class="sxs-lookup"><span data-stu-id="43f46-152">Compiling</span></span>
- <span data-ttu-id="43f46-153">Terminplanung</span><span class="sxs-lookup"><span data-stu-id="43f46-153">Scheduling</span></span>
- <span data-ttu-id="43f46-154">In warteschlangen</span><span class="sxs-lookup"><span data-stu-id="43f46-154">Queued</span></span>
- <span data-ttu-id="43f46-155">Starten</span><span class="sxs-lookup"><span data-stu-id="43f46-155">Starting</span></span>
- <span data-ttu-id="43f46-156">Angehalten</span><span class="sxs-lookup"><span data-stu-id="43f46-156">Paused</span></span>
- <span data-ttu-id="43f46-157">Ausführen</span><span class="sxs-lookup"><span data-stu-id="43f46-157">Running</span></span>
- <span data-ttu-id="43f46-158">Beendet</span><span class="sxs-lookup"><span data-stu-id="43f46-158">Ended</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f46-159">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="43f46-159">-SubmittedAfter</span></span>
<span data-ttu-id="43f46-160">Gibt einen Datumsfilter an.</span><span class="sxs-lookup"><span data-stu-id="43f46-160">Specifies a date filter.</span></span>
<span data-ttu-id="43f46-161">Verwenden Sie diesen Parameter, um das Ergebnis der Auftragsliste nach Aufträgen zu filtern, die nach dem angegebenen Datum übermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="43f46-161">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f46-162">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="43f46-162">-SubmittedBefore</span></span>
<span data-ttu-id="43f46-163">Gibt einen Datumsfilter an.</span><span class="sxs-lookup"><span data-stu-id="43f46-163">Specifies a date filter.</span></span>
<span data-ttu-id="43f46-164">Verwenden Sie diesen Parameter, um das Ergebnis der Auftragsliste nach Aufträgen zu filtern, die vor dem angegebenen Datum übermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="43f46-164">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f46-165">-Submitter</span><span class="sxs-lookup"><span data-stu-id="43f46-165">-Submitter</span></span>
<span data-ttu-id="43f46-166">Gibt die E-Mail-Adresse eines Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="43f46-166">Specifies the email address of a user.</span></span>
<span data-ttu-id="43f46-167">Verwenden Sie diesen Parameter, um die Auftragslistenergebnisse nach Aufträgen zu filtern, die von einem bestimmten Benutzer übermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="43f46-167">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f46-168">-Top</span><span class="sxs-lookup"><span data-stu-id="43f46-168">-Top</span></span>
<span data-ttu-id="43f46-169">Ein optionaler Wert, der angibt, wie viele Aufträge zurückzukehren sind.</span><span class="sxs-lookup"><span data-stu-id="43f46-169">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="43f46-170">Standardwert ist 500</span><span class="sxs-lookup"><span data-stu-id="43f46-170">Default value is 500</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f46-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43f46-171">CommonParameters</span></span>
<span data-ttu-id="43f46-172">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43f46-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43f46-173">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43f46-173">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43f46-174">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="43f46-174">INPUTS</span></span>

### <span data-ttu-id="43f46-175">System.String</span><span class="sxs-lookup"><span data-stu-id="43f46-175">System.String</span></span>

### <span data-ttu-id="43f46-176">System.Guid</span><span class="sxs-lookup"><span data-stu-id="43f46-176">System.Guid</span></span>

### <span data-ttu-id="43f46-177">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData</span><span class="sxs-lookup"><span data-stu-id="43f46-177">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData</span></span>

### <span data-ttu-id="43f46-178">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="43f46-178">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="43f46-179">Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]</span><span class="sxs-lookup"><span data-stu-id="43f46-179">Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]</span></span>

### <span data-ttu-id="43f46-180">Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]</span><span class="sxs-lookup"><span data-stu-id="43f46-180">Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]</span></span>

### <span data-ttu-id="43f46-181">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="43f46-181">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="43f46-182">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="43f46-182">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="43f46-183">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="43f46-183">OUTPUTS</span></span>

### <span data-ttu-id="43f46-184">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span><span class="sxs-lookup"><span data-stu-id="43f46-184">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="43f46-185">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="43f46-185">NOTES</span></span>

## <span data-ttu-id="43f46-186">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="43f46-186">RELATED LINKS</span></span>

[<span data-ttu-id="43f46-187">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="43f46-187">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="43f46-188">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="43f46-188">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="43f46-189">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="43f46-189">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


