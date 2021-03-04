---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobpipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
ms.openlocfilehash: 9e925e1bd118a9ac5f676ee666cb945f22d1ffac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937032"
---
# <span data-ttu-id="8745d-101">Get-AzDataLakeAnalyticsJobPipeline</span><span class="sxs-lookup"><span data-stu-id="8745d-101">Get-AzDataLakeAnalyticsJobPipeline</span></span>

## <span data-ttu-id="8745d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8745d-102">SYNOPSIS</span></span>
<span data-ttu-id="8745d-103">Ruft eine Data Lake Analytics-Auftragspipeline oder -pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="8745d-103">Gets a Data Lake Analytics Job pipeline or pipelines.</span></span>

## <span data-ttu-id="8745d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8745d-104">SYNTAX</span></span>

### <span data-ttu-id="8745d-105">GetAllInAccount (Standard)</span><span class="sxs-lookup"><span data-stu-id="8745d-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8745d-106">GetBySpecificJobPipeline</span><span class="sxs-lookup"><span data-stu-id="8745d-106">GetBySpecificJobPipeline</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-PipelineId] <Guid> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8745d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8745d-107">DESCRIPTION</span></span>
<span data-ttu-id="8745d-108">Die **Get-AzDataLakeAnalyticsJobPipeline** ruft eine angegebene Azure Data Lake Analytics-Auftragspipeline oder eine Liste der Pipelines ab.</span><span class="sxs-lookup"><span data-stu-id="8745d-108">The **Get-AzDataLakeAnalyticsJobPipeline** gets a specified Azure Data Lake Analytics Job pipeline or a list of pipelines.</span></span>

## <span data-ttu-id="8745d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8745d-109">EXAMPLES</span></span>

### <span data-ttu-id="8745d-110">Beispiel 1: Erhalten einer angegebenen Pipeline</span><span class="sxs-lookup"><span data-stu-id="8745d-110">Example 1: Get a specified pipeline</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -Account "contosoadla" -PipelineId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="8745d-111">Dieser Befehl ruft die angegebene Pipeline mit der ID "83cb7ad2-3523-4b82-b909-d478b0d8aea3" im Konto "contosoadla" ab.</span><span class="sxs-lookup"><span data-stu-id="8745d-111">This command gets the specified pipeline with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="8745d-112">Beispiel 2: Erhalten einer Liste aller Pipelines im Konto</span><span class="sxs-lookup"><span data-stu-id="8745d-112">Example 2: Get a list of all pipelines in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -AccountName "contosoadla"
```

<span data-ttu-id="8745d-113">Dieser Befehl ruft eine Liste aller Pipelines im Konto "contosoadla" ab.</span><span class="sxs-lookup"><span data-stu-id="8745d-113">This command gets a list of all pipelines in the account "contosoadla"</span></span>

## <span data-ttu-id="8745d-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8745d-114">PARAMETERS</span></span>

### <span data-ttu-id="8745d-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="8745d-115">-Account</span></span>
<span data-ttu-id="8745d-116">Name des Data Lake Analytics-Kontonamens, unter dem die Auftragspipeline abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8745d-116">Name of the Data Lake Analytics account name under which want to retrieve the job pipeline.</span></span>

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

### <span data-ttu-id="8745d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8745d-117">-DefaultProfile</span></span>
<span data-ttu-id="8745d-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="8745d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8745d-119">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="8745d-119">-PipelineId</span></span>
<span data-ttu-id="8745d-120">ID der bestimmten Auftragspipeline, für die Informationen zurücksennen sollen.</span><span class="sxs-lookup"><span data-stu-id="8745d-120">ID of the specific job pipeline to return information for.</span></span>

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

### <span data-ttu-id="8745d-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="8745d-121">-SubmittedAfter</span></span>
<span data-ttu-id="8745d-122">Ein optionaler Filter, der auftragspipeline(n) zurückgibt, die nur nach dem angegebenen Zeitpunkt übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="8745d-122">An optional filter which returns job pipeline(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="8745d-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="8745d-123">-SubmittedBefore</span></span>
<span data-ttu-id="8745d-124">Ein optionaler Filter, der auftragspipeline(n) zurückgibt, die nur vor dem angegebenen Zeitpunkt übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="8745d-124">An optional filter which returns job pipeline(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="8745d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8745d-125">CommonParameters</span></span>
<span data-ttu-id="8745d-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8745d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8745d-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8745d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8745d-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8745d-128">INPUTS</span></span>

### <span data-ttu-id="8745d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="8745d-129">System.String</span></span>

### <span data-ttu-id="8745d-130">System.Guid</span><span class="sxs-lookup"><span data-stu-id="8745d-130">System.Guid</span></span>

### <span data-ttu-id="8745d-131">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8745d-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8745d-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8745d-132">OUTPUTS</span></span>

### <span data-ttu-id="8745d-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span><span class="sxs-lookup"><span data-stu-id="8745d-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span></span>

## <span data-ttu-id="8745d-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8745d-134">NOTES</span></span>

## <span data-ttu-id="8745d-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8745d-135">RELATED LINKS</span></span>
