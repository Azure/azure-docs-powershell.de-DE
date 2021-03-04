---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: c02a88cdb550e1ec9cb343b286d3211045873820
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932979"
---
# <span data-ttu-id="d022c-101">Get-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="d022c-101">Get-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="d022c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d022c-102">SYNOPSIS</span></span>
<span data-ttu-id="d022c-103">Ruft die Diensttopologie ab.</span><span class="sxs-lookup"><span data-stu-id="d022c-103">Gets the service topology.</span></span>

## <span data-ttu-id="d022c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d022c-104">SYNTAX</span></span>

### <span data-ttu-id="d022c-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="d022c-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d022c-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d022c-106">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d022c-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="d022c-107">InputObject</span></span>
```
Get-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d022c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d022c-108">DESCRIPTION</span></span>
<span data-ttu-id="d022c-109">Das **Cmdlet Get-AzDeploymentManagerServiceTopology** erhält eine Diensttopologie.</span><span class="sxs-lookup"><span data-stu-id="d022c-109">The **Get-AzDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="d022c-110">Sie können dieses Objekt lokal ändern und dann Änderungen an der Topologie mithilfe des cmdlets Set-AzDeploymentManagerServiceTopology anwenden.</span><span class="sxs-lookup"><span data-stu-id="d022c-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="d022c-111">Geben Sie die Diensttopologie nach ihrem Namen und dem Ressourcengruppennamen an.</span><span class="sxs-lookup"><span data-stu-id="d022c-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="d022c-112">Alternativ können Sie das ServiceTopology-Objekt oder die ResourceId bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d022c-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="d022c-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d022c-113">EXAMPLES</span></span>

### <span data-ttu-id="d022c-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d022c-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="d022c-115">Dieser Befehl ruft eine Diensttopologie namens ContosoServiceTopology in der ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="d022c-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="d022c-116">Beispiel 2: Holen Sie sich eine Diensttopologie mithilfe des Ressourcenbezeichners.</span><span class="sxs-lookup"><span data-stu-id="d022c-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="d022c-117">Dieser Befehl ruft eine Diensttopologie namens ContosoServiceTopology in der ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="d022c-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="d022c-118">Beispiel 3: Holen Sie sich eine Diensttopologie mithilfe des Diensttopologieobjekts.</span><span class="sxs-lookup"><span data-stu-id="d022c-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="d022c-119">Dieser Befehl ruft eine Diensttopologie ab, deren Name und ResourceGroup mit den Eigenschaften Name und ResourceGroupName des $serviceTopologyObject übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="d022c-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="d022c-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d022c-120">PARAMETERS</span></span>

### <span data-ttu-id="d022c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d022c-121">-DefaultProfile</span></span>
<span data-ttu-id="d022c-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d022c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d022c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d022c-123">-InputObject</span></span>
<span data-ttu-id="d022c-124">Diensttopologieressourcenobjekt.</span><span class="sxs-lookup"><span data-stu-id="d022c-124">Service topology resource object.</span></span>

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

### <span data-ttu-id="d022c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d022c-125">-Name</span></span>
<span data-ttu-id="d022c-126">Der Name der Diensttopologie.</span><span class="sxs-lookup"><span data-stu-id="d022c-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="d022c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d022c-127">-ResourceGroupName</span></span>
<span data-ttu-id="d022c-128">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d022c-128">The resource group.</span></span>

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

### <span data-ttu-id="d022c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d022c-129">-ResourceId</span></span>
<span data-ttu-id="d022c-130">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="d022c-130">The resource identifier.</span></span>

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

### <span data-ttu-id="d022c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d022c-131">CommonParameters</span></span>
<span data-ttu-id="d022c-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d022c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d022c-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d022c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d022c-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d022c-134">INPUTS</span></span>

### <span data-ttu-id="d022c-135">System.String</span><span class="sxs-lookup"><span data-stu-id="d022c-135">System.String</span></span>

### <span data-ttu-id="d022c-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="d022c-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="d022c-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d022c-137">OUTPUTS</span></span>

### <span data-ttu-id="d022c-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="d022c-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="d022c-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d022c-139">NOTES</span></span>

## <span data-ttu-id="d022c-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d022c-140">RELATED LINKS</span></span>
