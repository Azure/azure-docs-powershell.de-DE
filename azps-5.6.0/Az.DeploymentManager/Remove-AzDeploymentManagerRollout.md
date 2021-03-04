---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
ms.openlocfilehash: 3ade9bfd724a84e162c0cedd937f2255ebb5b6a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932963"
---
# <span data-ttu-id="841ab-101">Remove-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="841ab-101">Remove-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="841ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="841ab-102">SYNOPSIS</span></span>
<span data-ttu-id="841ab-103">Löscht das Rollout.</span><span class="sxs-lookup"><span data-stu-id="841ab-103">Deletes the rollout.</span></span>

## <span data-ttu-id="841ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="841ab-104">SYNTAX</span></span>

### <span data-ttu-id="841ab-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="841ab-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="841ab-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="841ab-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="841ab-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="841ab-107">InputObject</span></span>
```
Remove-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="841ab-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="841ab-108">DESCRIPTION</span></span>
<span data-ttu-id="841ab-109">Das **Cmdlet Remove-AzDeploymentManagerRollout** löscht ein Rollout in einem Terminalzustand.</span><span class="sxs-lookup"><span data-stu-id="841ab-109">The **Remove-AzDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="841ab-110">Geben Sie das Rollout nach dem Namen und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="841ab-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="841ab-111">Alternativ können Sie das Rolloutobjekt oder die ResourceId bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="841ab-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="841ab-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="841ab-112">EXAMPLES</span></span>

### <span data-ttu-id="841ab-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="841ab-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="841ab-114">Mit diesem Befehl wird ein Rollout mit dem Namen ContosoRollout in der ContosoResourceGroup gelöscht.</span><span class="sxs-lookup"><span data-stu-id="841ab-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="841ab-115">Beispiel 2: Löschen eines Rollouts mithilfe des Ressourcenbezeichners</span><span class="sxs-lookup"><span data-stu-id="841ab-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="841ab-116">Mit diesem Befehl wird ein Rollout mit dem Namen ContosoRollout in der ContosoResourceGroup gelöscht.</span><span class="sxs-lookup"><span data-stu-id="841ab-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="841ab-117">Beispiel 3: Löschen eines Rollouts mithilfe des Rolloutobjekts.</span><span class="sxs-lookup"><span data-stu-id="841ab-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="841ab-118">Mit diesem Befehl wird ein Rollout gelöscht, dessen Name und Ressourcengruppe den Eigenschaften Name und ResourceGroupName des $rolloutObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="841ab-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="841ab-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="841ab-119">PARAMETERS</span></span>

### <span data-ttu-id="841ab-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="841ab-120">-DefaultProfile</span></span>
<span data-ttu-id="841ab-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="841ab-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="841ab-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="841ab-122">-InputObject</span></span>
<span data-ttu-id="841ab-123">Die ressource, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="841ab-123">The resource to be removed.</span></span>

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

### <span data-ttu-id="841ab-124">-Name</span><span class="sxs-lookup"><span data-stu-id="841ab-124">-Name</span></span>
<span data-ttu-id="841ab-125">Der Name des Rollouts.</span><span class="sxs-lookup"><span data-stu-id="841ab-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="841ab-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="841ab-126">-PassThru</span></span>
<span data-ttu-id="841ab-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="841ab-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="841ab-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="841ab-128">-ResourceGroupName</span></span>
<span data-ttu-id="841ab-129">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="841ab-129">The resource group.</span></span>

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

### <span data-ttu-id="841ab-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="841ab-130">-ResourceId</span></span>
<span data-ttu-id="841ab-131">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="841ab-131">The resource identifier.</span></span>

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

### <span data-ttu-id="841ab-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="841ab-132">-Confirm</span></span>
<span data-ttu-id="841ab-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="841ab-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="841ab-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="841ab-134">-WhatIf</span></span>
<span data-ttu-id="841ab-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="841ab-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="841ab-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="841ab-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="841ab-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="841ab-137">CommonParameters</span></span>
<span data-ttu-id="841ab-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="841ab-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="841ab-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="841ab-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="841ab-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="841ab-140">INPUTS</span></span>

### <span data-ttu-id="841ab-141">System.String</span><span class="sxs-lookup"><span data-stu-id="841ab-141">System.String</span></span>

### <span data-ttu-id="841ab-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="841ab-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="841ab-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="841ab-143">OUTPUTS</span></span>

### <span data-ttu-id="841ab-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="841ab-144">System.Boolean</span></span>

## <span data-ttu-id="841ab-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="841ab-145">NOTES</span></span>

## <span data-ttu-id="841ab-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="841ab-146">RELATED LINKS</span></span>
