---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
ms.openlocfilehash: 826089ca0db48e89138e9df78f0aa483b110ba30
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471679"
---
# <span data-ttu-id="5459a-101">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5459a-101">Get-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="5459a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5459a-102">SYNOPSIS</span></span>
<span data-ttu-id="5459a-103">Ruft Daten zu Stream Analytics-Aufträgen ab.</span><span class="sxs-lookup"><span data-stu-id="5459a-103">Gets Stream Analytics jobs information.</span></span>

## <span data-ttu-id="5459a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5459a-104">SYNTAX</span></span>

### <span data-ttu-id="5459a-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5459a-105">ByResourceGroup</span></span>
```
Get-AzStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5459a-106">BySubscription</span><span class="sxs-lookup"><span data-stu-id="5459a-106">BySubscription</span></span>
```
Get-AzStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5459a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5459a-107">DESCRIPTION</span></span>
<span data-ttu-id="5459a-108">Das **Cmdlet "Get-AzStreamAnalyticsJob"** listet alle Stream Analytics-Aufträge auf, die im Abonnement von Azure oder einer bestimmten Ressourcengruppe definiert wurden, oder ruft Auftragsinformationen zu einem bestimmten Auftrag innerhalb einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="5459a-108">The **Get-AzStreamAnalyticsJob** cmdlet lists all Stream Analytics jobs defined in the Azure subscription or specified resource group or gets job information about a specific job within a resource group.</span></span>

## <span data-ttu-id="5459a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5459a-109">EXAMPLES</span></span>

### <span data-ttu-id="5459a-110">BEISPIEL 1: Informationen zu allen Aufträgen in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="5459a-110">EXAMPLE 1: Get information about all jobs in a subscription</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob
```

<span data-ttu-id="5459a-111">Dieser Befehl gibt Informationen zu allen Stream Analytics-Aufträgen im Abonnement von Azure zurück.</span><span class="sxs-lookup"><span data-stu-id="5459a-111">This command returns information about all the Stream Analytics jobs in the Azure subscription.</span></span>

### <span data-ttu-id="5459a-112">BEISPIEL 2: Erhalten von Informationen zu allen Aufträgen in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="5459a-112">EXAMPLE 2: Get information about all jobs in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

<span data-ttu-id="5459a-113">Dieser Befehl gibt Informationen zu allen Stream Analytics-Aufträgen in der Ressourcengruppe "StreamAnalytics-Default-West-US" zurück.</span><span class="sxs-lookup"><span data-stu-id="5459a-113">This command returns information about all the Stream Analytics jobs in the resource group StreamAnalytics-Default-West-US.</span></span>

### <span data-ttu-id="5459a-114">BEISPIEL 3: Erhalten von Informationen zu einem bestimmten Auftrag in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="5459a-114">EXAMPLE 3: Get information about a specific job in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="5459a-115">Dieser Befehl gibt Informationen über den Stream Analytics-Auftrag "StreamingJob" in der Ressourcengruppe "StreamAnalytics-Default-West-US" zurück.</span><span class="sxs-lookup"><span data-stu-id="5459a-115">This command returns information about the Stream Analytics job StreamingJob in the resource group StreamAnalytics-Default-West-US.</span></span>

## <span data-ttu-id="5459a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5459a-116">PARAMETERS</span></span>

### <span data-ttu-id="5459a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5459a-117">-DefaultProfile</span></span>
<span data-ttu-id="5459a-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5459a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5459a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5459a-119">-Name</span></span>
<span data-ttu-id="5459a-120">Gibt den Namen des abzurufenden Azure Stream Analytics-Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="5459a-120">Specifies the name of the Azure Stream Analytics job to retrieve.</span></span>

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

### <span data-ttu-id="5459a-121">-NoExpand</span><span class="sxs-lookup"><span data-stu-id="5459a-121">-NoExpand</span></span>
<span data-ttu-id="5459a-122">Gibt an, dass das Cmdlet den Azure Stream Analytics-Auftrag abruft, aber keine Informationen zu seinen Eingaben, Ausgaben und Transformationen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="5459a-122">Indicates the cmdlet will retrieve the Azure Stream Analytics job, but not return information on its inputs, outputs, and transformation.</span></span>

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

### <span data-ttu-id="5459a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5459a-123">-ResourceGroupName</span></span>
<span data-ttu-id="5459a-124">Gibt den Namen der Ressourcengruppe an, zu der der Azure Stream Analytics-Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="5459a-124">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="5459a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5459a-125">CommonParameters</span></span>
<span data-ttu-id="5459a-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5459a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5459a-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5459a-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5459a-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5459a-128">INPUTS</span></span>

### <span data-ttu-id="5459a-129">System.String</span><span class="sxs-lookup"><span data-stu-id="5459a-129">System.String</span></span>

### <span data-ttu-id="5459a-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5459a-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5459a-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5459a-131">OUTPUTS</span></span>

### <span data-ttu-id="5459a-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span><span class="sxs-lookup"><span data-stu-id="5459a-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="5459a-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5459a-133">NOTES</span></span>

## <span data-ttu-id="5459a-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5459a-134">RELATED LINKS</span></span>

[<span data-ttu-id="5459a-135">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5459a-135">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="5459a-136">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5459a-136">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="5459a-137">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5459a-137">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="5459a-138">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="5459a-138">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


