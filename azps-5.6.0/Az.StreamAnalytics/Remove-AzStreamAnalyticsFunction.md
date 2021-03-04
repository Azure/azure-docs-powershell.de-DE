---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/remove-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 1a500f883b6896e91767f0f7d560ee28e4bfc9f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929520"
---
# <span data-ttu-id="6964d-101">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="6964d-101">Remove-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="6964d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6964d-102">SYNOPSIS</span></span>
<span data-ttu-id="6964d-103">Löscht eine Funktion aus einem Stream Analytics-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="6964d-103">Deletes a function from a Stream Analytics job.</span></span>

## <span data-ttu-id="6964d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6964d-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6964d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6964d-105">DESCRIPTION</span></span>
<span data-ttu-id="6964d-106">Das **Cmdlet Remove-AzStreamAnalyticsFunction** löscht eine Funktion asynchron aus einem Azure Stream Analytics-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="6964d-106">The **Remove-AzStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="6964d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6964d-107">EXAMPLES</span></span>

### <span data-ttu-id="6964d-108">Beispiel 1: Entfernen einer Stream Analytics-Funktion</span><span class="sxs-lookup"><span data-stu-id="6964d-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="6964d-109">Mit diesem Befehl wird die Funktion "ScoreTweet" aus dem Auftrag mit dem Namen StreamJob22 entfernt.</span><span class="sxs-lookup"><span data-stu-id="6964d-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="6964d-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6964d-110">PARAMETERS</span></span>

### <span data-ttu-id="6964d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6964d-111">-DefaultProfile</span></span>
<span data-ttu-id="6964d-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6964d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6964d-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="6964d-113">-JobName</span></span>
<span data-ttu-id="6964d-114">Gibt den Namen des Datenstromanalyseauftrags an, zu dem eine Funktion gehört.</span><span class="sxs-lookup"><span data-stu-id="6964d-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="6964d-115">Dieses Cmdlet entfernt eine Funktion aus dem Auftrag, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="6964d-115">This cmdlet removes a function from the job that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6964d-116">-Name</span><span class="sxs-lookup"><span data-stu-id="6964d-116">-Name</span></span>
<span data-ttu-id="6964d-117">Gibt den Namen der Stream Analytics-Funktion an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="6964d-117">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6964d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6964d-118">-ResourceGroupName</span></span>
<span data-ttu-id="6964d-119">Gibt den Namen der Ressourcengruppe an, zu der eine Stream Analytics-Funktion gehört.</span><span class="sxs-lookup"><span data-stu-id="6964d-119">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="6964d-120">Dieses Cmdlet löscht eine Funktion in der Ressourcengruppe, die von diesem Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6964d-120">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6964d-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6964d-121">-Confirm</span></span>
<span data-ttu-id="6964d-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6964d-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6964d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6964d-123">-WhatIf</span></span>
<span data-ttu-id="6964d-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6964d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6964d-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6964d-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6964d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6964d-126">CommonParameters</span></span>
<span data-ttu-id="6964d-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6964d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6964d-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6964d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6964d-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6964d-129">INPUTS</span></span>

### <span data-ttu-id="6964d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6964d-130">System.String</span></span>

## <span data-ttu-id="6964d-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6964d-131">OUTPUTS</span></span>

### <span data-ttu-id="6964d-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6964d-132">System.Boolean</span></span>

## <span data-ttu-id="6964d-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6964d-133">NOTES</span></span>

## <span data-ttu-id="6964d-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6964d-134">RELATED LINKS</span></span>

[<span data-ttu-id="6964d-135">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="6964d-135">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="6964d-136">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="6964d-136">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="6964d-137">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="6964d-137">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


