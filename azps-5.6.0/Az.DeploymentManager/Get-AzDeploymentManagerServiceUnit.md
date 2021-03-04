---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/get-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 2910afe209a83e07e65cc04b9ffa371fe4ed72d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925792"
---
# <span data-ttu-id="4bc3a-101">Get-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="4bc3a-101">Get-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="4bc3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bc3a-102">SYNOPSIS</span></span>
<span data-ttu-id="4bc3a-103">Ruft die Diensteinheit ab.</span><span class="sxs-lookup"><span data-stu-id="4bc3a-103">Gets the service unit.</span></span>

## <span data-ttu-id="4bc3a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4bc3a-104">SYNTAX</span></span>

### <span data-ttu-id="4bc3a-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="4bc3a-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bc3a-106">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="4bc3a-106">ByServiceObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bc3a-107">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="4bc3a-107">ByServiceResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bc3a-108">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="4bc3a-108">ByTopologyObjectAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4bc3a-109">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="4bc3a-109">ByTopologyResourceAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bc3a-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4bc3a-110">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4bc3a-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="4bc3a-111">InputObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bc3a-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4bc3a-112">DESCRIPTION</span></span>
<span data-ttu-id="4bc3a-113">Das **Cmdlet Get-AzDeploymentManagerServiceUnit** ruft eine Diensteinheit in einem Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="4bc3a-113">The **Get-AzDeploymentManagerServiceUnit** cmdlet gets a service unit in a service.</span></span>

<span data-ttu-id="4bc3a-114">Geben Sie die Diensteinheit nach dem Namen, dem Dienst, unter dem sie definiert wurde, dem Namen der Diensttopologie und dem Ressourcengruppennamen an.</span><span class="sxs-lookup"><span data-stu-id="4bc3a-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="4bc3a-115">Alternativ können Sie das ServiceUnit-Objekt oder die ResourceId bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="4bc3a-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

<span data-ttu-id="4bc3a-116">Sie können dieses Objekt lokal ändern und dann änderungen auf die Diensteinheit anwenden, indem Sie das cmdlet Set-AzDeploymentManagerServiceUnit verwenden.</span><span class="sxs-lookup"><span data-stu-id="4bc3a-116">You can modify this object locally, and then apply changes to the service unit by using the Set-AzDeploymentManagerServiceUnit cmdlet.</span></span>

## <span data-ttu-id="4bc3a-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4bc3a-117">EXAMPLES</span></span>

### <span data-ttu-id="4bc3a-118">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4bc3a-118">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="4bc3a-119">Dieser Befehl ruft eine Diensteinheit namens ContosoService1Storage unter einem Dienst ContosoService1 in einer Diensttopologie namens ContosoServiceTopology in der ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="4bc3a-119">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="4bc3a-120">Beispiel 2: Holen Sie sich eine Diensteinheit mit dem Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="4bc3a-120">Example 2: Get a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="4bc3a-121">Dieser Befehl ruft eine Diensteinheit namens ContosoService1Storage unter einem Dienst ContosoService1 in einer Diensttopologie namens ContosoServiceTopology in der ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="4bc3a-121">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="4bc3a-122">Beispiel 3: Holen Sie sich eine Diensteinheit mithilfe des Diensteinheitsobjekts.</span><span class="sxs-lookup"><span data-stu-id="4bc3a-122">Example 3: Get a service unit using the service unit object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="4bc3a-123">Dieser Befehl ruft eine Diensteinheit ab, deren Name, Dienstname, Diensttopologiename und Ressourcengruppe den Eigenschaften Name, ServiceName, ServiceTopologyName und ResourceGroupName des $serviceUnitObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="4bc3a-123">This command gets a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="4bc3a-124">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4bc3a-124">PARAMETERS</span></span>

### <span data-ttu-id="4bc3a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bc3a-125">-DefaultProfile</span></span>
<span data-ttu-id="4bc3a-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4bc3a-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bc3a-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4bc3a-127">-InputObject</span></span>
<span data-ttu-id="4bc3a-128">Ressourcenobjekt der Diensteinheit.</span><span class="sxs-lookup"><span data-stu-id="4bc3a-128">Service unit resource object.</span></span>

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

### <span data-ttu-id="4bc3a-129">-Name</span><span class="sxs-lookup"><span data-stu-id="4bc3a-129">-Name</span></span>
<span data-ttu-id="4bc3a-130">Der Name der Diensteinheit.</span><span class="sxs-lookup"><span data-stu-id="4bc3a-130">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bc3a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bc3a-131">-ResourceGroupName</span></span>
<span data-ttu-id="4bc3a-132">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4bc3a-132">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bc3a-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4bc3a-133">-ResourceId</span></span>
<span data-ttu-id="4bc3a-134">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="4bc3a-134">The resource identifier.</span></span>

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

### <span data-ttu-id="4bc3a-135">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4bc3a-135">-ServiceName</span></span>
<span data-ttu-id="4bc3a-136">Der Name des Diensts, zu dem die Diensteinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="4bc3a-136">The name of the service the service unit is part of.</span></span>

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

### <span data-ttu-id="4bc3a-137">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="4bc3a-137">-ServiceObject</span></span>
<span data-ttu-id="4bc3a-138">Das Dienstobjekt, in dem die Diensteinheit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4bc3a-138">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="4bc3a-139">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="4bc3a-139">-ServiceResourceId</span></span>
<span data-ttu-id="4bc3a-140">Der Dienstressourcenbezeichner, in dem die Diensteinheit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4bc3a-140">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="4bc3a-141">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="4bc3a-141">-ServiceTopologyName</span></span>
<span data-ttu-id="4bc3a-142">Der Name der Diensttopologie, zu der die Diensteinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="4bc3a-142">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="4bc3a-143">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="4bc3a-143">-ServiceTopologyObject</span></span>
<span data-ttu-id="4bc3a-144">Das Diensttopologieobjekt, in dem die Diensteinheit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4bc3a-144">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="4bc3a-145">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="4bc3a-145">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="4bc3a-146">Der Ressourcenbezeichner für die Diensttopologie, in dem die Diensteinheit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4bc3a-146">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="4bc3a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bc3a-147">CommonParameters</span></span>
<span data-ttu-id="4bc3a-148">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bc3a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bc3a-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4bc3a-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bc3a-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4bc3a-150">INPUTS</span></span>

### <span data-ttu-id="4bc3a-151">System.String</span><span class="sxs-lookup"><span data-stu-id="4bc3a-151">System.String</span></span>

### <span data-ttu-id="4bc3a-152">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="4bc3a-152">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="4bc3a-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4bc3a-153">OUTPUTS</span></span>

### <span data-ttu-id="4bc3a-154">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="4bc3a-154">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="4bc3a-155">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4bc3a-155">NOTES</span></span>

## <span data-ttu-id="4bc3a-156">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4bc3a-156">RELATED LINKS</span></span>
