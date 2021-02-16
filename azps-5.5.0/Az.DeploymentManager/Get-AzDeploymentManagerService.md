---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
ms.openlocfilehash: da59c17b7aef90cd3f5c5b374d663292153be140
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144241"
---
# <span data-ttu-id="c031c-101">Get-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="c031c-101">Get-AzDeploymentManagerService</span></span>

## <span data-ttu-id="c031c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c031c-102">SYNOPSIS</span></span>
<span data-ttu-id="c031c-103">Ruft den Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="c031c-103">Gets the service.</span></span>

## <span data-ttu-id="c031c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c031c-104">SYNTAX</span></span>

### <span data-ttu-id="c031c-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="c031c-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c031c-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="c031c-106">ByServiceTopologyObject</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c031c-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="c031c-107">ByServiceTopologyResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c031c-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c031c-108">ResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c031c-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="c031c-109">InputObject</span></span>
```
Get-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c031c-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c031c-110">DESCRIPTION</span></span>
<span data-ttu-id="c031c-111">Das **Cmdlet "Get-AzDeploymentManagerService"** ruft einen Dienst unter einer Diensttopologie ab und gibt ein Objekt zurück, das den Dienst darstellt.</span><span class="sxs-lookup"><span data-stu-id="c031c-111">The **Get-AzDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="c031c-112">Geben Sie den Dienst nach seinem Namen, der Diensttopologie, in der er sich befindet, und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c031c-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="c031c-113">Alternativ können Sie das Objekt "Service" oder die "ResourceId" bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c031c-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="c031c-114">Sie können dieses Objekt lokal ändern und dann Änderungen an dem Dienst mithilfe des cmdlets Set-AzDeploymentManagerService anwenden.</span><span class="sxs-lookup"><span data-stu-id="c031c-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="c031c-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c031c-115">EXAMPLES</span></span>

### <span data-ttu-id="c031c-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c031c-116">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="c031c-117">Dieser Befehl ruft den Dienst "ContosoService1" in einer Diensttopologie namens "ContosoServiceTopology" in der ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="c031c-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="c031c-118">Beispiel 2: Einen Dienst mit dem Ressourcenbezeichner erhalten.</span><span class="sxs-lookup"><span data-stu-id="c031c-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="c031c-119">Dieser Befehl ruft den Dienst "ContosoService1" in einer Diensttopologie namens "ContosoServiceTopology" in der ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="c031c-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="c031c-120">Beispiel 3: Einen Dienst mithilfe des Dienstobjekts erhalten.</span><span class="sxs-lookup"><span data-stu-id="c031c-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="c031c-121">Dieser Befehl ruft einen Dienst ab, dessen Name, Name der Diensttopologie und ResourceGroup mit den Eigenschaften "Name", "ServiceTopologyName" bzw. "ResourceGroupName" der $serviceObject übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="c031c-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
 

## <span data-ttu-id="c031c-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c031c-122">PARAMETERS</span></span>

### <span data-ttu-id="c031c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c031c-123">-DefaultProfile</span></span>
<span data-ttu-id="c031c-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c031c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c031c-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c031c-125">-InputObject</span></span>
<span data-ttu-id="c031c-126">Dienstobjekt.</span><span class="sxs-lookup"><span data-stu-id="c031c-126">Service object.</span></span>

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

### <span data-ttu-id="c031c-127">-Name</span><span class="sxs-lookup"><span data-stu-id="c031c-127">-Name</span></span>
<span data-ttu-id="c031c-128">Der Name des Diensts.</span><span class="sxs-lookup"><span data-stu-id="c031c-128">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c031c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c031c-129">-ResourceGroupName</span></span>
<span data-ttu-id="c031c-130">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c031c-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c031c-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c031c-131">-ResourceId</span></span>
<span data-ttu-id="c031c-132">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="c031c-132">The resource identifier.</span></span>

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

### <span data-ttu-id="c031c-133">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="c031c-133">-ServiceTopologyName</span></span>
<span data-ttu-id="c031c-134">Der Name der Diensttopologie.</span><span class="sxs-lookup"><span data-stu-id="c031c-134">The name of the service topology.</span></span>

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

### <span data-ttu-id="c031c-135">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="c031c-135">-ServiceTopologyObject</span></span>
<span data-ttu-id="c031c-136">Das Diensttopologieobjekt, in dem der Dienst erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c031c-136">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c031c-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="c031c-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="c031c-138">Der Ressourcenbezeichner der Diensttopologie, in dem der Dienst erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c031c-138">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c031c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c031c-139">CommonParameters</span></span>
<span data-ttu-id="c031c-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c031c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c031c-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c031c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c031c-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c031c-142">INPUTS</span></span>

### <span data-ttu-id="c031c-143">System.String</span><span class="sxs-lookup"><span data-stu-id="c031c-143">System.String</span></span>

### <span data-ttu-id="c031c-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="c031c-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="c031c-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c031c-145">OUTPUTS</span></span>

### <span data-ttu-id="c031c-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="c031c-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="c031c-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c031c-147">NOTES</span></span>

## <span data-ttu-id="c031c-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c031c-148">RELATED LINKS</span></span>
