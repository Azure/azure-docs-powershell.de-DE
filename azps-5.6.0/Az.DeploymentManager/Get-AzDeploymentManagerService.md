---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
ms.openlocfilehash: 12a2e8b27697436a38753c054f178878b9ed3bd1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932984"
---
# <span data-ttu-id="21d61-101">Get-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="21d61-101">Get-AzDeploymentManagerService</span></span>

## <span data-ttu-id="21d61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21d61-102">SYNOPSIS</span></span>
<span data-ttu-id="21d61-103">Ruft den Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="21d61-103">Gets the service.</span></span>

## <span data-ttu-id="21d61-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21d61-104">SYNTAX</span></span>

### <span data-ttu-id="21d61-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="21d61-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21d61-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="21d61-106">ByServiceTopologyObject</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="21d61-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="21d61-107">ByServiceTopologyResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21d61-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="21d61-108">ResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="21d61-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="21d61-109">InputObject</span></span>
```
Get-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="21d61-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="21d61-110">DESCRIPTION</span></span>
<span data-ttu-id="21d61-111">Das **Get-AzDeploymentManagerService-Cmdlet** ruft einen Dienst unter einer Diensttopologie ab und gibt ein -Objekt zurück, das den Dienst darstellt.</span><span class="sxs-lookup"><span data-stu-id="21d61-111">The **Get-AzDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="21d61-112">Geben Sie den Dienst nach seinem Namen, der Diensttopologie, in der er sich befindet, und dem Ressourcengruppennamen an.</span><span class="sxs-lookup"><span data-stu-id="21d61-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="21d61-113">Alternativ können Sie das Dienstobjekt oder die ResourceId bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="21d61-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="21d61-114">Sie können dieses Objekt lokal ändern und dann Änderungen auf den Dienst anwenden, indem Sie das cmdlet Set-AzDeploymentManagerService verwenden.</span><span class="sxs-lookup"><span data-stu-id="21d61-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="21d61-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="21d61-115">EXAMPLES</span></span>

### <span data-ttu-id="21d61-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="21d61-116">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="21d61-117">Dieser Befehl ruft einen Dienst namens ContosoService1 in einer Diensttopologie namens ContosoServiceTopology in der ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="21d61-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="21d61-118">Beispiel 2: Einen Dienst mit dem Ressourcenbezeichner erhalten.</span><span class="sxs-lookup"><span data-stu-id="21d61-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="21d61-119">Dieser Befehl ruft einen Dienst namens ContosoService1 in einer Diensttopologie namens ContosoServiceTopology in der ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="21d61-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="21d61-120">Beispiel 3: Einen Dienst mit dem Dienstobjekt erhalten.</span><span class="sxs-lookup"><span data-stu-id="21d61-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="21d61-121">Dieser Befehl ruft einen Dienst ab, dessen Name, Diensttopologiename und Ressourcengruppe den Eigenschaften Name, ServiceTopologyName und ResourceGroupName des $serviceObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="21d61-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
 

## <span data-ttu-id="21d61-122">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="21d61-122">PARAMETERS</span></span>

### <span data-ttu-id="21d61-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21d61-123">-DefaultProfile</span></span>
<span data-ttu-id="21d61-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="21d61-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21d61-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21d61-125">-InputObject</span></span>
<span data-ttu-id="21d61-126">Dienstobjekt.</span><span class="sxs-lookup"><span data-stu-id="21d61-126">Service object.</span></span>

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

### <span data-ttu-id="21d61-127">-Name</span><span class="sxs-lookup"><span data-stu-id="21d61-127">-Name</span></span>
<span data-ttu-id="21d61-128">Der Name des Diensts.</span><span class="sxs-lookup"><span data-stu-id="21d61-128">The name of the service.</span></span>

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

### <span data-ttu-id="21d61-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21d61-129">-ResourceGroupName</span></span>
<span data-ttu-id="21d61-130">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="21d61-130">The resource group.</span></span>

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

### <span data-ttu-id="21d61-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21d61-131">-ResourceId</span></span>
<span data-ttu-id="21d61-132">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="21d61-132">The resource identifier.</span></span>

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

### <span data-ttu-id="21d61-133">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="21d61-133">-ServiceTopologyName</span></span>
<span data-ttu-id="21d61-134">Der Name der Diensttopologie.</span><span class="sxs-lookup"><span data-stu-id="21d61-134">The name of the service topology.</span></span>

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

### <span data-ttu-id="21d61-135">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="21d61-135">-ServiceTopologyObject</span></span>
<span data-ttu-id="21d61-136">Das Diensttopologieobjekt, in dem der Dienst erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="21d61-136">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="21d61-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="21d61-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="21d61-138">Der Ressourcenbezeichner der Diensttopologie, in dem der Dienst erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="21d61-138">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="21d61-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21d61-139">CommonParameters</span></span>
<span data-ttu-id="21d61-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21d61-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21d61-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21d61-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21d61-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="21d61-142">INPUTS</span></span>

### <span data-ttu-id="21d61-143">System.String</span><span class="sxs-lookup"><span data-stu-id="21d61-143">System.String</span></span>

### <span data-ttu-id="21d61-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="21d61-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="21d61-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="21d61-145">OUTPUTS</span></span>

### <span data-ttu-id="21d61-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="21d61-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="21d61-147">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="21d61-147">NOTES</span></span>

## <span data-ttu-id="21d61-148">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="21d61-148">RELATED LINKS</span></span>
