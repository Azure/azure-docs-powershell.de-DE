---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/remove-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
ms.openlocfilehash: 183aa9dd5cc7da6e0d86c1fa1018bcfe405c0f7e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929496"
---
# <span data-ttu-id="b010b-101">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b010b-101">Remove-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="b010b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b010b-102">SYNOPSIS</span></span>
<span data-ttu-id="b010b-103">Entfernt einen Stream Analytics-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="b010b-103">Removes a Stream Analytics job.</span></span>

## <span data-ttu-id="b010b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b010b-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b010b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b010b-105">DESCRIPTION</span></span>
<span data-ttu-id="b010b-106">Das **Cmdlet Remove-AzStreamAnalyticsJob** löscht asynchron einen bestimmten Stream Analytics-Auftrag in Azure.</span><span class="sxs-lookup"><span data-stu-id="b010b-106">The **Remove-AzStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="b010b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b010b-107">EXAMPLES</span></span>

### <span data-ttu-id="b010b-108">BEISPIEL 1: Entfernen eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="b010b-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="b010b-109">Mit diesem Befehl wird der Auftrag StreamingJob entfernt.</span><span class="sxs-lookup"><span data-stu-id="b010b-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="b010b-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b010b-110">PARAMETERS</span></span>

### <span data-ttu-id="b010b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b010b-111">-DefaultProfile</span></span>
<span data-ttu-id="b010b-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b010b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b010b-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b010b-113">-Name</span></span>
<span data-ttu-id="b010b-114">Gibt den Namen des zu entfernenden Azure Stream Analytics-Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="b010b-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="b010b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b010b-115">-ResourceGroupName</span></span>
<span data-ttu-id="b010b-116">Gibt den Namen der Ressourcengruppe an, zu der der Azure Stream Analytics-Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="b010b-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="b010b-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b010b-117">-Confirm</span></span>
<span data-ttu-id="b010b-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b010b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b010b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b010b-119">-WhatIf</span></span>
<span data-ttu-id="b010b-120">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b010b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b010b-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b010b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b010b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b010b-122">CommonParameters</span></span>
<span data-ttu-id="b010b-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b010b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b010b-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b010b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b010b-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b010b-125">INPUTS</span></span>

### <span data-ttu-id="b010b-126">System.String</span><span class="sxs-lookup"><span data-stu-id="b010b-126">System.String</span></span>

## <span data-ttu-id="b010b-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b010b-127">OUTPUTS</span></span>

### <span data-ttu-id="b010b-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b010b-128">System.Boolean</span></span>

## <span data-ttu-id="b010b-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b010b-129">NOTES</span></span>

## <span data-ttu-id="b010b-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b010b-130">RELATED LINKS</span></span>

[<span data-ttu-id="b010b-131">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b010b-131">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="b010b-132">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b010b-132">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="b010b-133">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b010b-133">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="b010b-134">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b010b-134">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


