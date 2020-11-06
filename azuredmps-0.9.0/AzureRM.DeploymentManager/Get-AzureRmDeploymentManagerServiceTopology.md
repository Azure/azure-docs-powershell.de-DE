---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: f5e0b1e0b2e85eb3c17a53b0108e853535712db1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475749"
---
# <span data-ttu-id="2ffda-101">Get-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="2ffda-101">Get-AzureRmDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="2ffda-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2ffda-102">SYNOPSIS</span></span>
<span data-ttu-id="2ffda-103">Ruft eine Dienst Topologie ab.</span><span class="sxs-lookup"><span data-stu-id="2ffda-103">Gets a service topology.</span></span>

## <span data-ttu-id="2ffda-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ffda-104">SYNTAX</span></span>

### <span data-ttu-id="2ffda-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="2ffda-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ffda-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ffda-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ffda-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="2ffda-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerServiceTopology [-ServiceTopology] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ffda-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ffda-108">DESCRIPTION</span></span>
<span data-ttu-id="2ffda-109">Das Cmdlet " **Get-AzureRmDeploymentManagerServiceTopology** " Ruft eine Dienst Topologie ab.</span><span class="sxs-lookup"><span data-stu-id="2ffda-109">The **Get-AzureRmDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="2ffda-110">Sie können dieses Objekt lokal ändern und dann mithilfe des Set-AzureRmDeploymentManagerServiceTopology-Cmdlets Änderungen an der Topologie vornehmen.</span><span class="sxs-lookup"><span data-stu-id="2ffda-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzureRmDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="2ffda-111">Geben Sie die Dienst Topologie nach dem Namen und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2ffda-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="2ffda-112">Alternativ können Sie das ServiceTopology-Objekt oder die resourcecode-Objekt bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="2ffda-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="2ffda-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2ffda-113">EXAMPLES</span></span>

### <span data-ttu-id="2ffda-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2ffda-114">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="2ffda-115">Dieser Befehl ruft eine Dienst Topologie mit dem Namen ContosoServiceTopology in der ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2ffda-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="2ffda-116">Beispiel 2: Abrufen einer Dienst Topologie mithilfe des Ressourcenbezeichners.</span><span class="sxs-lookup"><span data-stu-id="2ffda-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="2ffda-117">Dieser Befehl ruft eine Dienst Topologie mit dem Namen ContosoServiceTopology in der ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2ffda-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="2ffda-118">Beispiel 3: Abrufen einer Dienst Topologie mithilfe des Dienst Topologie-Objekts.</span><span class="sxs-lookup"><span data-stu-id="2ffda-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ServiceTopology $serviceTopologyObject
```

<span data-ttu-id="2ffda-119">Dieser Befehl ruft eine Dienst Topologie ab, deren Name und ResourceGroup den Namen-und ResourceGroupName-Eigenschaften der $serviceTopologyObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="2ffda-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="2ffda-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ffda-120">PARAMETERS</span></span>

### <span data-ttu-id="2ffda-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ffda-121">-DefaultProfile</span></span>
<span data-ttu-id="2ffda-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2ffda-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ffda-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2ffda-123">-Name</span></span>
<span data-ttu-id="2ffda-124">Der Name der Dienst Topologie.</span><span class="sxs-lookup"><span data-stu-id="2ffda-124">The name of the service topology.</span></span>

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

### <span data-ttu-id="2ffda-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ffda-125">-ResourceGroupName</span></span>
<span data-ttu-id="2ffda-126">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2ffda-126">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ffda-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2ffda-127">-ResourceId</span></span>
<span data-ttu-id="2ffda-128">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="2ffda-128">The resource identifier.</span></span>

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

### <span data-ttu-id="2ffda-129">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="2ffda-129">-ServiceTopology</span></span>
<span data-ttu-id="2ffda-130">Ressourcenobjekt der Dienst Topologie.</span><span class="sxs-lookup"><span data-stu-id="2ffda-130">Service topology resource object.</span></span>

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

### <span data-ttu-id="2ffda-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ffda-131">CommonParameters</span></span>
<span data-ttu-id="2ffda-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ffda-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ffda-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ffda-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ffda-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2ffda-134">INPUTS</span></span>

### <span data-ttu-id="2ffda-135">Keine</span><span class="sxs-lookup"><span data-stu-id="2ffda-135">None</span></span>

## <span data-ttu-id="2ffda-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2ffda-136">OUTPUTS</span></span>

### <span data-ttu-id="2ffda-137">Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="2ffda-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="2ffda-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="2ffda-138">NOTES</span></span>

## <span data-ttu-id="2ffda-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2ffda-139">RELATED LINKS</span></span>

[<span data-ttu-id="2ffda-140">Neu – AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="2ffda-140">New-AzureRmDeploymentManagerServiceTopology</span></span>](./New-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="2ffda-141">Remove-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="2ffda-141">Remove-AzureRmDeploymentManagerServiceTopology</span></span>](./Remove-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="2ffda-142">Satz-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="2ffda-142">Set-AzureRmDeploymentManagerServiceTopology</span></span>](./Set-AzureRmDeploymentManagerServiceTopology.md)