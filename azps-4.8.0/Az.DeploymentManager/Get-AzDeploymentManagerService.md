---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
ms.openlocfilehash: da59c17b7aef90cd3f5c5b374d663292153be140
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008535"
---
# <span data-ttu-id="ba868-101">Get-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="ba868-101">Get-AzDeploymentManagerService</span></span>

## <span data-ttu-id="ba868-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ba868-102">SYNOPSIS</span></span>
<span data-ttu-id="ba868-103">Ruft den Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="ba868-103">Gets the service.</span></span>

## <span data-ttu-id="ba868-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba868-104">SYNTAX</span></span>

### <span data-ttu-id="ba868-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="ba868-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba868-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="ba868-106">ByServiceTopologyObject</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ba868-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="ba868-107">ByServiceTopologyResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba868-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba868-108">ResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ba868-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="ba868-109">InputObject</span></span>
```
Get-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba868-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba868-110">DESCRIPTION</span></span>
<span data-ttu-id="ba868-111">Das Cmdlet " **Get-AzDeploymentManagerService** " Ruft einen Dienst unter einer Dienst Topologie ab und gibt ein Objekt zurück, das diesen Dienst darstellt.</span><span class="sxs-lookup"><span data-stu-id="ba868-111">The **Get-AzDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="ba868-112">Geben Sie den Dienst nach dem Namen, der Dienst Topologie und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ba868-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="ba868-113">Alternativ können Sie das Dienstobjekt oder die ressourcensource-Funktion angeben.</span><span class="sxs-lookup"><span data-stu-id="ba868-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="ba868-114">Sie können dieses Objekt lokal ändern und dann mithilfe des Set-AzDeploymentManagerService-Cmdlets Änderungen am Dienst vornehmen.</span><span class="sxs-lookup"><span data-stu-id="ba868-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="ba868-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ba868-115">EXAMPLES</span></span>

### <span data-ttu-id="ba868-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ba868-116">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="ba868-117">Dieser Befehl ruft einen Dienst mit dem Namen ContosoService1 in einer Dienst Topologie mit dem Namen ContosoServiceTopology im ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="ba868-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="ba868-118">Beispiel 2: Abrufen eines Diensts mithilfe des Ressourcenbezeichners.</span><span class="sxs-lookup"><span data-stu-id="ba868-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="ba868-119">Dieser Befehl ruft einen Dienst mit dem Namen ContosoService1 in einer Dienst Topologie mit dem Namen ContosoServiceTopology im ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="ba868-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="ba868-120">Beispiel 3: Abrufen eines Diensts mithilfe des Dienstobjekts.</span><span class="sxs-lookup"><span data-stu-id="ba868-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="ba868-121">Dieser Befehl ruft einen Dienst ab, dessen Name, Dienst topologiename und ResourceGroup mit den Eigenschaften Name, ServiceTopologyName und ResourceGroupName der $serviceObject übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="ba868-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
 

## <span data-ttu-id="ba868-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba868-122">PARAMETERS</span></span>

### <span data-ttu-id="ba868-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba868-123">-DefaultProfile</span></span>
<span data-ttu-id="ba868-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ba868-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba868-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ba868-125">-InputObject</span></span>
<span data-ttu-id="ba868-126">Dienstobjekt.</span><span class="sxs-lookup"><span data-stu-id="ba868-126">Service object.</span></span>

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

### <span data-ttu-id="ba868-127">-Name</span><span class="sxs-lookup"><span data-stu-id="ba868-127">-Name</span></span>
<span data-ttu-id="ba868-128">Der Name des Diensts.</span><span class="sxs-lookup"><span data-stu-id="ba868-128">The name of the service.</span></span>

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

### <span data-ttu-id="ba868-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba868-129">-ResourceGroupName</span></span>
<span data-ttu-id="ba868-130">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ba868-130">The resource group.</span></span>

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

### <span data-ttu-id="ba868-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ba868-131">-ResourceId</span></span>
<span data-ttu-id="ba868-132">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="ba868-132">The resource identifier.</span></span>

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

### <span data-ttu-id="ba868-133">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="ba868-133">-ServiceTopologyName</span></span>
<span data-ttu-id="ba868-134">Der Name der Dienst Topologie.</span><span class="sxs-lookup"><span data-stu-id="ba868-134">The name of the service topology.</span></span>

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

### <span data-ttu-id="ba868-135">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="ba868-135">-ServiceTopologyObject</span></span>
<span data-ttu-id="ba868-136">Das Dienst Topologie-Objekt, in dem der Dienst erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ba868-136">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="ba868-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="ba868-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="ba868-138">Der Dienst Topologie-Ressourcenbezeichner, in dem der Dienst erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ba868-138">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="ba868-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba868-139">CommonParameters</span></span>
<span data-ttu-id="ba868-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba868-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba868-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba868-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba868-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ba868-142">INPUTS</span></span>

### <span data-ttu-id="ba868-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ba868-143">System.String</span></span>

### <span data-ttu-id="ba868-144">Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="ba868-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="ba868-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ba868-145">OUTPUTS</span></span>

### <span data-ttu-id="ba868-146">Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="ba868-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="ba868-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="ba868-147">NOTES</span></span>

## <span data-ttu-id="ba868-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ba868-148">RELATED LINKS</span></span>
