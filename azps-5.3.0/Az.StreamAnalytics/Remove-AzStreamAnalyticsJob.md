---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
ms.openlocfilehash: 65d0e40fd522d223eed2d0462e5c66beb9e9709a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471671"
---
# <span data-ttu-id="a612f-101">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a612f-101">Remove-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="a612f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a612f-102">SYNOPSIS</span></span>
<span data-ttu-id="a612f-103">Entfernt einen Stream analytics-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="a612f-103">Removes a Stream Analytics job.</span></span>

## <span data-ttu-id="a612f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a612f-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a612f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a612f-105">DESCRIPTION</span></span>
<span data-ttu-id="a612f-106">Das **Cmdlet "Remove-AzStreamAnalyticsJob"** löscht asynchron einen bestimmten Stream analytics-Auftrag in Azure.</span><span class="sxs-lookup"><span data-stu-id="a612f-106">The **Remove-AzStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="a612f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a612f-107">EXAMPLES</span></span>

### <span data-ttu-id="a612f-108">BEISPIEL 1: Entfernen eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="a612f-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="a612f-109">Mit diesem Befehl wird der Auftrag "StreamingJob" entfernt.</span><span class="sxs-lookup"><span data-stu-id="a612f-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="a612f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a612f-110">PARAMETERS</span></span>

### <span data-ttu-id="a612f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a612f-111">-DefaultProfile</span></span>
<span data-ttu-id="a612f-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a612f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a612f-113">-Name</span><span class="sxs-lookup"><span data-stu-id="a612f-113">-Name</span></span>
<span data-ttu-id="a612f-114">Gibt den Namen des zu entfernenden Azure Stream Analytics-Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="a612f-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="a612f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a612f-115">-ResourceGroupName</span></span>
<span data-ttu-id="a612f-116">Gibt den Namen der Ressourcengruppe an, zu der der Azure Stream Analytics-Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="a612f-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="a612f-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a612f-117">-Confirm</span></span>
<span data-ttu-id="a612f-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a612f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a612f-119">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a612f-119">-WhatIf</span></span>
<span data-ttu-id="a612f-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a612f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a612f-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a612f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a612f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a612f-122">CommonParameters</span></span>
<span data-ttu-id="a612f-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a612f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a612f-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a612f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a612f-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a612f-125">INPUTS</span></span>

### <span data-ttu-id="a612f-126">System.String</span><span class="sxs-lookup"><span data-stu-id="a612f-126">System.String</span></span>

## <span data-ttu-id="a612f-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a612f-127">OUTPUTS</span></span>

### <span data-ttu-id="a612f-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a612f-128">System.Boolean</span></span>

## <span data-ttu-id="a612f-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a612f-129">NOTES</span></span>

## <span data-ttu-id="a612f-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a612f-130">RELATED LINKS</span></span>

[<span data-ttu-id="a612f-131">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a612f-131">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="a612f-132">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a612f-132">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="a612f-133">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a612f-133">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="a612f-134">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a612f-134">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


