---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 695a10eb71cc2c4bd1a6bc7eef6cba265d524fe6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661193"
---
# <span data-ttu-id="34d0a-101">Remove-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="34d0a-101">Remove-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="34d0a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="34d0a-102">SYNOPSIS</span></span>
<span data-ttu-id="34d0a-103">Löscht die Dienst Topologie.</span><span class="sxs-lookup"><span data-stu-id="34d0a-103">Deletes the service topology.</span></span> <span data-ttu-id="34d0a-104">Alle Dienste, die unter einer Dienst Topologie erstellt wurden, müssen vor dem Löschen der Dienst Topologie gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="34d0a-104">All services created under a service topology need to be deleted before deleting the service topology.</span></span>

## <span data-ttu-id="34d0a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="34d0a-105">SYNTAX</span></span>

### <span data-ttu-id="34d0a-106">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="34d0a-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34d0a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="34d0a-107">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34d0a-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="34d0a-108">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34d0a-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34d0a-109">DESCRIPTION</span></span>
<span data-ttu-id="34d0a-110">Das Cmdlet **Remove-AzDeploymentManagerServiceTopology** löscht eine Dienst Topologie.</span><span class="sxs-lookup"><span data-stu-id="34d0a-110">The **Remove-AzDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="34d0a-111">Geben Sie die Dienst Topologie nach dem Namen und dem Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="34d0a-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="34d0a-112">Alternativ können Sie das ServiceTopology-Objekt oder die resourcecode-Objekt bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="34d0a-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="34d0a-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="34d0a-113">EXAMPLES</span></span>

### <span data-ttu-id="34d0a-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="34d0a-114">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="34d0a-115">Dieser Befehl löscht eine Dienst Topologie mit dem Namen ContosoServiceTopology in der ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="34d0a-115">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="34d0a-116">Beispiel 2: Löschen einer Dienst Topologie mithilfe des Ressourcenbezeichners</span><span class="sxs-lookup"><span data-stu-id="34d0a-116">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="34d0a-117">Dieser Befehl löscht eine Dienst Topologie mit dem Namen ContosoServiceTopology in der ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="34d0a-117">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="34d0a-118">Beispiel 3: Löschen einer Dienst Topologie mithilfe des Dienst Topologie-Objekts</span><span class="sxs-lookup"><span data-stu-id="34d0a-118">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="34d0a-119">Mit diesem Befehl wird eine Dienst Topologie gelöscht, deren Name und ResourceGroup den Namen-und ResourceGroupName-Eigenschaften der $serviceTopologyObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="34d0a-119">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="34d0a-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="34d0a-120">PARAMETERS</span></span>

### <span data-ttu-id="34d0a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34d0a-121">-DefaultProfile</span></span>
<span data-ttu-id="34d0a-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="34d0a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34d0a-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="34d0a-123">-InputObject</span></span>
<span data-ttu-id="34d0a-124">Die Ressource, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="34d0a-124">The resource to be removed.</span></span>

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

### <span data-ttu-id="34d0a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="34d0a-125">-Name</span></span>
<span data-ttu-id="34d0a-126">Der Name der Dienst Topologie.</span><span class="sxs-lookup"><span data-stu-id="34d0a-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="34d0a-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34d0a-127">-PassThru</span></span>
<span data-ttu-id="34d0a-128">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="34d0a-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="34d0a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34d0a-129">-ResourceGroupName</span></span>
<span data-ttu-id="34d0a-130">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="34d0a-130">The resource group.</span></span>

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

### <span data-ttu-id="34d0a-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="34d0a-131">-ResourceId</span></span>
<span data-ttu-id="34d0a-132">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="34d0a-132">The resource identifier.</span></span>

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

### <span data-ttu-id="34d0a-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="34d0a-133">-Confirm</span></span>
<span data-ttu-id="34d0a-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="34d0a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34d0a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34d0a-135">-WhatIf</span></span>
<span data-ttu-id="34d0a-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="34d0a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34d0a-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="34d0a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34d0a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34d0a-138">CommonParameters</span></span>
<span data-ttu-id="34d0a-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34d0a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34d0a-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34d0a-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34d0a-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="34d0a-141">INPUTS</span></span>

### <span data-ttu-id="34d0a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="34d0a-142">System.String</span></span>

### <span data-ttu-id="34d0a-143">Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="34d0a-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="34d0a-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="34d0a-144">OUTPUTS</span></span>

### <span data-ttu-id="34d0a-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="34d0a-145">System.Boolean</span></span>

## <span data-ttu-id="34d0a-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="34d0a-146">NOTES</span></span>

## <span data-ttu-id="34d0a-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="34d0a-147">RELATED LINKS</span></span>
