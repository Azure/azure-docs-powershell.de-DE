---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
ms.openlocfilehash: 5e4af2ef006e51cee135dd642bcae7282940e8be
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165244"
---
# <span data-ttu-id="72c7e-101">Remove-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="72c7e-101">Remove-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="72c7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72c7e-102">SYNOPSIS</span></span>
<span data-ttu-id="72c7e-103">Löscht den Schritt.</span><span class="sxs-lookup"><span data-stu-id="72c7e-103">Deletes the step.</span></span>

## <span data-ttu-id="72c7e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72c7e-104">SYNTAX</span></span>

### <span data-ttu-id="72c7e-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="72c7e-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72c7e-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="72c7e-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72c7e-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="72c7e-107">InputObject</span></span>
```
Remove-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72c7e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="72c7e-108">DESCRIPTION</span></span>
<span data-ttu-id="72c7e-109">Das **Cmdlet "Remove-AzDeploymentManagerStep"** löscht einen Schritt.</span><span class="sxs-lookup"><span data-stu-id="72c7e-109">The **Remove-AzDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="72c7e-110">Geben Sie den Schritt durch seinen Namen und den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="72c7e-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="72c7e-111">Alternativ können Sie das Objekt "Step" oder die "ResourceId" bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="72c7e-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="72c7e-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="72c7e-112">EXAMPLES</span></span>

### <span data-ttu-id="72c7e-113">Beispiel 1: Entfernen eines Schritts</span><span class="sxs-lookup"><span data-stu-id="72c7e-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="72c7e-114">Mit diesem Befehl wird ein Schritt namens "ContosoService1WaitStep" in "ContosoResourceGroup" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="72c7e-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="72c7e-115">Beispiel 2: Entfernen eines Schritts mithilfe des Ressourcenbezeichners</span><span class="sxs-lookup"><span data-stu-id="72c7e-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="72c7e-116">Mit diesem Befehl wird ein Schritt namens "ContosoService1WaitStep" in "ContosoResourceGroup" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="72c7e-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="72c7e-117">Beispiel 3: Entfernen eines Schritts mithilfe eines objekts, das von der New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="72c7e-117">Example 3: Remove a step using an object returned by New-AzDeploymentManagerStep</span></span>
### <span data-ttu-id="72c7e-118">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="72c7e-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="72c7e-119">Mit diesem Befehl wird ein Schritt gelöscht, dessen Name und Ressourcengruppe mit den Eigenschaften "Name" bzw. "ResourceGroupName" des $stepObject übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="72c7e-119">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="72c7e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72c7e-120">PARAMETERS</span></span>

### <span data-ttu-id="72c7e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72c7e-121">-DefaultProfile</span></span>
<span data-ttu-id="72c7e-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="72c7e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72c7e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72c7e-123">-InputObject</span></span>
<span data-ttu-id="72c7e-124">Der Schritt, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="72c7e-124">The step to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72c7e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="72c7e-125">-Name</span></span>
<span data-ttu-id="72c7e-126">Der Name des Schritts.</span><span class="sxs-lookup"><span data-stu-id="72c7e-126">The name of the step.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72c7e-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72c7e-127">-PassThru</span></span>
<span data-ttu-id="72c7e-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="72c7e-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="72c7e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72c7e-129">-ResourceGroupName</span></span>
<span data-ttu-id="72c7e-130">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="72c7e-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72c7e-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72c7e-131">-ResourceId</span></span>
<span data-ttu-id="72c7e-132">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="72c7e-132">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72c7e-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="72c7e-133">-Confirm</span></span>
<span data-ttu-id="72c7e-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="72c7e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72c7e-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="72c7e-135">-WhatIf</span></span>
<span data-ttu-id="72c7e-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="72c7e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72c7e-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="72c7e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72c7e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72c7e-138">CommonParameters</span></span>
<span data-ttu-id="72c7e-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72c7e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72c7e-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72c7e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72c7e-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="72c7e-141">INPUTS</span></span>

### <span data-ttu-id="72c7e-142">System.String</span><span class="sxs-lookup"><span data-stu-id="72c7e-142">System.String</span></span>

### <span data-ttu-id="72c7e-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="72c7e-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="72c7e-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="72c7e-144">OUTPUTS</span></span>

### <span data-ttu-id="72c7e-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="72c7e-145">System.Boolean</span></span>

## <span data-ttu-id="72c7e-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="72c7e-146">NOTES</span></span>

## <span data-ttu-id="72c7e-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="72c7e-147">RELATED LINKS</span></span>
