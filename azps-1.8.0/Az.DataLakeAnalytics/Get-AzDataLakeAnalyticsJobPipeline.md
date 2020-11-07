---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobpipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
ms.openlocfilehash: 5b9046e085e7aaba09e9a13fd641f9c8986ccfd8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661302"
---
# <span data-ttu-id="6e5c3-101">Get-AzDataLakeAnalyticsJobPipeline</span><span class="sxs-lookup"><span data-stu-id="6e5c3-101">Get-AzDataLakeAnalyticsJobPipeline</span></span>

## <span data-ttu-id="6e5c3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6e5c3-102">SYNOPSIS</span></span>
<span data-ttu-id="6e5c3-103">Ruft eine Data Lake Analytics-Auftragspipeline oder Pipelines ab.</span><span class="sxs-lookup"><span data-stu-id="6e5c3-103">Gets a Data Lake Analytics Job pipeline or pipelines.</span></span>

## <span data-ttu-id="6e5c3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e5c3-104">SYNTAX</span></span>

### <span data-ttu-id="6e5c3-105">GetAllInAccount (Standard)</span><span class="sxs-lookup"><span data-stu-id="6e5c3-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e5c3-106">GetBySpecificJobPipeline</span><span class="sxs-lookup"><span data-stu-id="6e5c3-106">GetBySpecificJobPipeline</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-PipelineId] <Guid> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e5c3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e5c3-107">DESCRIPTION</span></span>
<span data-ttu-id="6e5c3-108">Die **Get-AzDataLakeAnalyticsJobPipeline-** Funktion Ruft eine angegebene Azure Data Lake Analytics-Auftragspipeline oder eine Liste von Pipelines ab.</span><span class="sxs-lookup"><span data-stu-id="6e5c3-108">The **Get-AzDataLakeAnalyticsJobPipeline** gets a specified Azure Data Lake Analytics Job pipeline or a list of pipelines.</span></span>

## <span data-ttu-id="6e5c3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6e5c3-109">EXAMPLES</span></span>

### <span data-ttu-id="6e5c3-110">Beispiel 1: Abrufen einer angegebenen Pipeline</span><span class="sxs-lookup"><span data-stu-id="6e5c3-110">Example 1: Get a specified pipeline</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -Account "contosoadla" -PipelineId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="6e5c3-111">Dieser Befehl ruft die angegebene Pipeline mit der ID ' 83cb7ad2-3523-4b82-b909-d478b0d8aea3 ' im Konto ' contosoadla ' ab.</span><span class="sxs-lookup"><span data-stu-id="6e5c3-111">This command gets the specified pipeline with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="6e5c3-112">Beispiel 2: Abrufen einer Liste aller Pipelines im Konto</span><span class="sxs-lookup"><span data-stu-id="6e5c3-112">Example 2: Get a list of all pipelines in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -AccountName "contosoadla"
```

<span data-ttu-id="6e5c3-113">Dieser Befehl ruft eine Liste aller Pipelines im Konto "contosoadla" ab.</span><span class="sxs-lookup"><span data-stu-id="6e5c3-113">This command gets a list of all pipelines in the account "contosoadla"</span></span>

## <span data-ttu-id="6e5c3-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e5c3-114">PARAMETERS</span></span>

### <span data-ttu-id="6e5c3-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="6e5c3-115">-Account</span></span>
<span data-ttu-id="6e5c3-116">Name des Daten Lake Analytics-Kontonamens, unter dem die Auftragspipeline abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6e5c3-116">Name of the Data Lake Analytics account name under which want to retrieve the job pipeline.</span></span>

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

### <span data-ttu-id="6e5c3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e5c3-117">-DefaultProfile</span></span>
<span data-ttu-id="6e5c3-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6e5c3-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e5c3-119">-Pipeline-Nr</span><span class="sxs-lookup"><span data-stu-id="6e5c3-119">-PipelineId</span></span>
<span data-ttu-id="6e5c3-120">Die ID der jeweiligen Auftragspipeline, für die Informationen zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6e5c3-120">ID of the specific job pipeline to return information for.</span></span>

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

### <span data-ttu-id="6e5c3-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="6e5c3-121">-SubmittedAfter</span></span>
<span data-ttu-id="6e5c3-122">Ein optionaler Filter, der die Job-Pipeline (s) nur nach der angegebenen Zeit zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="6e5c3-122">An optional filter which returns job pipeline(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="6e5c3-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="6e5c3-123">-SubmittedBefore</span></span>
<span data-ttu-id="6e5c3-124">Ein optionaler Filter, der die Auftragspipeline (n) zurückgibt, die nur vor der angegebenen Zeit übermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="6e5c3-124">An optional filter which returns job pipeline(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="6e5c3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e5c3-125">CommonParameters</span></span>
<span data-ttu-id="6e5c3-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e5c3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e5c3-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e5c3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e5c3-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6e5c3-128">INPUTS</span></span>

### <span data-ttu-id="6e5c3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6e5c3-129">System.String</span></span>

### <span data-ttu-id="6e5c3-130">System. GUID</span><span class="sxs-lookup"><span data-stu-id="6e5c3-130">System.Guid</span></span>

### <span data-ttu-id="6e5c3-131">System. Nullable ' 1 [[System. DateTimeOffset, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6e5c3-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6e5c3-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6e5c3-132">OUTPUTS</span></span>

### <span data-ttu-id="6e5c3-133">Microsoft. Azure. Commands. DataLakeAnalytics. Models. PSJobPipelineInformation</span><span class="sxs-lookup"><span data-stu-id="6e5c3-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span></span>

## <span data-ttu-id="6e5c3-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="6e5c3-134">NOTES</span></span>

## <span data-ttu-id="6e5c3-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6e5c3-135">RELATED LINKS</span></span>
