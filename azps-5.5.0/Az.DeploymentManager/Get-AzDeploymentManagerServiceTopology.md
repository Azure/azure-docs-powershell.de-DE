---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: f3d85ef89bbc6d427801120f5c7a3a37a8fc855a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144236"
---
# <span data-ttu-id="89fd0-101">Get-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="89fd0-101">Get-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="89fd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89fd0-102">SYNOPSIS</span></span>
<span data-ttu-id="89fd0-103">Ruft die Diensttopologie ab.</span><span class="sxs-lookup"><span data-stu-id="89fd0-103">Gets the service topology.</span></span>

## <span data-ttu-id="89fd0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89fd0-104">SYNTAX</span></span>

### <span data-ttu-id="89fd0-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="89fd0-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89fd0-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="89fd0-106">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="89fd0-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="89fd0-107">InputObject</span></span>
```
Get-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89fd0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="89fd0-108">DESCRIPTION</span></span>
<span data-ttu-id="89fd0-109">Das **Cmdlet "Get-AzDeploymentManagerServiceTopology"** ruft eine Diensttopologie ab.</span><span class="sxs-lookup"><span data-stu-id="89fd0-109">The **Get-AzDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="89fd0-110">Sie können dieses Objekt lokal ändern und dann Änderungen an der Topologie mithilfe des Set-AzDeploymentManagerServiceTopology anwenden.</span><span class="sxs-lookup"><span data-stu-id="89fd0-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="89fd0-111">Geben Sie die Diensttopologie durch ihren Namen und den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="89fd0-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="89fd0-112">Alternativ können Sie das Objekt "ServiceTopology" oder die "ResourceId" bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="89fd0-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="89fd0-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="89fd0-113">EXAMPLES</span></span>

### <span data-ttu-id="89fd0-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="89fd0-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="89fd0-115">Dieser Befehl ruft eine Diensttopologie namens "ContosoServiceTopology" in der ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="89fd0-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="89fd0-116">Beispiel 2: Erhalten einer Diensttopologie mithilfe des Ressourcenbezeichners.</span><span class="sxs-lookup"><span data-stu-id="89fd0-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="89fd0-117">Dieser Befehl ruft eine Diensttopologie namens "ContosoServiceTopology" in der ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="89fd0-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="89fd0-118">Beispiel 3: Erhalten einer Diensttopologie mithilfe des Diensttopologieobjekts.</span><span class="sxs-lookup"><span data-stu-id="89fd0-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="89fd0-119">Dieser Befehl ruft eine Diensttopologie ab, deren Name und Ressourcengruppe mit den Eigenschaften "Name" bzw. "ResourceGroupName" des $serviceTopologyObject übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="89fd0-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="89fd0-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89fd0-120">PARAMETERS</span></span>

### <span data-ttu-id="89fd0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89fd0-121">-DefaultProfile</span></span>
<span data-ttu-id="89fd0-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="89fd0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89fd0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89fd0-123">-InputObject</span></span>
<span data-ttu-id="89fd0-124">Ressourcenobjekt der Diensttopologie.</span><span class="sxs-lookup"><span data-stu-id="89fd0-124">Service topology resource object.</span></span>

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

### <span data-ttu-id="89fd0-125">-Name</span><span class="sxs-lookup"><span data-stu-id="89fd0-125">-Name</span></span>
<span data-ttu-id="89fd0-126">Der Name der Diensttopologie.</span><span class="sxs-lookup"><span data-stu-id="89fd0-126">The name of the service topology.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89fd0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89fd0-127">-ResourceGroupName</span></span>
<span data-ttu-id="89fd0-128">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="89fd0-128">The resource group.</span></span>

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

### <span data-ttu-id="89fd0-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89fd0-129">-ResourceId</span></span>
<span data-ttu-id="89fd0-130">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="89fd0-130">The resource identifier.</span></span>

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

### <span data-ttu-id="89fd0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89fd0-131">CommonParameters</span></span>
<span data-ttu-id="89fd0-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89fd0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89fd0-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89fd0-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89fd0-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="89fd0-134">INPUTS</span></span>

### <span data-ttu-id="89fd0-135">System.String</span><span class="sxs-lookup"><span data-stu-id="89fd0-135">System.String</span></span>

### <span data-ttu-id="89fd0-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="89fd0-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="89fd0-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="89fd0-137">OUTPUTS</span></span>

### <span data-ttu-id="89fd0-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="89fd0-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="89fd0-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="89fd0-139">NOTES</span></span>

## <span data-ttu-id="89fd0-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="89fd0-140">RELATED LINKS</span></span>
