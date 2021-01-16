---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
ms.openlocfilehash: 826089ca0db48e89138e9df78f0aa483b110ba30
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366427"
---
# <span data-ttu-id="4fa27-101">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4fa27-101">Get-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="4fa27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fa27-102">SYNOPSIS</span></span>
<span data-ttu-id="4fa27-103">Ruft Daten zu Stream Analytics-Aufträgen ab.</span><span class="sxs-lookup"><span data-stu-id="4fa27-103">Gets Stream Analytics jobs information.</span></span>

## <span data-ttu-id="4fa27-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4fa27-104">SYNTAX</span></span>

### <span data-ttu-id="4fa27-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4fa27-105">ByResourceGroup</span></span>
```
Get-AzStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fa27-106">BySubscription</span><span class="sxs-lookup"><span data-stu-id="4fa27-106">BySubscription</span></span>
```
Get-AzStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fa27-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4fa27-107">DESCRIPTION</span></span>
<span data-ttu-id="4fa27-108">Das **Cmdlet "Get-AzStreamAnalyticsJob"** listet alle Stream Analytics-Aufträge auf, die im Abonnement von Azure oder einer angegebenen Ressourcengruppe definiert wurden, oder ruft Auftragsinformationen zu einem bestimmten Auftrag innerhalb einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="4fa27-108">The **Get-AzStreamAnalyticsJob** cmdlet lists all Stream Analytics jobs defined in the Azure subscription or specified resource group or gets job information about a specific job within a resource group.</span></span>

## <span data-ttu-id="4fa27-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4fa27-109">EXAMPLES</span></span>

### <span data-ttu-id="4fa27-110">BEISPIEL 1: Erhalten von Informationen zu allen Aufträgen in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="4fa27-110">EXAMPLE 1: Get information about all jobs in a subscription</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob
```

<span data-ttu-id="4fa27-111">Dieser Befehl gibt Informationen zu allen Stream Analytics-Aufträgen im Abonnement von Azure zurück.</span><span class="sxs-lookup"><span data-stu-id="4fa27-111">This command returns information about all the Stream Analytics jobs in the Azure subscription.</span></span>

### <span data-ttu-id="4fa27-112">BEISPIEL 2: Erhalten von Informationen zu allen Aufträgen in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="4fa27-112">EXAMPLE 2: Get information about all jobs in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

<span data-ttu-id="4fa27-113">Dieser Befehl gibt Informationen zu allen Stream Analytics-Aufträgen in der Ressourcengruppe "StreamAnalytics-Default-West-US" zurück.</span><span class="sxs-lookup"><span data-stu-id="4fa27-113">This command returns information about all the Stream Analytics jobs in the resource group StreamAnalytics-Default-West-US.</span></span>

### <span data-ttu-id="4fa27-114">BEISPIEL 3: Erhalten von Informationen zu einem bestimmten Auftrag in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="4fa27-114">EXAMPLE 3: Get information about a specific job in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="4fa27-115">Dieser Befehl gibt Informationen über den Stream Analytics-Auftrag "StreamingJob" in der Ressourcengruppe "StreamAnalytics-Default-West-US" zurück.</span><span class="sxs-lookup"><span data-stu-id="4fa27-115">This command returns information about the Stream Analytics job StreamingJob in the resource group StreamAnalytics-Default-West-US.</span></span>

## <span data-ttu-id="4fa27-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4fa27-116">PARAMETERS</span></span>

### <span data-ttu-id="4fa27-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fa27-117">-DefaultProfile</span></span>
<span data-ttu-id="4fa27-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4fa27-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fa27-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4fa27-119">-Name</span></span>
<span data-ttu-id="4fa27-120">Gibt den Namen des abzurufenden Azure Stream Analytics-Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="4fa27-120">Specifies the name of the Azure Stream Analytics job to retrieve.</span></span>

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

### <span data-ttu-id="4fa27-121">-NoExpand</span><span class="sxs-lookup"><span data-stu-id="4fa27-121">-NoExpand</span></span>
<span data-ttu-id="4fa27-122">Gibt an, dass das Cmdlet den Azure Stream Analytics-Auftrag abruft, aber keine Informationen zu seinen Eingaben, Ausgaben und Transformationen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4fa27-122">Indicates the cmdlet will retrieve the Azure Stream Analytics job, but not return information on its inputs, outputs, and transformation.</span></span>

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

### <span data-ttu-id="4fa27-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fa27-123">-ResourceGroupName</span></span>
<span data-ttu-id="4fa27-124">Gibt den Namen der Ressourcengruppe an, zu der der Azure Stream Analytics-Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="4fa27-124">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="4fa27-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fa27-125">CommonParameters</span></span>
<span data-ttu-id="4fa27-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fa27-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fa27-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fa27-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fa27-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4fa27-128">INPUTS</span></span>

### <span data-ttu-id="4fa27-129">System.String</span><span class="sxs-lookup"><span data-stu-id="4fa27-129">System.String</span></span>

### <span data-ttu-id="4fa27-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4fa27-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4fa27-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4fa27-131">OUTPUTS</span></span>

### <span data-ttu-id="4fa27-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span><span class="sxs-lookup"><span data-stu-id="4fa27-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="4fa27-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4fa27-133">NOTES</span></span>

## <span data-ttu-id="4fa27-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4fa27-134">RELATED LINKS</span></span>

[<span data-ttu-id="4fa27-135">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4fa27-135">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="4fa27-136">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4fa27-136">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="4fa27-137">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4fa27-137">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="4fa27-138">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4fa27-138">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


