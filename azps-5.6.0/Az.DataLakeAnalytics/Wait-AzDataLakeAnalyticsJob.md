---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/wait-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: f735dc3f213069c1ecf5bbae9d1d5cf24dda98a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920592"
---
# <span data-ttu-id="20a59-101">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="20a59-101">Wait-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="20a59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20a59-102">SYNOPSIS</span></span>
<span data-ttu-id="20a59-103">Wartet, bis ein Auftrag abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="20a59-103">Waits for a job to complete.</span></span>

## <span data-ttu-id="20a59-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20a59-104">SYNTAX</span></span>

```
Wait-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20a59-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="20a59-105">DESCRIPTION</span></span>
<span data-ttu-id="20a59-106">Das **Cmdlet Wait-AzDataLakeAnalyticsJob** wartet auf den Abschluss eines Azure Data Lake Analytics-Auftrags.</span><span class="sxs-lookup"><span data-stu-id="20a59-106">The **Wait-AzDataLakeAnalyticsJob** cmdlet waits for an Azure Data Lake Analytics job to complete.</span></span>

## <span data-ttu-id="20a59-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="20a59-107">EXAMPLES</span></span>

### <span data-ttu-id="20a59-108">Beispiel 1: Warten, bis ein Auftrag abgeschlossen ist</span><span class="sxs-lookup"><span data-stu-id="20a59-108">Example 1: Wait for a job to complete</span></span>
```
PS C:\>Wait-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="20a59-109">Der folgende Befehl wartet, bis der Auftrag mit der angegebenen ID abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="20a59-109">The following command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="20a59-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="20a59-110">PARAMETERS</span></span>

### <span data-ttu-id="20a59-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="20a59-111">-Account</span></span>
<span data-ttu-id="20a59-112">Gibt den Namen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="20a59-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="20a59-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20a59-113">-DefaultProfile</span></span>
<span data-ttu-id="20a59-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="20a59-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20a59-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="20a59-115">-JobId</span></span>
<span data-ttu-id="20a59-116">Gibt die ID des Auftrags an, für den gewartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="20a59-116">Specifies the ID of the job for which to wait.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20a59-117">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="20a59-117">-TimeoutInSeconds</span></span>
<span data-ttu-id="20a59-118">Gibt die Anzahl der Sekunden an, die vor dem Beenden des Wartevorgangs gewartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="20a59-118">Specifies the number of seconds to wait before exiting the wait operation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20a59-119">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="20a59-119">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="20a59-120">Geben Sie die Anzahl der Sekunden an, die zwischen jeder Überprüfung des Auftragszustands verstrichen sind.</span><span class="sxs-lookup"><span data-stu-id="20a59-120">Specify the number of seconds that elapse between each check of the job state.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20a59-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20a59-121">CommonParameters</span></span>
<span data-ttu-id="20a59-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20a59-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20a59-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20a59-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20a59-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="20a59-124">INPUTS</span></span>

### <span data-ttu-id="20a59-125">System.String</span><span class="sxs-lookup"><span data-stu-id="20a59-125">System.String</span></span>

### <span data-ttu-id="20a59-126">System.Guid</span><span class="sxs-lookup"><span data-stu-id="20a59-126">System.Guid</span></span>

### <span data-ttu-id="20a59-127">System.Int32</span><span class="sxs-lookup"><span data-stu-id="20a59-127">System.Int32</span></span>

## <span data-ttu-id="20a59-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="20a59-128">OUTPUTS</span></span>

### <span data-ttu-id="20a59-129">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span><span class="sxs-lookup"><span data-stu-id="20a59-129">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="20a59-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="20a59-130">NOTES</span></span>

## <span data-ttu-id="20a59-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="20a59-131">RELATED LINKS</span></span>

[<span data-ttu-id="20a59-132">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="20a59-132">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="20a59-133">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="20a59-133">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="20a59-134">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="20a59-134">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)


