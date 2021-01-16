---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/stop-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
ms.openlocfilehash: cd59cd39fb2834bed2162a257905fea643c0a767
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294526"
---
# <span data-ttu-id="16918-101">Stop-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="16918-101">Stop-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="16918-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16918-102">SYNOPSIS</span></span>
<span data-ttu-id="16918-103">Beendet das Rollout.</span><span class="sxs-lookup"><span data-stu-id="16918-103">Stops the rollout.</span></span>

## <span data-ttu-id="16918-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16918-104">SYNTAX</span></span>

### <span data-ttu-id="16918-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="16918-105">Interactive (Default)</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16918-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="16918-106">ResourceId</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16918-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="16918-107">InputObject</span></span>
```
Stop-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16918-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="16918-108">DESCRIPTION</span></span>
<span data-ttu-id="16918-109">Das **Cmdlet "Stop-AzDeploymentManagerRollout"** beendet den aktuellen Rollout und gibt ein Objekt zurück, das den aktuellen Status des Rollouts darstellt.</span><span class="sxs-lookup"><span data-stu-id="16918-109">The **Stop-AzDeploymentManagerRollout** cmdlet stops a rollout in progress and returns an object that represents the current state of the rollout.</span></span>
<span data-ttu-id="16918-110">Geben Sie das Rollout durch den Namen und den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="16918-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="16918-111">Alternativ können Sie das Rollout-Objekt oder die ResourceId bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="16918-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="16918-112">Beachten Sie, dass ein beendetes Rollout nicht fortgesetzt oder neu gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="16918-112">Note that once a rollout is stopped, it cannot be resumed or restarted.</span></span> <span data-ttu-id="16918-113">Sie können nur ein neues Rollout erstellen.</span><span class="sxs-lookup"><span data-stu-id="16918-113">You can only create a new rollout.</span></span>

## <span data-ttu-id="16918-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="16918-114">EXAMPLES</span></span>

### <span data-ttu-id="16918-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="16918-115">Example 1</span></span>
```powershell
PS C:\> Stop-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="16918-116">Dieser Befehl stoppt das Rollout "ContosoRollout" in der ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="16918-116">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="16918-117">Beispiel 2: Beenden eines Rollouts mithilfe des Ressourcenbezeichners</span><span class="sxs-lookup"><span data-stu-id="16918-117">Example 2: Stop a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="16918-118">Dieser Befehl stoppt das Rollout "ContosoRollout" in der ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="16918-118">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="16918-119">Beispiel 3: Beenden eines Rollouts mithilfe des Rolloutobjekts.</span><span class="sxs-lookup"><span data-stu-id="16918-119">Example 3: Stop a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="16918-120">Dieser Befehl stoppt ein Rollout, dessen Name und Ressourcengruppe mit den Eigenschaften "Name" bzw. "ResourceGroupName" des $rolloutObject übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="16918-120">This command stops a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="16918-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16918-121">PARAMETERS</span></span>

### <span data-ttu-id="16918-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16918-122">-DefaultProfile</span></span>
<span data-ttu-id="16918-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="16918-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16918-124">-Force</span><span class="sxs-lookup"><span data-stu-id="16918-124">-Force</span></span>
<span data-ttu-id="16918-125">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="16918-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="16918-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16918-126">-InputObject</span></span>
<span data-ttu-id="16918-127">Das Rollout, das entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="16918-127">The rollout to be removed.</span></span>

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

### <span data-ttu-id="16918-128">-Name</span><span class="sxs-lookup"><span data-stu-id="16918-128">-Name</span></span>
<span data-ttu-id="16918-129">Der Name des Rollouts.</span><span class="sxs-lookup"><span data-stu-id="16918-129">The name of the rollout.</span></span>

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

### <span data-ttu-id="16918-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16918-130">-ResourceGroupName</span></span>
<span data-ttu-id="16918-131">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="16918-131">The resource group.</span></span>

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

### <span data-ttu-id="16918-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16918-132">-ResourceId</span></span>
<span data-ttu-id="16918-133">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="16918-133">The resource identifier.</span></span>

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

### <span data-ttu-id="16918-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16918-134">-Confirm</span></span>
<span data-ttu-id="16918-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="16918-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16918-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="16918-136">-WhatIf</span></span>
<span data-ttu-id="16918-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="16918-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16918-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="16918-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16918-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16918-139">CommonParameters</span></span>
<span data-ttu-id="16918-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16918-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16918-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16918-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16918-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="16918-142">INPUTS</span></span>

### <span data-ttu-id="16918-143">System.String</span><span class="sxs-lookup"><span data-stu-id="16918-143">System.String</span></span>

### <span data-ttu-id="16918-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="16918-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="16918-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="16918-145">OUTPUTS</span></span>

### <span data-ttu-id="16918-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="16918-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="16918-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="16918-147">NOTES</span></span>

## <span data-ttu-id="16918-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="16918-148">RELATED LINKS</span></span>
