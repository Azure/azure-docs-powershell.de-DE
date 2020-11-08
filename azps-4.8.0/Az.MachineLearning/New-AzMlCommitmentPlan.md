---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
ms.openlocfilehash: 7d3d65e10864848cb1564b7137321c911c153ce0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009230"
---
# <span data-ttu-id="dff5b-101">New-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="dff5b-101">New-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="dff5b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dff5b-102">SYNOPSIS</span></span>
<span data-ttu-id="dff5b-103">Erstellt einen neuen Verpflichtungs Plan.</span><span class="sxs-lookup"><span data-stu-id="dff5b-103">Creates a new commitment plan.</span></span>

## <span data-ttu-id="dff5b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dff5b-104">SYNTAX</span></span>

```
New-AzMlCommitmentPlan -ResourceGroupName <String> -Location <String> -Name <String> -SkuName <String>
 -SkuTier <String> [-SkuCapacity <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dff5b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dff5b-105">DESCRIPTION</span></span>
<span data-ttu-id="dff5b-106">Erstellt einen Azure Machine Learning-Verpflichtungs Plan in einer vorhandenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dff5b-106">Creates an Azure Machine Learning commitment plan in an existing resource group.</span></span>
<span data-ttu-id="dff5b-107">Wenn in der Ressourcengruppe ein zusageplan mit demselben Namen vorhanden ist, fungiert der Anruf als Aktualisierungsvorgang, und der vorhandene obligoplan wird überschrieben.</span><span class="sxs-lookup"><span data-stu-id="dff5b-107">If a commitment plan with the same name exists in the resource group, the call acts as an update operation and the existing commitment plan is overwritten.</span></span>

## <span data-ttu-id="dff5b-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dff5b-108">EXAMPLES</span></span>

### <span data-ttu-id="dff5b-109">Beispiel 1: Erstellen eines neuen Verpflichtungs Plans</span><span class="sxs-lookup"><span data-stu-id="dff5b-109">Example 1: Create a new commitment plan</span></span>
```
New-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Location "South Central US" -SkuName DevTest -SkuTier Standard -SkuCapacity 1
```

<span data-ttu-id="dff5b-110">Erstellt einen neuen Azure Machine Learning Commitment Plan mit dem Namen "MyCommitmentPlanName" in der Gruppe "myresourcegroup" und in der Region Süd-Zentralamerika.</span><span class="sxs-lookup"><span data-stu-id="dff5b-110">Creates a new Azure Machine Learning commitment plan named "MyCommitmentPlanName" in the "MyResourceGroup" group and South Central US region.</span></span> <span data-ttu-id="dff5b-111">In diesem Beispiel wird die SKU-DevTest/-Standard verwendet, was bedeutet, dass die Ressourcen, die vom Commitment-Plan bereitgestellt werden, durch die Grenzwerte von DevTest/Standard definiert werden.</span><span class="sxs-lookup"><span data-stu-id="dff5b-111">In this example, the SKU DevTest/Standard is used, meaning the resources provided by the commitment plan will be defined by the limits of DevTest/Standard.</span></span> <span data-ttu-id="dff5b-112">Das SkuCapacity in diesem Beispiel ist 1, was bedeutet, dass die Kosten des Plans 1X die Kosten von DevTest und die Ressourcen, die der Plan enthält, 1X sind, was DevTest bietet.</span><span class="sxs-lookup"><span data-stu-id="dff5b-112">The SkuCapacity in this example is 1, meaning the cost of the plan will be 1x the cost of DevTest, and the resources the plan contains will be 1x what DevTest provides.</span></span>

## <span data-ttu-id="dff5b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="dff5b-113">PARAMETERS</span></span>

### <span data-ttu-id="dff5b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dff5b-114">-DefaultProfile</span></span>
<span data-ttu-id="dff5b-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="dff5b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dff5b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="dff5b-116">-Force</span></span>
<span data-ttu-id="dff5b-117">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="dff5b-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="dff5b-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="dff5b-118">-Location</span></span>
<span data-ttu-id="dff5b-119">Der Speicherort des Azure-ml-obligoplan.</span><span class="sxs-lookup"><span data-stu-id="dff5b-119">The location of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="dff5b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="dff5b-120">-Name</span></span>
<span data-ttu-id="dff5b-121">Der Name des Azure-ml-obligoplan.</span><span class="sxs-lookup"><span data-stu-id="dff5b-121">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="dff5b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dff5b-122">-ResourceGroupName</span></span>
<span data-ttu-id="dff5b-123">Der Name der Ressourcengruppe für den Azure-ml-Verpflichtungs Plan.</span><span class="sxs-lookup"><span data-stu-id="dff5b-123">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="dff5b-124">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="dff5b-124">-SkuCapacity</span></span>
<span data-ttu-id="dff5b-125">Die Kapazität der SKU, die verwendet werden soll, wenn der Azure-ml-Verpflichtungs Plan bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="dff5b-125">The capacity of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="dff5b-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="dff5b-126">-SkuName</span></span>
<span data-ttu-id="dff5b-127">Der Name der SKU, die bei der Bereitstellung des Azure-ml-Obligo-Plans zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="dff5b-127">The name of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="dff5b-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="dff5b-128">-SkuTier</span></span>
<span data-ttu-id="dff5b-129">Die Ebene der SKU, die bei der Bereitstellung des Azure-ml-Obligo-Plans zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="dff5b-129">The tier of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="dff5b-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dff5b-130">-Confirm</span></span>
<span data-ttu-id="dff5b-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dff5b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dff5b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dff5b-132">-WhatIf</span></span>
<span data-ttu-id="dff5b-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dff5b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dff5b-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dff5b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dff5b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dff5b-135">CommonParameters</span></span>
<span data-ttu-id="dff5b-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dff5b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dff5b-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dff5b-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dff5b-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dff5b-138">INPUTS</span></span>

### <span data-ttu-id="dff5b-139">Keine</span><span class="sxs-lookup"><span data-stu-id="dff5b-139">None</span></span>

## <span data-ttu-id="dff5b-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dff5b-140">OUTPUTS</span></span>

### <span data-ttu-id="dff5b-141">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="dff5b-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="dff5b-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="dff5b-142">NOTES</span></span>
<span data-ttu-id="dff5b-143">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="dff5b-143">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="dff5b-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dff5b-144">RELATED LINKS</span></span>
