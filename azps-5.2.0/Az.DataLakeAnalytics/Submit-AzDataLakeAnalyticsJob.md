---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/submit-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 2fcd30c523508620d7d7ed20ebce60facc2678a0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301360"
---
# <span data-ttu-id="66af2-101">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="66af2-101">Submit-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="66af2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66af2-102">SYNOPSIS</span></span>
<span data-ttu-id="66af2-103">Übermittelt einen Auftrag.</span><span class="sxs-lookup"><span data-stu-id="66af2-103">Submits a job.</span></span>

## <span data-ttu-id="66af2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66af2-104">SYNTAX</span></span>

### <span data-ttu-id="66af2-105">SubmitUSqlJobWithScriptPath</span><span class="sxs-lookup"><span data-stu-id="66af2-105">SubmitUSqlJobWithScriptPath</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66af2-106">SubmitUSqlJob</span><span class="sxs-lookup"><span data-stu-id="66af2-106">SubmitUSqlJob</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66af2-107">SubmitUSqlJobWithScriptPathAndRecurrence</span><span class="sxs-lookup"><span data-stu-id="66af2-107">SubmitUSqlJobWithScriptPathAndRecurrence</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66af2-108">SubmitUSqlJobWithRecurrence</span><span class="sxs-lookup"><span data-stu-id="66af2-108">SubmitUSqlJobWithRecurrence</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66af2-109">SubmitUSqlJobWithScriptPathAndPipeline</span><span class="sxs-lookup"><span data-stu-id="66af2-109">SubmitUSqlJobWithScriptPathAndPipeline</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="66af2-110">SubmitUSqlJobWithPipeline</span><span class="sxs-lookup"><span data-stu-id="66af2-110">SubmitUSqlJobWithPipeline</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="66af2-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="66af2-111">DESCRIPTION</span></span>
<span data-ttu-id="66af2-112">Das **Cmdlet "Submit-AzDataLakeAnalyticsJob"** übermittelt einen Azure Data Lake Analytics-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="66af2-112">The **Submit-AzDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="66af2-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="66af2-113">EXAMPLES</span></span>

