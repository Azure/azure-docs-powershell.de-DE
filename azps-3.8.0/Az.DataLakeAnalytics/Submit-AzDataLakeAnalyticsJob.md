---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/submit-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 2fcd30c523508620d7d7ed20ebce60facc2678a0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995294"
---
# <span data-ttu-id="93501-101">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="93501-101">Submit-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="93501-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="93501-102">SYNOPSIS</span></span>
<span data-ttu-id="93501-103">Sendet einen Job.</span><span class="sxs-lookup"><span data-stu-id="93501-103">Submits a job.</span></span>

## <span data-ttu-id="93501-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="93501-104">SYNTAX</span></span>

### <span data-ttu-id="93501-105">SubmitUSqlJobWithScriptPath</span><span class="sxs-lookup"><span data-stu-id="93501-105">SubmitUSqlJobWithScriptPath</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93501-106">SubmitUSqlJob</span><span class="sxs-lookup"><span data-stu-id="93501-106">SubmitUSqlJob</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93501-107">SubmitUSqlJobWithScriptPathAndRecurrence</span><span class="sxs-lookup"><span data-stu-id="93501-107">SubmitUSqlJobWithScriptPathAndRecurrence</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93501-108">SubmitUSqlJobWithRecurrence</span><span class="sxs-lookup"><span data-stu-id="93501-108">SubmitUSqlJobWithRecurrence</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93501-109">SubmitUSqlJobWithScriptPathAndPipeline</span><span class="sxs-lookup"><span data-stu-id="93501-109">SubmitUSqlJobWithScriptPathAndPipeline</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="93501-110">SubmitUSqlJobWithPipeline</span><span class="sxs-lookup"><span data-stu-id="93501-110">SubmitUSqlJobWithPipeline</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="93501-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93501-111">DESCRIPTION</span></span>
<span data-ttu-id="93501-112">Mit dem **Submit-AzDataLakeAnalyticsJob-** Cmdlet wird ein Azure Data Lake-Analyse Auftrag übermittelt.</span><span class="sxs-lookup"><span data-stu-id="93501-112">The **Submit-AzDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="93501-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="93501-113">EXAMPLES</span></span>

