---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/move-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
ms.openlocfilehash: 96f686fe395ce20d4eabe32f8df2b5821384ab0d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650673"
---
# <span data-ttu-id="46a82-101">Move-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="46a82-101">Move-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="46a82-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46a82-102">SYNOPSIS</span></span>
<span data-ttu-id="46a82-103">Verschiebt eine zubindungs Zuordnung von einem obligoplan in einen anderen.</span><span class="sxs-lookup"><span data-stu-id="46a82-103">Moves a commitment association from one commitment plan to another.</span></span>

## <span data-ttu-id="46a82-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46a82-104">SYNTAX</span></span>

```
Move-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="46a82-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46a82-105">DESCRIPTION</span></span>
<span data-ttu-id="46a82-106">Verschiebt eine Obligo-Zuordnungs Ressource aus dem übergeordneten obligoplan in einen anderen Verpflichtungs Plan.</span><span class="sxs-lookup"><span data-stu-id="46a82-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="46a82-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46a82-107">EXAMPLES</span></span>

### <span data-ttu-id="46a82-108">Beispiel 1: Verschieben einer Verpflichtungs Zuordnung</span><span class="sxs-lookup"><span data-stu-id="46a82-108">Example 1: Move a commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="46a82-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="46a82-109">PARAMETERS</span></span>

### <span data-ttu-id="46a82-110">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="46a82-110">-CommitmentPlanName</span></span>
<span data-ttu-id="46a82-111">Der Name des Azure-ml-obligoplan.</span><span class="sxs-lookup"><span data-stu-id="46a82-111">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="46a82-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46a82-112">-DefaultProfile</span></span>
<span data-ttu-id="46a82-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="46a82-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46a82-114">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="46a82-114">-DestinationPlanId</span></span>
<span data-ttu-id="46a82-115">Die Azure-Ressourcen-ID des Ziels Azure ml-Verpflichtungs Plan.</span><span class="sxs-lookup"><span data-stu-id="46a82-115">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="46a82-116">-Name</span><span class="sxs-lookup"><span data-stu-id="46a82-116">-Name</span></span>
<span data-ttu-id="46a82-117">Der Name der Azure ml Commitment Association.</span><span class="sxs-lookup"><span data-stu-id="46a82-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="46a82-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46a82-118">-ResourceGroupName</span></span>
<span data-ttu-id="46a82-119">Der Name der Ressourcengruppe für die Azure ml Commitment Association.</span><span class="sxs-lookup"><span data-stu-id="46a82-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="46a82-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="46a82-120">-Confirm</span></span>
<span data-ttu-id="46a82-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46a82-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46a82-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46a82-122">-WhatIf</span></span>
<span data-ttu-id="46a82-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46a82-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46a82-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46a82-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46a82-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46a82-125">CommonParameters</span></span>
<span data-ttu-id="46a82-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46a82-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46a82-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46a82-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46a82-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46a82-128">INPUTS</span></span>

### <span data-ttu-id="46a82-129">Keine</span><span class="sxs-lookup"><span data-stu-id="46a82-129">None</span></span>

## <span data-ttu-id="46a82-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46a82-130">OUTPUTS</span></span>

### <span data-ttu-id="46a82-131">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="46a82-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="46a82-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="46a82-132">NOTES</span></span>
<span data-ttu-id="46a82-133">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="46a82-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="46a82-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46a82-134">RELATED LINKS</span></span>
