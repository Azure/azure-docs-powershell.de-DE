---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
ms.openlocfilehash: 4828471d684e82d67a10bed7340cc560e843210a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297178"
---
# <span data-ttu-id="ee61e-101">Remove-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="ee61e-101">Remove-AzDeploymentManagerService</span></span>

## <span data-ttu-id="ee61e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ee61e-102">SYNOPSIS</span></span>
<span data-ttu-id="ee61e-103">Löscht den Dienst..</span><span class="sxs-lookup"><span data-stu-id="ee61e-103">Deletes the service..</span></span> <span data-ttu-id="ee61e-104">Alle Serviceeinheiten, die unter einem Dienst erstellt wurden, müssen vor dem Löschen des Diensts gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="ee61e-104">All service units created under a service need to be deleted before deleting the service.</span></span>

## <span data-ttu-id="ee61e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee61e-105">SYNTAX</span></span>

### <span data-ttu-id="ee61e-106">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="ee61e-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee61e-107">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="ee61e-107">ByServiceTopologyObject</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee61e-108">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="ee61e-108">ByServiceTopologyResourceId</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee61e-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee61e-109">ResourceId</span></span>
```
Remove-AzDeploymentManagerService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee61e-110">InputObject</span><span class="sxs-lookup"><span data-stu-id="ee61e-110">InputObject</span></span>
```
Remove-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee61e-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee61e-111">DESCRIPTION</span></span>
<span data-ttu-id="ee61e-112">Das Cmdlet **Remove-AzDeploymentManagerService** löscht einen Dienst unter einer Dienst Topologie.</span><span class="sxs-lookup"><span data-stu-id="ee61e-112">The **Remove-AzDeploymentManagerService** cmdlet deletes a service under a service topology.</span></span>
<span data-ttu-id="ee61e-113">Geben Sie den Dienst nach dem Namen, der Dienst Topologie und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ee61e-113">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="ee61e-114">Alternativ können Sie das Dienstobjekt oder die ressourcensource-Funktion angeben.</span><span class="sxs-lookup"><span data-stu-id="ee61e-114">Alternately, you can provide the Service object or the ResourceId.</span></span>

## <span data-ttu-id="ee61e-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ee61e-115">EXAMPLES</span></span>

### <span data-ttu-id="ee61e-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ee61e-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="ee61e-117">Dieser Befehl löscht einen Dienst mit dem Namen ContosoService1 in einer Dienst Topologie mit dem Namen ContosoServiceTopology im ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ee61e-117">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="ee61e-118">Beispiel 2: Löschen eines Diensts mit dem Ressourcenbezeichner</span><span class="sxs-lookup"><span data-stu-id="ee61e-118">Example 2: Delete a service using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="ee61e-119">Dieser Befehl löscht einen Dienst mit dem Namen ContosoService1 in einer Dienst Topologie mit dem Namen ContosoServiceTopology im ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ee61e-119">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="ee61e-120">Beispiel 3: Löschen eines Diensts mit dem Dienstobjekt</span><span class="sxs-lookup"><span data-stu-id="ee61e-120">Example 3: Delete a service using the service object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="ee61e-121">Mit diesem Befehl wird ein Dienst gelöscht, dessen Name, Dienst topologiename und ResourceGroup den Eigenschaften Name, ServiceTopologyName und ResourceGroupName der $serviceObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="ee61e-121">This command deletes a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="ee61e-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee61e-122">PARAMETERS</span></span>

### <span data-ttu-id="ee61e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee61e-123">-DefaultProfile</span></span>
<span data-ttu-id="ee61e-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ee61e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee61e-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ee61e-125">-InputObject</span></span>
<span data-ttu-id="ee61e-126">Dienstobjekt.</span><span class="sxs-lookup"><span data-stu-id="ee61e-126">Service object.</span></span>

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

### <span data-ttu-id="ee61e-127">-Name</span><span class="sxs-lookup"><span data-stu-id="ee61e-127">-Name</span></span>
<span data-ttu-id="ee61e-128">Der Name des Diensts.</span><span class="sxs-lookup"><span data-stu-id="ee61e-128">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee61e-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee61e-129">-PassThru</span></span>
<span data-ttu-id="ee61e-130">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="ee61e-130">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee61e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee61e-131">-ResourceGroupName</span></span>
<span data-ttu-id="ee61e-132">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ee61e-132">The resource group.</span></span>

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

### <span data-ttu-id="ee61e-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ee61e-133">-ResourceId</span></span>
<span data-ttu-id="ee61e-134">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="ee61e-134">The resource identifier.</span></span>

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

### <span data-ttu-id="ee61e-135">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="ee61e-135">-ServiceTopologyName</span></span>
<span data-ttu-id="ee61e-136">Der Name der Dienst Topologie.</span><span class="sxs-lookup"><span data-stu-id="ee61e-136">The name of the service topology.</span></span>

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

### <span data-ttu-id="ee61e-137">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="ee61e-137">-ServiceTopologyObject</span></span>
<span data-ttu-id="ee61e-138">Das Dienst Topologie-Objekt, in dem der Dienst erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ee61e-138">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee61e-139">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="ee61e-139">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="ee61e-140">Der Dienst Topologie-Ressourcenbezeichner, in dem der Dienst erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ee61e-140">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee61e-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ee61e-141">-Confirm</span></span>
<span data-ttu-id="ee61e-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ee61e-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee61e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee61e-143">-WhatIf</span></span>
<span data-ttu-id="ee61e-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ee61e-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee61e-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ee61e-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee61e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee61e-146">CommonParameters</span></span>
<span data-ttu-id="ee61e-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee61e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee61e-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee61e-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee61e-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ee61e-149">INPUTS</span></span>

### <span data-ttu-id="ee61e-150">System. String</span><span class="sxs-lookup"><span data-stu-id="ee61e-150">System.String</span></span>

### <span data-ttu-id="ee61e-151">Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="ee61e-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="ee61e-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ee61e-152">OUTPUTS</span></span>

### <span data-ttu-id="ee61e-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ee61e-153">System.Boolean</span></span>

## <span data-ttu-id="ee61e-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="ee61e-154">NOTES</span></span>

## <span data-ttu-id="ee61e-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ee61e-155">RELATED LINKS</span></span>
