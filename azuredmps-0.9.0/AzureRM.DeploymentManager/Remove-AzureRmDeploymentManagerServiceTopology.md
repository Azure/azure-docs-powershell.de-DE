---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: be95f5fffe4483c74d8b1438819cf084eaa0693b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474813"
---
# <span data-ttu-id="5d23d-101">Remove-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="5d23d-101">Remove-AzureRmDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="5d23d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5d23d-102">SYNOPSIS</span></span>
<span data-ttu-id="5d23d-103">Löscht eine Dienst Topologie und alle zugehörigen Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="5d23d-103">Deletes a service topology and all its resources.</span></span>

## <span data-ttu-id="5d23d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d23d-104">SYNTAX</span></span>

### <span data-ttu-id="5d23d-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="5d23d-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d23d-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d23d-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerServiceTopology [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d23d-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="5d23d-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerServiceTopology [-ServiceTopology] <PSServiceTopologyResource> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d23d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d23d-108">DESCRIPTION</span></span>
<span data-ttu-id="5d23d-109">Das Cmdlet **Remove-AzureRmDeploymentManagerServiceTopology** löscht eine Dienst Topologie.</span><span class="sxs-lookup"><span data-stu-id="5d23d-109">The **Remove-AzureRmDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="5d23d-110">Geben Sie die Dienst Topologie nach dem Namen und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="5d23d-110">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="5d23d-111">Alternativ können Sie das ServiceTopology-Objekt oder die resourcecode-Objekt bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5d23d-111">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="5d23d-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5d23d-112">EXAMPLES</span></span>

### <span data-ttu-id="5d23d-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5d23d-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="5d23d-114">Dieser Befehl löscht eine Dienst Topologie mit dem Namen ContosoServiceTopology in der ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5d23d-114">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="5d23d-115">Beispiel 2: Löschen einer Dienst Topologie mithilfe des Ressourcenbezeichners</span><span class="sxs-lookup"><span data-stu-id="5d23d-115">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="5d23d-116">Dieser Befehl löscht eine Dienst Topologie mit dem Namen ContosoServiceTopology in der ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5d23d-116">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="5d23d-117">Beispiel 3: Löschen einer Dienst Topologie mithilfe des Dienst Topologie-Objekts</span><span class="sxs-lookup"><span data-stu-id="5d23d-117">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -ServiceTopology $serviceTopologyObject
```

<span data-ttu-id="5d23d-118">Mit diesem Befehl wird eine Dienst Topologie gelöscht, deren Name und ResourceGroup den Namen-und ResourceGroupName-Eigenschaften der $serviceTopologyObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5d23d-118">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="5d23d-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d23d-119">PARAMETERS</span></span>

### <span data-ttu-id="5d23d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d23d-120">-DefaultProfile</span></span>
<span data-ttu-id="5d23d-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5d23d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d23d-122">-Force</span><span class="sxs-lookup"><span data-stu-id="5d23d-122">-Force</span></span>
<span data-ttu-id="5d23d-123">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="5d23d-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5d23d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="5d23d-124">-Name</span></span>
<span data-ttu-id="5d23d-125">Der Name der Dienst Topologie.</span><span class="sxs-lookup"><span data-stu-id="5d23d-125">The name of the service topology.</span></span>

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

### <span data-ttu-id="5d23d-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d23d-126">-PassThru</span></span>
<span data-ttu-id="5d23d-127">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="5d23d-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5d23d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d23d-128">-ResourceGroupName</span></span>
<span data-ttu-id="5d23d-129">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5d23d-129">The resource group.</span></span>

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

### <span data-ttu-id="5d23d-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5d23d-130">-ResourceId</span></span>
<span data-ttu-id="5d23d-131">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="5d23d-131">The resource identifier.</span></span>

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

### <span data-ttu-id="5d23d-132">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="5d23d-132">-ServiceTopology</span></span>
<span data-ttu-id="5d23d-133">Die Ressource, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5d23d-133">The resource to be removed.</span></span>

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

### <span data-ttu-id="5d23d-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5d23d-134">-Confirm</span></span>
<span data-ttu-id="5d23d-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5d23d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d23d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d23d-136">-WhatIf</span></span>
<span data-ttu-id="5d23d-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5d23d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d23d-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d23d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d23d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d23d-139">CommonParameters</span></span>
<span data-ttu-id="5d23d-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d23d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d23d-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d23d-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d23d-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5d23d-142">INPUTS</span></span>

### <span data-ttu-id="5d23d-143">Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="5d23d-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="5d23d-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5d23d-144">OUTPUTS</span></span>

### <span data-ttu-id="5d23d-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5d23d-145">System.Boolean</span></span>

## <span data-ttu-id="5d23d-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="5d23d-146">NOTES</span></span>

## <span data-ttu-id="5d23d-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5d23d-147">RELATED LINKS</span></span>

[<span data-ttu-id="5d23d-148">Neu – AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="5d23d-148">New-AzureRmDeploymentManagerServiceTopology</span></span>](./New-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="5d23d-149">Get-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="5d23d-149">Get-AzureRmDeploymentManagerServiceTopology</span></span>](./Get-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="5d23d-150">Satz-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="5d23d-150">Set-AzureRmDeploymentManagerServiceTopology</span></span>](./Set-AzureRmDeploymentManagerServiceTopology.md)