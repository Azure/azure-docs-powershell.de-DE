---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 4a91c2f8fdda1d2cda7c75f0cf7cfab165701f3d
ms.sourcegitcommit: e57be0da5162efeb0a01f396e2343dd137920063
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "99572104"
---
# <span data-ttu-id="3a211-101">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="3a211-101">Get-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="3a211-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a211-102">SYNOPSIS</span></span>
<span data-ttu-id="3a211-103">Ruft einen Dienst in einer Diensttopologie ab.</span><span class="sxs-lookup"><span data-stu-id="3a211-103">Gets a service in a service topology.</span></span>

## <span data-ttu-id="3a211-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a211-104">SYNTAX</span></span>

### <span data-ttu-id="3a211-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="3a211-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a211-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="3a211-106">ByServiceTopologyObject</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a211-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="3a211-107">ByServiceTopologyResourceId</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a211-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3a211-108">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3a211-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="3a211-109">InputObject</span></span>
```
Get-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3a211-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3a211-110">DESCRIPTION</span></span>
<span data-ttu-id="3a211-111">Das **Cmdlet "Get-AzureRmDeploymentManagerService"** ruft einen Dienst unter einer Diensttopologie ab und gibt ein Objekt zurück, das den Dienst darstellt.</span><span class="sxs-lookup"><span data-stu-id="3a211-111">The **Get-AzureRmDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="3a211-112">Geben Sie den Dienst nach seinem Namen, der Diensttopologie, in der er sich befindet, und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="3a211-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="3a211-113">Alternativ können Sie das Objekt "Service" oder die "ResourceId" bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="3a211-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="3a211-114">Sie können dieses Objekt lokal ändern und dann Änderungen an dem Dienst mithilfe des cmdlets Set-AzureRmDeploymentManagerService anwenden.</span><span class="sxs-lookup"><span data-stu-id="3a211-114">You can modify this object locally, and then apply changes to the service by using the Set-AzureRmDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="3a211-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3a211-115">EXAMPLES</span></span>

### <span data-ttu-id="3a211-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3a211-116">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="3a211-117">Dieser Befehl ruft den Dienst "ContosoService1" in einer Diensttopologie namens "ContosoServiceTopology" in der ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="3a211-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="3a211-118">Beispiel 2: Einen Dienst mit dem Ressourcenbezeichner erhalten.</span><span class="sxs-lookup"><span data-stu-id="3a211-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="3a211-119">Dieser Befehl ruft den Dienst "ContosoService1" in einer Diensttopologie namens "ContosoServiceTopology" in der ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="3a211-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="3a211-120">Beispiel 3: Einen Dienst mithilfe des Dienstobjekts erhalten.</span><span class="sxs-lookup"><span data-stu-id="3a211-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="3a211-121">Dieser Befehl ruft einen Dienst ab, dessen Name, Name der Diensttopologie und ResourceGroup mit den Eigenschaften "Name", "ServiceTopologyName" bzw. "ResourceGroupName" der $serviceObject übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="3a211-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="3a211-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a211-122">PARAMETERS</span></span>

### <span data-ttu-id="3a211-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a211-123">-DefaultProfile</span></span>
<span data-ttu-id="3a211-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3a211-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a211-125">-Name</span><span class="sxs-lookup"><span data-stu-id="3a211-125">-Name</span></span>
<span data-ttu-id="3a211-126">Der Name des Diensts.</span><span class="sxs-lookup"><span data-stu-id="3a211-126">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a211-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a211-127">-ResourceGroupName</span></span>
<span data-ttu-id="3a211-128">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3a211-128">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a211-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3a211-129">-ResourceId</span></span>
<span data-ttu-id="3a211-130">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="3a211-130">The resource identifier.</span></span>

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

### <span data-ttu-id="3a211-131">-Service</span><span class="sxs-lookup"><span data-stu-id="3a211-131">-Service</span></span>
<span data-ttu-id="3a211-132">Dienstobjekt.</span><span class="sxs-lookup"><span data-stu-id="3a211-132">Service object.</span></span>

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

### <span data-ttu-id="3a211-133">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="3a211-133">-ServiceTopology</span></span>
<span data-ttu-id="3a211-134">Das Diensttopologieobjekt, in dem der Dienst erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3a211-134">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="3a211-135">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="3a211-135">-ServiceTopologyName</span></span>
<span data-ttu-id="3a211-136">Der Name der Diensttopologie.</span><span class="sxs-lookup"><span data-stu-id="3a211-136">The name of the service topology.</span></span>

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

### <span data-ttu-id="3a211-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="3a211-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="3a211-138">Der Ressourcenbezeichner der Diensttopologie, in dem der Dienst erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3a211-138">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="3a211-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a211-139">CommonParameters</span></span>
<span data-ttu-id="3a211-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a211-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a211-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a211-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a211-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3a211-142">INPUTS</span></span>

### <span data-ttu-id="3a211-143">Keine</span><span class="sxs-lookup"><span data-stu-id="3a211-143">None</span></span>

## <span data-ttu-id="3a211-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3a211-144">OUTPUTS</span></span>

### <span data-ttu-id="3a211-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="3a211-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="3a211-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3a211-146">NOTES</span></span>

## <span data-ttu-id="3a211-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3a211-147">RELATED LINKS</span></span>

[<span data-ttu-id="3a211-148">New-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="3a211-148">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="3a211-149">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="3a211-149">Remove-AzureRmDeploymentManagerService</span></span>](./Remove-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="3a211-150">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="3a211-150">Set-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)
