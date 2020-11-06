---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: f329468dce9c520eb647bb0d927ba91de64a5c33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474730"
---
# <span data-ttu-id="86ec2-101">Remove-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="86ec2-101">Remove-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="86ec2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="86ec2-102">SYNOPSIS</span></span>
<span data-ttu-id="86ec2-103">Löscht einen Rollout.</span><span class="sxs-lookup"><span data-stu-id="86ec2-103">Deletes a rollout.</span></span>

## <span data-ttu-id="86ec2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="86ec2-104">SYNTAX</span></span>

### <span data-ttu-id="86ec2-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="86ec2-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86ec2-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="86ec2-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86ec2-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="86ec2-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86ec2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="86ec2-108">DESCRIPTION</span></span>
<span data-ttu-id="86ec2-109">Das Cmdlet **Remove-AzureRmDeploymentManagerRollout** löscht ein Rollout in einem Terminal Zustand.</span><span class="sxs-lookup"><span data-stu-id="86ec2-109">The **Remove-AzureRmDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="86ec2-110">Geben Sie den Rollout nach dem Namen und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="86ec2-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="86ec2-111">Alternativ können Sie das Rollout-Objekt oder die "Resourcen-Nr" bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="86ec2-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="86ec2-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="86ec2-112">EXAMPLES</span></span>

### <span data-ttu-id="86ec2-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="86ec2-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="86ec2-114">Dieser Befehl löscht ein Rollout mit dem Namen ContosoRollout in der ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="86ec2-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="86ec2-115">Beispiel 2: Löschen eines Rollouts mit dem Ressourcenbezeichner</span><span class="sxs-lookup"><span data-stu-id="86ec2-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="86ec2-116">Dieser Befehl löscht ein Rollout mit dem Namen ContosoRollout in der ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="86ec2-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="86ec2-117">Beispiel 3: Löschen eines Rollouts mit dem Rollout-Objekt</span><span class="sxs-lookup"><span data-stu-id="86ec2-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="86ec2-118">Mit diesem Befehl wird ein Rollout gelöscht, dessen Name und ResourceGroup den Namen-und ResourceGroupName-Eigenschaften der $rolloutObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="86ec2-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="86ec2-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="86ec2-119">PARAMETERS</span></span>

### <span data-ttu-id="86ec2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86ec2-120">-DefaultProfile</span></span>
<span data-ttu-id="86ec2-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="86ec2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86ec2-122">-Force</span><span class="sxs-lookup"><span data-stu-id="86ec2-122">-Force</span></span>
<span data-ttu-id="86ec2-123">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="86ec2-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="86ec2-124">-Name</span><span class="sxs-lookup"><span data-stu-id="86ec2-124">-Name</span></span>
<span data-ttu-id="86ec2-125">Der Name des Rollouts.</span><span class="sxs-lookup"><span data-stu-id="86ec2-125">The name of the rollout.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86ec2-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86ec2-126">-PassThru</span></span>
<span data-ttu-id="86ec2-127">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="86ec2-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="86ec2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86ec2-128">-ResourceGroupName</span></span>
<span data-ttu-id="86ec2-129">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="86ec2-129">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86ec2-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="86ec2-130">-ResourceId</span></span>
<span data-ttu-id="86ec2-131">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="86ec2-131">The resource identifier.</span></span>

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

### <span data-ttu-id="86ec2-132">-Rollout</span><span class="sxs-lookup"><span data-stu-id="86ec2-132">-Rollout</span></span>
<span data-ttu-id="86ec2-133">Die Ressource, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="86ec2-133">The resource to be removed.</span></span>

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

### <span data-ttu-id="86ec2-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="86ec2-134">-Confirm</span></span>
<span data-ttu-id="86ec2-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="86ec2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86ec2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86ec2-136">-WhatIf</span></span>
<span data-ttu-id="86ec2-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="86ec2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86ec2-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="86ec2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86ec2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86ec2-139">CommonParameters</span></span>
<span data-ttu-id="86ec2-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86ec2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86ec2-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86ec2-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86ec2-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="86ec2-142">INPUTS</span></span>

### <span data-ttu-id="86ec2-143">Microsoft. Azure. Commands. deploymentmanager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="86ec2-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="86ec2-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="86ec2-144">OUTPUTS</span></span>

### <span data-ttu-id="86ec2-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="86ec2-145">System.Boolean</span></span>

## <span data-ttu-id="86ec2-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="86ec2-146">NOTES</span></span>

## <span data-ttu-id="86ec2-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="86ec2-147">RELATED LINKS</span></span>

[<span data-ttu-id="86ec2-148">Get-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="86ec2-148">Get-AzureRmDeploymentManagerRollout</span></span>](./Get-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="86ec2-149">Stopp-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="86ec2-149">Stop-AzureRmDeploymentManagerRollout</span></span>](./Stop-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="86ec2-150">Neustart-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="86ec2-150">Restart-AzureRmDeploymentManagerRollout</span></span>](./Restart-AzureRmDeploymentManagerRollout.md)