---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
ms.openlocfilehash: 284e568e1748c8bf6da3c5d43c27acb046be6172
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932960"
---
# <span data-ttu-id="81fac-101">Remove-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="81fac-101">Remove-AzDeploymentManagerService</span></span>

## <span data-ttu-id="81fac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81fac-102">SYNOPSIS</span></span>
<span data-ttu-id="81fac-103">Löscht den Dienst.</span><span class="sxs-lookup"><span data-stu-id="81fac-103">Deletes the service..</span></span> <span data-ttu-id="81fac-104">Alle service units created under a service need to be deleted before deleted the service.</span><span class="sxs-lookup"><span data-stu-id="81fac-104">All service units created under a service need to be deleted before deleting the service.</span></span>

## <span data-ttu-id="81fac-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81fac-105">SYNTAX</span></span>

### <span data-ttu-id="81fac-106">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="81fac-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="81fac-107">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="81fac-107">ByServiceTopologyObject</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81fac-108">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="81fac-108">ByServiceTopologyResourceId</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81fac-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="81fac-109">ResourceId</span></span>
```
Remove-AzDeploymentManagerService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81fac-110">InputObject</span><span class="sxs-lookup"><span data-stu-id="81fac-110">InputObject</span></span>
```
Remove-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81fac-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="81fac-111">DESCRIPTION</span></span>
<span data-ttu-id="81fac-112">Das **Cmdlet Remove-AzDeploymentManagerService** löscht einen Dienst unter einer Diensttopologie.</span><span class="sxs-lookup"><span data-stu-id="81fac-112">The **Remove-AzDeploymentManagerService** cmdlet deletes a service under a service topology.</span></span>
<span data-ttu-id="81fac-113">Geben Sie den Dienst nach seinem Namen, der Diensttopologie, in der er sich befindet, und dem Ressourcengruppennamen an.</span><span class="sxs-lookup"><span data-stu-id="81fac-113">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="81fac-114">Alternativ können Sie das Dienstobjekt oder die ResourceId bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="81fac-114">Alternately, you can provide the Service object or the ResourceId.</span></span>

## <span data-ttu-id="81fac-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="81fac-115">EXAMPLES</span></span>

### <span data-ttu-id="81fac-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="81fac-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="81fac-117">Mit diesem Befehl wird ein Dienst namens ContosoService1 in einer Diensttopologie namens ContosoServiceTopology in der ContosoResourceGroup gelöscht.</span><span class="sxs-lookup"><span data-stu-id="81fac-117">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="81fac-118">Beispiel 2: Löschen eines Diensts mit dem Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="81fac-118">Example 2: Delete a service using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="81fac-119">Mit diesem Befehl wird ein Dienst namens ContosoService1 in einer Diensttopologie namens ContosoServiceTopology in der ContosoResourceGroup gelöscht.</span><span class="sxs-lookup"><span data-stu-id="81fac-119">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="81fac-120">Beispiel 3: Löschen eines Diensts mit dem Dienstobjekt.</span><span class="sxs-lookup"><span data-stu-id="81fac-120">Example 3: Delete a service using the service object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="81fac-121">Mit diesem Befehl wird ein Dienst gelöscht, dessen Name, Diensttopologiename und Ressourcengruppe den Eigenschaften Name, ServiceTopologyName und ResourceGroupName des $serviceObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="81fac-121">This command deletes a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="81fac-122">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="81fac-122">PARAMETERS</span></span>

### <span data-ttu-id="81fac-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81fac-123">-DefaultProfile</span></span>
<span data-ttu-id="81fac-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="81fac-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81fac-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81fac-125">-InputObject</span></span>
<span data-ttu-id="81fac-126">Dienstobjekt.</span><span class="sxs-lookup"><span data-stu-id="81fac-126">Service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81fac-127">-Name</span><span class="sxs-lookup"><span data-stu-id="81fac-127">-Name</span></span>
<span data-ttu-id="81fac-128">Der Name des Diensts.</span><span class="sxs-lookup"><span data-stu-id="81fac-128">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81fac-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81fac-129">-PassThru</span></span>
<span data-ttu-id="81fac-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="81fac-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="81fac-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81fac-131">-ResourceGroupName</span></span>
<span data-ttu-id="81fac-132">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="81fac-132">The resource group.</span></span>

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

### <span data-ttu-id="81fac-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81fac-133">-ResourceId</span></span>
<span data-ttu-id="81fac-134">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="81fac-134">The resource identifier.</span></span>

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

### <span data-ttu-id="81fac-135">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="81fac-135">-ServiceTopologyName</span></span>
<span data-ttu-id="81fac-136">Der Name der Diensttopologie.</span><span class="sxs-lookup"><span data-stu-id="81fac-136">The name of the service topology.</span></span>

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

### <span data-ttu-id="81fac-137">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="81fac-137">-ServiceTopologyObject</span></span>
<span data-ttu-id="81fac-138">Das Diensttopologieobjekt, in dem der Dienst erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="81fac-138">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81fac-139">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="81fac-139">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="81fac-140">Der Ressourcenbezeichner der Diensttopologie, in dem der Dienst erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="81fac-140">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81fac-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="81fac-141">-Confirm</span></span>
<span data-ttu-id="81fac-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="81fac-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81fac-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81fac-143">-WhatIf</span></span>
<span data-ttu-id="81fac-144">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="81fac-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81fac-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="81fac-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81fac-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81fac-146">CommonParameters</span></span>
<span data-ttu-id="81fac-147">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81fac-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81fac-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81fac-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81fac-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="81fac-149">INPUTS</span></span>

### <span data-ttu-id="81fac-150">System.String</span><span class="sxs-lookup"><span data-stu-id="81fac-150">System.String</span></span>

### <span data-ttu-id="81fac-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="81fac-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="81fac-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="81fac-152">OUTPUTS</span></span>

### <span data-ttu-id="81fac-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="81fac-153">System.Boolean</span></span>

## <span data-ttu-id="81fac-154">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="81fac-154">NOTES</span></span>

## <span data-ttu-id="81fac-155">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="81fac-155">RELATED LINKS</span></span>
