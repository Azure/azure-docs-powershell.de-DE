---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/new-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
ms.openlocfilehash: f5386f3c971159f2a33353efeb380164447ee295
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928976"
---
# <span data-ttu-id="fc05c-101">New-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="fc05c-101">New-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="fc05c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc05c-102">SYNOPSIS</span></span>
<span data-ttu-id="fc05c-103">Erstellt einen neuen Verpflichtungsplan.</span><span class="sxs-lookup"><span data-stu-id="fc05c-103">Creates a new commitment plan.</span></span>

## <span data-ttu-id="fc05c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc05c-104">SYNTAX</span></span>

```
New-AzMlCommitmentPlan -ResourceGroupName <String> -Location <String> -Name <String> -SkuName <String>
 -SkuTier <String> [-SkuCapacity <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc05c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fc05c-105">DESCRIPTION</span></span>
<span data-ttu-id="fc05c-106">Erstellt einen Azure Machine Learning-Verpflichtungsplan in einer vorhandenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fc05c-106">Creates an Azure Machine Learning commitment plan in an existing resource group.</span></span>
<span data-ttu-id="fc05c-107">Wenn in der Ressourcengruppe ein Verpflichtungsplan mit demselben Namen vorhanden ist, fungiert der Aufruf als Aktualisierungsvorgang, und der vorhandene Verpflichtungsplan wird überschrieben.</span><span class="sxs-lookup"><span data-stu-id="fc05c-107">If a commitment plan with the same name exists in the resource group, the call acts as an update operation and the existing commitment plan is overwritten.</span></span>

## <span data-ttu-id="fc05c-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fc05c-108">EXAMPLES</span></span>

### <span data-ttu-id="fc05c-109">Beispiel 1: Erstellen eines neuen Verpflichtungsplans</span><span class="sxs-lookup"><span data-stu-id="fc05c-109">Example 1: Create a new commitment plan</span></span>
```
New-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Location "South Central US" -SkuName DevTest -SkuTier Standard -SkuCapacity 1
```

<span data-ttu-id="fc05c-110">Erstellt einen neuen Azure Machine Learning-Verpflichtungsplan mit dem Namen "MyCommitmentPlanName" in der Gruppe "MyResourceGroup" und region "South Central US".</span><span class="sxs-lookup"><span data-stu-id="fc05c-110">Creates a new Azure Machine Learning commitment plan named "MyCommitmentPlanName" in the "MyResourceGroup" group and South Central US region.</span></span> <span data-ttu-id="fc05c-111">In diesem Beispiel wird der SKU DevTest/Standard verwendet, was bedeutet, dass die vom Verpflichtungsplan bereitgestellten Ressourcen durch die Grenzwerte von DevTest/Standard definiert werden.</span><span class="sxs-lookup"><span data-stu-id="fc05c-111">In this example, the SKU DevTest/Standard is used, meaning the resources provided by the commitment plan will be defined by the limits of DevTest/Standard.</span></span> <span data-ttu-id="fc05c-112">Die SkuKapazität in diesem Beispiel ist 1, d. h., die Kosten des Plans sind 1x der Kosten von DevTest, und die Ressourcen, die der Plan enthält, sind 1x der von DevTest zur Verfügung stellen.</span><span class="sxs-lookup"><span data-stu-id="fc05c-112">The SkuCapacity in this example is 1, meaning the cost of the plan will be 1x the cost of DevTest, and the resources the plan contains will be 1x what DevTest provides.</span></span>

## <span data-ttu-id="fc05c-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fc05c-113">PARAMETERS</span></span>

### <span data-ttu-id="fc05c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc05c-114">-DefaultProfile</span></span>
<span data-ttu-id="fc05c-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="fc05c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc05c-116">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="fc05c-116">-Force</span></span>
<span data-ttu-id="fc05c-117">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="fc05c-117">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc05c-118">-Location</span><span class="sxs-lookup"><span data-stu-id="fc05c-118">-Location</span></span>
<span data-ttu-id="fc05c-119">Der Speicherort des Azure ML-Verpflichtungsplans.</span><span class="sxs-lookup"><span data-stu-id="fc05c-119">The location of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="fc05c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="fc05c-120">-Name</span></span>
<span data-ttu-id="fc05c-121">Der Name des Azure ML-Verpflichtungsplans.</span><span class="sxs-lookup"><span data-stu-id="fc05c-121">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="fc05c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc05c-122">-ResourceGroupName</span></span>
<span data-ttu-id="fc05c-123">Der Name der Ressourcengruppe für den Azure ML-Verpflichtungsplan.</span><span class="sxs-lookup"><span data-stu-id="fc05c-123">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="fc05c-124">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="fc05c-124">-SkuCapacity</span></span>
<span data-ttu-id="fc05c-125">Die Kapazität der SKU, die sie bei der Bereitstellung des Azure ML-Verpflichtungsplans verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="fc05c-125">The capacity of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc05c-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fc05c-126">-SkuName</span></span>
<span data-ttu-id="fc05c-127">Der Name der SKU, die beim Bereitstellen des Azure ML-Verpflichtungsplans verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc05c-127">The name of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="fc05c-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="fc05c-128">-SkuTier</span></span>
<span data-ttu-id="fc05c-129">Die Stufe der SKU, die beim Bereitstellen des Azure ML-Verpflichtungsplans verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc05c-129">The tier of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="fc05c-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fc05c-130">-Confirm</span></span>
<span data-ttu-id="fc05c-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fc05c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc05c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc05c-132">-WhatIf</span></span>
<span data-ttu-id="fc05c-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fc05c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc05c-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fc05c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc05c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc05c-135">CommonParameters</span></span>
<span data-ttu-id="fc05c-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc05c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc05c-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc05c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc05c-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fc05c-138">INPUTS</span></span>

### <span data-ttu-id="fc05c-139">Keine</span><span class="sxs-lookup"><span data-stu-id="fc05c-139">None</span></span>

## <span data-ttu-id="fc05c-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fc05c-140">OUTPUTS</span></span>

### <span data-ttu-id="fc05c-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="fc05c-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="fc05c-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fc05c-142">NOTES</span></span>
<span data-ttu-id="fc05c-143">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="fc05c-143">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="fc05c-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fc05c-144">RELATED LINKS</span></span>
