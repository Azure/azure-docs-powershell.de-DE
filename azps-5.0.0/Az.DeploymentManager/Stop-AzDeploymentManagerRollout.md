---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/stop-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
ms.openlocfilehash: cd59cd39fb2834bed2162a257905fea643c0a767
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297123"
---
# <span data-ttu-id="b9a81-101">Stop-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="b9a81-101">Stop-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="b9a81-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b9a81-102">SYNOPSIS</span></span>
<span data-ttu-id="b9a81-103">Beendet den Rollout.</span><span class="sxs-lookup"><span data-stu-id="b9a81-103">Stops the rollout.</span></span>

## <span data-ttu-id="b9a81-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9a81-104">SYNTAX</span></span>

### <span data-ttu-id="b9a81-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="b9a81-105">Interactive (Default)</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9a81-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9a81-106">ResourceId</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9a81-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b9a81-107">InputObject</span></span>
```
Stop-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9a81-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b9a81-108">DESCRIPTION</span></span>
<span data-ttu-id="b9a81-109">Das Cmdlet **Stop-AzDeploymentManagerRollout** verhindert, dass ein Rollout in Bearbeitung ist, und gibt ein Objekt zurück, das den aktuellen Status des Rollouts darstellt.</span><span class="sxs-lookup"><span data-stu-id="b9a81-109">The **Stop-AzDeploymentManagerRollout** cmdlet stops a rollout in progress and returns an object that represents the current state of the rollout.</span></span>
<span data-ttu-id="b9a81-110">Geben Sie den Rollout nach dem Namen und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b9a81-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="b9a81-111">Alternativ können Sie das Rollout-Objekt oder die "Resourcen-Nr" bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b9a81-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="b9a81-112">Beachten Sie, dass ein Rollout nicht mehr fortgesetzt oder neu gestartet werden kann, nachdem ein Rollout beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="b9a81-112">Note that once a rollout is stopped, it cannot be resumed or restarted.</span></span> <span data-ttu-id="b9a81-113">Sie können nur einen neuen Rollout erstellen.</span><span class="sxs-lookup"><span data-stu-id="b9a81-113">You can only create a new rollout.</span></span>

## <span data-ttu-id="b9a81-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b9a81-114">EXAMPLES</span></span>

### <span data-ttu-id="b9a81-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b9a81-115">Example 1</span></span>
```powershell
PS C:\> Stop-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="b9a81-116">Dieser Befehl beendet ein Rollout mit dem Namen ContosoRollout in der ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b9a81-116">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="b9a81-117">Beispiel 2: Beenden eines Rollouts mit dem Ressourcenbezeichner</span><span class="sxs-lookup"><span data-stu-id="b9a81-117">Example 2: Stop a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="b9a81-118">Dieser Befehl beendet ein Rollout mit dem Namen ContosoRollout in der ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b9a81-118">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="b9a81-119">Beispiel 3: Beenden eines Rollouts mit dem Rollout-Objekt</span><span class="sxs-lookup"><span data-stu-id="b9a81-119">Example 3: Stop a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="b9a81-120">Mit diesem Befehl wird ein Rollout beendet, dessen Name und ResourceGroup den Namen-und ResourceGroupName-Eigenschaften der $rolloutObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b9a81-120">This command stops a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="b9a81-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9a81-121">PARAMETERS</span></span>

### <span data-ttu-id="b9a81-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9a81-122">-DefaultProfile</span></span>
<span data-ttu-id="b9a81-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b9a81-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9a81-124">-Force</span><span class="sxs-lookup"><span data-stu-id="b9a81-124">-Force</span></span>
<span data-ttu-id="b9a81-125">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="b9a81-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b9a81-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b9a81-126">-InputObject</span></span>
<span data-ttu-id="b9a81-127">Der Rollout, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b9a81-127">The rollout to be removed.</span></span>

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

### <span data-ttu-id="b9a81-128">-Name</span><span class="sxs-lookup"><span data-stu-id="b9a81-128">-Name</span></span>
<span data-ttu-id="b9a81-129">Der Name des Rollouts.</span><span class="sxs-lookup"><span data-stu-id="b9a81-129">The name of the rollout.</span></span>

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

### <span data-ttu-id="b9a81-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9a81-130">-ResourceGroupName</span></span>
<span data-ttu-id="b9a81-131">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b9a81-131">The resource group.</span></span>

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

### <span data-ttu-id="b9a81-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b9a81-132">-ResourceId</span></span>
<span data-ttu-id="b9a81-133">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="b9a81-133">The resource identifier.</span></span>

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

### <span data-ttu-id="b9a81-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b9a81-134">-Confirm</span></span>
<span data-ttu-id="b9a81-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b9a81-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9a81-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9a81-136">-WhatIf</span></span>
<span data-ttu-id="b9a81-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b9a81-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9a81-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b9a81-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9a81-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9a81-139">CommonParameters</span></span>
<span data-ttu-id="b9a81-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9a81-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9a81-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9a81-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9a81-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b9a81-142">INPUTS</span></span>

### <span data-ttu-id="b9a81-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b9a81-143">System.String</span></span>

### <span data-ttu-id="b9a81-144">Microsoft. Azure. Commands. deploymentmanager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="b9a81-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="b9a81-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b9a81-145">OUTPUTS</span></span>

### <span data-ttu-id="b9a81-146">Microsoft. Azure. Commands. deploymentmanager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="b9a81-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="b9a81-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="b9a81-147">NOTES</span></span>

## <span data-ttu-id="b9a81-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b9a81-148">RELATED LINKS</span></span>
