---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
ms.openlocfilehash: 26808bd3db72f8618505045b2b20f6d0b56806da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929547"
---
# <span data-ttu-id="5ad6f-101">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5ad6f-101">Get-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="5ad6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ad6f-102">SYNOPSIS</span></span>
<span data-ttu-id="5ad6f-103">Ruft Daten zu Stream Analytics-Aufträgen ab.</span><span class="sxs-lookup"><span data-stu-id="5ad6f-103">Gets Stream Analytics jobs information.</span></span>

## <span data-ttu-id="5ad6f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ad6f-104">SYNTAX</span></span>

### <span data-ttu-id="5ad6f-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5ad6f-105">ByResourceGroup</span></span>
```
Get-AzStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ad6f-106">BySubscription</span><span class="sxs-lookup"><span data-stu-id="5ad6f-106">BySubscription</span></span>
```
Get-AzStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ad6f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5ad6f-107">DESCRIPTION</span></span>
<span data-ttu-id="5ad6f-108">Das **Get-AzStreamAnalyticsJob-Cmdlet** listet alle im Azure-Abonnement oder einer angegebenen Ressourcengruppe definierten Stream Analytics-Aufträge auf oder ruft Auftragsinformationen zu einem bestimmten Auftrag innerhalb einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="5ad6f-108">The **Get-AzStreamAnalyticsJob** cmdlet lists all Stream Analytics jobs defined in the Azure subscription or specified resource group or gets job information about a specific job within a resource group.</span></span>

## <span data-ttu-id="5ad6f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5ad6f-109">EXAMPLES</span></span>

### <span data-ttu-id="5ad6f-110">BEISPIEL 1: Informationen zu allen Aufträgen in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="5ad6f-110">EXAMPLE 1: Get information about all jobs in a subscription</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob
```

<span data-ttu-id="5ad6f-111">Dieser Befehl gibt Informationen zu allen Stream Analytics-Aufträgen im Azure-Abonnement zurück.</span><span class="sxs-lookup"><span data-stu-id="5ad6f-111">This command returns information about all the Stream Analytics jobs in the Azure subscription.</span></span>

### <span data-ttu-id="5ad6f-112">BEISPIEL 2: Informationen zu allen Aufträgen in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="5ad6f-112">EXAMPLE 2: Get information about all jobs in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

<span data-ttu-id="5ad6f-113">Dieser Befehl gibt Informationen zu allen Stream Analytics-Aufträgen in der Ressourcengruppe StreamAnalytics-Default-West-US zurück.</span><span class="sxs-lookup"><span data-stu-id="5ad6f-113">This command returns information about all the Stream Analytics jobs in the resource group StreamAnalytics-Default-West-US.</span></span>

### <span data-ttu-id="5ad6f-114">BEISPIEL 3: Informationen zu einem bestimmten Auftrag in einer Ressourcengruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="5ad6f-114">EXAMPLE 3: Get information about a specific job in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="5ad6f-115">Dieser Befehl gibt Informationen zum Stream Analytics-Auftrag StreamingJob in der Ressourcengruppe StreamAnalytics-Default-West-US zurück.</span><span class="sxs-lookup"><span data-stu-id="5ad6f-115">This command returns information about the Stream Analytics job StreamingJob in the resource group StreamAnalytics-Default-West-US.</span></span>

## <span data-ttu-id="5ad6f-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5ad6f-116">PARAMETERS</span></span>

### <span data-ttu-id="5ad6f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ad6f-117">-DefaultProfile</span></span>
<span data-ttu-id="5ad6f-118">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5ad6f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ad6f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5ad6f-119">-Name</span></span>
<span data-ttu-id="5ad6f-120">Gibt den Namen des abzurufenden Azure Stream Analytics-Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="5ad6f-120">Specifies the name of the Azure Stream Analytics job to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ad6f-121">-NoExpand</span><span class="sxs-lookup"><span data-stu-id="5ad6f-121">-NoExpand</span></span>
<span data-ttu-id="5ad6f-122">Gibt an, dass das Cmdlet den Azure Stream Analytics-Auftrag abruft, aber keine Informationen zu seinen Eingaben, Ausgaben und Transformationen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="5ad6f-122">Indicates the cmdlet will retrieve the Azure Stream Analytics job, but not return information on its inputs, outputs, and transformation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ad6f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ad6f-123">-ResourceGroupName</span></span>
<span data-ttu-id="5ad6f-124">Gibt den Namen der Ressourcengruppe an, zu der der Azure Stream Analytics-Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="5ad6f-124">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ad6f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ad6f-125">CommonParameters</span></span>
<span data-ttu-id="5ad6f-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ad6f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ad6f-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ad6f-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ad6f-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5ad6f-128">INPUTS</span></span>

### <span data-ttu-id="5ad6f-129">System.String</span><span class="sxs-lookup"><span data-stu-id="5ad6f-129">System.String</span></span>

### <span data-ttu-id="5ad6f-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5ad6f-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5ad6f-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5ad6f-131">OUTPUTS</span></span>

### <span data-ttu-id="5ad6f-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span><span class="sxs-lookup"><span data-stu-id="5ad6f-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="5ad6f-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5ad6f-133">NOTES</span></span>

## <span data-ttu-id="5ad6f-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5ad6f-134">RELATED LINKS</span></span>

[<span data-ttu-id="5ad6f-135">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5ad6f-135">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="5ad6f-136">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5ad6f-136">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="5ad6f-137">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5ad6f-137">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="5ad6f-138">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5ad6f-138">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


