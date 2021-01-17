---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
ms.openlocfilehash: 8593853817739438176b70424ab529f0811d90de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385915"
---
# <span data-ttu-id="60b32-101">Remove-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="60b32-101">Remove-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="60b32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60b32-102">SYNOPSIS</span></span>
<span data-ttu-id="60b32-103">Löscht einen Verpflichtungsplan.</span><span class="sxs-lookup"><span data-stu-id="60b32-103">Deletes a commitment plan.</span></span>

## <span data-ttu-id="60b32-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60b32-104">SYNTAX</span></span>

### <span data-ttu-id="60b32-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="60b32-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60b32-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="60b32-106">RemoveByObject</span></span>
```
Remove-AzMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60b32-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60b32-107">DESCRIPTION</span></span>
<span data-ttu-id="60b32-108">Löscht einen Azure Machine Learning-Verpflichtungsplan.</span><span class="sxs-lookup"><span data-stu-id="60b32-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="60b32-109">Beachten Sie, dass Verpflichtungspläne mit Verpflichtungszuordnungen nicht gelöscht werden können.</span><span class="sxs-lookup"><span data-stu-id="60b32-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="60b32-110">Verpflichtungszuordnungen können nur von der Zielressource gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="60b32-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="60b32-111">Wenn Sie beispielsweise einen Azure Machine Learning-Webdienst löschen, wird auch die Verpflichtungs zuordnung gelöscht, die den Webdienst einem Verpflichtungsplan zu ordnet.</span><span class="sxs-lookup"><span data-stu-id="60b32-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="60b32-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="60b32-112">EXAMPLES</span></span>

### <span data-ttu-id="60b32-113">Beispiel 1: Löschen eines Verpflichtungsplans</span><span class="sxs-lookup"><span data-stu-id="60b32-113">Example 1: Delete a commitment plan</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="60b32-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60b32-114">PARAMETERS</span></span>

### <span data-ttu-id="60b32-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60b32-115">-DefaultProfile</span></span>
<span data-ttu-id="60b32-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="60b32-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60b32-117">-Force</span><span class="sxs-lookup"><span data-stu-id="60b32-117">-Force</span></span>
<span data-ttu-id="60b32-118">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="60b32-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="60b32-119">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="60b32-119">-MlCommitmentPlan</span></span>
<span data-ttu-id="60b32-120">Das Machine Learning-Webdienstobjekt.</span><span class="sxs-lookup"><span data-stu-id="60b32-120">The machine learning web service object.</span></span>

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

### <span data-ttu-id="60b32-121">-Name</span><span class="sxs-lookup"><span data-stu-id="60b32-121">-Name</span></span>
<span data-ttu-id="60b32-122">Der Name des Azure ML-Verpflichtungsplans.</span><span class="sxs-lookup"><span data-stu-id="60b32-122">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="60b32-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60b32-123">-ResourceGroupName</span></span>
<span data-ttu-id="60b32-124">Der Name der Ressourcengruppe für den Azure ML-Verpflichtungsplan.</span><span class="sxs-lookup"><span data-stu-id="60b32-124">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="60b32-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60b32-125">-Confirm</span></span>
<span data-ttu-id="60b32-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="60b32-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60b32-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="60b32-127">-WhatIf</span></span>
<span data-ttu-id="60b32-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="60b32-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60b32-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="60b32-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60b32-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60b32-130">CommonParameters</span></span>
<span data-ttu-id="60b32-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60b32-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60b32-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60b32-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60b32-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="60b32-133">INPUTS</span></span>

### <span data-ttu-id="60b32-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="60b32-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="60b32-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="60b32-135">OUTPUTS</span></span>

### <span data-ttu-id="60b32-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="60b32-136">System.Void</span></span>

## <span data-ttu-id="60b32-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="60b32-137">NOTES</span></span>
<span data-ttu-id="60b32-138">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="60b32-138">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="60b32-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="60b32-139">RELATED LINKS</span></span>
