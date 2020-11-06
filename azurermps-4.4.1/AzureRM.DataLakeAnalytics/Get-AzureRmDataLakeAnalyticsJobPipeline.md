---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobPipeline.md
ms.openlocfilehash: 838fb221952a97234c31c514aa82fc30be7e2f25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505073"
---
# <span data-ttu-id="18789-101">Get-AzureRmDataLakeAnalyticsJobPipeline</span><span class="sxs-lookup"><span data-stu-id="18789-101">Get-AzureRmDataLakeAnalyticsJobPipeline</span></span>

## <span data-ttu-id="18789-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="18789-102">SYNOPSIS</span></span>
<span data-ttu-id="18789-103">Ruft eine Data Lake Analytics-Auftragspipeline oder Pipelines ab.</span><span class="sxs-lookup"><span data-stu-id="18789-103">Gets a Data Lake Analytics Job pipeline or pipelines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18789-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="18789-104">SYNTAX</span></span>

### <span data-ttu-id="18789-105">Alle im Konto (Standard)</span><span class="sxs-lookup"><span data-stu-id="18789-105">All In Account (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJobPipeline [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18789-106">Spezifische Job-Pipeline</span><span class="sxs-lookup"><span data-stu-id="18789-106">Specific Job Pipeline</span></span>
```
Get-AzureRmDataLakeAnalyticsJobPipeline [-Account] <String> [-PipelineId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18789-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="18789-107">DESCRIPTION</span></span>
<span data-ttu-id="18789-108">Die **Get-AzureRmDataLakeAnalyticsJobPipeline-** Funktion Ruft eine angegebene Azure Data Lake Analytics-Auftragspipeline oder eine Liste von Pipelines ab.</span><span class="sxs-lookup"><span data-stu-id="18789-108">The **Get-AzureRmDataLakeAnalyticsJobPipeline** gets a specified Azure Data Lake Analytics Job pipeline or a list of pipelines.</span></span>

## <span data-ttu-id="18789-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="18789-109">EXAMPLES</span></span>

### <span data-ttu-id="18789-110">Beispiel 1: Abrufen einer angegebenen Pipeline</span><span class="sxs-lookup"><span data-stu-id="18789-110">Example 1: Get a specified pipeline</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobPipeline -Account "contosoadla" -PipelineId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="18789-111">Dieser Befehl ruft die angegebene Pipeline mit der ID ' 83cb7ad2-3523-4b82-b909-d478b0d8aea3 ' im Konto ' contosoadla ' ab.</span><span class="sxs-lookup"><span data-stu-id="18789-111">This command gets the specified pipeline with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="18789-112">Beispiel 2: Abrufen einer Liste aller Pipelines im Konto</span><span class="sxs-lookup"><span data-stu-id="18789-112">Example 2: Get a list of all pipelines in the account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobPipeline -AccountName "contosoadla"
```

<span data-ttu-id="18789-113">Dieser Befehl ruft eine Liste aller Pipelines im Konto "contosoadla" ab.</span><span class="sxs-lookup"><span data-stu-id="18789-113">This command gets a list of all pipelines in the account "contosoadla"</span></span>

## <span data-ttu-id="18789-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="18789-114">PARAMETERS</span></span>

### <span data-ttu-id="18789-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="18789-115">-Account</span></span>
<span data-ttu-id="18789-116">Name des Daten Lake Analytics-Kontonamens, unter dem die Auftragspipeline abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="18789-116">Name of the Data Lake Analytics account name under which want to retrieve the job pipeline.</span></span>

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

### <span data-ttu-id="18789-117">-Pipeline-Nr</span><span class="sxs-lookup"><span data-stu-id="18789-117">-PipelineId</span></span>
<span data-ttu-id="18789-118">Die ID der jeweiligen Auftragspipeline, für die Informationen zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="18789-118">ID of the specific job pipeline to return information for.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Specific Job Pipeline
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18789-119">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="18789-119">-SubmittedAfter</span></span>
<span data-ttu-id="18789-120">Ein optionaler Filter, der die Job-Pipeline (s) nur nach der angegebenen Zeit zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="18789-120">An optional filter which returns job pipeline(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="18789-121">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="18789-121">-SubmittedBefore</span></span>
<span data-ttu-id="18789-122">Ein optionaler Filter, der die Auftragspipeline (n) zurückgibt, die nur vor der angegebenen Zeit übermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="18789-122">An optional filter which returns job pipeline(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="18789-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18789-123">-DefaultProfile</span></span>
<span data-ttu-id="18789-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="18789-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18789-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18789-125">CommonParameters</span></span>
<span data-ttu-id="18789-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18789-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18789-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18789-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18789-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="18789-128">INPUTS</span></span>

### <span data-ttu-id="18789-129">System. String</span><span class="sxs-lookup"><span data-stu-id="18789-129">System.String</span></span>

### <span data-ttu-id="18789-130">System. GUID</span><span class="sxs-lookup"><span data-stu-id="18789-130">System.Guid</span></span>

## <span data-ttu-id="18789-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="18789-131">OUTPUTS</span></span>

### <span data-ttu-id="18789-132">Microsoft. Azure. Commands. DataLakeAnalytics. Models. PSJobPipelineInformation</span><span class="sxs-lookup"><span data-stu-id="18789-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span></span>

## <span data-ttu-id="18789-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="18789-133">NOTES</span></span>

## <span data-ttu-id="18789-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="18789-134">RELATED LINKS</span></span>

