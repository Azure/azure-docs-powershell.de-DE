---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: e83f619bd14a2e0ba2012a206d0c3dffd5204863
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661911"
---
# <span data-ttu-id="3abd4-101">Get-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="3abd4-101">Get-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="3abd4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3abd4-102">SYNOPSIS</span></span>
<span data-ttu-id="3abd4-103">Ruft eine Diensteinheit ab.</span><span class="sxs-lookup"><span data-stu-id="3abd4-103">Gets a service unit.</span></span>

## <span data-ttu-id="3abd4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3abd4-104">SYNTAX</span></span>

### <span data-ttu-id="3abd4-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="3abd4-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3abd4-106">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="3abd4-106">ByServiceObject</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String>
 [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3abd4-107">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="3abd4-107">ByServiceResourceId</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3abd4-108">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="3abd4-108">ByTopologyObjectAndServiceName</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3abd4-109">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="3abd4-109">ByTopologyResourceAndServiceName</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3abd4-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3abd4-110">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3abd4-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="3abd4-111">InputObject</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ServiceUnit] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3abd4-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3abd4-112">DESCRIPTION</span></span>
<span data-ttu-id="3abd4-113">Das Cmdlet " **Get-AzureRmDeploymentManagerServiceUnit** " Ruft eine Diensteinheit in einem Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="3abd4-113">The **Get-AzureRmDeploymentManagerServiceUnit** cmdlet gets a service unit in a service.</span></span>

<span data-ttu-id="3abd4-114">Geben Sie die Diensteinheit nach dem Namen, dem Dienst, unter dem Sie definiert wurde, dem Namen der Dienst Topologie und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="3abd4-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="3abd4-115">Alternativ können Sie das Serviceunit-Objekt oder die resourcecode-Objekt bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="3abd4-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

<span data-ttu-id="3abd4-116">Sie können dieses Objekt lokal ändern und dann mithilfe des Set-AzureRmDeploymentManagerServiceUnit-Cmdlets Änderungen an der Diensteinheit vornehmen.</span><span class="sxs-lookup"><span data-stu-id="3abd4-116">You can modify this object locally, and then apply changes to the service unit by using the Set-AzureRmDeploymentManagerServiceUnit cmdlet.</span></span>

## <span data-ttu-id="3abd4-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3abd4-117">EXAMPLES</span></span>

### <span data-ttu-id="3abd4-118">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3abd4-118">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="3abd4-119">Dieser Befehl ruft eine Diensteinheit mit dem Namen ContosoService1Storage unter einem Dienst ContosoService1 in einer Dienst Topologie mit dem Namen ContosoServiceTopology im ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="3abd4-119">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="3abd4-120">Beispiel 2: Abrufen einer Diensteinheit mithilfe des Ressourcenbezeichners.</span><span class="sxs-lookup"><span data-stu-id="3abd4-120">Example 2: Get a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="3abd4-121">Dieser Befehl ruft eine Diensteinheit mit dem Namen ContosoService1Storage unter einem Dienst ContosoService1 in einer Dienst Topologie mit dem Namen ContosoServiceTopology im ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="3abd4-121">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="3abd4-122">Beispiel 3: Abrufen einer Serviceeinheit mithilfe des Service Unit-Objekts.</span><span class="sxs-lookup"><span data-stu-id="3abd4-122">Example 3: Get a service unit using the service unit object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceUnit -ServiceUnit $serviceUnitObject
```

<span data-ttu-id="3abd4-123">Dieser Befehl ruft eine Diensteinheit ab, deren Name, Dienstname, Dienst topologiename und ResourceGroup mit den Eigenschaften Name, Service Name, ServiceTopologyName und ResourceGroupName der $serviceUnitObject übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="3abd4-123">This command gets a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="3abd4-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="3abd4-124">PARAMETERS</span></span>

### <span data-ttu-id="3abd4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3abd4-125">-DefaultProfile</span></span>
<span data-ttu-id="3abd4-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3abd4-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3abd4-127">-Name</span><span class="sxs-lookup"><span data-stu-id="3abd4-127">-Name</span></span>
<span data-ttu-id="3abd4-128">Der Name der Serviceeinheit.</span><span class="sxs-lookup"><span data-stu-id="3abd4-128">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3abd4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3abd4-129">-ResourceGroupName</span></span>
<span data-ttu-id="3abd4-130">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3abd4-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3abd4-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3abd4-131">-ResourceId</span></span>
<span data-ttu-id="3abd4-132">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="3abd4-132">The resource identifier.</span></span>

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

### <span data-ttu-id="3abd4-133">-Service</span><span class="sxs-lookup"><span data-stu-id="3abd4-133">-Service</span></span>
<span data-ttu-id="3abd4-134">Das Dienstobjekt, in dem die Serviceeinheit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3abd4-134">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="3abd4-135">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3abd4-135">-ServiceName</span></span>
<span data-ttu-id="3abd4-136">Der Name des Diensts, zu dem die Serviceeinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="3abd4-136">The name of the service the service unit is part of.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3abd4-137">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="3abd4-137">-ServiceResourceId</span></span>
<span data-ttu-id="3abd4-138">Der Dienst Ressourcenbezeichner, in dem die Diensteinheit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3abd4-138">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="3abd4-139">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="3abd4-139">-ServiceTopology</span></span>
<span data-ttu-id="3abd4-140">Das Service Topology-Objekt, in dem die Diensteinheit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3abd4-140">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="3abd4-141">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="3abd4-141">-ServiceTopologyName</span></span>
<span data-ttu-id="3abd4-142">Der Name der Dienst Topologie, zu der die Serviceeinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="3abd4-142">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="3abd4-143">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="3abd4-143">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="3abd4-144">Der Dienst Topologie-Ressourcenbezeichner, in dem die Diensteinheit erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3abd4-144">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="3abd4-145">-ServiceUnit</span><span class="sxs-lookup"><span data-stu-id="3abd4-145">-ServiceUnit</span></span>
<span data-ttu-id="3abd4-146">Ressourcenobjekt der Diensteinheit.</span><span class="sxs-lookup"><span data-stu-id="3abd4-146">Service unit resource object.</span></span>

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

### <span data-ttu-id="3abd4-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3abd4-147">CommonParameters</span></span>
<span data-ttu-id="3abd4-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3abd4-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3abd4-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3abd4-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3abd4-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3abd4-150">INPUTS</span></span>

### <span data-ttu-id="3abd4-151">Keine</span><span class="sxs-lookup"><span data-stu-id="3abd4-151">None</span></span>

## <span data-ttu-id="3abd4-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3abd4-152">OUTPUTS</span></span>

### <span data-ttu-id="3abd4-153">Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="3abd4-153">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="3abd4-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="3abd4-154">NOTES</span></span>

## <span data-ttu-id="3abd4-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3abd4-155">RELATED LINKS</span></span>

[<span data-ttu-id="3abd4-156">Neu – AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="3abd4-156">New-AzureRmDeploymentManagerServiceUnit</span></span>](./New-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="3abd4-157">Remove-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="3abd4-157">Remove-AzureRmDeploymentManagerServiceUnit</span></span>](./Remove-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="3abd4-158">Satz-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="3abd4-158">Set-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)