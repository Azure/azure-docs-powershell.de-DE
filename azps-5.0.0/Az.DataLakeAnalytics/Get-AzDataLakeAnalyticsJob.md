---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 02e0678b9c86643df9cd4bfc2192908ed4748249
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298095"
---
# <span data-ttu-id="96c3b-101">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="96c3b-101">Get-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="96c3b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="96c3b-102">SYNOPSIS</span></span>
<span data-ttu-id="96c3b-103">Ruft einen Daten See-Analyse Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="96c3b-103">Gets a Data Lake Analytics job.</span></span>

## <span data-ttu-id="96c3b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="96c3b-104">SYNTAX</span></span>

### <span data-ttu-id="96c3b-105">GetAllInResourceGroupAndAccount (Standard)</span><span class="sxs-lookup"><span data-stu-id="96c3b-105">GetAllInResourceGroupAndAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96c3b-106">GetBySpecificJobInformation</span><span class="sxs-lookup"><span data-stu-id="96c3b-106">GetBySpecificJobInformation</span></span>
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96c3b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96c3b-107">DESCRIPTION</span></span>
<span data-ttu-id="96c3b-108">Das Cmdlet " **Get-AzDataLakeAnalyticsJob** " Ruft einen Azure Data Lake-Analyse Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="96c3b-108">The **Get-AzDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="96c3b-109">Wenn Sie keinen Auftrag angeben, ruft dieses Cmdlet alle Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="96c3b-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="96c3b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="96c3b-110">EXAMPLES</span></span>

### <span data-ttu-id="96c3b-111">Beispiel 1: Abrufen eines angegebenen Auftrags</span><span class="sxs-lookup"><span data-stu-id="96c3b-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="96c3b-112">Mit diesem Befehl wird der Auftrag mit der angegebenen ID abgerufen.</span><span class="sxs-lookup"><span data-stu-id="96c3b-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="96c3b-113">Beispiel 2: Abrufen von Aufträgen, die in der letzten Woche gesendet wurden</span><span class="sxs-lookup"><span data-stu-id="96c3b-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="96c3b-114">Dieser Befehl ruft in der letzten Woche gesendete Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="96c3b-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="96c3b-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="96c3b-115">PARAMETERS</span></span>

### <span data-ttu-id="96c3b-116">-Konto</span><span class="sxs-lookup"><span data-stu-id="96c3b-116">-Account</span></span>
<span data-ttu-id="96c3b-117">Gibt den Namen eines Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="96c3b-117">Specifies the name of a Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="96c3b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96c3b-118">-DefaultProfile</span></span>
<span data-ttu-id="96c3b-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="96c3b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96c3b-120">-Include</span><span class="sxs-lookup"><span data-stu-id="96c3b-120">-Include</span></span>
<span data-ttu-id="96c3b-121">Gibt Optionen an, die den Typ zusätzlicher Informationen angeben, die über den Auftrag abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="96c3b-121">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="96c3b-122">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="96c3b-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="96c3b-123">Keine</span><span class="sxs-lookup"><span data-stu-id="96c3b-123">None</span></span>
- <span data-ttu-id="96c3b-124">Debuginfo</span><span class="sxs-lookup"><span data-stu-id="96c3b-124">DebugInfo</span></span>
- <span data-ttu-id="96c3b-125">Statistiken</span><span class="sxs-lookup"><span data-stu-id="96c3b-125">Statistics</span></span>
- <span data-ttu-id="96c3b-126">Alle</span><span class="sxs-lookup"><span data-stu-id="96c3b-126">All</span></span>

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

### <span data-ttu-id="96c3b-127">-JobId</span><span class="sxs-lookup"><span data-stu-id="96c3b-127">-JobId</span></span>
<span data-ttu-id="96c3b-128">Gibt die ID des abzurufenden Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="96c3b-128">Specifies the ID of the job to get.</span></span>

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

