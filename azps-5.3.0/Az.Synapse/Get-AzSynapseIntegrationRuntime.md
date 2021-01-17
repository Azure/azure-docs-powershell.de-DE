---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 285c0877441cabf51c723a472208cc002867fa7a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460023"
---
# <span data-ttu-id="ac96b-101">Get-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ac96b-101">Get-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="ac96b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac96b-102">SYNOPSIS</span></span>
<span data-ttu-id="ac96b-103">Ruft Informationen zu Integrations-Runtime-Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="ac96b-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="ac96b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ac96b-104">SYNTAX</span></span>

### <span data-ttu-id="ac96b-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ac96b-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac96b-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac96b-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime [-Name <String>] -WorkspaceObject <PSSynapseWorkspace> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac96b-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac96b-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -ResourceId <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ac96b-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac96b-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac96b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ac96b-109">DESCRIPTION</span></span>
<span data-ttu-id="ac96b-110">Das **Cmdlet "Get-AzSynapseIntegrationRuntime"** ruft Informationen zu Integrationslaufzeiten in einem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="ac96b-110">The **Get-AzSynapseIntegrationRuntime** cmdlet gets information about integration runtimes in a workspace.</span></span>
<span data-ttu-id="ac96b-111">Wenn Sie den Namen einer Integrationslaufzeit angeben, ruft dieses Cmdlet Informationen zu dieser Integrationslaufzeit ab.</span><span class="sxs-lookup"><span data-stu-id="ac96b-111">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="ac96b-112">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Integrationslaufzeiten in einem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="ac96b-112">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a workspace.</span></span>

## <span data-ttu-id="ac96b-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ac96b-113">EXAMPLES</span></span>

### <span data-ttu-id="ac96b-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ac96b-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="ac96b-115">Listen Sie alle Integrationslaufzeiten im Arbeitsbereich "ContosoWorkspace" auf.</span><span class="sxs-lookup"><span data-stu-id="ac96b-115">List all integration runtimes in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="ac96b-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ac96b-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="ac96b-117">Dieser Befehl zeigt Informationen zur Integrationslaufzeit mit dem Namen "test-selfhost-ir" im Arbeitsbereich "ContosoWorkspace" an.</span><span class="sxs-lookup"><span data-stu-id="ac96b-117">This command displays information about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="ac96b-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ac96b-118">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Status
```

<span data-ttu-id="ac96b-119">Dieser Befehl zeigt den Detailstatus der Integrationslaufzeit mit dem Namen "test-selfhost-ir" im Arbeitsbereich "ContosoWorkspace" an.</span><span class="sxs-lookup"><span data-stu-id="ac96b-119">This command displays detail status about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="ac96b-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac96b-120">PARAMETERS</span></span>

### <span data-ttu-id="ac96b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac96b-121">-DefaultProfile</span></span>
<span data-ttu-id="ac96b-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ac96b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac96b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac96b-123">-InputObject</span></span>
<span data-ttu-id="ac96b-124">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ac96b-124">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac96b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ac96b-125">-Name</span></span>
<span data-ttu-id="ac96b-126">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="ac96b-126">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac96b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac96b-127">-ResourceGroupName</span></span>
<span data-ttu-id="ac96b-128">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="ac96b-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac96b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac96b-129">-ResourceId</span></span>
<span data-ttu-id="ac96b-130">Ressourcenbezeichner der Laufzeit der Synapse-Integration.</span><span class="sxs-lookup"><span data-stu-id="ac96b-130">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac96b-131">-Status</span><span class="sxs-lookup"><span data-stu-id="ac96b-131">-Status</span></span>
<span data-ttu-id="ac96b-132">Der Detailstatus der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="ac96b-132">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="ac96b-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ac96b-133">-WorkspaceName</span></span>
<span data-ttu-id="ac96b-134">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="ac96b-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac96b-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ac96b-135">-WorkspaceObject</span></span>
<span data-ttu-id="ac96b-136">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="ac96b-136">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac96b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac96b-137">CommonParameters</span></span>
<span data-ttu-id="ac96b-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac96b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac96b-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ac96b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac96b-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ac96b-140">INPUTS</span></span>

### <span data-ttu-id="ac96b-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ac96b-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ac96b-142">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ac96b-142">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="ac96b-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ac96b-143">OUTPUTS</span></span>

### <span data-ttu-id="ac96b-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ac96b-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="ac96b-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ac96b-145">NOTES</span></span>

## <span data-ttu-id="ac96b-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ac96b-146">RELATED LINKS</span></span>
