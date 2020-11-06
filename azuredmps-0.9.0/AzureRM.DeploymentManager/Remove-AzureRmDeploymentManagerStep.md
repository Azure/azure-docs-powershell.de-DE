---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: 3abceb6c3c270378c911036967698f459cbe063a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474817"
---
# <span data-ttu-id="84f71-101">Remove-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="84f71-101">Remove-AzureRmDeploymentManagerStep</span></span>

## <span data-ttu-id="84f71-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="84f71-102">SYNOPSIS</span></span>
<span data-ttu-id="84f71-103">Löscht einen Schritt.</span><span class="sxs-lookup"><span data-stu-id="84f71-103">Deletes a step.</span></span>

## <span data-ttu-id="84f71-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="84f71-104">SYNTAX</span></span>

### <span data-ttu-id="84f71-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="84f71-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84f71-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="84f71-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerStep [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84f71-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="84f71-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerStep [-Step] <PSStepResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84f71-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="84f71-108">DESCRIPTION</span></span>
<span data-ttu-id="84f71-109">Das Cmdlet **Remove-AzureRmDeploymentManagerStep** löscht einen Schritt.</span><span class="sxs-lookup"><span data-stu-id="84f71-109">The **Remove-AzureRmDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="84f71-110">Geben Sie den Schritt mit dem Namen und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="84f71-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="84f71-111">Alternativ können Sie das Step-Objekt oder die "Resourcen-Nr" angeben.</span><span class="sxs-lookup"><span data-stu-id="84f71-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="84f71-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="84f71-112">EXAMPLES</span></span>
### <span data-ttu-id="84f71-113">Beispiel 1: Entfernen eines Schritts</span><span class="sxs-lookup"><span data-stu-id="84f71-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="84f71-114">Dieser Befehl löscht einen Schritt mit dem Namen ContosoService1WaitStep in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="84f71-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="84f71-115">Beispiel 2: Entfernen eines Schritts mit dem Ressourcenbezeichner</span><span class="sxs-lookup"><span data-stu-id="84f71-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="84f71-116">Dieser Befehl löscht einen Schritt mit dem Namen ContosoService1WaitStep in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="84f71-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="84f71-117">Beispiel 3: Entfernen eines Schritts mit einem von New-AzureRmDeploymentManagerStep zurückgegebenen Objekt</span><span class="sxs-lookup"><span data-stu-id="84f71-117">Example 3: Remove a step using an object returned by New-AzureRmDeploymentManagerStep</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerStep -Step $stepObject
```

 <span data-ttu-id="84f71-118">Dieser Befehl löscht einen Schritt, dessen Name und ResourceGroup den Namen-und ResourceGroupName-Eigenschaften der $stepObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="84f71-118">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="84f71-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="84f71-119">PARAMETERS</span></span>

### <span data-ttu-id="84f71-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84f71-120">-DefaultProfile</span></span>
<span data-ttu-id="84f71-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="84f71-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84f71-122">-Force</span><span class="sxs-lookup"><span data-stu-id="84f71-122">-Force</span></span>
<span data-ttu-id="84f71-123">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="84f71-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="84f71-124">-Name</span><span class="sxs-lookup"><span data-stu-id="84f71-124">-Name</span></span>
<span data-ttu-id="84f71-125">Der Name des Schritts.</span><span class="sxs-lookup"><span data-stu-id="84f71-125">The name of the step.</span></span>

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

### <span data-ttu-id="84f71-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84f71-126">-PassThru</span></span>
<span data-ttu-id="84f71-127">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="84f71-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="84f71-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84f71-128">-ResourceGroupName</span></span>
<span data-ttu-id="84f71-129">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="84f71-129">The resource group.</span></span>

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

### <span data-ttu-id="84f71-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="84f71-130">-ResourceId</span></span>
<span data-ttu-id="84f71-131">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="84f71-131">The resource identifier.</span></span>

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

### <span data-ttu-id="84f71-132">-Step</span><span class="sxs-lookup"><span data-stu-id="84f71-132">-Step</span></span>
<span data-ttu-id="84f71-133">Der Schritt, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="84f71-133">The step to be removed.</span></span>

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

### <span data-ttu-id="84f71-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="84f71-134">-Confirm</span></span>
<span data-ttu-id="84f71-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="84f71-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84f71-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84f71-136">-WhatIf</span></span>
<span data-ttu-id="84f71-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="84f71-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84f71-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="84f71-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84f71-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84f71-139">CommonParameters</span></span>
<span data-ttu-id="84f71-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84f71-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="84f71-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84f71-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84f71-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="84f71-142">INPUTS</span></span>

### <span data-ttu-id="84f71-143">System. String</span><span class="sxs-lookup"><span data-stu-id="84f71-143">System.String</span></span>

### <span data-ttu-id="84f71-144">Microsoft. Azure. Commands. deploymentmanager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="84f71-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="84f71-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="84f71-145">OUTPUTS</span></span>

### <span data-ttu-id="84f71-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="84f71-146">System.Boolean</span></span>

## <span data-ttu-id="84f71-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="84f71-147">NOTES</span></span>

## <span data-ttu-id="84f71-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="84f71-148">RELATED LINKS</span></span>
