---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 4b2cd4ef2dde674b10d51dc378578acbd13c4a7b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474729"
---
# <span data-ttu-id="540a9-101">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="540a9-101">Remove-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="540a9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="540a9-102">SYNOPSIS</span></span>
<span data-ttu-id="540a9-103">Löscht einen Dienst in einer Dienst Topologie.</span><span class="sxs-lookup"><span data-stu-id="540a9-103">Deletes a service in a service topology.</span></span>

## <span data-ttu-id="540a9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="540a9-104">SYNTAX</span></span>

### <span data-ttu-id="540a9-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="540a9-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="540a9-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="540a9-106">ByServiceTopologyObject</span></span>
```
Remove-AzureRmDeploymentManagerService [-Name] <String> [-ServiceTopology] <PSServiceTopologyResource> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="540a9-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="540a9-107">ByServiceTopologyResourceId</span></span>
```
Remove-AzureRmDeploymentManagerService [-Name] <String> [-ServiceTopologyResourceId] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="540a9-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="540a9-108">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerService [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="540a9-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="540a9-109">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="540a9-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="540a9-110">DESCRIPTION</span></span>
<span data-ttu-id="540a9-111">Das Cmdlet **Remove-AzureRmDeploymentManagerService** löscht einen Dienst unter einer Dienst Topologie.</span><span class="sxs-lookup"><span data-stu-id="540a9-111">The **Remove-AzureRmDeploymentManagerService** cmdlet deletes a service under a service topology.</span></span>
<span data-ttu-id="540a9-112">Geben Sie den Dienst nach dem Namen, der Dienst Topologie und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="540a9-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="540a9-113">Alternativ können Sie das Dienstobjekt oder die ressourcensource-Funktion angeben.</span><span class="sxs-lookup"><span data-stu-id="540a9-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

## <span data-ttu-id="540a9-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="540a9-114">EXAMPLES</span></span>

### <span data-ttu-id="540a9-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="540a9-115">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="540a9-116">Dieser Befehl löscht einen Dienst mit dem Namen ContosoService1 in einer Dienst Topologie mit dem Namen ContosoServiceTopology im ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="540a9-116">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="540a9-117">Beispiel 2: Löschen eines Diensts mit dem Ressourcenbezeichner</span><span class="sxs-lookup"><span data-stu-id="540a9-117">Example 2: Delete a service using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="540a9-118">Dieser Befehl löscht einen Dienst mit dem Namen ContosoService1 in einer Dienst Topologie mit dem Namen ContosoServiceTopology im ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="540a9-118">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="540a9-119">Beispiel 3: Löschen eines Diensts mit dem Dienstobjekt</span><span class="sxs-lookup"><span data-stu-id="540a9-119">Example 3: Delete a service using the service object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="540a9-120">Mit diesem Befehl wird ein Dienst gelöscht, dessen Name, Dienst topologiename und ResourceGroup den Eigenschaften Name, ServiceTopologyName und ResourceGroupName der $serviceObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="540a9-120">This command deletes a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="540a9-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="540a9-121">PARAMETERS</span></span>

### <span data-ttu-id="540a9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="540a9-122">-DefaultProfile</span></span>
<span data-ttu-id="540a9-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="540a9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="540a9-124">-Force</span><span class="sxs-lookup"><span data-stu-id="540a9-124">-Force</span></span>
<span data-ttu-id="540a9-125">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="540a9-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="540a9-126">-Name</span><span class="sxs-lookup"><span data-stu-id="540a9-126">-Name</span></span>
<span data-ttu-id="540a9-127">Der Name des Diensts.</span><span class="sxs-lookup"><span data-stu-id="540a9-127">The name of the service.</span></span>

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

### <span data-ttu-id="540a9-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="540a9-128">-PassThru</span></span>
<span data-ttu-id="540a9-129">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="540a9-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="540a9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="540a9-130">-ResourceGroupName</span></span>
<span data-ttu-id="540a9-131">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="540a9-131">The resource group.</span></span>

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

### <span data-ttu-id="540a9-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="540a9-132">-ResourceId</span></span>
<span data-ttu-id="540a9-133">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="540a9-133">The resource identifier.</span></span>

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

### <span data-ttu-id="540a9-134">-Service</span><span class="sxs-lookup"><span data-stu-id="540a9-134">-Service</span></span>
<span data-ttu-id="540a9-135">Die Ressource, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="540a9-135">The resource to be removed.</span></span>

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

### <span data-ttu-id="540a9-136">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="540a9-136">-ServiceTopology</span></span>
<span data-ttu-id="540a9-137">Das Dienst Topologie-Objekt, in dem der Dienst erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="540a9-137">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="540a9-138">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="540a9-138">-ServiceTopologyName</span></span>
<span data-ttu-id="540a9-139">Der Name der Dienst Topologie, zu der der Dienst gehört.</span><span class="sxs-lookup"><span data-stu-id="540a9-139">The name of the service topology the service belongs to.</span></span>

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

### <span data-ttu-id="540a9-140">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="540a9-140">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="540a9-141">Der Dienst Topologie-Ressourcenbezeichner, in dem der Dienst erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="540a9-141">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="540a9-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="540a9-142">-Confirm</span></span>
<span data-ttu-id="540a9-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="540a9-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="540a9-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="540a9-144">-WhatIf</span></span>
<span data-ttu-id="540a9-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="540a9-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="540a9-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="540a9-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="540a9-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="540a9-147">CommonParameters</span></span>
<span data-ttu-id="540a9-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="540a9-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="540a9-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="540a9-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="540a9-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="540a9-150">INPUTS</span></span>

### <span data-ttu-id="540a9-151">Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="540a9-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="540a9-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="540a9-152">OUTPUTS</span></span>

### <span data-ttu-id="540a9-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="540a9-153">System.Boolean</span></span>

## <span data-ttu-id="540a9-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="540a9-154">NOTES</span></span>

## <span data-ttu-id="540a9-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="540a9-155">RELATED LINKS</span></span>

[<span data-ttu-id="540a9-156">Neu – AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="540a9-156">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="540a9-157">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="540a9-157">Get-AzureRmDeploymentManagerService</span></span>](./Get-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="540a9-158">Satz-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="540a9-158">Set-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)