### <span data-ttu-id="93501-114">Beispiel 1: Einreichen eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="93501-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32
```

<span data-ttu-id="93501-115">Mit diesem Befehl wird ein Data Lake-Analyse Auftrag übermittelt.</span><span class="sxs-lookup"><span data-stu-id="93501-115">This command submits a Data Lake Analytics job.</span></span>

### <span data-ttu-id="93501-116">Beispiel 2: Übermitteln eines Auftrags mit Skriptparametern</span><span class="sxs-lookup"><span data-stu-id="93501-116">Example 2: Submit a job with script parameters</span></span>
```
PS C:\>$parameters = [ordered]@{}
$parameters["Department"] = "Sales"
$parameters["NumRecords"] = 1000
$parameters["StartDateTime"] = (Get-Date).AddDays(-14)
Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32 -ScriptParameter $parameters
```

<span data-ttu-id="93501-117">U-SQL-Skriptparameter werden über den Hauptskript Inhalten vorangestellt, beispielsweise: Declare @Department String = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = New DateTime (2017; 12; 6; 0; 0; 0; 0);</span><span class="sxs-lookup"><span data-stu-id="93501-117">U-SQL script parameters are prepended above the main script contents, e.g.: DECLARE @Department string = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = new DateTime(2017, 12, 6, 0, 0, 0, 0);</span></span>

## <span data-ttu-id="93501-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="93501-118">PARAMETERS</span></span>

### <span data-ttu-id="93501-119">-Konto</span><span class="sxs-lookup"><span data-stu-id="93501-119">-Account</span></span>
<span data-ttu-id="93501-120">Name des Daten Lake Analytics-Kontos, unter dem der Auftrag übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="93501-120">Name of Data Lake Analytics account under which the job will be submitted.</span></span>

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

### <span data-ttu-id="93501-121">-AnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="93501-121">-AnalyticsUnits</span></span>
<span data-ttu-id="93501-122">Die für diesen Auftrag zu verwendenden Analyseeinheiten.</span><span class="sxs-lookup"><span data-stu-id="93501-122">The analytics units to use for this job.</span></span> <span data-ttu-id="93501-123">In der Regel führen mehr Analyseeinheiten, die einem Skript gewidmet sind, zu schnelleren Skript Ausführungszeiten.</span><span class="sxs-lookup"><span data-stu-id="93501-123">Typically, more analytics units dedicated to a script results in faster script execution time.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: DegreeOfParallelism

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93501-124">-CompileMode</span><span class="sxs-lookup"><span data-stu-id="93501-124">-CompileMode</span></span>
<span data-ttu-id="93501-125">Der Typ der Kompilierung, die für diesen Auftrag ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="93501-125">The type of compilation to be done on this job.</span></span> <span data-ttu-id="93501-126">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="93501-126">Valid values:</span></span> 
- <span data-ttu-id="93501-127">Semantic (führt nur semantische Prüfungen und notwendige Plausibilitätsprüfungen durch)</span><span class="sxs-lookup"><span data-stu-id="93501-127">Semantic (Only performs semantic checks and necessary sanity checks)</span></span>
- <span data-ttu-id="93501-128">Vollständige Kompilierung</span><span class="sxs-lookup"><span data-stu-id="93501-128">Full (Full compilation)</span></span>
- <span data-ttu-id="93501-129">Singlebox (vollständige Kompilierung lokal durchgeführt)</span><span class="sxs-lookup"><span data-stu-id="93501-129">SingleBox (Full compilation performed locally)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Semantic, Full, SingleBox

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93501-130">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="93501-130">-CompileOnly</span></span>
<span data-ttu-id="93501-131">Gibt an, dass die Übermittlung den Auftrag nur erstellen und nicht ausführen sollte, wenn er auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="93501-131">Indicates that the submission should only build the job and not execute if set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93501-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93501-132">-DefaultProfile</span></span>
<span data-ttu-id="93501-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="93501-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93501-134">-Name</span><span class="sxs-lookup"><span data-stu-id="93501-134">-Name</span></span>
<span data-ttu-id="93501-135">Der Anzeigename des Auftrags, der gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="93501-135">The friendly name of the job to submit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93501-136">-Pipeline-Nr</span><span class="sxs-lookup"><span data-stu-id="93501-136">-PipelineId</span></span>
<span data-ttu-id="93501-137">Eine ID, die angibt, dass die Übermittlung dieses Auftrags Teil einer Reihe von wiederkehrenden Aufträgen und auch einer Job-Pipeline zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="93501-137">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93501-138">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="93501-138">-PipelineName</span></span>
<span data-ttu-id="93501-139">Ein optionaler Anzeigename für die Pipeline, die diesem Auftrag zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="93501-139">An optional friendly name for the pipeline associated with this job.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93501-140">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="93501-140">-PipelineUri</span></span>
<span data-ttu-id="93501-141">Ein optionaler URI, der mit dem Ursprungs Dienst verknüpft ist, der dieser Pipeline zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="93501-141">An optional uri that links to the originating service associated with this pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93501-142">-Priorität</span><span class="sxs-lookup"><span data-stu-id="93501-142">-Priority</span></span>
<span data-ttu-id="93501-143">Die Priorität des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="93501-143">The priority of the job.</span></span> <span data-ttu-id="93501-144">Wenn keine Angabe erfolgt, lautet die Priorität 1000.</span><span class="sxs-lookup"><span data-stu-id="93501-144">If not specified, the priority is 1000.</span></span> <span data-ttu-id="93501-145">Eine niedrigere Zahl kennzeichnet eine höhere Auftragspriorität.</span><span class="sxs-lookup"><span data-stu-id="93501-145">A lower number indicates a higher job priority.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93501-146">-Serien-Nr</span><span class="sxs-lookup"><span data-stu-id="93501-146">-RecurrenceId</span></span>
<span data-ttu-id="93501-147">Eine ID, die angibt, dass die Übermittlung dieses Auftrags Teil einer Reihe von wiederkehrenden Aufträgen mit derselben Serien-ID ist.</span><span class="sxs-lookup"><span data-stu-id="93501-147">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93501-148">-Serienname</span><span class="sxs-lookup"><span data-stu-id="93501-148">-RecurrenceName</span></span>
<span data-ttu-id="93501-149">Ein optionaler Anzeigename für die Serien Korrelation zwischen Aufträgen.</span><span class="sxs-lookup"><span data-stu-id="93501-149">An optional friendly name for the recurrence correlation between jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93501-150">-RunId</span><span class="sxs-lookup"><span data-stu-id="93501-150">-RunId</span></span>
<span data-ttu-id="93501-151">Eine ID, die diese bestimmte Durchlauf Iteration der Pipeline identifiziert.</span><span class="sxs-lookup"><span data-stu-id="93501-151">An ID that identifies this specific run iteration of the pipeline.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93501-152">-Runtime</span><span class="sxs-lookup"><span data-stu-id="93501-152">-Runtime</span></span>
<span data-ttu-id="93501-153">Optional können Sie die für den Auftrag zu verwendende Version der Laufzeit einstellen.</span><span class="sxs-lookup"><span data-stu-id="93501-153">Optionally set the version of the runtime to use for the job.</span></span> <span data-ttu-id="93501-154">Wenn Sie nicht mehr verwendet wird, wird die Standardlaufzeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="93501-154">If left unset, the default runtime is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93501-155">-Skript</span><span class="sxs-lookup"><span data-stu-id="93501-155">-Script</span></span>
<span data-ttu-id="93501-156">Skript zum Ausführen (Inline geschrieben).</span><span class="sxs-lookup"><span data-stu-id="93501-156">Script to execute (written inline).</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJob, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93501-157">-Scriptparameter</span><span class="sxs-lookup"><span data-stu-id="93501-157">-ScriptParameter</span></span>
<span data-ttu-id="93501-158">Die Skriptparameter für diesen Auftrag als Wörterbuch mit Parameternamen (Zeichenfolge) für Werte (eine beliebige Kombination aus Byte, SByte, int, uint (oder UInt32), Long, ULONG (oder UInt64), float, Double, Decimal, Short (oder Int16), ushort (oder UInt16), Char, String, DateTime, bool, GUID oder Byte []).</span><span class="sxs-lookup"><span data-stu-id="93501-158">The script parameters for this job, as a dictionary of parameter names (string) to values (any combination of byte, sbyte, int, uint (or uint32), long, ulong (or uint64), float, double, decimal, short (or int16), ushort (or uint16), char, string, DateTime, bool, Guid, or byte[]).</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93501-159">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="93501-159">-ScriptPath</span></span>
<span data-ttu-id="93501-160">Der Pfad zur zu übermittelnden Skriptdatei.</span><span class="sxs-lookup"><span data-stu-id="93501-160">Path to the script file to submit.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPath, SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithScriptPathAndPipeline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93501-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93501-161">CommonParameters</span></span>
<span data-ttu-id="93501-162">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93501-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93501-163">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93501-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93501-164">Eingaben</span><span class="sxs-lookup"><span data-stu-id="93501-164">INPUTS</span></span>

### <span data-ttu-id="93501-165">System. String</span><span class="sxs-lookup"><span data-stu-id="93501-165">System.String</span></span>

### <span data-ttu-id="93501-166">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="93501-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="93501-167">System. Int32</span><span class="sxs-lookup"><span data-stu-id="93501-167">System.Int32</span></span>

### <span data-ttu-id="93501-168">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="93501-168">System.Collections.IDictionary</span></span>

### <span data-ttu-id="93501-169">System. GUID</span><span class="sxs-lookup"><span data-stu-id="93501-169">System.Guid</span></span>

### <span data-ttu-id="93501-170">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="93501-170">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="93501-171">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="93501-171">OUTPUTS</span></span>

### <span data-ttu-id="93501-172">Microsoft. Azure. Management. datalake. Analytics. Models. JobInformation</span><span class="sxs-lookup"><span data-stu-id="93501-172">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="93501-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="93501-173">NOTES</span></span>

## <span data-ttu-id="93501-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="93501-174">RELATED LINKS</span></span>

[<span data-ttu-id="93501-175">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="93501-175">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="93501-176">Stopp-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="93501-176">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="93501-177">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="93501-177">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


