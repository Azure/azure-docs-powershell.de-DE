---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: ca480d266f4ab7706841fb901fa714dbe632ec2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476789"
---
# <span data-ttu-id="96578-101">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="96578-101">Get-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="96578-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="96578-102">SYNOPSIS</span></span>
<span data-ttu-id="96578-103">Ruft einen Daten See-Analyse Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="96578-103">Gets a Data Lake Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96578-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="96578-104">SYNTAX</span></span>

### <span data-ttu-id="96578-105">GetAllInResourceGroupAndAccount (Standard)</span><span class="sxs-lookup"><span data-stu-id="96578-105">GetAllInResourceGroupAndAccount (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96578-106">GetBySpecificJobInformation</span><span class="sxs-lookup"><span data-stu-id="96578-106">GetBySpecificJobInformation</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96578-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96578-107">DESCRIPTION</span></span>
<span data-ttu-id="96578-108">Das Cmdlet " **Get-AzureRmDataLakeAnalyticsJob** " Ruft einen Azure Data Lake-Analyse Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="96578-108">The **Get-AzureRmDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="96578-109">Wenn Sie keinen Auftrag angeben, ruft dieses Cmdlet alle Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="96578-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="96578-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="96578-110">EXAMPLES</span></span>

### <span data-ttu-id="96578-111">Beispiel 1: Abrufen eines angegebenen Auftrags</span><span class="sxs-lookup"><span data-stu-id="96578-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="96578-112">Mit diesem Befehl wird der Auftrag mit der angegebenen ID abgerufen.</span><span class="sxs-lookup"><span data-stu-id="96578-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="96578-113">Beispiel 2: Abrufen von Aufträgen, die in der letzten Woche gesendet wurden</span><span class="sxs-lookup"><span data-stu-id="96578-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="96578-114">Dieser Befehl ruft in der letzten Woche gesendete Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="96578-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="96578-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="96578-115">PARAMETERS</span></span>

### <span data-ttu-id="96578-116">-Konto</span><span class="sxs-lookup"><span data-stu-id="96578-116">-Account</span></span>
<span data-ttu-id="96578-117">Gibt den Namen eines Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="96578-117">Specifies the name of a Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96578-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96578-118">-DefaultProfile</span></span>
<span data-ttu-id="96578-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="96578-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96578-120">-Include</span><span class="sxs-lookup"><span data-stu-id="96578-120">-Include</span></span>
<span data-ttu-id="96578-121">Gibt Optionen an, die den Typ zusätzlicher Informationen angeben, die über den Auftrag abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="96578-121">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="96578-122">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="96578-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="96578-123">Keine</span><span class="sxs-lookup"><span data-stu-id="96578-123">None</span></span>
- <span data-ttu-id="96578-124">Debuginfo</span><span class="sxs-lookup"><span data-stu-id="96578-124">DebugInfo</span></span>
- <span data-ttu-id="96578-125">Statistiken</span><span class="sxs-lookup"><span data-stu-id="96578-125">Statistics</span></span>
- <span data-ttu-id="96578-126">Alle</span><span class="sxs-lookup"><span data-stu-id="96578-126">All</span></span>

```yaml
Type: ExtendedJobData
Parameter Sets: GetBySpecificJobInformation
Aliases: 
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96578-127">-JobId</span><span class="sxs-lookup"><span data-stu-id="96578-127">-JobId</span></span>
<span data-ttu-id="96578-128">Gibt die ID des abzurufenden Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="96578-128">Specifies the ID of the job to get.</span></span>

```yaml
Type: Guid
Parameter Sets: GetBySpecificJobInformation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96578-129">-Name</span><span class="sxs-lookup"><span data-stu-id="96578-129">-Name</span></span>
<span data-ttu-id="96578-130">Gibt einen Namen an, der zum Filtern der Auftragslisten Ergebnisse verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="96578-130">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="96578-131">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="96578-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="96578-132">Keine</span><span class="sxs-lookup"><span data-stu-id="96578-132">None</span></span>
- <span data-ttu-id="96578-133">Debuginfo</span><span class="sxs-lookup"><span data-stu-id="96578-133">DebugInfo</span></span>
- <span data-ttu-id="96578-134">Statistiken</span><span class="sxs-lookup"><span data-stu-id="96578-134">Statistics</span></span>
- <span data-ttu-id="96578-135">Alle</span><span class="sxs-lookup"><span data-stu-id="96578-135">All</span></span>

```yaml
Type: String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96578-136">-Pipeline-Nr</span><span class="sxs-lookup"><span data-stu-id="96578-136">-PipelineId</span></span>
<span data-ttu-id="96578-137">Eine optionale ID, die angibt, dass nur Aufträge, die Teil der angegebenen Pipeline sind, zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="96578-137">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

```yaml
Type: Guid
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96578-138">-Serien-Nr</span><span class="sxs-lookup"><span data-stu-id="96578-138">-RecurrenceId</span></span>
<span data-ttu-id="96578-139">Eine optionale ID, die angibt, dass nur Aufträge, die Teil der angegebenen Serie sind, zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="96578-139">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