### <span data-ttu-id="66af2-114">Beispiel 1: Übermitteln eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="66af2-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32
```

<span data-ttu-id="66af2-115">Mit diesem Befehl wird ein Data Lake Analytics-Auftrag übermittelt.</span><span class="sxs-lookup"><span data-stu-id="66af2-115">This command submits a Data Lake Analytics job.</span></span>

### <span data-ttu-id="66af2-116">Beispiel 2: Übermitteln eines Auftrags mit Skriptparametern</span><span class="sxs-lookup"><span data-stu-id="66af2-116">Example 2: Submit a job with script parameters</span></span>
```
PS C:\>$parameters = [ordered]@{}
$parameters["Department"] = "Sales"
$parameters["NumRecords"] = 1000
$parameters["StartDateTime"] = (Get-Date).AddDays(-14)
Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32 -ScriptParameter $parameters
```

<span data-ttu-id="66af2-117">#SQL Skriptparameter werden oberhalb des Hauptskriptinhalts festgelegt, z. B.: #A0 @Department = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = new DateTime(2017; 12; 6; 0; 0; 0; 0; 0);</span><span class="sxs-lookup"><span data-stu-id="66af2-117">U-SQL script parameters are prepended above the main script contents, e.g.: DECLARE @Department string = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = new DateTime(2017, 12, 6, 0, 0, 0, 0);</span></span>

## <span data-ttu-id="66af2-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66af2-118">PARAMETERS</span></span>

### <span data-ttu-id="66af2-119">-Konto</span><span class="sxs-lookup"><span data-stu-id="66af2-119">-Account</span></span>
<span data-ttu-id="66af2-120">Name des Data Lake Analytics-Kontos, unter dem der Auftrag übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="66af2-120">Name of Data Lake Analytics account under which the job will be submitted.</span></span>

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

### <span data-ttu-id="66af2-121">-AnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="66af2-121">-AnalyticsUnits</span></span>
<span data-ttu-id="66af2-122">Die Analyseeinheiten, die für diesen Auftrag verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="66af2-122">The analytics units to use for this job.</span></span> <span data-ttu-id="66af2-123">In der Regel führen mehr Analyseeinheiten, die einem Skript gewidmet sind, zu einer schnelleren Skriptausführungszeit.</span><span class="sxs-lookup"><span data-stu-id="66af2-123">Typically, more analytics units dedicated to a script results in faster script execution time.</span></span>

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

### <span data-ttu-id="66af2-124">-CompileMode</span><span class="sxs-lookup"><span data-stu-id="66af2-124">-CompileMode</span></span>
<span data-ttu-id="66af2-125">Die Art der Kompilierung, die für diesen Auftrag durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="66af2-125">The type of compilation to be done on this job.</span></span> <span data-ttu-id="66af2-126">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="66af2-126">Valid values:</span></span> 
- <span data-ttu-id="66af2-127">Semantik (führt nur semantische Überprüfungen und erforderliche Überprüfungen der Sanität aus)</span><span class="sxs-lookup"><span data-stu-id="66af2-127">Semantic (Only performs semantic checks and necessary sanity checks)</span></span>
- <span data-ttu-id="66af2-128">Vollständig (vollständige Kompilierung)</span><span class="sxs-lookup"><span data-stu-id="66af2-128">Full (Full compilation)</span></span>
- <span data-ttu-id="66af2-129">SingleBox (vollständige kompilierung lokal ausgeführt)</span><span class="sxs-lookup"><span data-stu-id="66af2-129">SingleBox (Full compilation performed locally)</span></span>

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

### <span data-ttu-id="66af2-130">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="66af2-130">-CompileOnly</span></span>
<span data-ttu-id="66af2-131">Gibt an, dass die Übermittlung den Auftrag nur erstellen und nicht ausführen soll, wenn dies auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="66af2-131">Indicates that the submission should only build the job and not execute if set to true.</span></span>

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

### <span data-ttu-id="66af2-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66af2-132">-DefaultProfile</span></span>
<span data-ttu-id="66af2-133">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="66af2-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66af2-134">-Name</span><span class="sxs-lookup"><span data-stu-id="66af2-134">-Name</span></span>
<span data-ttu-id="66af2-135">Der Anzeigename des zu übermittelnde Auftrags.</span><span class="sxs-lookup"><span data-stu-id="66af2-135">The friendly name of the job to submit.</span></span>

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

### <span data-ttu-id="66af2-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="66af2-136">-PipelineId</span></span>
<span data-ttu-id="66af2-137">Eine ID, die die Übermittlung dieses Auftrags angibt, ist Teil einer Reihe wiederkehrender Aufträge und außerdem mit einer Auftragspipeline verknüpft.</span><span class="sxs-lookup"><span data-stu-id="66af2-137">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

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

### <span data-ttu-id="66af2-138">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="66af2-138">-PipelineName</span></span>
<span data-ttu-id="66af2-139">Ein optionaler Anzeigename für die diesem Auftrag zugeordnete Pipeline.</span><span class="sxs-lookup"><span data-stu-id="66af2-139">An optional friendly name for the pipeline associated with this job.</span></span>

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

### <span data-ttu-id="66af2-140">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="66af2-140">-PipelineUri</span></span>
<span data-ttu-id="66af2-141">Ein optionaler URI, der mit dem ursprungsenden Dienst verknüpft ist, der dieser Pipeline zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="66af2-141">An optional uri that links to the originating service associated with this pipeline.</span></span>

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

### <span data-ttu-id="66af2-142">-Priority</span><span class="sxs-lookup"><span data-stu-id="66af2-142">-Priority</span></span>
<span data-ttu-id="66af2-143">Die Priorität des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="66af2-143">The priority of the job.</span></span> <span data-ttu-id="66af2-144">Wenn keine Angabe ausgeführt wird, hat die Priorität "1000".</span><span class="sxs-lookup"><span data-stu-id="66af2-144">If not specified, the priority is 1000.</span></span> <span data-ttu-id="66af2-145">Eine niedrigere Zahl weist auf eine höhere Auftragspriorität hin.</span><span class="sxs-lookup"><span data-stu-id="66af2-145">A lower number indicates a higher job priority.</span></span>

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

### <span data-ttu-id="66af2-146">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="66af2-146">-RecurrenceId</span></span>
<span data-ttu-id="66af2-147">Eine ID, die die Übermittlung dieses Auftrags angibt, ist Teil einer Reihe von wiederkehrenden Aufträgen mit derselben Serien-ID.</span><span class="sxs-lookup"><span data-stu-id="66af2-147">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

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

### <span data-ttu-id="66af2-148">-RecurrenceName</span><span class="sxs-lookup"><span data-stu-id="66af2-148">-RecurrenceName</span></span>
<span data-ttu-id="66af2-149">Optionaler Anzeigename für die wiederkehrende Korrelation zwischen Aufträgen.</span><span class="sxs-lookup"><span data-stu-id="66af2-149">An optional friendly name for the recurrence correlation between jobs.</span></span>

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

### <span data-ttu-id="66af2-150">-RunId</span><span class="sxs-lookup"><span data-stu-id="66af2-150">-RunId</span></span>
<span data-ttu-id="66af2-151">Eine ID, die diese spezifische Ausführungsiteration der Pipeline identifiziert.</span><span class="sxs-lookup"><span data-stu-id="66af2-151">An ID that identifies this specific run iteration of the pipeline.</span></span>

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

### <span data-ttu-id="66af2-152">-Runtime</span><span class="sxs-lookup"><span data-stu-id="66af2-152">-Runtime</span></span>
<span data-ttu-id="66af2-153">Legen Sie optional die für den Auftrag zu verwendende Version der Laufzeit festgelegt.</span><span class="sxs-lookup"><span data-stu-id="66af2-153">Optionally set the version of the runtime to use for the job.</span></span> <span data-ttu-id="66af2-154">Wenn dies nicht festgelegt ist, wird die Standardlaufzeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="66af2-154">If left unset, the default runtime is used.</span></span>

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

### <span data-ttu-id="66af2-155">-Script</span><span class="sxs-lookup"><span data-stu-id="66af2-155">-Script</span></span>
<span data-ttu-id="66af2-156">Auszuführende Skripts (inline geschrieben).</span><span class="sxs-lookup"><span data-stu-id="66af2-156">Script to execute (written inline).</span></span>

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

### <span data-ttu-id="66af2-157">-ScriptParameter</span><span class="sxs-lookup"><span data-stu-id="66af2-157">-ScriptParameter</span></span>
<span data-ttu-id="66af2-158">Die Skriptparameter für diesen Auftrag als Wörterbuch mit Parameternamen (Zeichenfolge) für Werte (eine beliebige Kombination aus Byte, SBYTE, Int, uint (oder uint32), long, ulong (oder uint64), float, double, decimal, short (oder int16), ushort (oder uint16), char, string, DateTime, bool, Guid oder byte[]).</span><span class="sxs-lookup"><span data-stu-id="66af2-158">The script parameters for this job, as a dictionary of parameter names (string) to values (any combination of byte, sbyte, int, uint (or uint32), long, ulong (or uint64), float, double, decimal, short (or int16), ushort (or uint16), char, string, DateTime, bool, Guid, or byte[]).</span></span>

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

### <span data-ttu-id="66af2-159">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="66af2-159">-ScriptPath</span></span>
<span data-ttu-id="66af2-160">Pfad zu der skriptdatei, die übermittelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="66af2-160">Path to the script file to submit.</span></span>

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

### <span data-ttu-id="66af2-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66af2-161">CommonParameters</span></span>
<span data-ttu-id="66af2-162">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66af2-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66af2-163">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66af2-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66af2-164">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="66af2-164">INPUTS</span></span>

### <span data-ttu-id="66af2-165">System.String</span><span class="sxs-lookup"><span data-stu-id="66af2-165">System.String</span></span>

### <span data-ttu-id="66af2-166">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="66af2-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="66af2-167">System.Int32</span><span class="sxs-lookup"><span data-stu-id="66af2-167">System.Int32</span></span>

### <span data-ttu-id="66af2-168">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="66af2-168">System.Collections.IDictionary</span></span>

### <span data-ttu-id="66af2-169">System.Guid</span><span class="sxs-lookup"><span data-stu-id="66af2-169">System.Guid</span></span>

### <span data-ttu-id="66af2-170">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="66af2-170">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="66af2-171">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="66af2-171">OUTPUTS</span></span>

### <span data-ttu-id="66af2-172">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span><span class="sxs-lookup"><span data-stu-id="66af2-172">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="66af2-173">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="66af2-173">NOTES</span></span>

## <span data-ttu-id="66af2-174">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="66af2-174">RELATED LINKS</span></span>

[<span data-ttu-id="66af2-175">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="66af2-175">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="66af2-176">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="66af2-176">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="66af2-177">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="66af2-177">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


