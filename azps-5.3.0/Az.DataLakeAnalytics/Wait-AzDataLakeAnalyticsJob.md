---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/wait-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 047d0c7c9b141f10ee3f1be2ba1e739960f2e5bc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470500"
---
# <span data-ttu-id="73510-101">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="73510-101">Wait-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="73510-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73510-102">SYNOPSIS</span></span>
<span data-ttu-id="73510-103">Wartet auf den Abschluss eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="73510-103">Waits for a job to complete.</span></span>

## <span data-ttu-id="73510-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="73510-104">SYNTAX</span></span>

```
Wait-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73510-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="73510-105">DESCRIPTION</span></span>
<span data-ttu-id="73510-106">Das **Cmdlet "Wait-AzDataLakeAnalyticsJob"** wartet auf den Abschluss eines Azure Data Lake Analytics-Auftrags.</span><span class="sxs-lookup"><span data-stu-id="73510-106">The **Wait-AzDataLakeAnalyticsJob** cmdlet waits for an Azure Data Lake Analytics job to complete.</span></span>

## <span data-ttu-id="73510-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="73510-107">EXAMPLES</span></span>

### <span data-ttu-id="73510-108">Beispiel 1: Warten auf den Abschluss eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="73510-108">Example 1: Wait for a job to complete</span></span>
```
PS C:\>Wait-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="73510-109">Der folgende Befehl wartet auf den Abschluss des Auftrags mit der angegebenen ID.</span><span class="sxs-lookup"><span data-stu-id="73510-109">The following command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="73510-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73510-110">PARAMETERS</span></span>

### <span data-ttu-id="73510-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="73510-111">-Account</span></span>
<span data-ttu-id="73510-112">Gibt den Namen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="73510-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="73510-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73510-113">-DefaultProfile</span></span>
<span data-ttu-id="73510-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="73510-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="73510-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="73510-115">-JobId</span></span>
<span data-ttu-id="73510-116">Gibt die ID des Auftrags an, für den gewartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="73510-116">Specifies the ID of the job for which to wait.</span></span>

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

### <span data-ttu-id="73510-117">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="73510-117">-TimeoutInSeconds</span></span>
<span data-ttu-id="73510-118">Gibt die Anzahl der Sekunden an, die vor dem Beenden des Wartevorgangs gewartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="73510-118">Specifies the number of seconds to wait before exiting the wait operation.</span></span>

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

### <span data-ttu-id="73510-119">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="73510-119">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="73510-120">Geben Sie die Anzahl von Sekunden an, die zwischen den einzelnen Überprüfungen des Auftragsstatus verstrichen sind.</span><span class="sxs-lookup"><span data-stu-id="73510-120">Specify the number of seconds that elapse between each check of the job state.</span></span>

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

### <span data-ttu-id="73510-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73510-121">CommonParameters</span></span>
<span data-ttu-id="73510-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73510-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73510-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73510-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73510-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="73510-124">INPUTS</span></span>

### <span data-ttu-id="73510-125">System.String</span><span class="sxs-lookup"><span data-stu-id="73510-125">System.String</span></span>

### <span data-ttu-id="73510-126">System.Guid</span><span class="sxs-lookup"><span data-stu-id="73510-126">System.Guid</span></span>

### <span data-ttu-id="73510-127">System.Int32</span><span class="sxs-lookup"><span data-stu-id="73510-127">System.Int32</span></span>

## <span data-ttu-id="73510-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="73510-128">OUTPUTS</span></span>

### <span data-ttu-id="73510-129">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span><span class="sxs-lookup"><span data-stu-id="73510-129">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="73510-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="73510-130">NOTES</span></span>

## <span data-ttu-id="73510-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="73510-131">RELATED LINKS</span></span>

[<span data-ttu-id="73510-132">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="73510-132">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="73510-133">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="73510-133">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="73510-134">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="73510-134">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)