### <span data-ttu-id="96c3b-129">-Name</span><span class="sxs-lookup"><span data-stu-id="96c3b-129">-Name</span></span>
<span data-ttu-id="96c3b-130">Gibt einen Namen an, der zum Filtern der Auftragslisten Ergebnisse verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="96c3b-130">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="96c3b-131">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="96c3b-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="96c3b-132">Keine</span><span class="sxs-lookup"><span data-stu-id="96c3b-132">None</span></span>
- <span data-ttu-id="96c3b-133">Debuginfo</span><span class="sxs-lookup"><span data-stu-id="96c3b-133">DebugInfo</span></span>
- <span data-ttu-id="96c3b-134">Statistiken</span><span class="sxs-lookup"><span data-stu-id="96c3b-134">Statistics</span></span>
- <span data-ttu-id="96c3b-135">Alle</span><span class="sxs-lookup"><span data-stu-id="96c3b-135">All</span></span>

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

### <span data-ttu-id="96c3b-136">-Pipeline-Nr</span><span class="sxs-lookup"><span data-stu-id="96c3b-136">-PipelineId</span></span>
<span data-ttu-id="96c3b-137">Eine optionale ID, die angibt, dass nur Aufträge, die Teil der angegebenen Pipeline sind, zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="96c3b-137">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

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

### <span data-ttu-id="96c3b-138">-Serien-Nr</span><span class="sxs-lookup"><span data-stu-id="96c3b-138">-RecurrenceId</span></span>
<span data-ttu-id="96c3b-139">Eine optionale ID, die angibt, dass nur Aufträge, die Teil der angegebenen Serie sind, zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="96c3b-139">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

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

### <span data-ttu-id="96c3b-140">-Ergebnis</span><span class="sxs-lookup"><span data-stu-id="96c3b-140">-Result</span></span>
<span data-ttu-id="96c3b-141">Gibt einen Ergebnisfilter für die Auftragsergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="96c3b-141">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="96c3b-142">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="96c3b-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="96c3b-143">Keine</span><span class="sxs-lookup"><span data-stu-id="96c3b-143">None</span></span>
- <span data-ttu-id="96c3b-144">Storniert</span><span class="sxs-lookup"><span data-stu-id="96c3b-144">Cancelled</span></span>
- <span data-ttu-id="96c3b-145">Fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="96c3b-145">Failed</span></span>
- <span data-ttu-id="96c3b-146">Erfolgreich</span><span class="sxs-lookup"><span data-stu-id="96c3b-146">Succeeded</span></span>

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

### <span data-ttu-id="96c3b-147">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="96c3b-147">-State</span></span>
<span data-ttu-id="96c3b-148">Gibt einen Zustandsfilter für die Auftragsergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="96c3b-148">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="96c3b-149">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="96c3b-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="96c3b-150">Akzeptiert</span><span class="sxs-lookup"><span data-stu-id="96c3b-150">Accepted</span></span>
- <span data-ttu-id="96c3b-151">Neu</span><span class="sxs-lookup"><span data-stu-id="96c3b-151">New</span></span>
- <span data-ttu-id="96c3b-152">Kompilieren</span><span class="sxs-lookup"><span data-stu-id="96c3b-152">Compiling</span></span>
- <span data-ttu-id="96c3b-153">Planung</span><span class="sxs-lookup"><span data-stu-id="96c3b-153">Scheduling</span></span>
- <span data-ttu-id="96c3b-154">Queued</span><span class="sxs-lookup"><span data-stu-id="96c3b-154">Queued</span></span>
- <span data-ttu-id="96c3b-155">Ausgangs</span><span class="sxs-lookup"><span data-stu-id="96c3b-155">Starting</span></span>
- <span data-ttu-id="96c3b-156">Pausiert</span><span class="sxs-lookup"><span data-stu-id="96c3b-156">Paused</span></span>
- <span data-ttu-id="96c3b-157">Ausgeführt</span><span class="sxs-lookup"><span data-stu-id="96c3b-157">Running</span></span>
- <span data-ttu-id="96c3b-158">Beendet</span><span class="sxs-lookup"><span data-stu-id="96c3b-158">Ended</span></span>

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

