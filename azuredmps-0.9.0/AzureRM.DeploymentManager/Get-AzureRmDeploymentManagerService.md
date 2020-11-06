---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerservice
schema: 2.0.0
content_git_url: ''
ms.openlocfilehash: 655cfeeae35d1b48bbfe2149fd4262dffe72ae09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475745"
---
# <span data-ttu-id="f4dde-101">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="f4dde-101">Get-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="f4dde-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f4dde-102">SYNOPSIS</span></span>
<span data-ttu-id="f4dde-103">Ruft einen Dienst in einer Dienst Topologie ab.</span><span class="sxs-lookup"><span data-stu-id="f4dde-103">Gets a service in a service topology.</span></span>

## <span data-ttu-id="f4dde-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4dde-104">SYNTAX</span></span>

### <span data-ttu-id="f4dde-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="f4dde-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4dde-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="f4dde-106">ByServiceTopologyObject</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4dde-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="f4dde-107">ByServiceTopologyResourceId</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4dde-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4dde-108">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f4dde-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="f4dde-109">InputObject</span></span>
```
Get-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4dde-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4dde-110">DESCRIPTION</span></span>
<span data-ttu-id="f4dde-111">Das Cmdlet " **Get-AzureRmDeploymentManagerService** " Ruft einen Dienst unter einer Dienst Topologie ab und gibt ein Objekt zurück, das diesen Dienst darstellt.</span><span class="sxs-lookup"><span data-stu-id="f4dde-111">The **Get-AzureRmDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="f4dde-112">Geben Sie den Dienst nach dem Namen, der Dienst Topologie und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="f4dde-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="f4dde-113">Alternativ können Sie das Dienstobjekt oder die ressourcensource-Funktion angeben.</span><span class="sxs-lookup"><span data-stu-id="f4dde-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="f4dde-114">Sie können dieses Objekt lokal ändern und dann mithilfe des Set-AzureRmDeploymentManagerService-Cmdlets Änderungen am Dienst vornehmen.</span><span class="sxs-lookup"><span data-stu-id="f4dde-114">You can modify this object locally, and then apply changes to the service by using the Set-AzureRmDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="f4dde-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f4dde-115">EXAMPLES</span></span>

### <span data-ttu-id="f4dde-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f4dde-116">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="f4dde-117">Dieser Befehl ruft einen Dienst mit dem Namen ContosoService1 in einer Dienst Topologie mit dem Namen ContosoServiceTopology im ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="f4dde-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="f4dde-118">Beispiel 2: Abrufen eines Diensts mithilfe des Ressourcenbezeichners.</span><span class="sxs-lookup"><span data-stu-id="f4dde-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="f4dde-119">Dieser Befehl ruft einen Dienst mit dem Namen ContosoService1 in einer Dienst Topologie mit dem Namen ContosoServiceTopology im ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="f4dde-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="f4dde-120">Beispiel 3: Abrufen eines Diensts mithilfe des Dienstobjekts.</span><span class="sxs-lookup"><span data-stu-id="f4dde-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="f4dde-121">Dieser Befehl ruft einen Dienst ab, dessen Name, Dienst topologiename und ResourceGroup mit den Eigenschaften Name, ServiceTopologyName und ResourceGroupName der $serviceObject übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="f4dde-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="f4dde-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4dde-122">PARAMETERS</span></span>

### <span data-ttu-id="f4dde-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4dde-123">-DefaultProfile</span></span>
<span data-ttu-id="f4dde-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f4dde-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4dde-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f4dde-125">-Name</span></span>
<span data-ttu-id="f4dde-126">Der Name des Diensts.</span><span class="sxs-lookup"><span data-stu-id="f4dde-126">The name of the service.</span></span>

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

### <span data-ttu-id="f4dde-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4dde-127">-ResourceGroupName</span></span>
<span data-ttu-id="f4dde-128">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f4dde-128">The resource group.</span></span>

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

### <span data-ttu-id="f4dde-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f4dde-129">-ResourceId</span></span>
<span data-ttu-id="f4dde-130">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="f4dde-130">The resource identifier.</span></span>

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

### <span data-ttu-id="f4dde-131">-Service</span><span class="sxs-lookup"><span data-stu-id="f4dde-131">-Service</span></span>
<span data-ttu-id="f4dde-132">Dienstobjekt.</span><span class="sxs-lookup"><span data-stu-id="f4dde-132">Service object.</span></span>

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

### <span data-ttu-id="f4dde-133">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="f4dde-133">-ServiceTopology</span></span>
<span data-ttu-id="f4dde-134">Das Dienst Topologie-Objekt, in dem der Dienst erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f4dde-134">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="f4dde-135">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="f4dde-135">-ServiceTopologyName</span></span>
<span data-ttu-id="f4dde-136">Der Name der Dienst Topologie.</span><span class="sxs-lookup"><span data-stu-id="f4dde-136">The name of the service topology.</span></span>

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

### <span data-ttu-id="f4dde-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="f4dde-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="f4dde-138">Der Dienst Topologie-Ressourcenbezeichner, in dem der Dienst erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f4dde-138">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="f4dde-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4dde-139">CommonParameters</span></span>
<span data-ttu-id="f4dde-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4dde-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4dde-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4dde-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4dde-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f4dde-142">INPUTS</span></span>

### <span data-ttu-id="f4dde-143">Keine</span><span class="sxs-lookup"><span data-stu-id="f4dde-143">None</span></span>

## <span data-ttu-id="f4dde-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f4dde-144">OUTPUTS</span></span>

### <span data-ttu-id="f4dde-145">Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="f4dde-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="f4dde-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="f4dde-146">NOTES</span></span>

## <span data-ttu-id="f4dde-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f4dde-147">RELATED LINKS</span></span>

[<span data-ttu-id="f4dde-148">Neu – AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="f4dde-148">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="f4dde-149">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="f4dde-149">Remove-AzureRmDeploymentManagerService</span></span>](./Remove-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="f4dde-150">Satz-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="f4dde-150">Set-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)