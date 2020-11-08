---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
ms.openlocfilehash: 5e4af2ef006e51cee135dd642bcae7282940e8be
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004583"
---
# <span data-ttu-id="1fb5e-101">Remove-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="1fb5e-101">Remove-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="1fb5e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1fb5e-102">SYNOPSIS</span></span>
<span data-ttu-id="1fb5e-103">Löscht den Schritt.</span><span class="sxs-lookup"><span data-stu-id="1fb5e-103">Deletes the step.</span></span>

## <span data-ttu-id="1fb5e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1fb5e-104">SYNTAX</span></span>

### <span data-ttu-id="1fb5e-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="1fb5e-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fb5e-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fb5e-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fb5e-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="1fb5e-107">InputObject</span></span>
```
Remove-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fb5e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1fb5e-108">DESCRIPTION</span></span>
<span data-ttu-id="1fb5e-109">Das Cmdlet **Remove-AzDeploymentManagerStep** löscht einen Schritt.</span><span class="sxs-lookup"><span data-stu-id="1fb5e-109">The **Remove-AzDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="1fb5e-110">Geben Sie den Schritt mit dem Namen und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1fb5e-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="1fb5e-111">Alternativ können Sie das Step-Objekt oder die "Resourcen-Nr" angeben.</span><span class="sxs-lookup"><span data-stu-id="1fb5e-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="1fb5e-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1fb5e-112">EXAMPLES</span></span>

### <span data-ttu-id="1fb5e-113">Beispiel 1: Entfernen eines Schritts</span><span class="sxs-lookup"><span data-stu-id="1fb5e-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="1fb5e-114">Dieser Befehl löscht einen Schritt mit dem Namen ContosoService1WaitStep in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1fb5e-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="1fb5e-115">Beispiel 2: Entfernen eines Schritts mit dem Ressourcenbezeichner</span><span class="sxs-lookup"><span data-stu-id="1fb5e-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="1fb5e-116">Dieser Befehl löscht einen Schritt mit dem Namen ContosoService1WaitStep in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1fb5e-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="1fb5e-117">Beispiel 3: Entfernen eines Schritts mit einem von New-AzDeploymentManagerStep zurückgegebenen Objekt</span><span class="sxs-lookup"><span data-stu-id="1fb5e-117">Example 3: Remove a step using an object returned by New-AzDeploymentManagerStep</span></span>
### <span data-ttu-id="1fb5e-118">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1fb5e-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="1fb5e-119">Dieser Befehl löscht einen Schritt, dessen Name und ResourceGroup den Namen-und ResourceGroupName-Eigenschaften der $stepObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1fb5e-119">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="1fb5e-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="1fb5e-120">PARAMETERS</span></span>

### <span data-ttu-id="1fb5e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fb5e-121">-DefaultProfile</span></span>
<span data-ttu-id="1fb5e-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1fb5e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fb5e-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1fb5e-123">-InputObject</span></span>
<span data-ttu-id="1fb5e-124">Der Schritt, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1fb5e-124">The step to be removed.</span></span>

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

### <span data-ttu-id="1fb5e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="1fb5e-125">-Name</span></span>
<span data-ttu-id="1fb5e-126">Der Name des Schritts.</span><span class="sxs-lookup"><span data-stu-id="1fb5e-126">The name of the step.</span></span>

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

### <span data-ttu-id="1fb5e-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1fb5e-127">-PassThru</span></span>
<span data-ttu-id="1fb5e-128">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="1fb5e-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1fb5e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fb5e-129">-ResourceGroupName</span></span>
<span data-ttu-id="1fb5e-130">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1fb5e-130">The resource group.</span></span>

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

### <span data-ttu-id="1fb5e-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1fb5e-131">-ResourceId</span></span>
<span data-ttu-id="1fb5e-132">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="1fb5e-132">The resource identifier.</span></span>

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

### <span data-ttu-id="1fb5e-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1fb5e-133">-Confirm</span></span>
<span data-ttu-id="1fb5e-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1fb5e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fb5e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fb5e-135">-WhatIf</span></span>
<span data-ttu-id="1fb5e-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1fb5e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fb5e-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1fb5e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fb5e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fb5e-138">CommonParameters</span></span>
<span data-ttu-id="1fb5e-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fb5e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fb5e-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1fb5e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fb5e-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1fb5e-141">INPUTS</span></span>

### <span data-ttu-id="1fb5e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="1fb5e-142">System.String</span></span>

### <span data-ttu-id="1fb5e-143">Microsoft. Azure. Commands. deploymentmanager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="1fb5e-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="1fb5e-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1fb5e-144">OUTPUTS</span></span>

### <span data-ttu-id="1fb5e-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1fb5e-145">System.Boolean</span></span>

## <span data-ttu-id="1fb5e-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="1fb5e-146">NOTES</span></span>

## <span data-ttu-id="1fb5e-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1fb5e-147">RELATED LINKS</span></span>
