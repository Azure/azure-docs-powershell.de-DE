---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
ms.openlocfilehash: 96f5f9e3dd0390d714b0ee7a74b3f585b46dcc1b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925768"
---
# <span data-ttu-id="0ed3d-101">Remove-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="0ed3d-101">Remove-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="0ed3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ed3d-102">SYNOPSIS</span></span>
<span data-ttu-id="0ed3d-103">Löscht den Schritt.</span><span class="sxs-lookup"><span data-stu-id="0ed3d-103">Deletes the step.</span></span>

## <span data-ttu-id="0ed3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0ed3d-104">SYNTAX</span></span>

### <span data-ttu-id="0ed3d-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="0ed3d-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ed3d-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ed3d-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ed3d-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="0ed3d-107">InputObject</span></span>
```
Remove-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ed3d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0ed3d-108">DESCRIPTION</span></span>
<span data-ttu-id="0ed3d-109">Das **Cmdlet Remove-AzDeploymentManagerStep** löscht einen Schritt.</span><span class="sxs-lookup"><span data-stu-id="0ed3d-109">The **Remove-AzDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="0ed3d-110">Geben Sie den Schritt durch seinen Namen und den Ressourcengruppennamen an.</span><span class="sxs-lookup"><span data-stu-id="0ed3d-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="0ed3d-111">Alternativ können Sie das Step-Objekt oder die ResourceId bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0ed3d-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="0ed3d-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0ed3d-112">EXAMPLES</span></span>

### <span data-ttu-id="0ed3d-113">Beispiel 1: Entfernen eines Schritts</span><span class="sxs-lookup"><span data-stu-id="0ed3d-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="0ed3d-114">Mit diesem Befehl wird ein Schritt mit dem Namen ContosoService1WaitStep in ContosoResourceGroup gelöscht.</span><span class="sxs-lookup"><span data-stu-id="0ed3d-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="0ed3d-115">Beispiel 2: Entfernen eines Schritts mithilfe des Ressourcenbezeichners</span><span class="sxs-lookup"><span data-stu-id="0ed3d-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="0ed3d-116">Mit diesem Befehl wird ein Schritt mit dem Namen ContosoService1WaitStep in ContosoResourceGroup gelöscht.</span><span class="sxs-lookup"><span data-stu-id="0ed3d-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="0ed3d-117">Beispiel 3: Entfernen eines Schritts mithilfe eines von der New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="0ed3d-117">Example 3: Remove a step using an object returned by New-AzDeploymentManagerStep</span></span>
### <span data-ttu-id="0ed3d-118">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0ed3d-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="0ed3d-119">Mit diesem Befehl wird ein Schritt gelöscht, dessen Name und Ressourcengruppe den Eigenschaften Name und ResourceGroupName des $stepObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0ed3d-119">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="0ed3d-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0ed3d-120">PARAMETERS</span></span>

### <span data-ttu-id="0ed3d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ed3d-121">-DefaultProfile</span></span>
<span data-ttu-id="0ed3d-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0ed3d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ed3d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ed3d-123">-InputObject</span></span>
<span data-ttu-id="0ed3d-124">Der Zu entfernende Schritt.</span><span class="sxs-lookup"><span data-stu-id="0ed3d-124">The step to be removed.</span></span>

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

### <span data-ttu-id="0ed3d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="0ed3d-125">-Name</span></span>
<span data-ttu-id="0ed3d-126">Der Name des Schritts.</span><span class="sxs-lookup"><span data-stu-id="0ed3d-126">The name of the step.</span></span>

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

### <span data-ttu-id="0ed3d-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ed3d-127">-PassThru</span></span>
<span data-ttu-id="0ed3d-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="0ed3d-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0ed3d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ed3d-129">-ResourceGroupName</span></span>
<span data-ttu-id="0ed3d-130">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0ed3d-130">The resource group.</span></span>

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

### <span data-ttu-id="0ed3d-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ed3d-131">-ResourceId</span></span>
<span data-ttu-id="0ed3d-132">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="0ed3d-132">The resource identifier.</span></span>

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

### <span data-ttu-id="0ed3d-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0ed3d-133">-Confirm</span></span>
<span data-ttu-id="0ed3d-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0ed3d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ed3d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ed3d-135">-WhatIf</span></span>
<span data-ttu-id="0ed3d-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0ed3d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ed3d-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0ed3d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ed3d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ed3d-138">CommonParameters</span></span>
<span data-ttu-id="0ed3d-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ed3d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ed3d-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ed3d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ed3d-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0ed3d-141">INPUTS</span></span>

### <span data-ttu-id="0ed3d-142">System.String</span><span class="sxs-lookup"><span data-stu-id="0ed3d-142">System.String</span></span>

### <span data-ttu-id="0ed3d-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="0ed3d-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="0ed3d-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0ed3d-144">OUTPUTS</span></span>

### <span data-ttu-id="0ed3d-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0ed3d-145">System.Boolean</span></span>

## <span data-ttu-id="0ed3d-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0ed3d-146">NOTES</span></span>

## <span data-ttu-id="0ed3d-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0ed3d-147">RELATED LINKS</span></span>
