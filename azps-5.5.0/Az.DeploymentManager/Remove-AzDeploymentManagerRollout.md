---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
ms.openlocfilehash: 8e5e2c25f69d6e61c21a0f616f49079710c2d5db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174545"
---
# <span data-ttu-id="9ef41-101">Remove-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="9ef41-101">Remove-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="9ef41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ef41-102">SYNOPSIS</span></span>
<span data-ttu-id="9ef41-103">Löscht den Rollout.</span><span class="sxs-lookup"><span data-stu-id="9ef41-103">Deletes the rollout.</span></span>

## <span data-ttu-id="9ef41-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ef41-104">SYNTAX</span></span>

### <span data-ttu-id="9ef41-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="9ef41-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ef41-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ef41-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ef41-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="9ef41-107">InputObject</span></span>
```
Remove-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ef41-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9ef41-108">DESCRIPTION</span></span>
<span data-ttu-id="9ef41-109">Das **Cmdlet "Remove-AzDeploymentManagerRollout"** löscht ein Rollout in einem Terminalzustand.</span><span class="sxs-lookup"><span data-stu-id="9ef41-109">The **Remove-AzDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="9ef41-110">Geben Sie das Rollout durch den Namen und den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="9ef41-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="9ef41-111">Alternativ können Sie das Rollout-Objekt oder die ResourceId bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9ef41-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="9ef41-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9ef41-112">EXAMPLES</span></span>

### <span data-ttu-id="9ef41-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9ef41-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="9ef41-114">Mit diesem Befehl wird ein Rollout mit dem Namen "ContosoRollout" in der ContosoResourceGroup gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9ef41-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="9ef41-115">Beispiel 2: Löschen eines Rollouts mithilfe des Ressourcenbezeichners</span><span class="sxs-lookup"><span data-stu-id="9ef41-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="9ef41-116">Mit diesem Befehl wird ein Rollout mit dem Namen "ContosoRollout" in der ContosoResourceGroup gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9ef41-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="9ef41-117">Beispiel 3: Löschen eines Rollouts mithilfe des Rolloutobjekts.</span><span class="sxs-lookup"><span data-stu-id="9ef41-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="9ef41-118">Mit diesem Befehl wird ein Rollout gelöscht, dessen Name und Ressourcengruppe mit den Eigenschaften "Name" bzw. "ResourceGroupName" des $rolloutObject übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9ef41-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="9ef41-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ef41-119">PARAMETERS</span></span>

### <span data-ttu-id="9ef41-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ef41-120">-DefaultProfile</span></span>
<span data-ttu-id="9ef41-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ef41-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ef41-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ef41-122">-InputObject</span></span>
<span data-ttu-id="9ef41-123">Die ressource, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ef41-123">The resource to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ef41-124">-Name</span><span class="sxs-lookup"><span data-stu-id="9ef41-124">-Name</span></span>
<span data-ttu-id="9ef41-125">Der Name des Rollouts.</span><span class="sxs-lookup"><span data-stu-id="9ef41-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="9ef41-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ef41-126">-PassThru</span></span>
<span data-ttu-id="9ef41-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="9ef41-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9ef41-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ef41-128">-ResourceGroupName</span></span>
<span data-ttu-id="9ef41-129">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9ef41-129">The resource group.</span></span>

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

### <span data-ttu-id="9ef41-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ef41-130">-ResourceId</span></span>
<span data-ttu-id="9ef41-131">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="9ef41-131">The resource identifier.</span></span>

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

### <span data-ttu-id="9ef41-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ef41-132">-Confirm</span></span>
<span data-ttu-id="9ef41-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9ef41-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ef41-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9ef41-134">-WhatIf</span></span>
<span data-ttu-id="9ef41-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ef41-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ef41-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ef41-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ef41-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ef41-137">CommonParameters</span></span>
<span data-ttu-id="9ef41-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ef41-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ef41-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ef41-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ef41-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9ef41-140">INPUTS</span></span>

### <span data-ttu-id="9ef41-141">System.String</span><span class="sxs-lookup"><span data-stu-id="9ef41-141">System.String</span></span>

### <span data-ttu-id="9ef41-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="9ef41-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="9ef41-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9ef41-143">OUTPUTS</span></span>

### <span data-ttu-id="9ef41-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9ef41-144">System.Boolean</span></span>

## <span data-ttu-id="9ef41-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9ef41-145">NOTES</span></span>

## <span data-ttu-id="9ef41-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9ef41-146">RELATED LINKS</span></span>
