---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 54a48a025dff2bba2c1ad620237d0a84aacf7d7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651368"
---
# <span data-ttu-id="a4dfd-101">Get-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="a4dfd-101">Get-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="a4dfd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a4dfd-102">SYNOPSIS</span></span>
<span data-ttu-id="a4dfd-103">Ruft die Dienst Topologie ab.</span><span class="sxs-lookup"><span data-stu-id="a4dfd-103">Gets the service topology.</span></span>

## <span data-ttu-id="a4dfd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4dfd-104">SYNTAX</span></span>

### <span data-ttu-id="a4dfd-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="a4dfd-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4dfd-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4dfd-106">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a4dfd-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="a4dfd-107">InputObject</span></span>
```
Get-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4dfd-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a4dfd-108">DESCRIPTION</span></span>
<span data-ttu-id="a4dfd-109">Das Cmdlet " **Get-AzDeploymentManagerServiceTopology** " Ruft eine Dienst Topologie ab.</span><span class="sxs-lookup"><span data-stu-id="a4dfd-109">The **Get-AzDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="a4dfd-110">Sie können dieses Objekt lokal ändern und dann mithilfe des Set-AzDeploymentManagerServiceTopology-Cmdlets Änderungen an der Topologie vornehmen.</span><span class="sxs-lookup"><span data-stu-id="a4dfd-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="a4dfd-111">Geben Sie die Dienst Topologie nach dem Namen und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="a4dfd-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="a4dfd-112">Alternativ können Sie das ServiceTopology-Objekt oder die resourcecode-Objekt bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a4dfd-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="a4dfd-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a4dfd-113">EXAMPLES</span></span>

### <span data-ttu-id="a4dfd-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a4dfd-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="a4dfd-115">Dieser Befehl ruft eine Dienst Topologie mit dem Namen ContosoServiceTopology in der ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a4dfd-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="a4dfd-116">Beispiel 2: Abrufen einer Dienst Topologie mithilfe des Ressourcenbezeichners.</span><span class="sxs-lookup"><span data-stu-id="a4dfd-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="a4dfd-117">Dieser Befehl ruft eine Dienst Topologie mit dem Namen ContosoServiceTopology in der ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a4dfd-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="a4dfd-118">Beispiel 3: Abrufen einer Dienst Topologie mithilfe des Dienst Topologie-Objekts.</span><span class="sxs-lookup"><span data-stu-id="a4dfd-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="a4dfd-119">Dieser Befehl ruft eine Dienst Topologie ab, deren Name und ResourceGroup den Namen-und ResourceGroupName-Eigenschaften der $serviceTopologyObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a4dfd-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="a4dfd-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4dfd-120">PARAMETERS</span></span>

### <span data-ttu-id="a4dfd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4dfd-121">-DefaultProfile</span></span>
<span data-ttu-id="a4dfd-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a4dfd-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4dfd-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a4dfd-123">-InputObject</span></span>
<span data-ttu-id="a4dfd-124">Ressourcenobjekt der Dienst Topologie.</span><span class="sxs-lookup"><span data-stu-id="a4dfd-124">Service topology resource object.</span></span>

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

### <span data-ttu-id="a4dfd-125">-Name</span><span class="sxs-lookup"><span data-stu-id="a4dfd-125">-Name</span></span>
<span data-ttu-id="a4dfd-126">Der Name der Dienst Topologie.</span><span class="sxs-lookup"><span data-stu-id="a4dfd-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="a4dfd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4dfd-127">-ResourceGroupName</span></span>
<span data-ttu-id="a4dfd-128">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a4dfd-128">The resource group.</span></span>

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

### <span data-ttu-id="a4dfd-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a4dfd-129">-ResourceId</span></span>
<span data-ttu-id="a4dfd-130">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="a4dfd-130">The resource identifier.</span></span>

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

### <span data-ttu-id="a4dfd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4dfd-131">CommonParameters</span></span>
<span data-ttu-id="a4dfd-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4dfd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4dfd-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4dfd-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4dfd-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a4dfd-134">INPUTS</span></span>

### <span data-ttu-id="a4dfd-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a4dfd-135">System.String</span></span>

### <span data-ttu-id="a4dfd-136">Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="a4dfd-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="a4dfd-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a4dfd-137">OUTPUTS</span></span>

### <span data-ttu-id="a4dfd-138">Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="a4dfd-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="a4dfd-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="a4dfd-139">NOTES</span></span>

## <span data-ttu-id="a4dfd-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a4dfd-140">RELATED LINKS</span></span>
