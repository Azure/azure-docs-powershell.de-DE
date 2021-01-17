---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/restart-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
ms.openlocfilehash: ba7b62d42764f5098868e6a15eb073cb6b898e82
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471631"
---
# <span data-ttu-id="28b94-101">Restart-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="28b94-101">Restart-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="28b94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28b94-102">SYNOPSIS</span></span>
<span data-ttu-id="28b94-103">Startet einen fehlgeschlagenen Rollout neu.</span><span class="sxs-lookup"><span data-stu-id="28b94-103">Restarts a failed rollout.</span></span>

## <span data-ttu-id="28b94-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="28b94-104">SYNTAX</span></span>

### <span data-ttu-id="28b94-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="28b94-105">Interactive (Default)</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28b94-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="28b94-106">ResourceId</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceId] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28b94-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="28b94-107">InputObject</span></span>
```
Restart-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28b94-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="28b94-108">DESCRIPTION</span></span>
<span data-ttu-id="28b94-109">Das **Cmdlet "Restart-AzDeploymentManagerRollout"** startet ein fehlgeschlagenes Rollout neu und gibt ein Objekt zurück, das diesen Rollout mit allen detaillierten Informationen zum Fortschritt des Rollouts darstellt.</span><span class="sxs-lookup"><span data-stu-id="28b94-109">The **Restart-AzDeploymentManagerRollout** cmdlet restarts a failed rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="28b94-110">Geben Sie das Rollout durch den Namen und den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="28b94-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="28b94-111">Alternativ können Sie das Rollout-Objekt oder die ResourceId bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="28b94-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>
<span data-ttu-id="28b94-112">Mit dem optionalen Parameter "SkipSucceeded" können Sie alle erfolgreichen Schritte aus der vorherigen Ausführung des Rollouts überspringen.</span><span class="sxs-lookup"><span data-stu-id="28b94-112">Optional parameter SkipSucceeded allows you to skip all the succeeded steps in the previous run of the rollout.</span></span>

## <span data-ttu-id="28b94-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="28b94-113">EXAMPLES</span></span>

### <span data-ttu-id="28b94-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="28b94-114">Example 1</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="28b94-115">Mit diesem Befehl wird ein Rollout mit dem Namen "ContosoRollout" in der ContosoResourceGroup neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="28b94-115">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="28b94-116">Das Flag "SkipSucceeded" gibt an, dass alle Schritte, die bereits erfolgreich ausgeführt wurden, übersprungen werden sollten und die Ausführung an der Stelle fortgesetzt werden sollte, an der sie zuletzt fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="28b94-116">The SkipSucceeded flag indicates that all the steps that already ran successfully should be skipped and the rollout should continue execution from where it last failed.</span></span>

### <span data-ttu-id="28b94-117">Beispiel 2: Neustarten eines Rollouts mithilfe des Ressourcenbezeichners</span><span class="sxs-lookup"><span data-stu-id="28b94-117">Example 2: Restart a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="28b94-118">Mit diesem Befehl wird ein Rollout mit dem Namen "ContosoRollout" in der ContosoResourceGroup neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="28b94-118">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="28b94-119">Beispiel 3: Neustarten eines Rollouts mithilfe des Rolloutobjekts.</span><span class="sxs-lookup"><span data-stu-id="28b94-119">Example 3: Restart a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="28b94-120">Mit diesem Befehl wird ein Rollout neu gestartet, dessen Name und Ressourcengruppe mit den Eigenschaften "Name" bzw. "ResourceGroupName" des $rolloutObject übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="28b94-120">This command restarts a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="28b94-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28b94-121">PARAMETERS</span></span>

### <span data-ttu-id="28b94-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28b94-122">-DefaultProfile</span></span>
<span data-ttu-id="28b94-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="28b94-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28b94-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28b94-124">-InputObject</span></span>
<span data-ttu-id="28b94-125">Die ressource, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="28b94-125">The resource to be removed.</span></span>

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

### <span data-ttu-id="28b94-126">-Name</span><span class="sxs-lookup"><span data-stu-id="28b94-126">-Name</span></span>
<span data-ttu-id="28b94-127">Der Name des Rollouts.</span><span class="sxs-lookup"><span data-stu-id="28b94-127">The name of the rollout.</span></span>

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

### <span data-ttu-id="28b94-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28b94-128">-ResourceGroupName</span></span>
<span data-ttu-id="28b94-129">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="28b94-129">The resource group.</span></span>

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

### <span data-ttu-id="28b94-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28b94-130">-ResourceId</span></span>
<span data-ttu-id="28b94-131">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="28b94-131">The resource identifier.</span></span>

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

### <span data-ttu-id="28b94-132">-SkipSucceeded</span><span class="sxs-lookup"><span data-stu-id="28b94-132">-SkipSucceeded</span></span>
<span data-ttu-id="28b94-133">Überspringen Sie Schritte, die im vorherigen Ausführen des Rollouts erfolgreich waren.</span><span class="sxs-lookup"><span data-stu-id="28b94-133">Skip steps that succeeded in the previous run of the rollout.</span></span>

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

### <span data-ttu-id="28b94-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28b94-134">-Confirm</span></span>
<span data-ttu-id="28b94-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="28b94-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28b94-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="28b94-136">-WhatIf</span></span>
<span data-ttu-id="28b94-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="28b94-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28b94-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="28b94-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28b94-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28b94-139">CommonParameters</span></span>
<span data-ttu-id="28b94-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28b94-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28b94-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28b94-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28b94-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="28b94-142">INPUTS</span></span>

### <span data-ttu-id="28b94-143">System.String</span><span class="sxs-lookup"><span data-stu-id="28b94-143">System.String</span></span>

### <span data-ttu-id="28b94-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="28b94-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="28b94-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="28b94-145">OUTPUTS</span></span>

### <span data-ttu-id="28b94-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="28b94-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="28b94-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="28b94-147">NOTES</span></span>

## <span data-ttu-id="28b94-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="28b94-148">RELATED LINKS</span></span>
