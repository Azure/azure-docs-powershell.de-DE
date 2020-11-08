---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: f3d85ef89bbc6d427801120f5c7a3a37a8fc855a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004600"
---
# <span data-ttu-id="7f6d2-101">Get-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="7f6d2-101">Get-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="7f6d2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7f6d2-102">SYNOPSIS</span></span>
<span data-ttu-id="7f6d2-103">Ruft die Dienst Topologie ab.</span><span class="sxs-lookup"><span data-stu-id="7f6d2-103">Gets the service topology.</span></span>

## <span data-ttu-id="7f6d2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f6d2-104">SYNTAX</span></span>

### <span data-ttu-id="7f6d2-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="7f6d2-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f6d2-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f6d2-106">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7f6d2-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="7f6d2-107">InputObject</span></span>
```
Get-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f6d2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f6d2-108">DESCRIPTION</span></span>
<span data-ttu-id="7f6d2-109">Das Cmdlet " **Get-AzDeploymentManagerServiceTopology** " Ruft eine Dienst Topologie ab.</span><span class="sxs-lookup"><span data-stu-id="7f6d2-109">The **Get-AzDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="7f6d2-110">Sie können dieses Objekt lokal ändern und dann mithilfe des Set-AzDeploymentManagerServiceTopology-Cmdlets Änderungen an der Topologie vornehmen.</span><span class="sxs-lookup"><span data-stu-id="7f6d2-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="7f6d2-111">Geben Sie die Dienst Topologie nach dem Namen und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="7f6d2-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="7f6d2-112">Alternativ können Sie das ServiceTopology-Objekt oder die resourcecode-Objekt bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7f6d2-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="7f6d2-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f6d2-113">EXAMPLES</span></span>

### <span data-ttu-id="7f6d2-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7f6d2-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="7f6d2-115">Dieser Befehl ruft eine Dienst Topologie mit dem Namen ContosoServiceTopology in der ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7f6d2-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="7f6d2-116">Beispiel 2: Abrufen einer Dienst Topologie mithilfe des Ressourcenbezeichners.</span><span class="sxs-lookup"><span data-stu-id="7f6d2-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="7f6d2-117">Dieser Befehl ruft eine Dienst Topologie mit dem Namen ContosoServiceTopology in der ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7f6d2-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="7f6d2-118">Beispiel 3: Abrufen einer Dienst Topologie mithilfe des Dienst Topologie-Objekts.</span><span class="sxs-lookup"><span data-stu-id="7f6d2-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="7f6d2-119">Dieser Befehl ruft eine Dienst Topologie ab, deren Name und ResourceGroup den Namen-und ResourceGroupName-Eigenschaften der $serviceTopologyObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="7f6d2-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="7f6d2-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f6d2-120">PARAMETERS</span></span>

### <span data-ttu-id="7f6d2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f6d2-121">-DefaultProfile</span></span>
<span data-ttu-id="7f6d2-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7f6d2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f6d2-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7f6d2-123">-InputObject</span></span>
<span data-ttu-id="7f6d2-124">Ressourcenobjekt der Dienst Topologie.</span><span class="sxs-lookup"><span data-stu-id="7f6d2-124">Service topology resource object.</span></span>

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

### <span data-ttu-id="7f6d2-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7f6d2-125">-Name</span></span>
<span data-ttu-id="7f6d2-126">Der Name der Dienst Topologie.</span><span class="sxs-lookup"><span data-stu-id="7f6d2-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="7f6d2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f6d2-127">-ResourceGroupName</span></span>
<span data-ttu-id="7f6d2-128">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7f6d2-128">The resource group.</span></span>

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

### <span data-ttu-id="7f6d2-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7f6d2-129">-ResourceId</span></span>
<span data-ttu-id="7f6d2-130">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="7f6d2-130">The resource identifier.</span></span>

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

### <span data-ttu-id="7f6d2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f6d2-131">CommonParameters</span></span>
<span data-ttu-id="7f6d2-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f6d2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f6d2-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f6d2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f6d2-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7f6d2-134">INPUTS</span></span>

### <span data-ttu-id="7f6d2-135">System. String</span><span class="sxs-lookup"><span data-stu-id="7f6d2-135">System.String</span></span>

### <span data-ttu-id="7f6d2-136">Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="7f6d2-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="7f6d2-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7f6d2-137">OUTPUTS</span></span>

### <span data-ttu-id="7f6d2-138">Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="7f6d2-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="7f6d2-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="7f6d2-139">NOTES</span></span>

## <span data-ttu-id="7f6d2-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7f6d2-140">RELATED LINKS</span></span>
