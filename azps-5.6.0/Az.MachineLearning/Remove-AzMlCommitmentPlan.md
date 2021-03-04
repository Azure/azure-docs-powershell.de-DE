---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/remove-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
ms.openlocfilehash: 287db082c5cbe842b0a92b124870effb77068912
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922891"
---
# <span data-ttu-id="1c333-101">Remove-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="1c333-101">Remove-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="1c333-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c333-102">SYNOPSIS</span></span>
<span data-ttu-id="1c333-103">Löscht einen Verpflichtungsplan.</span><span class="sxs-lookup"><span data-stu-id="1c333-103">Deletes a commitment plan.</span></span>

## <span data-ttu-id="1c333-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c333-104">SYNTAX</span></span>

### <span data-ttu-id="1c333-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1c333-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c333-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="1c333-106">RemoveByObject</span></span>
```
Remove-AzMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c333-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1c333-107">DESCRIPTION</span></span>
<span data-ttu-id="1c333-108">Löscht einen Azure Machine Learning-Verpflichtungsplan.</span><span class="sxs-lookup"><span data-stu-id="1c333-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="1c333-109">Beachten Sie, dass Verpflichtungspläne mit Verpflichtungszuordnungen nicht gelöscht werden können.</span><span class="sxs-lookup"><span data-stu-id="1c333-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="1c333-110">Verpflichtungszuordnungen können nur von ihrer Zielressource gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="1c333-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="1c333-111">Wenn Sie beispielsweise einen Azure Machine Learning-Webdienst löschen, wird auch die Verpflichtungs zuordnung gelöscht, die den Webdienst einem Verpflichtungsplan zu ordnet.</span><span class="sxs-lookup"><span data-stu-id="1c333-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="1c333-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1c333-112">EXAMPLES</span></span>

### <span data-ttu-id="1c333-113">Beispiel 1: Löschen eines Verpflichtungsplans</span><span class="sxs-lookup"><span data-stu-id="1c333-113">Example 1: Delete a commitment plan</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="1c333-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1c333-114">PARAMETERS</span></span>

### <span data-ttu-id="1c333-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c333-115">-DefaultProfile</span></span>
<span data-ttu-id="1c333-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="1c333-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c333-117">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="1c333-117">-Force</span></span>
<span data-ttu-id="1c333-118">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="1c333-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1c333-119">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="1c333-119">-MlCommitmentPlan</span></span>
<span data-ttu-id="1c333-120">Das Machine Learning-Webdienstobjekt.</span><span class="sxs-lookup"><span data-stu-id="1c333-120">The machine learning web service object.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c333-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1c333-121">-Name</span></span>
<span data-ttu-id="1c333-122">Der Name des Azure ML-Verpflichtungsplans.</span><span class="sxs-lookup"><span data-stu-id="1c333-122">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c333-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c333-123">-ResourceGroupName</span></span>
<span data-ttu-id="1c333-124">Der Name der Ressourcengruppe für den Azure ML-Verpflichtungsplan.</span><span class="sxs-lookup"><span data-stu-id="1c333-124">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c333-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1c333-125">-Confirm</span></span>
<span data-ttu-id="1c333-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1c333-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c333-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c333-127">-WhatIf</span></span>
<span data-ttu-id="1c333-128">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1c333-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c333-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1c333-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c333-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c333-130">CommonParameters</span></span>
<span data-ttu-id="1c333-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c333-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c333-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c333-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c333-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1c333-133">INPUTS</span></span>

### <span data-ttu-id="1c333-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="1c333-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="1c333-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1c333-135">OUTPUTS</span></span>

### <span data-ttu-id="1c333-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="1c333-136">System.Void</span></span>

## <span data-ttu-id="1c333-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1c333-137">NOTES</span></span>
<span data-ttu-id="1c333-138">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="1c333-138">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="1c333-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1c333-139">RELATED LINKS</span></span>
