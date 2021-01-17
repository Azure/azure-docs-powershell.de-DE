---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobpipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
ms.openlocfilehash: 1d13d1b6e55831c972457c5a6a5aadc427ecb3a6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472605"
---
# <span data-ttu-id="3d3c9-101">Get-AzDataLakeAnalyticsJobPipeline</span><span class="sxs-lookup"><span data-stu-id="3d3c9-101">Get-AzDataLakeAnalyticsJobPipeline</span></span>

## <span data-ttu-id="3d3c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d3c9-102">SYNOPSIS</span></span>
<span data-ttu-id="3d3c9-103">Ruft eine Datensee-Analyseauftrag-Pipeline oder -Pipelines ab.</span><span class="sxs-lookup"><span data-stu-id="3d3c9-103">Gets a Data Lake Analytics Job pipeline or pipelines.</span></span>

## <span data-ttu-id="3d3c9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d3c9-104">SYNTAX</span></span>

### <span data-ttu-id="3d3c9-105">GetAllInAccount (Standard)</span><span class="sxs-lookup"><span data-stu-id="3d3c9-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d3c9-106">GetBySpecificJobPipeline</span><span class="sxs-lookup"><span data-stu-id="3d3c9-106">GetBySpecificJobPipeline</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-PipelineId] <Guid> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d3c9-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3d3c9-107">DESCRIPTION</span></span>
<span data-ttu-id="3d3c9-108">Die **Get-AzDataLakeAnalyticsJobPipeline** ruft eine angegebene Pipeline für Azure Data Lake Analytics Job oder eine Liste von Pipelines ab.</span><span class="sxs-lookup"><span data-stu-id="3d3c9-108">The **Get-AzDataLakeAnalyticsJobPipeline** gets a specified Azure Data Lake Analytics Job pipeline or a list of pipelines.</span></span>

## <span data-ttu-id="3d3c9-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3d3c9-109">EXAMPLES</span></span>

### <span data-ttu-id="3d3c9-110">Beispiel 1: Erhalten einer angegebenen Pipeline</span><span class="sxs-lookup"><span data-stu-id="3d3c9-110">Example 1: Get a specified pipeline</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -Account "contosoadla" -PipelineId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="3d3c9-111">Dieser Befehl ruft die angegebene Pipeline mit der ID '83cb7ad2-3523-4b82-b909-d478b0d8aea3' im Konto 'contosoadla' ab.</span><span class="sxs-lookup"><span data-stu-id="3d3c9-111">This command gets the specified pipeline with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="3d3c9-112">Beispiel 2: Erhalten einer Liste aller Pipelines im Konto</span><span class="sxs-lookup"><span data-stu-id="3d3c9-112">Example 2: Get a list of all pipelines in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -AccountName "contosoadla"
```

<span data-ttu-id="3d3c9-113">Dieser Befehl ruft eine Liste aller Pipelines im Konto "contosoadla" ab.</span><span class="sxs-lookup"><span data-stu-id="3d3c9-113">This command gets a list of all pipelines in the account "contosoadla"</span></span>

## <span data-ttu-id="3d3c9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d3c9-114">PARAMETERS</span></span>

### <span data-ttu-id="3d3c9-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="3d3c9-115">-Account</span></span>
<span data-ttu-id="3d3c9-116">Der Name des Data Lake Analytics-Kontonamens, unter dem die Auftragspipeline abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="3d3c9-116">Name of the Data Lake Analytics account name under which want to retrieve the job pipeline.</span></span>

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

### <span data-ttu-id="3d3c9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d3c9-117">-DefaultProfile</span></span>
<span data-ttu-id="3d3c9-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="3d3c9-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d3c9-119">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="3d3c9-119">-PipelineId</span></span>
<span data-ttu-id="3d3c9-120">DIE ID der auftragsspezifischen Pipeline, für die Informationen zurücksentfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3d3c9-120">ID of the specific job pipeline to return information for.</span></span>

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobPipeline
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d3c9-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="3d3c9-121">-SubmittedAfter</span></span>
<span data-ttu-id="3d3c9-122">Ein optionaler Filter, der Auftragspipeline(en) zurückgibt, die nur nach der angegebenen Zeit übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="3d3c9-122">An optional filter which returns job pipeline(s) only submitted after the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d3c9-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="3d3c9-123">-SubmittedBefore</span></span>
<span data-ttu-id="3d3c9-124">Ein optionaler Filter, der Auftragspipeline(en) zurückgibt, die nur vor dem angegebenen Zeitpunkt übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="3d3c9-124">An optional filter which returns job pipeline(s) only submitted before the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d3c9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d3c9-125">CommonParameters</span></span>
<span data-ttu-id="3d3c9-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d3c9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d3c9-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d3c9-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d3c9-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3d3c9-128">INPUTS</span></span>

### <span data-ttu-id="3d3c9-129">System.String</span><span class="sxs-lookup"><span data-stu-id="3d3c9-129">System.String</span></span>

### <span data-ttu-id="3d3c9-130">System.Guid</span><span class="sxs-lookup"><span data-stu-id="3d3c9-130">System.Guid</span></span>

### <span data-ttu-id="3d3c9-131">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3d3c9-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="3d3c9-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3d3c9-132">OUTPUTS</span></span>

### <span data-ttu-id="3d3c9-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span><span class="sxs-lookup"><span data-stu-id="3d3c9-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span></span>

## <span data-ttu-id="3d3c9-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3d3c9-134">NOTES</span></span>

## <span data-ttu-id="3d3c9-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3d3c9-135">RELATED LINKS</span></span>
