---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/move-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
ms.openlocfilehash: c127ff40690658a98f9d0f0fa670cddfca123f89
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305912"
---
# <span data-ttu-id="fde04-101">Move-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="fde04-101">Move-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="fde04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fde04-102">SYNOPSIS</span></span>
<span data-ttu-id="fde04-103">Verschiebt einen Verpflichtungsverbund von einem Verpflichtungsplan zu einem anderen.</span><span class="sxs-lookup"><span data-stu-id="fde04-103">Moves a commitment association from one commitment plan to another.</span></span>

## <span data-ttu-id="fde04-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fde04-104">SYNTAX</span></span>

```
Move-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fde04-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fde04-105">DESCRIPTION</span></span>
<span data-ttu-id="fde04-106">Verschiebt eine Verpflichtungszuordnungsressource aus ihrem übergeordneten Verpflichtungsplan in einen anderen Verpflichtungsplan.</span><span class="sxs-lookup"><span data-stu-id="fde04-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="fde04-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fde04-107">EXAMPLES</span></span>

### <span data-ttu-id="fde04-108">Beispiel 1: Verschieben einer Verpflichtungs zuordnung</span><span class="sxs-lookup"><span data-stu-id="fde04-108">Example 1: Move a commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="fde04-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fde04-109">PARAMETERS</span></span>

### <span data-ttu-id="fde04-110">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="fde04-110">-CommitmentPlanName</span></span>
<span data-ttu-id="fde04-111">Der Name des Azure ML-Verpflichtungsplans.</span><span class="sxs-lookup"><span data-stu-id="fde04-111">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fde04-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fde04-112">-DefaultProfile</span></span>
<span data-ttu-id="fde04-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="fde04-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fde04-114">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="fde04-114">-DestinationPlanId</span></span>
<span data-ttu-id="fde04-115">Die Azure-Ressourcen-ID des Azure ML-Ziel-Verpflichtungsplans.</span><span class="sxs-lookup"><span data-stu-id="fde04-115">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fde04-116">-Name</span><span class="sxs-lookup"><span data-stu-id="fde04-116">-Name</span></span>
<span data-ttu-id="fde04-117">Der Name der Azure ML-Verpflichtungs zuordnung.</span><span class="sxs-lookup"><span data-stu-id="fde04-117">The name of the Azure ML commitment association.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fde04-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fde04-118">-ResourceGroupName</span></span>
<span data-ttu-id="fde04-119">Der Name der Ressourcengruppe für die Azure ML-Verpflichtungszuordnung.</span><span class="sxs-lookup"><span data-stu-id="fde04-119">The name of the resource group for the Azure ML commitment association.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fde04-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fde04-120">-Confirm</span></span>
<span data-ttu-id="fde04-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fde04-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fde04-122">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fde04-122">-WhatIf</span></span>
<span data-ttu-id="fde04-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fde04-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fde04-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fde04-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fde04-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fde04-125">CommonParameters</span></span>
<span data-ttu-id="fde04-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fde04-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fde04-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fde04-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fde04-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fde04-128">INPUTS</span></span>

### <span data-ttu-id="fde04-129">Keine</span><span class="sxs-lookup"><span data-stu-id="fde04-129">None</span></span>

## <span data-ttu-id="fde04-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fde04-130">OUTPUTS</span></span>

### <span data-ttu-id="fde04-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="fde04-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="fde04-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fde04-132">NOTES</span></span>
<span data-ttu-id="fde04-133">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="fde04-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="fde04-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fde04-134">RELATED LINKS</span></span>
