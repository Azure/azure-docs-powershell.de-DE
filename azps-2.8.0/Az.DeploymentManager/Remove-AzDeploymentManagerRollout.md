---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
ms.openlocfilehash: 066026331fa43af06fc2e3314ccb97d06a0f9b50
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651351"
---
# <span data-ttu-id="1301f-101">Remove-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="1301f-101">Remove-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="1301f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1301f-102">SYNOPSIS</span></span>
<span data-ttu-id="1301f-103">Löscht den Rollout.</span><span class="sxs-lookup"><span data-stu-id="1301f-103">Deletes the rollout.</span></span>

## <span data-ttu-id="1301f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1301f-104">SYNTAX</span></span>

### <span data-ttu-id="1301f-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="1301f-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1301f-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1301f-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1301f-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="1301f-107">InputObject</span></span>
```
Remove-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1301f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1301f-108">DESCRIPTION</span></span>
<span data-ttu-id="1301f-109">Das Cmdlet **Remove-AzDeploymentManagerRollout** löscht ein Rollout in einem Terminal Zustand.</span><span class="sxs-lookup"><span data-stu-id="1301f-109">The **Remove-AzDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="1301f-110">Geben Sie den Rollout nach dem Namen und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1301f-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="1301f-111">Alternativ können Sie das Rollout-Objekt oder die "Resourcen-Nr" bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="1301f-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="1301f-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1301f-112">EXAMPLES</span></span>

### <span data-ttu-id="1301f-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1301f-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="1301f-114">Dieser Befehl löscht ein Rollout mit dem Namen ContosoRollout in der ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1301f-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="1301f-115">Beispiel 2: Löschen eines Rollouts mit dem Ressourcenbezeichner</span><span class="sxs-lookup"><span data-stu-id="1301f-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="1301f-116">Dieser Befehl löscht ein Rollout mit dem Namen ContosoRollout in der ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1301f-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="1301f-117">Beispiel 3: Löschen eines Rollouts mit dem Rollout-Objekt</span><span class="sxs-lookup"><span data-stu-id="1301f-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="1301f-118">Mit diesem Befehl wird ein Rollout gelöscht, dessen Name und ResourceGroup den Namen-und ResourceGroupName-Eigenschaften der $rolloutObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1301f-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="1301f-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="1301f-119">PARAMETERS</span></span>

### <span data-ttu-id="1301f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1301f-120">-DefaultProfile</span></span>
<span data-ttu-id="1301f-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1301f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1301f-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1301f-122">-InputObject</span></span>
<span data-ttu-id="1301f-123">Die Ressource, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1301f-123">The resource to be removed.</span></span>

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

### <span data-ttu-id="1301f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1301f-124">-Name</span></span>
<span data-ttu-id="1301f-125">Der Name des Rollouts.</span><span class="sxs-lookup"><span data-stu-id="1301f-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="1301f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1301f-126">-PassThru</span></span>
<span data-ttu-id="1301f-127">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="1301f-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1301f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1301f-128">-ResourceGroupName</span></span>
<span data-ttu-id="1301f-129">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1301f-129">The resource group.</span></span>

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

### <span data-ttu-id="1301f-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1301f-130">-ResourceId</span></span>
<span data-ttu-id="1301f-131">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="1301f-131">The resource identifier.</span></span>

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

### <span data-ttu-id="1301f-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1301f-132">-Confirm</span></span>
<span data-ttu-id="1301f-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1301f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1301f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1301f-134">-WhatIf</span></span>
<span data-ttu-id="1301f-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1301f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1301f-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1301f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1301f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1301f-137">CommonParameters</span></span>
<span data-ttu-id="1301f-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1301f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1301f-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1301f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1301f-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1301f-140">INPUTS</span></span>

### <span data-ttu-id="1301f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="1301f-141">System.String</span></span>

### <span data-ttu-id="1301f-142">Microsoft. Azure. Commands. deploymentmanager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="1301f-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="1301f-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1301f-143">OUTPUTS</span></span>

### <span data-ttu-id="1301f-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1301f-144">System.Boolean</span></span>

## <span data-ttu-id="1301f-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="1301f-145">NOTES</span></span>

## <span data-ttu-id="1301f-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1301f-146">RELATED LINKS</span></span>