### <span data-ttu-id="96c3b-159">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="96c3b-159">-SubmittedAfter</span></span>
<span data-ttu-id="96c3b-160">Gibt einen Datumsfilter an.</span><span class="sxs-lookup"><span data-stu-id="96c3b-160">Specifies a date filter.</span></span>
<span data-ttu-id="96c3b-161">Verwenden Sie diesen Parameter, um das Ergebnis der Auftragsliste in Aufträge zu filtern, die nach dem angegebenen Datum gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="96c3b-161">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

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

### <span data-ttu-id="96c3b-162">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="96c3b-162">-SubmittedBefore</span></span>
<span data-ttu-id="96c3b-163">Gibt einen Datumsfilter an.</span><span class="sxs-lookup"><span data-stu-id="96c3b-163">Specifies a date filter.</span></span>
<span data-ttu-id="96c3b-164">Verwenden Sie diesen Parameter, um das Ergebnis der Auftragsliste in Aufträge zu filtern, die vor dem angegebenen Datum übermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="96c3b-164">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

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

### <span data-ttu-id="96c3b-165">-Submitter</span><span class="sxs-lookup"><span data-stu-id="96c3b-165">-Submitter</span></span>
<span data-ttu-id="96c3b-166">Gibt die e-Mail-Adresse eines Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="96c3b-166">Specifies the email address of a user.</span></span>
<span data-ttu-id="96c3b-167">Verwenden Sie diesen Parameter, um die Auftragslisten Ergebnisse nach Aufträgen zu filtern, die von einem bestimmten Benutzer übermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="96c3b-167">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

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

### <span data-ttu-id="96c3b-168">-Top</span><span class="sxs-lookup"><span data-stu-id="96c3b-168">-Top</span></span>
<span data-ttu-id="96c3b-169">Ein optionaler Wert, der die Anzahl der Aufträge angibt, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="96c3b-169">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="96c3b-170">Der Standardwert ist 500.</span><span class="sxs-lookup"><span data-stu-id="96c3b-170">Default value is 500</span></span>

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

### <span data-ttu-id="96c3b-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96c3b-171">CommonParameters</span></span>
<span data-ttu-id="96c3b-172">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96c3b-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96c3b-173">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96c3b-173">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96c3b-174">Eingaben</span><span class="sxs-lookup"><span data-stu-id="96c3b-174">INPUTS</span></span>

### <span data-ttu-id="96c3b-175">System. String</span><span class="sxs-lookup"><span data-stu-id="96c3b-175">System.String</span></span>

### <span data-ttu-id="96c3b-176">System. GUID</span><span class="sxs-lookup"><span data-stu-id="96c3b-176">System.Guid</span></span>

### <span data-ttu-id="96c3b-177">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsEnums + ExtendedJobData</span><span class="sxs-lookup"><span data-stu-id="96c3b-177">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData</span></span>

### <span data-ttu-id="96c3b-178">System. Nullable ' 1 [[System. DateTimeOffset, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="96c3b-178">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="96c3b-179">Microsoft. Azure. Management. datalake. Analytics. Models. JobState []</span><span class="sxs-lookup"><span data-stu-id="96c3b-179">Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]</span></span>

### <span data-ttu-id="96c3b-180">Microsoft. Azure. Management. datalake. Analytics. Models. JobResult []</span><span class="sxs-lookup"><span data-stu-id="96c3b-180">Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]</span></span>

### <span data-ttu-id="96c3b-181">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="96c3b-181">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="96c3b-182">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="96c3b-182">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="96c3b-183">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="96c3b-183">OUTPUTS</span></span>

### <span data-ttu-id="96c3b-184">Microsoft. Azure. Management. datalake. Analytics. Models. JobInformation</span><span class="sxs-lookup"><span data-stu-id="96c3b-184">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="96c3b-185">Notizen</span><span class="sxs-lookup"><span data-stu-id="96c3b-185">NOTES</span></span>

## <span data-ttu-id="96c3b-186">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="96c3b-186">RELATED LINKS</span></span>

[<span data-ttu-id="96c3b-187">Stopp-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="96c3b-187">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="96c3b-188">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="96c3b-188">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="96c3b-189">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="96c3b-189">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


