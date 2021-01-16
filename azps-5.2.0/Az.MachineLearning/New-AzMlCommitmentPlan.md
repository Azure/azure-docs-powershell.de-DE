---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
ms.openlocfilehash: 7d3d65e10864848cb1564b7137321c911c153ce0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98300824"
---
# <span data-ttu-id="68ece-101">New-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="68ece-101">New-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="68ece-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68ece-102">SYNOPSIS</span></span>
<span data-ttu-id="68ece-103">Erstellt einen neuen Verpflichtungsplan.</span><span class="sxs-lookup"><span data-stu-id="68ece-103">Creates a new commitment plan.</span></span>

## <span data-ttu-id="68ece-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="68ece-104">SYNTAX</span></span>

```
New-AzMlCommitmentPlan -ResourceGroupName <String> -Location <String> -Name <String> -SkuName <String>
 -SkuTier <String> [-SkuCapacity <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68ece-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="68ece-105">DESCRIPTION</span></span>
<span data-ttu-id="68ece-106">Erstellt einen Azure Machine Learning-Verpflichtungsplan in einer vorhandenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="68ece-106">Creates an Azure Machine Learning commitment plan in an existing resource group.</span></span>
<span data-ttu-id="68ece-107">Wenn in der Ressourcengruppe ein Verpflichtungsplan mit demselben Namen vorhanden ist, fungiert der Aufruf als Aktualisierungsvorgang, und der vorhandene Verpflichtungsplan wird überschrieben.</span><span class="sxs-lookup"><span data-stu-id="68ece-107">If a commitment plan with the same name exists in the resource group, the call acts as an update operation and the existing commitment plan is overwritten.</span></span>

## <span data-ttu-id="68ece-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="68ece-108">EXAMPLES</span></span>

### <span data-ttu-id="68ece-109">Beispiel 1: Erstellen eines neuen Verpflichtungsplans</span><span class="sxs-lookup"><span data-stu-id="68ece-109">Example 1: Create a new commitment plan</span></span>
```
New-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Location "South Central US" -SkuName DevTest -SkuTier Standard -SkuCapacity 1
```

<span data-ttu-id="68ece-110">Erstellt einen neuen Azure Machine Learning-Verpflichtungsplan mit dem Namen "MyCommitmentPlanName" in der Gruppe "MyResourceGroup" und der Region "USA, Süden-Mitte".</span><span class="sxs-lookup"><span data-stu-id="68ece-110">Creates a new Azure Machine Learning commitment plan named "MyCommitmentPlanName" in the "MyResourceGroup" group and South Central US region.</span></span> <span data-ttu-id="68ece-111">In diesem Beispiel wird die SKU DevTest/Standard verwendet, was bedeutet, dass die vom Verpflichtungsplan bereitgestellten Ressourcen durch die Beschränkungen von DevTest/Standard definiert werden.</span><span class="sxs-lookup"><span data-stu-id="68ece-111">In this example, the SKU DevTest/Standard is used, meaning the resources provided by the commitment plan will be defined by the limits of DevTest/Standard.</span></span> <span data-ttu-id="68ece-112">Die Sku1 in diesem Beispiel ist 1. Dies bedeutet, dass die Kosten des Plans 1x den Kosten von DevTest und die im Plan enthaltenen Ressourcen 1x dem von DevTest zur Verfügung stellen.</span><span class="sxs-lookup"><span data-stu-id="68ece-112">The SkuCapacity in this example is 1, meaning the cost of the plan will be 1x the cost of DevTest, and the resources the plan contains will be 1x what DevTest provides.</span></span>

## <span data-ttu-id="68ece-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68ece-113">PARAMETERS</span></span>

### <span data-ttu-id="68ece-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68ece-114">-DefaultProfile</span></span>
<span data-ttu-id="68ece-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="68ece-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68ece-116">-Force</span><span class="sxs-lookup"><span data-stu-id="68ece-116">-Force</span></span>
<span data-ttu-id="68ece-117">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="68ece-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="68ece-118">-Location</span><span class="sxs-lookup"><span data-stu-id="68ece-118">-Location</span></span>
<span data-ttu-id="68ece-119">Der Speicherort des Azure ML-Verpflichtungsplans.</span><span class="sxs-lookup"><span data-stu-id="68ece-119">The location of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="68ece-120">-Name</span><span class="sxs-lookup"><span data-stu-id="68ece-120">-Name</span></span>
<span data-ttu-id="68ece-121">Der Name des Azure ML-Verpflichtungsplans.</span><span class="sxs-lookup"><span data-stu-id="68ece-121">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="68ece-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68ece-122">-ResourceGroupName</span></span>
<span data-ttu-id="68ece-123">Der Name der Ressourcengruppe für den Azure ML-Verpflichtungsplan.</span><span class="sxs-lookup"><span data-stu-id="68ece-123">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="68ece-124">-Sku1</span><span class="sxs-lookup"><span data-stu-id="68ece-124">-SkuCapacity</span></span>
<span data-ttu-id="68ece-125">Die Kapazität der SKU, die beim Bereitstellen des Azure ML-Verpflichtungsplans verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="68ece-125">The capacity of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="68ece-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="68ece-126">-SkuName</span></span>
<span data-ttu-id="68ece-127">Der Name der SKU, die beim Bereitstellen des Azure ML-Verpflichtungsplans verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="68ece-127">The name of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="68ece-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="68ece-128">-SkuTier</span></span>
<span data-ttu-id="68ece-129">Die Stufe der SKU, die beim Bereitstellen des Azure ML-Verpflichtungsplans verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="68ece-129">The tier of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="68ece-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="68ece-130">-Confirm</span></span>
<span data-ttu-id="68ece-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="68ece-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68ece-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="68ece-132">-WhatIf</span></span>
<span data-ttu-id="68ece-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="68ece-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68ece-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="68ece-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68ece-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68ece-135">CommonParameters</span></span>
<span data-ttu-id="68ece-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68ece-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68ece-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68ece-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68ece-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="68ece-138">INPUTS</span></span>

### <span data-ttu-id="68ece-139">Keine</span><span class="sxs-lookup"><span data-stu-id="68ece-139">None</span></span>

## <span data-ttu-id="68ece-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="68ece-140">OUTPUTS</span></span>

### <span data-ttu-id="68ece-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="68ece-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="68ece-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="68ece-142">NOTES</span></span>
<span data-ttu-id="68ece-143">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="68ece-143">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="68ece-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="68ece-144">RELATED LINKS</span></span>
