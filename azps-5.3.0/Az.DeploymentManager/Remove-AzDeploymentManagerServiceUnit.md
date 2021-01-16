---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: d4248a13282824c60e698b2257b3e38a78ce3a6f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387343"
---
# <span data-ttu-id="2f5f4-101">Remove-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="2f5f4-101">Remove-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="2f5f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f5f4-102">SYNOPSIS</span></span>
<span data-ttu-id="2f5f4-103">Löscht die Diensteinheit.</span><span class="sxs-lookup"><span data-stu-id="2f5f4-103">Deletes the service unit.</span></span>

## <span data-ttu-id="2f5f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f5f4-104">SYNTAX</span></span>

### <span data-ttu-id="2f5f4-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="2f5f4-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f5f4-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="2f5f4-106">ByTopologyObjectAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f5f4-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="2f5f4-107">ByTopologyResourceAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f5f4-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="2f5f4-108">ByServiceObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f5f4-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="2f5f4-109">ByServiceResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f5f4-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f5f4-110">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f5f4-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="2f5f4-111">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f5f4-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2f5f4-112">DESCRIPTION</span></span>
<span data-ttu-id="2f5f4-113">Das **Cmdlet "Remove-AzDeploymentManagerServiceUnit"** löscht eine Diensteinheit in einem Dienst.</span><span class="sxs-lookup"><span data-stu-id="2f5f4-113">The **Remove-AzDeploymentManagerServiceUnit** cmdlet deletes a service unit in a service.</span></span>

<span data-ttu-id="2f5f4-114">Geben Sie die Diensteinheit durch ihren Namen, den Dienst, unter dem sie definiert wurde, den Namen der Diensttopologie und den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2f5f4-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="2f5f4-115">Alternativ können Sie das Objekt "ServiceUnit" oder die "ResourceId" bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="2f5f4-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

## <span data-ttu-id="2f5f4-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2f5f4-116">EXAMPLES</span></span>

### <span data-ttu-id="2f5f4-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2f5f4-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="2f5f4-118">Mit diesem Befehl wird eine Diensteinheit namens "ContosoService1Storage" unter einem Dienst "ContosoService1" in einer Diensttopologie namens "ContosoServiceTopology" in der ContosoResourceGroup gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2f5f4-118">This command deletes a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="2f5f4-119">Beispiel 2: Löschen einer Diensteinheit mithilfe des Ressourcenbezeichners.</span><span class="sxs-lookup"><span data-stu-id="2f5f4-119">Example 2: Delete a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="2f5f4-120">Dieser Befehl ruft eine Diensteinheit namens "ContosoService1Storage" unter einem Dienst "ContosoService1" in einer Diensttopologie namens "ContosoServiceTopology" in der ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="2f5f4-120">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="2f5f4-121">Beispiel 3: Löschen einer Diensteinheit mithilfe des Diensteinheitsobjekts.</span><span class="sxs-lookup"><span data-stu-id="2f5f4-121">Example 3: Delete a service unit using the service unit object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="2f5f4-122">Mit diesem Befehl wird eine Diensteinheit gelöscht, deren Name, Dienstname, Name der Diensttopologie und Ressourcengruppe mit den Eigenschaften "Name", "ServiceName", "ServiceTopologyName" bzw. "ResourceGroupName" der $serviceUnitObject übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="2f5f4-122">This command deletes a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="2f5f4-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f5f4-123">PARAMETERS</span></span>

### <span data-ttu-id="2f5f4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f5f4-124">-DefaultProfile</span></span>
<span data-ttu-id="2f5f4-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2f5f4-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f5f4-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f5f4-126">-InputObject</span></span>
<span data-ttu-id="2f5f4-127">Ressourcenobjekt der Diensteinheit.</span><span class="sxs-lookup"><span data-stu-id="2f5f4-127">Service unit resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f5f4-128">-Name</span><span class="sxs-lookup"><span data-stu-id="2f5f4-128">-Name</span></span>
<span data-ttu-id="2f5f4-129">Der Name der Diensteinheit.</span><span class="sxs-lookup"><span data-stu-id="2f5f4-129">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName, ByServiceObject, ByServiceResourceId
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f5f4-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f5f4-130">-PassThru</span></span>
<span data-ttu-id="2f5f4-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="2f5f4-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2f5f4-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f5f4-132">-ResourceGroupName</span></span>
<span data-ttu-id="2f5f4-133">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2f5f4-133">The resource group.</span></span>

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

### <span data-ttu-id="2f5f4-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f5f4-134">-ResourceId</span></span>
<span data-ttu-id="2f5f4-135">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="2f5f4-135">The resource identifier.</span></span>

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

### <span data-ttu-id="2f5f4-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2f5f4-136">-ServiceName</span></span>
<span data-ttu-id="2f5f4-137">Der Name des Diensts, zu dem die Diensteinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="2f5f4-137">The name of the service the service unit is part of.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f5f4-138">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="2f5f4-138">-ServiceObject</span></span>
<span data-ttu-id="2f5f4-139">Das Dienstobjekt, in dem die Diensteinheit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2f5f4-139">The service object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: ByServiceObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f5f4-140">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="2f5f4-140">-ServiceResourceId</span></span>
<span data-ttu-id="2f5f4-141">Der Bezeichner der Dienstressource, in dem die Diensteinheit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2f5f4-141">The service resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f5f4-142">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="2f5f4-142">-ServiceTopologyName</span></span>
<span data-ttu-id="2f5f4-143">Der Name der Diensttopologie, zu der die Diensteinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="2f5f4-143">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="2f5f4-144">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="2f5f4-144">-ServiceTopologyObject</span></span>
<span data-ttu-id="2f5f4-145">Das Diensttopologieobjekt, in dem die Diensteinheit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2f5f4-145">The service topology object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByTopologyObjectAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f5f4-146">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="2f5f4-146">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="2f5f4-147">Der Ressourcenbezeichner für die Diensttopologie, in dem die Diensteinheit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2f5f4-147">The service topology resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f5f4-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f5f4-148">-Confirm</span></span>
<span data-ttu-id="2f5f4-149">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2f5f4-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f5f4-150">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2f5f4-150">-WhatIf</span></span>
<span data-ttu-id="2f5f4-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2f5f4-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f5f4-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f5f4-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f5f4-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f5f4-153">CommonParameters</span></span>
<span data-ttu-id="2f5f4-154">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f5f4-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f5f4-155">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f5f4-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f5f4-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2f5f4-156">INPUTS</span></span>

### <span data-ttu-id="2f5f4-157">System.String</span><span class="sxs-lookup"><span data-stu-id="2f5f4-157">System.String</span></span>

### <span data-ttu-id="2f5f4-158">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="2f5f4-158">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="2f5f4-159">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2f5f4-159">OUTPUTS</span></span>

### <span data-ttu-id="2f5f4-160">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2f5f4-160">System.Boolean</span></span>

## <span data-ttu-id="2f5f4-161">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2f5f4-161">NOTES</span></span>

## <span data-ttu-id="2f5f4-162">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2f5f4-162">RELATED LINKS</span></span>
