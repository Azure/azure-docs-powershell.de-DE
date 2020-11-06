---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 6a172de918e8b0675abaf01edf2ec198dae75b5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505077"
---
# <span data-ttu-id="0db46-101">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0db46-101">Get-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="0db46-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0db46-102">SYNOPSIS</span></span>
<span data-ttu-id="0db46-103">Ruft einen Daten See-Analyse Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="0db46-103">Gets a Data Lake Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0db46-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0db46-104">SYNTAX</span></span>

### <span data-ttu-id="0db46-105">Alle in Ressourcengruppe und-Konto (Standard)</span><span class="sxs-lookup"><span data-stu-id="0db46-105">All In Resource Group and Account (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0db46-106">Spezifische JobInformation</span><span class="sxs-lookup"><span data-stu-id="0db46-106">Specific JobInformation</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0db46-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0db46-107">DESCRIPTION</span></span>
<span data-ttu-id="0db46-108">Das Cmdlet " **Get-AzureRmDataLakeAnalyticsJob** " Ruft einen Azure Data Lake-Analyse Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="0db46-108">The **Get-AzureRmDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="0db46-109">Wenn Sie keinen Auftrag angeben, ruft dieses Cmdlet alle Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="0db46-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="0db46-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0db46-110">EXAMPLES</span></span>

### <span data-ttu-id="0db46-111">Beispiel 1: Abrufen eines angegebenen Auftrags</span><span class="sxs-lookup"><span data-stu-id="0db46-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="0db46-112">Mit diesem Befehl wird der Auftrag mit der angegebenen ID abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0db46-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="0db46-113">Beispiel 2: Abrufen von Aufträgen, die in der letzten Woche gesendet wurden</span><span class="sxs-lookup"><span data-stu-id="0db46-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="0db46-114">Dieser Befehl ruft in der letzten Woche gesendete Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="0db46-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="0db46-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="0db46-115">PARAMETERS</span></span>

