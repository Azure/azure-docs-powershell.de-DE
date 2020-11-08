---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: f80f67270652d9c9edef38c9eb793074acd95a27
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004595"
---
# <span data-ttu-id="5a96d-101">Get-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="5a96d-101">Get-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="5a96d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5a96d-102">SYNOPSIS</span></span>
<span data-ttu-id="5a96d-103">Ruft die Diensteinheit ab.</span><span class="sxs-lookup"><span data-stu-id="5a96d-103">Gets the service unit.</span></span>

## <span data-ttu-id="5a96d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a96d-104">SYNTAX</span></span>

### <span data-ttu-id="5a96d-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="5a96d-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a96d-106">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="5a96d-106">ByServiceObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a96d-107">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="5a96d-107">ByServiceResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a96d-108">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="5a96d-108">ByTopologyObjectAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5a96d-109">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="5a96d-109">ByTopologyResourceAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a96d-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a96d-110">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5a96d-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="5a96d-111">InputObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a96d-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a96d-112">DESCRIPTION</span></span>
<span data-ttu-id="5a96d-113">Das Cmdlet " **Get-AzDeploymentManagerServiceUnit** " Ruft eine Diensteinheit in einem Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="5a96d-113">The **Get-AzDeploymentManagerServiceUnit** cmdlet gets a service unit in a service.</span></span>

<span data-ttu-id="5a96d-114">Geben Sie die Diensteinheit nach dem Namen, dem Dienst, unter dem Sie definiert wurde, dem Namen der Dienst Topologie und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="5a96d-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="5a96d-115">Alternativ können Sie das Serviceunit-Objekt oder die resourcecode-Objekt bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5a96d-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

<span data-ttu-id="5a96d-116">Sie können dieses Objekt lokal ändern und dann mithilfe des Set-AzDeploymentManagerServiceUnit-Cmdlets Änderungen an der Diensteinheit vornehmen.</span><span class="sxs-lookup"><span data-stu-id="5a96d-116">You can modify this object locally, and then apply changes to the service unit by using the Set-AzDeploymentManagerServiceUnit cmdlet.</span></span>

## <span data-ttu-id="5a96d-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5a96d-117">EXAMPLES</span></span>

### <span data-ttu-id="5a96d-118">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5a96d-118">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="5a96d-119">Dieser Befehl ruft eine Diensteinheit mit dem Namen ContosoService1Storage unter einem Dienst ContosoService1 in einer Dienst Topologie mit dem Namen ContosoServiceTopology im ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="5a96d-119">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="5a96d-120">Beispiel 2: Abrufen einer Diensteinheit mithilfe des Ressourcenbezeichners.</span><span class="sxs-lookup"><span data-stu-id="5a96d-120">Example 2: Get a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="5a96d-121">Dieser Befehl ruft eine Diensteinheit mit dem Namen ContosoService1Storage unter einem Dienst ContosoService1 in einer Dienst Topologie mit dem Namen ContosoServiceTopology im ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="5a96d-121">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="5a96d-122">Beispiel 3: Abrufen einer Serviceeinheit mithilfe des Service Unit-Objekts.</span><span class="sxs-lookup"><span data-stu-id="5a96d-122">Example 3: Get a service unit using the service unit object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="5a96d-123">Dieser Befehl ruft eine Diensteinheit ab, deren Name, Dienstname, Dienst topologiename und ResourceGroup mit den Eigenschaften Name, Service Name, ServiceTopologyName und ResourceGroupName der $serviceUnitObject übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="5a96d-123">This command gets a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="5a96d-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a96d-124">PARAMETERS</span></span>

### <span data-ttu-id="5a96d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a96d-125">-DefaultProfile</span></span>
<span data-ttu-id="5a96d-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5a96d-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a96d-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5a96d-127">-InputObject</span></span>
<span data-ttu-id="5a96d-128">Ressourcenobjekt der Diensteinheit.</span><span class="sxs-lookup"><span data-stu-id="5a96d-128">Service unit resource object.</span></span>

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

### <span data-ttu-id="5a96d-129">-Name</span><span class="sxs-lookup"><span data-stu-id="5a96d-129">-Name</span></span>
<span data-ttu-id="5a96d-130">Der Name der Serviceeinheit.</span><span class="sxs-lookup"><span data-stu-id="5a96d-130">The name of the service unit.</span></span>

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

### <span data-ttu-id="5a96d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a96d-131">-ResourceGroupName</span></span>
<span data-ttu-id="5a96d-132">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5a96d-132">The resource group.</span></span>

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

### <span data-ttu-id="5a96d-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5a96d-133">-ResourceId</span></span>
<span data-ttu-id="5a96d-134">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="5a96d-134">The resource identifier.</span></span>

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

### <span data-ttu-id="5a96d-135">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5a96d-135">-ServiceName</span></span>
<span data-ttu-id="5a96d-136">Der Name des Diensts, zu dem die Serviceeinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="5a96d-136">The name of the service the service unit is part of.</span></span>

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

### <span data-ttu-id="5a96d-137">-Serviceobject</span><span class="sxs-lookup"><span data-stu-id="5a96d-137">-ServiceObject</span></span>
<span data-ttu-id="5a96d-138">Das Dienstobjekt, in dem die Serviceeinheit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a96d-138">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="5a96d-139">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="5a96d-139">-ServiceResourceId</span></span>
<span data-ttu-id="5a96d-140">Der Dienst Ressourcenbezeichner, in dem die Diensteinheit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a96d-140">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="5a96d-141">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="5a96d-141">-ServiceTopologyName</span></span>
<span data-ttu-id="5a96d-142">Der Name der Dienst Topologie, zu der die Serviceeinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="5a96d-142">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="5a96d-143">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="5a96d-143">-ServiceTopologyObject</span></span>
<span data-ttu-id="5a96d-144">Das Service Topology-Objekt, in dem die Diensteinheit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a96d-144">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="5a96d-145">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="5a96d-145">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="5a96d-146">Der Dienst Topologie-Ressourcenbezeichner, in dem die Diensteinheit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a96d-146">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="5a96d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a96d-147">CommonParameters</span></span>
<span data-ttu-id="5a96d-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a96d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a96d-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a96d-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a96d-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5a96d-150">INPUTS</span></span>

### <span data-ttu-id="5a96d-151">System. String</span><span class="sxs-lookup"><span data-stu-id="5a96d-151">System.String</span></span>

### <span data-ttu-id="5a96d-152">Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="5a96d-152">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="5a96d-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5a96d-153">OUTPUTS</span></span>

### <span data-ttu-id="5a96d-154">Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="5a96d-154">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="5a96d-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="5a96d-155">NOTES</span></span>

## <span data-ttu-id="5a96d-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5a96d-156">RELATED LINKS</span></span>
