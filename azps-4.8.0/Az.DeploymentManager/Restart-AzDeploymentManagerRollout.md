---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/restart-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
ms.openlocfilehash: ba7b62d42764f5098868e6a15eb073cb6b898e82
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173014"
---
# <span data-ttu-id="d58f8-101">Restart-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="d58f8-101">Restart-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="d58f8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d58f8-102">SYNOPSIS</span></span>
<span data-ttu-id="d58f8-103">Startet einen fehlgeschlagenen Rollout erneut.</span><span class="sxs-lookup"><span data-stu-id="d58f8-103">Restarts a failed rollout.</span></span>

## <span data-ttu-id="d58f8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d58f8-104">SYNTAX</span></span>

### <span data-ttu-id="d58f8-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="d58f8-105">Interactive (Default)</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d58f8-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d58f8-106">ResourceId</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceId] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d58f8-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="d58f8-107">InputObject</span></span>
```
Restart-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d58f8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d58f8-108">DESCRIPTION</span></span>
<span data-ttu-id="d58f8-109">Mit dem Cmdlet " **Restart-AzDeploymentManagerRollout** " wird ein fehlgeschlagener Rollout neu gestartet, und es wird ein Objekt zurückgegeben, das diesen Rollout mit allen detaillierten Informationen zum Fortschritt des Rollouts darstellt.</span><span class="sxs-lookup"><span data-stu-id="d58f8-109">The **Restart-AzDeploymentManagerRollout** cmdlet restarts a failed rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="d58f8-110">Geben Sie den Rollout nach dem Namen und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="d58f8-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="d58f8-111">Alternativ können Sie das Rollout-Objekt oder die "Resourcen-Nr" bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d58f8-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>
<span data-ttu-id="d58f8-112">Mit dem optionalen Parameter SkipSucceeded können Sie alle erfolgreichen Schritte in der vorherigen Ausführung des Rollouts überspringen.</span><span class="sxs-lookup"><span data-stu-id="d58f8-112">Optional parameter SkipSucceeded allows you to skip all the succeeded steps in the previous run of the rollout.</span></span>

## <span data-ttu-id="d58f8-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d58f8-113">EXAMPLES</span></span>

### <span data-ttu-id="d58f8-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d58f8-114">Example 1</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="d58f8-115">Mit diesem Befehl wird ein Rollout mit dem Namen ContosoRollout im ContosoResourceGroup neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="d58f8-115">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="d58f8-116">Das SkipSucceeded-Flag gibt an, dass alle bereits erfolgreich ausgeführten Schritte übersprungen werden sollten und dass der Rollout weiterhin ausgeführt werden soll, wenn der letzte Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="d58f8-116">The SkipSucceeded flag indicates that all the steps that already ran successfully should be skipped and the rollout should continue execution from where it last failed.</span></span>

### <span data-ttu-id="d58f8-117">Beispiel 2: Erneutes Starten eines Rollouts mit dem Ressourcenbezeichner</span><span class="sxs-lookup"><span data-stu-id="d58f8-117">Example 2: Restart a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="d58f8-118">Mit diesem Befehl wird ein Rollout mit dem Namen ContosoRollout im ContosoResourceGroup neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="d58f8-118">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="d58f8-119">Beispiel 3: Starten Sie einen Rollout mit dem Rollout-Objekt neu.</span><span class="sxs-lookup"><span data-stu-id="d58f8-119">Example 3: Restart a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="d58f8-120">Mit diesem Befehl wird ein Rollout neu gestartet, dessen Name und ResourceGroup den Namen-und ResourceGroupName-Eigenschaften der $rolloutObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d58f8-120">This command restarts a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="d58f8-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="d58f8-121">PARAMETERS</span></span>

### <span data-ttu-id="d58f8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d58f8-122">-DefaultProfile</span></span>
<span data-ttu-id="d58f8-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d58f8-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d58f8-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d58f8-124">-InputObject</span></span>
<span data-ttu-id="d58f8-125">Die Ressource, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d58f8-125">The resource to be removed.</span></span>

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

### <span data-ttu-id="d58f8-126">-Name</span><span class="sxs-lookup"><span data-stu-id="d58f8-126">-Name</span></span>
<span data-ttu-id="d58f8-127">Der Name des Rollouts.</span><span class="sxs-lookup"><span data-stu-id="d58f8-127">The name of the rollout.</span></span>

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

### <span data-ttu-id="d58f8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d58f8-128">-ResourceGroupName</span></span>
<span data-ttu-id="d58f8-129">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d58f8-129">The resource group.</span></span>

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

### <span data-ttu-id="d58f8-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d58f8-130">-ResourceId</span></span>
<span data-ttu-id="d58f8-131">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="d58f8-131">The resource identifier.</span></span>

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

### <span data-ttu-id="d58f8-132">-SkipSucceeded</span><span class="sxs-lookup"><span data-stu-id="d58f8-132">-SkipSucceeded</span></span>
<span data-ttu-id="d58f8-133">Überspringen Sie die Schritte, die bei der vorherigen Ausführung des Rollouts erfolgreich waren.</span><span class="sxs-lookup"><span data-stu-id="d58f8-133">Skip steps that succeeded in the previous run of the rollout.</span></span>

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

### <span data-ttu-id="d58f8-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d58f8-134">-Confirm</span></span>
<span data-ttu-id="d58f8-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d58f8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d58f8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d58f8-136">-WhatIf</span></span>
<span data-ttu-id="d58f8-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d58f8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d58f8-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d58f8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d58f8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d58f8-139">CommonParameters</span></span>
<span data-ttu-id="d58f8-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d58f8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d58f8-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d58f8-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d58f8-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d58f8-142">INPUTS</span></span>

### <span data-ttu-id="d58f8-143">System. String</span><span class="sxs-lookup"><span data-stu-id="d58f8-143">System.String</span></span>

### <span data-ttu-id="d58f8-144">Microsoft. Azure. Commands. deploymentmanager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="d58f8-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="d58f8-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d58f8-145">OUTPUTS</span></span>

### <span data-ttu-id="d58f8-146">Microsoft. Azure. Commands. deploymentmanager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="d58f8-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="d58f8-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="d58f8-147">NOTES</span></span>

## <span data-ttu-id="d58f8-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d58f8-148">RELATED LINKS</span></span>