### <span data-ttu-id="0db46-116">-Konto</span><span class="sxs-lookup"><span data-stu-id="0db46-116">-Account</span></span>
<span data-ttu-id="0db46-117">Gibt den Namen eines Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="0db46-117">Specifies the name of a Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="0db46-118">-Include</span><span class="sxs-lookup"><span data-stu-id="0db46-118">-Include</span></span>
<span data-ttu-id="0db46-119">Gibt Optionen an, die den Typ zusätzlicher Informationen angeben, die über den Auftrag abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0db46-119">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="0db46-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0db46-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0db46-121">Keine</span><span class="sxs-lookup"><span data-stu-id="0db46-121">None</span></span>
- <span data-ttu-id="0db46-122">Debuginfo</span><span class="sxs-lookup"><span data-stu-id="0db46-122">DebugInfo</span></span>
- <span data-ttu-id="0db46-123">Statistiken</span><span class="sxs-lookup"><span data-stu-id="0db46-123">Statistics</span></span>
- <span data-ttu-id="0db46-124">Alle</span><span class="sxs-lookup"><span data-stu-id="0db46-124">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData
Parameter Sets: Specific JobInformation
Aliases: 
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0db46-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="0db46-125">-JobId</span></span>
<span data-ttu-id="0db46-126">Gibt die ID des abzurufenden Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="0db46-126">Specifies the ID of the job to get.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Specific JobInformation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0db46-127">-Name</span><span class="sxs-lookup"><span data-stu-id="0db46-127">-Name</span></span>
<span data-ttu-id="0db46-128">Gibt einen Namen an, der zum Filtern der Auftragslisten Ergebnisse verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0db46-128">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="0db46-129">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0db46-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0db46-130">Keine</span><span class="sxs-lookup"><span data-stu-id="0db46-130">None</span></span>
- <span data-ttu-id="0db46-131">Debuginfo</span><span class="sxs-lookup"><span data-stu-id="0db46-131">DebugInfo</span></span>
- <span data-ttu-id="0db46-132">Statistiken</span><span class="sxs-lookup"><span data-stu-id="0db46-132">Statistics</span></span>
- <span data-ttu-id="0db46-133">Alle</span><span class="sxs-lookup"><span data-stu-id="0db46-133">All</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0db46-134">-Pipeline-Nr</span><span class="sxs-lookup"><span data-stu-id="0db46-134">-PipelineId</span></span>
<span data-ttu-id="0db46-135">Eine optionale ID, die angibt, dass nur Aufträge, die Teil der angegebenen Pipeline sind, zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0db46-135">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0db46-136">-Serien-Nr</span><span class="sxs-lookup"><span data-stu-id="0db46-136">-RecurrenceId</span></span>
<span data-ttu-id="0db46-137">Eine optionale ID, die angibt, dass nur Aufträge, die Teil der angegebenen Serie sind, zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0db46-137">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0db46-138">-Ergebnis</span><span class="sxs-lookup"><span data-stu-id="0db46-138">-Result</span></span>
<span data-ttu-id="0db46-139">Gibt einen Ergebnisfilter für die Auftragsergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="0db46-139">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="0db46-140">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0db46-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0db46-141">Keine</span><span class="sxs-lookup"><span data-stu-id="0db46-141">None</span></span>
- <span data-ttu-id="0db46-142">Storniert</span><span class="sxs-lookup"><span data-stu-id="0db46-142">Cancelled</span></span>
- <span data-ttu-id="0db46-143">Fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="0db46-143">Failed</span></span>
- <span data-ttu-id="0db46-144">Erfolgreich</span><span class="sxs-lookup"><span data-stu-id="0db46-144">Succeeded</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]
Parameter Sets: All In Resource Group and Account
Aliases: 
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0db46-145">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="0db46-145">-State</span></span>
<span data-ttu-id="0db46-146">Gibt einen Zustandsfilter für die Auftragsergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="0db46-146">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="0db46-147">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0db46-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0db46-148">Akzeptiert</span><span class="sxs-lookup"><span data-stu-id="0db46-148">Accepted</span></span>
- <span data-ttu-id="0db46-149">Neu</span><span class="sxs-lookup"><span data-stu-id="0db46-149">New</span></span>
- <span data-ttu-id="0db46-150">Kompilieren</span><span class="sxs-lookup"><span data-stu-id="0db46-150">Compiling</span></span>
- <span data-ttu-id="0db46-151">Planung</span><span class="sxs-lookup"><span data-stu-id="0db46-151">Scheduling</span></span>
- <span data-ttu-id="0db46-152">Queued</span><span class="sxs-lookup"><span data-stu-id="0db46-152">Queued</span></span>
- <span data-ttu-id="0db46-153">Ausgangs</span><span class="sxs-lookup"><span data-stu-id="0db46-153">Starting</span></span>
- <span data-ttu-id="0db46-154">Pausiert</span><span class="sxs-lookup"><span data-stu-id="0db46-154">Paused</span></span>
- <span data-ttu-id="0db46-155">Ausgeführt</span><span class="sxs-lookup"><span data-stu-id="0db46-155">Running</span></span>
- <span data-ttu-id="0db46-156">Beendet</span><span class="sxs-lookup"><span data-stu-id="0db46-156">Ended</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]
Parameter Sets: All In Resource Group and Account
Aliases: 
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0db46-157">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="0db46-157">-SubmittedAfter</span></span>
<span data-ttu-id="0db46-158">Gibt einen Datumsfilter an.</span><span class="sxs-lookup"><span data-stu-id="0db46-158">Specifies a date filter.</span></span>
<span data-ttu-id="0db46-159">Verwenden Sie diesen Parameter, um das Ergebnis der Auftragsliste in Aufträge zu filtern, die nach dem angegebenen Datum gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="0db46-159">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0db46-160">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="0db46-160">-SubmittedBefore</span></span>
<span data-ttu-id="0db46-161">Gibt einen Datumsfilter an.</span><span class="sxs-lookup"><span data-stu-id="0db46-161">Specifies a date filter.</span></span>
<span data-ttu-id="0db46-162">Verwenden Sie diesen Parameter, um das Ergebnis der Auftragsliste in Aufträge zu filtern, die vor dem angegebenen Datum übermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="0db46-162">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0db46-163">-Submitter</span><span class="sxs-lookup"><span data-stu-id="0db46-163">-Submitter</span></span>
<span data-ttu-id="0db46-164">Gibt die e-Mail-Adresse eines Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="0db46-164">Specifies the email address of a user.</span></span>
<span data-ttu-id="0db46-165">Verwenden Sie diesen Parameter, um die Auftragslisten Ergebnisse nach Aufträgen zu filtern, die von einem bestimmten Benutzer übermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="0db46-165">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0db46-166">-Top</span><span class="sxs-lookup"><span data-stu-id="0db46-166">-Top</span></span>
<span data-ttu-id="0db46-167">Ein optionaler Wert, der die Anzahl der Aufträge angibt, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0db46-167">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="0db46-168">Der Standardwert ist 500.</span><span class="sxs-lookup"><span data-stu-id="0db46-168">Default value is 500</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0db46-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0db46-169">-DefaultProfile</span></span>
<span data-ttu-id="0db46-170">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0db46-170">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0db46-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0db46-171">CommonParameters</span></span>
<span data-ttu-id="0db46-172">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0db46-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0db46-173">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0db46-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0db46-174">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0db46-174">INPUTS</span></span>

### <span data-ttu-id="0db46-175">GUID</span><span class="sxs-lookup"><span data-stu-id="0db46-175">Guid</span></span>
<span data-ttu-id="0db46-176">Der Parameter "JobID" akzeptiert den Wert vom Typ "GUID" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0db46-176">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="0db46-177">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0db46-177">OUTPUTS</span></span>

### <span data-ttu-id="0db46-178">JobInformation</span><span class="sxs-lookup"><span data-stu-id="0db46-178">JobInformation</span></span>
<span data-ttu-id="0db46-179">Die angegebenen Informationen zu Auftragsinformationen</span><span class="sxs-lookup"><span data-stu-id="0db46-179">The specified job information details</span></span>

### <span data-ttu-id="0db46-180">Liste<JobInformation></span><span class="sxs-lookup"><span data-stu-id="0db46-180">List<JobInformation></span></span>
<span data-ttu-id="0db46-181">Die Liste der Aufträge im angegebenen Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="0db46-181">The list of jobs in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="0db46-182">Notizen</span><span class="sxs-lookup"><span data-stu-id="0db46-182">NOTES</span></span>

## <span data-ttu-id="0db46-183">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0db46-183">RELATED LINKS</span></span>

[<span data-ttu-id="0db46-184">Stopp-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0db46-184">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="0db46-185">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0db46-185">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="0db46-186">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0db46-186">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