```yaml
Type: Guid
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96578-140">-Ergebnis</span><span class="sxs-lookup"><span data-stu-id="96578-140">-Result</span></span>
<span data-ttu-id="96578-141">Gibt einen Ergebnisfilter für die Auftragsergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="96578-141">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="96578-142">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="96578-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="96578-143">Keine</span><span class="sxs-lookup"><span data-stu-id="96578-143">None</span></span>
- <span data-ttu-id="96578-144">Storniert</span><span class="sxs-lookup"><span data-stu-id="96578-144">Cancelled</span></span>
- <span data-ttu-id="96578-145">Fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="96578-145">Failed</span></span>
- <span data-ttu-id="96578-146">Erfolgreich</span><span class="sxs-lookup"><span data-stu-id="96578-146">Succeeded</span></span>

```yaml
Type: JobResult[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96578-147">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="96578-147">-State</span></span>
<span data-ttu-id="96578-148">Gibt einen Zustandsfilter für die Auftragsergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="96578-148">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="96578-149">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="96578-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="96578-150">Akzeptiert</span><span class="sxs-lookup"><span data-stu-id="96578-150">Accepted</span></span>
- <span data-ttu-id="96578-151">Neu</span><span class="sxs-lookup"><span data-stu-id="96578-151">New</span></span>
- <span data-ttu-id="96578-152">Kompilieren</span><span class="sxs-lookup"><span data-stu-id="96578-152">Compiling</span></span>
- <span data-ttu-id="96578-153">Planung</span><span class="sxs-lookup"><span data-stu-id="96578-153">Scheduling</span></span>
- <span data-ttu-id="96578-154">Queued</span><span class="sxs-lookup"><span data-stu-id="96578-154">Queued</span></span>
- <span data-ttu-id="96578-155">Ausgangs</span><span class="sxs-lookup"><span data-stu-id="96578-155">Starting</span></span>
- <span data-ttu-id="96578-156">Pausiert</span><span class="sxs-lookup"><span data-stu-id="96578-156">Paused</span></span>
- <span data-ttu-id="96578-157">Ausgeführt</span><span class="sxs-lookup"><span data-stu-id="96578-157">Running</span></span>
- <span data-ttu-id="96578-158">Beendet</span><span class="sxs-lookup"><span data-stu-id="96578-158">Ended</span></span>

```yaml
Type: JobState[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96578-159">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="96578-159">-SubmittedAfter</span></span>
<span data-ttu-id="96578-160">Gibt einen Datumsfilter an.</span><span class="sxs-lookup"><span data-stu-id="96578-160">Specifies a date filter.</span></span>
<span data-ttu-id="96578-161">Verwenden Sie diesen Parameter, um das Ergebnis der Auftragsliste in Aufträge zu filtern, die nach dem angegebenen Datum gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="96578-161">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96578-162">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="96578-162">-SubmittedBefore</span></span>
<span data-ttu-id="96578-163">Gibt einen Datumsfilter an.</span><span class="sxs-lookup"><span data-stu-id="96578-163">Specifies a date filter.</span></span>
<span data-ttu-id="96578-164">Verwenden Sie diesen Parameter, um das Ergebnis der Auftragsliste in Aufträge zu filtern, die vor dem angegebenen Datum übermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="96578-164">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96578-165">-Submitter</span><span class="sxs-lookup"><span data-stu-id="96578-165">-Submitter</span></span>
<span data-ttu-id="96578-166">Gibt die e-Mail-Adresse eines Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="96578-166">Specifies the email address of a user.</span></span>
<span data-ttu-id="96578-167">Verwenden Sie diesen Parameter, um die Auftragslisten Ergebnisse nach Aufträgen zu filtern, die von einem bestimmten Benutzer übermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="96578-167">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

```yaml
Type: String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96578-168">-Top</span><span class="sxs-lookup"><span data-stu-id="96578-168">-Top</span></span>
<span data-ttu-id="96578-169">Ein optionaler Wert, der die Anzahl der Aufträge angibt, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="96578-169">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="96578-170">Der Standardwert ist 500.</span><span class="sxs-lookup"><span data-stu-id="96578-170">Default value is 500</span></span>

```yaml
Type: Int32
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96578-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96578-171">CommonParameters</span></span>
<span data-ttu-id="96578-172">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96578-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96578-173">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96578-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96578-174">Eingaben</span><span class="sxs-lookup"><span data-stu-id="96578-174">INPUTS</span></span>

### <span data-ttu-id="96578-175">GUID</span><span class="sxs-lookup"><span data-stu-id="96578-175">Guid</span></span>
<span data-ttu-id="96578-176">Der Parameter "JobID" akzeptiert den Wert vom Typ "GUID" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="96578-176">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="96578-177">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="96578-177">OUTPUTS</span></span>

### <span data-ttu-id="96578-178">JobInformation</span><span class="sxs-lookup"><span data-stu-id="96578-178">JobInformation</span></span>
<span data-ttu-id="96578-179">Die angegebenen Informationen zu Auftragsinformationen</span><span class="sxs-lookup"><span data-stu-id="96578-179">The specified job information details</span></span>

### <span data-ttu-id="96578-180">Liste<PSJobInformationBasic></span><span class="sxs-lookup"><span data-stu-id="96578-180">List<PSJobInformationBasic></span></span>
<span data-ttu-id="96578-181">Die Liste der Aufträge im angegebenen Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="96578-181">The list of jobs in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="96578-182">Notizen</span><span class="sxs-lookup"><span data-stu-id="96578-182">NOTES</span></span>

## <span data-ttu-id="96578-183">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="96578-183">RELATED LINKS</span></span>

[<span data-ttu-id="96578-184">Stopp-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="96578-184">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="96578-185">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="96578-185">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="96578-186">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="96578-186">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


