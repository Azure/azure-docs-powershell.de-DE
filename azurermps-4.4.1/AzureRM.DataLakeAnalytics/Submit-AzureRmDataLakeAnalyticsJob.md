---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: bb0ad536d738facdfe50bc7983517f4505ab4ef2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500073"
---
# <span data-ttu-id="bec16-101">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="bec16-101">Submit-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="bec16-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bec16-102">SYNOPSIS</span></span>
<span data-ttu-id="bec16-103">Sendet einen Job.</span><span class="sxs-lookup"><span data-stu-id="bec16-103">Submits a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bec16-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bec16-104">SYNTAX</span></span>

### <span data-ttu-id="bec16-105">Auftrag mit Skriptpfad für U-SQL übermitteln</span><span class="sxs-lookup"><span data-stu-id="bec16-105">Submit job with script path for U-SQL</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bec16-106">U-SQL-Auftrag einreichen</span><span class="sxs-lookup"><span data-stu-id="bec16-106">Submit U-SQL Job</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bec16-107">Job mit Skriptpfad für U-SQL mit reucurrence-Informationen übermitteln</span><span class="sxs-lookup"><span data-stu-id="bec16-107">Submit job with script path for U-SQL with reucurrence information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bec16-108">Senden eines U-SQL-Auftrags mit Serieninformationen</span><span class="sxs-lookup"><span data-stu-id="bec16-108">Submit U-SQL Job with recurrence information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bec16-109">Auftrag mit Skriptpfad für U-SQL mit reucurrence und Pipelineinformationen übermitteln</span><span class="sxs-lookup"><span data-stu-id="bec16-109">Submit job with script path for U-SQL with reucurrence and pipeline information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bec16-110">Senden eines U-SQL-Auftrags mit Serien-und Pipelineinformationen</span><span class="sxs-lookup"><span data-stu-id="bec16-110">Submit U-SQL Job with recurrence and pipeline information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bec16-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bec16-111">DESCRIPTION</span></span>
<span data-ttu-id="bec16-112">Mit dem **Submit-AzureRmDataLakeAnalyticsJob-** Cmdlet wird ein Azure Data Lake-Analyse Auftrag übermittelt.</span><span class="sxs-lookup"><span data-stu-id="bec16-112">The **Submit-AzureRmDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="bec16-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bec16-113">EXAMPLES</span></span>

