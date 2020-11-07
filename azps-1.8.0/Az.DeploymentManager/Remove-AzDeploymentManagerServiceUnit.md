---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 3ba27cf26ccc555ea79a2b46100bee6be7e3c7fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661189"
---
# <span data-ttu-id="efd78-101">Remove-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="efd78-101">Remove-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="efd78-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="efd78-102">SYNOPSIS</span></span>
<span data-ttu-id="efd78-103">Löscht die Serviceeinheit.</span><span class="sxs-lookup"><span data-stu-id="efd78-103">Deletes the service unit.</span></span>

## <span data-ttu-id="efd78-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="efd78-104">SYNTAX</span></span>

### <span data-ttu-id="efd78-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="efd78-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efd78-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="efd78-106">ByTopologyObjectAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efd78-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="efd78-107">ByTopologyResourceAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efd78-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="efd78-108">ByServiceObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efd78-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="efd78-109">ByServiceResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efd78-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="efd78-110">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efd78-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="efd78-111">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efd78-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="efd78-112">DESCRIPTION</span></span>
<span data-ttu-id="efd78-113">Das Cmdlet **Remove-AzDeploymentManagerServiceUnit** löscht eine Diensteinheit in einem Dienst.</span><span class="sxs-lookup"><span data-stu-id="efd78-113">The **Remove-AzDeploymentManagerServiceUnit** cmdlet deletes a service unit in a service.</span></span>

<span data-ttu-id="efd78-114">Geben Sie die Diensteinheit nach dem Namen, dem Dienst, unter dem Sie definiert wurde, dem Namen der Dienst Topologie und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="efd78-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="efd78-115">Alternativ können Sie das Serviceunit-Objekt oder die resourcecode-Objekt bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="efd78-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

## <span data-ttu-id="efd78-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="efd78-116">EXAMPLES</span></span>

### <span data-ttu-id="efd78-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="efd78-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="efd78-118">Dieser Befehl löscht eine Diensteinheit namens ContosoService1Storage unter einem Dienst ContosoService1 in einer Dienst Topologie mit dem Namen ContosoServiceTopology im ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="efd78-118">This command deletes a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="efd78-119">Beispiel 2: Löschen einer Diensteinheit mithilfe der Ressourcenkennung</span><span class="sxs-lookup"><span data-stu-id="efd78-119">Example 2: Delete a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="efd78-120">Dieser Befehl ruft eine Diensteinheit mit dem Namen ContosoService1Storage unter einem Dienst ContosoService1 in einer Dienst Topologie mit dem Namen ContosoServiceTopology im ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="efd78-120">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="efd78-121">Beispiel 3: Löschen einer Serviceeinheit mithilfe des Service Unit-Objekts.</span><span class="sxs-lookup"><span data-stu-id="efd78-121">Example 3: Delete a service unit using the service unit object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="efd78-122">Mit diesem Befehl wird eine Diensteinheit gelöscht, deren Name, Dienstname, Dienst topologiename und ResourceGroup mit den Eigenschaften Name, Service Name, ServiceTopologyName und ResourceGroupName der $serviceUnitObject übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="efd78-122">This command deletes a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="efd78-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="efd78-123">PARAMETERS</span></span>

### <span data-ttu-id="efd78-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efd78-124">-DefaultProfile</span></span>
<span data-ttu-id="efd78-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="efd78-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efd78-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="efd78-126">-InputObject</span></span>
<span data-ttu-id="efd78-127">Ressourcenobjekt der Diensteinheit.</span><span class="sxs-lookup"><span data-stu-id="efd78-127">Service unit resource object.</span></span>

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

### <span data-ttu-id="efd78-128">-Name</span><span class="sxs-lookup"><span data-stu-id="efd78-128">-Name</span></span>
<span data-ttu-id="efd78-129">Der Name der Serviceeinheit.</span><span class="sxs-lookup"><span data-stu-id="efd78-129">The name of the service unit.</span></span>

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

### <span data-ttu-id="efd78-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="efd78-130">-PassThru</span></span>
<span data-ttu-id="efd78-131">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="efd78-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="efd78-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efd78-132">-ResourceGroupName</span></span>
<span data-ttu-id="efd78-133">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="efd78-133">The resource group.</span></span>

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

### <span data-ttu-id="efd78-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="efd78-134">-ResourceId</span></span>
<span data-ttu-id="efd78-135">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="efd78-135">The resource identifier.</span></span>

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

### <span data-ttu-id="efd78-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="efd78-136">-ServiceName</span></span>
<span data-ttu-id="efd78-137">Der Name des Diensts, zu dem die Serviceeinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="efd78-137">The name of the service the service unit is part of.</span></span>

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

### <span data-ttu-id="efd78-138">-Serviceobject</span><span class="sxs-lookup"><span data-stu-id="efd78-138">-ServiceObject</span></span>
<span data-ttu-id="efd78-139">Das Dienstobjekt, in dem die Serviceeinheit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="efd78-139">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="efd78-140">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="efd78-140">-ServiceResourceId</span></span>
<span data-ttu-id="efd78-141">Der Dienst Ressourcenbezeichner, in dem die Diensteinheit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="efd78-141">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="efd78-142">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="efd78-142">-ServiceTopologyName</span></span>
<span data-ttu-id="efd78-143">Der Name der Dienst Topologie, zu der die Serviceeinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="efd78-143">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="efd78-144">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="efd78-144">-ServiceTopologyObject</span></span>
<span data-ttu-id="efd78-145">Das Service Topology-Objekt, in dem die Diensteinheit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="efd78-145">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="efd78-146">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="efd78-146">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="efd78-147">Der Dienst Topologie-Ressourcenbezeichner, in dem die Diensteinheit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="efd78-147">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="efd78-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="efd78-148">-Confirm</span></span>
<span data-ttu-id="efd78-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="efd78-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efd78-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efd78-150">-WhatIf</span></span>
<span data-ttu-id="efd78-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="efd78-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efd78-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="efd78-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efd78-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efd78-153">CommonParameters</span></span>
<span data-ttu-id="efd78-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efd78-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efd78-155">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efd78-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efd78-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="efd78-156">INPUTS</span></span>

### <span data-ttu-id="efd78-157">System. String</span><span class="sxs-lookup"><span data-stu-id="efd78-157">System.String</span></span>

### <span data-ttu-id="efd78-158">Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="efd78-158">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="efd78-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="efd78-159">OUTPUTS</span></span>

### <span data-ttu-id="efd78-160">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="efd78-160">System.Boolean</span></span>

## <span data-ttu-id="efd78-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="efd78-161">NOTES</span></span>

## <span data-ttu-id="efd78-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="efd78-162">RELATED LINKS</span></span>
