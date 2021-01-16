---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 7323883028d062cf11f4e1befe1ea42cb1f8bcb2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297819"
---
# <span data-ttu-id="5729b-101">Remove-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="5729b-101">Remove-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="5729b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5729b-102">SYNOPSIS</span></span>
<span data-ttu-id="5729b-103">Löscht die Diensttopologie.</span><span class="sxs-lookup"><span data-stu-id="5729b-103">Deletes the service topology.</span></span> <span data-ttu-id="5729b-104">Alle dienste, die unter einer Diensttopologie erstellt wurden, müssen gelöscht werden, bevor die Diensttopologie gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="5729b-104">All services created under a service topology need to be deleted before deleting the service topology.</span></span>

## <span data-ttu-id="5729b-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5729b-105">SYNTAX</span></span>

### <span data-ttu-id="5729b-106">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="5729b-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5729b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5729b-107">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5729b-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="5729b-108">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5729b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5729b-109">DESCRIPTION</span></span>
<span data-ttu-id="5729b-110">Das **Cmdlet "Remove-AzDeploymentManagerServiceTopology"** löscht eine Diensttopologie.</span><span class="sxs-lookup"><span data-stu-id="5729b-110">The **Remove-AzDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="5729b-111">Geben Sie die Diensttopologie durch ihren Namen und den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="5729b-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="5729b-112">Alternativ können Sie das Objekt "ServiceTopology" oder die "ResourceId" bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5729b-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="5729b-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5729b-113">EXAMPLES</span></span>

### <span data-ttu-id="5729b-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5729b-114">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="5729b-115">Mit diesem Befehl wird eine Diensttopologie namens "ContosoServiceTopology" in der ContosoResourceGroup gelöscht.</span><span class="sxs-lookup"><span data-stu-id="5729b-115">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="5729b-116">Beispiel 2: Löschen einer Diensttopologie mithilfe des Ressourcenbezeichners.</span><span class="sxs-lookup"><span data-stu-id="5729b-116">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="5729b-117">Mit diesem Befehl wird eine Diensttopologie mit dem Namen "ContosoServiceTopology" in der ContosoResourceGroup gelöscht.</span><span class="sxs-lookup"><span data-stu-id="5729b-117">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="5729b-118">Beispiel 3: Löschen einer Diensttopologie mithilfe des Diensttopologieobjekts.</span><span class="sxs-lookup"><span data-stu-id="5729b-118">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="5729b-119">Mit diesem Befehl wird eine Diensttopologie gelöscht, deren Name und Ressourcengruppe mit den Eigenschaften "Name" bzw. "ResourceGroupName" des $serviceTopologyObject übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="5729b-119">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="5729b-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5729b-120">PARAMETERS</span></span>

### <span data-ttu-id="5729b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5729b-121">-DefaultProfile</span></span>
<span data-ttu-id="5729b-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5729b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5729b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5729b-123">-InputObject</span></span>
<span data-ttu-id="5729b-124">Die ressource, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5729b-124">The resource to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5729b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="5729b-125">-Name</span></span>
<span data-ttu-id="5729b-126">Der Name der Diensttopologie.</span><span class="sxs-lookup"><span data-stu-id="5729b-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="5729b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5729b-127">-PassThru</span></span>
<span data-ttu-id="5729b-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="5729b-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5729b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5729b-129">-ResourceGroupName</span></span>
<span data-ttu-id="5729b-130">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5729b-130">The resource group.</span></span>

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

### <span data-ttu-id="5729b-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5729b-131">-ResourceId</span></span>
<span data-ttu-id="5729b-132">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="5729b-132">The resource identifier.</span></span>

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

### <span data-ttu-id="5729b-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5729b-133">-Confirm</span></span>
<span data-ttu-id="5729b-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5729b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5729b-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5729b-135">-WhatIf</span></span>
<span data-ttu-id="5729b-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5729b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5729b-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5729b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5729b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5729b-138">CommonParameters</span></span>
<span data-ttu-id="5729b-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5729b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5729b-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5729b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5729b-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5729b-141">INPUTS</span></span>

### <span data-ttu-id="5729b-142">System.String</span><span class="sxs-lookup"><span data-stu-id="5729b-142">System.String</span></span>

### <span data-ttu-id="5729b-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="5729b-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="5729b-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5729b-144">OUTPUTS</span></span>

### <span data-ttu-id="5729b-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5729b-145">System.Boolean</span></span>

## <span data-ttu-id="5729b-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5729b-146">NOTES</span></span>

## <span data-ttu-id="5729b-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5729b-147">RELATED LINKS</span></span>