### <span data-ttu-id="bec16-114">Beispiel 1: Einreichen eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="bec16-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -DegreeOfParallelism 32
```

<span data-ttu-id="bec16-115">Mit diesem Befehl wird ein Data Lake-Analyse Auftrag übermittelt.</span><span class="sxs-lookup"><span data-stu-id="bec16-115">This command submits a Data Lake Analytics job.</span></span>

## <span data-ttu-id="bec16-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="bec16-116">PARAMETERS</span></span>

### <span data-ttu-id="bec16-117">-Konto</span><span class="sxs-lookup"><span data-stu-id="bec16-117">-Account</span></span>
<span data-ttu-id="bec16-118">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="bec16-118">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="bec16-119">-CompileMode</span><span class="sxs-lookup"><span data-stu-id="bec16-119">-CompileMode</span></span>
<span data-ttu-id="bec16-120">Gibt den Kompilierungsmodus des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="bec16-120">Specifies the compilation mode of the job.</span></span>
<span data-ttu-id="bec16-121">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="bec16-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bec16-122">Semantik</span><span class="sxs-lookup"><span data-stu-id="bec16-122">Semantic</span></span>
- <span data-ttu-id="bec16-123">Voll</span><span class="sxs-lookup"><span data-stu-id="bec16-123">Full</span></span>
- <span data-ttu-id="bec16-124">Singlebox</span><span class="sxs-lookup"><span data-stu-id="bec16-124">SingleBox</span></span>

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

### <span data-ttu-id="bec16-125">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="bec16-125">-CompileOnly</span></span>
<span data-ttu-id="bec16-126">Gibt an, dass dieses Cmdlet den Auftrag ohne Ausführung kompiliert.</span><span class="sxs-lookup"><span data-stu-id="bec16-126">Indicates that this cmdlet compiles the job without running it.</span></span>

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

### <span data-ttu-id="bec16-127">-DegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="bec16-127">-DegreeOfParallelism</span></span>
<span data-ttu-id="bec16-128">Gibt die Daten Lake Analytics Units (DLAU) des Auftrags an, die die maximal zulässige Parallelität des Auftrags angeben.</span><span class="sxs-lookup"><span data-stu-id="bec16-128">Specifies the Data Lake Analytics Units (DLAU) of the job, which indicates the maximum allowable parallelism of the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bec16-129">-Name</span><span class="sxs-lookup"><span data-stu-id="bec16-129">-Name</span></span>
<span data-ttu-id="bec16-130">Gibt den Auftragsnamen an.</span><span class="sxs-lookup"><span data-stu-id="bec16-130">Specifies the job name.</span></span>

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

### <span data-ttu-id="bec16-131">-Pipeline-Nr</span><span class="sxs-lookup"><span data-stu-id="bec16-131">-PipelineId</span></span>
<span data-ttu-id="bec16-132">Eine ID, die angibt, dass die Übermittlung dieses Auftrags Teil einer Reihe von wiederkehrenden Aufträgen und auch einer Job-Pipeline zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="bec16-132">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bec16-133">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="bec16-133">-PipelineName</span></span>
<span data-ttu-id="bec16-134">Ein optionaler Anzeigename für die Pipeline, die diesem Auftrag zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="bec16-134">An optional friendly name for the pipeline associated with this job.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bec16-135">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="bec16-135">-PipelineUri</span></span>
<span data-ttu-id="bec16-136">Ein optionaler URI, der mit dem Ursprungs Dienst verknüpft ist, der dieser Pipeline zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="bec16-136">An optional uri that links to the originating service associated with this pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bec16-137">-Priorität</span><span class="sxs-lookup"><span data-stu-id="bec16-137">-Priority</span></span>
<span data-ttu-id="bec16-138">Gibt die Priorität des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="bec16-138">Specifies the priority of the job.</span></span>
<span data-ttu-id="bec16-139">Wenn keine Angabe erfolgt, lautet die Priorität 1000.</span><span class="sxs-lookup"><span data-stu-id="bec16-139">If not specified, the priority is 1000.</span></span>
<span data-ttu-id="bec16-140">Eine niedrige Zahl kennzeichnet eine höhere Auftragspriorität.</span><span class="sxs-lookup"><span data-stu-id="bec16-140">A low number indicates a higher job priority.</span></span>

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

### <span data-ttu-id="bec16-141">-Serien-Nr</span><span class="sxs-lookup"><span data-stu-id="bec16-141">-RecurrenceId</span></span>
<span data-ttu-id="bec16-142">Eine ID, die angibt, dass die Übermittlung dieses Auftrags Teil einer Reihe von wiederkehrenden Aufträgen mit derselben Serien-ID ist.</span><span class="sxs-lookup"><span data-stu-id="bec16-142">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Submit job with script path for U-SQL with reucurrence information, Submit U-SQL Job with recurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bec16-143">-Serienname</span><span class="sxs-lookup"><span data-stu-id="bec16-143">-RecurrenceName</span></span>
<span data-ttu-id="bec16-144">Ein optionaler Anzeigename für die Serien Korrelation zwischen Aufträgen.</span><span class="sxs-lookup"><span data-stu-id="bec16-144">An optional friendly name for the recurrence correlation between jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence information, Submit U-SQL Job with recurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bec16-145">-RunId</span><span class="sxs-lookup"><span data-stu-id="bec16-145">-RunId</span></span>
<span data-ttu-id="bec16-146">Eine ID, die diese bestimmte Durchlauf Iteration der Pipeline identifiziert.</span><span class="sxs-lookup"><span data-stu-id="bec16-146">An ID that identifies this specific run iteration of the pipeline.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bec16-147">-Runtime</span><span class="sxs-lookup"><span data-stu-id="bec16-147">-Runtime</span></span>
<span data-ttu-id="bec16-148">Gibt die Laufzeitversion des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="bec16-148">Specifies the runtime version of the job.</span></span>

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

### <span data-ttu-id="bec16-149">-Skript</span><span class="sxs-lookup"><span data-stu-id="bec16-149">-Script</span></span>
<span data-ttu-id="bec16-150">Gibt den Inhalt des Skripts an, das ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bec16-150">Specifies the contents of the script to run.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit U-SQL Job, Submit U-SQL Job with recurrence information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bec16-151">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="bec16-151">-ScriptPath</span></span>
<span data-ttu-id="bec16-152">Gibt den lokalen Dateipfad für das auszuführende Skript an.</span><span class="sxs-lookup"><span data-stu-id="bec16-152">Specifies the local file path to the script to run.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL, Submit job with script path for U-SQL with reucurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bec16-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bec16-153">-DefaultProfile</span></span>
<span data-ttu-id="bec16-154">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bec16-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bec16-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bec16-155">CommonParameters</span></span>
<span data-ttu-id="bec16-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bec16-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bec16-157">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bec16-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bec16-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bec16-158">INPUTS</span></span>

### <span data-ttu-id="bec16-159">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="bec16-159">String</span></span>
<span data-ttu-id="bec16-160">Der Parameter "Script" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="bec16-160">Parameter 'Script' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="bec16-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bec16-161">OUTPUTS</span></span>

### <span data-ttu-id="bec16-162">JobInformation</span><span class="sxs-lookup"><span data-stu-id="bec16-162">JobInformation</span></span>
<span data-ttu-id="bec16-163">Die anfänglichen Auftragsdetails für den gesendeten Auftrag.</span><span class="sxs-lookup"><span data-stu-id="bec16-163">The initial job details for the submitted job.</span></span>

## <span data-ttu-id="bec16-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="bec16-164">NOTES</span></span>

## <span data-ttu-id="bec16-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bec16-165">RELATED LINKS</span></span>

[<span data-ttu-id="bec16-166">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="bec16-166">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="bec16-167">Stopp-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="bec16-167">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="bec16-168">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="bec16-168">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


