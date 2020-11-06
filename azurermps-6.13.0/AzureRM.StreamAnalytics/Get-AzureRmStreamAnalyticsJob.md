---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: eef326688a81481d235fb85281739f0361a6233c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93475897"
---
# <span data-ttu-id="2eded-101">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2eded-101">Get-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="2eded-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2eded-102">SYNOPSIS</span></span>
<span data-ttu-id="2eded-103">Ruft Informationen zu Datenstrom Analyse Aufträgen ab.</span><span class="sxs-lookup"><span data-stu-id="2eded-103">Gets Stream Analytics jobs information.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2eded-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2eded-104">SYNTAX</span></span>

### <span data-ttu-id="2eded-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2eded-105">ByResourceGroup</span></span>
```
Get-AzureRmStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2eded-106">BySubscription</span><span class="sxs-lookup"><span data-stu-id="2eded-106">BySubscription</span></span>
```
Get-AzureRmStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2eded-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2eded-107">DESCRIPTION</span></span>
<span data-ttu-id="2eded-108">Das Cmdlet " **Get-AzureRmStreamAnalyticsJob** " listet alle Datenstrom Analyse Aufträge auf, die im Azure-Abonnement oder der angegebenen Ressourcengruppe definiert sind, oder es werden Auftragsinformationen zu einem bestimmten Auftrag innerhalb einer Ressourcengruppe abgerufen.</span><span class="sxs-lookup"><span data-stu-id="2eded-108">The **Get-AzureRmStreamAnalyticsJob** cmdlet lists all Stream Analytics jobs defined in the Azure subscription or specified resource group or gets job information about a specific job within a resource group.</span></span>

## <span data-ttu-id="2eded-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2eded-109">EXAMPLES</span></span>

### <span data-ttu-id="2eded-110">Beispiel 1: Abrufen von Informationen zu allen Aufträgen in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="2eded-110">EXAMPLE 1: Get information about all jobs in a subscription</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob
```

<span data-ttu-id="2eded-111">Dieser Befehl gibt Informationen zu allen Datenstrom Analyse Aufträgen im Azure-Abonnement zurück.</span><span class="sxs-lookup"><span data-stu-id="2eded-111">This command returns information about all the Stream Analytics jobs in the Azure subscription.</span></span>

### <span data-ttu-id="2eded-112">Beispiel 2: Abrufen von Informationen zu allen Aufträgen in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="2eded-112">EXAMPLE 2: Get information about all jobs in a resource group</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

<span data-ttu-id="2eded-113">Dieser Befehl gibt Informationen zu allen Datenstrom Analyse Aufträgen in der Ressourcengruppe StreamAnalytics-default-West-US zurück.</span><span class="sxs-lookup"><span data-stu-id="2eded-113">This command returns information about all the Stream Analytics jobs in the resource group StreamAnalytics-Default-West-US.</span></span>

### <span data-ttu-id="2eded-114">Beispiel 3: Abrufen von Informationen zu einem bestimmten Job in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="2eded-114">EXAMPLE 3: Get information about a specific job in a resource group</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="2eded-115">Dieser Befehl gibt Informationen zum Datenstrom Analyse-Auftrags StreamingJob in der Ressourcengruppe StreamAnalytics-default-West-US zurück.</span><span class="sxs-lookup"><span data-stu-id="2eded-115">This command returns information about the Stream Analytics job StreamingJob in the resource group StreamAnalytics-Default-West-US.</span></span>

## <span data-ttu-id="2eded-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="2eded-116">PARAMETERS</span></span>

### <span data-ttu-id="2eded-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eded-117">-DefaultProfile</span></span>
<span data-ttu-id="2eded-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2eded-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2eded-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2eded-119">-Name</span></span>
<span data-ttu-id="2eded-120">Gibt den Namen des abzurufenden Azure-Stream-Analyse Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="2eded-120">Specifies the name of the Azure Stream Analytics job to retrieve.</span></span>

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

### <span data-ttu-id="2eded-121">-NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="2eded-121">-NoExpand</span></span>
<span data-ttu-id="2eded-122">Gibt an, dass das Cmdlet den Azure-Stream-Analyse Auftrag abruft, aber keine Informationen zu den Eingaben, Ausgaben und der Transformation zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="2eded-122">Indicates the cmdlet will retrieve the Azure Stream Analytics job, but not return information on its inputs, outputs, and transformation.</span></span>

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

### <span data-ttu-id="2eded-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2eded-123">-ResourceGroupName</span></span>
<span data-ttu-id="2eded-124">Gibt den Namen der Ressourcengruppe an, zu der der Azure-Stream-Analyse Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="2eded-124">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="2eded-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eded-125">CommonParameters</span></span>
<span data-ttu-id="2eded-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eded-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eded-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2eded-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eded-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2eded-128">INPUTS</span></span>

### <span data-ttu-id="2eded-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2eded-129">System.String</span></span>

### <span data-ttu-id="2eded-130">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="2eded-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2eded-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2eded-131">OUTPUTS</span></span>

### <span data-ttu-id="2eded-132">Microsoft. Azure. Commands. StreamAnalytics. Models. PSJob</span><span class="sxs-lookup"><span data-stu-id="2eded-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="2eded-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="2eded-133">NOTES</span></span>

## <span data-ttu-id="2eded-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2eded-134">RELATED LINKS</span></span>

[<span data-ttu-id="2eded-135">Neu – AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2eded-135">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="2eded-136">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2eded-136">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="2eded-137">Anfang-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2eded-137">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="2eded-138">Stopp-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2eded-138">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


