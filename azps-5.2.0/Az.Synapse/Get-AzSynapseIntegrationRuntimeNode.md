---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 5df58da7ef5fa0829da27f4d6a46372f42bc9dc5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297352"
---
# <span data-ttu-id="9dbbb-101">Get-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="9dbbb-101">Get-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="9dbbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9dbbb-102">SYNOPSIS</span></span>
<span data-ttu-id="9dbbb-103">Ruft Informationen zu Integrations-Runtime-Knoten ab.</span><span class="sxs-lookup"><span data-stu-id="9dbbb-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="9dbbb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9dbbb-104">SYNTAX</span></span>

### <span data-ttu-id="9dbbb-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9dbbb-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9dbbb-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9dbbb-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9dbbb-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9dbbb-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9dbbb-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9dbbb-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9dbbb-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9dbbb-109">DESCRIPTION</span></span>
<span data-ttu-id="9dbbb-110">Das **Cmdlet "Get-AzSynapseIntegrationRuntimeNode"** ruft die Detailinformationen eines Integrationslaufzeitknotens ab.</span><span class="sxs-lookup"><span data-stu-id="9dbbb-110">The **Get-AzSynapseIntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="9dbbb-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9dbbb-111">EXAMPLES</span></span>

### <span data-ttu-id="9dbbb-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9dbbb-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'
```

<span data-ttu-id="9dbbb-113">Das Cmdlet ruft Informationen des Knotens "Node_1" in der selbst gehosteten Integrationslaufzeit "test-selfhost-ir" im Arbeitsbereich ContosoWorkspace ab.</span><span class="sxs-lookup"><span data-stu-id="9dbbb-113">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="9dbbb-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9dbbb-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress
```

<span data-ttu-id="9dbbb-115">Das Cmdlet ruft Informationen des Knotens "Node_1" in der selbst gehosteten Integrationslaufzeit "test-selfhost-ir" im Arbeitsbereich "test-df-eu2" ab, einschließlich der IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="9dbbb-115">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="9dbbb-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9dbbb-116">PARAMETERS</span></span>

### <span data-ttu-id="9dbbb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dbbb-117">-DefaultProfile</span></span>
<span data-ttu-id="9dbbb-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9dbbb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dbbb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9dbbb-119">-InputObject</span></span>
<span data-ttu-id="9dbbb-120">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9dbbb-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="9dbbb-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="9dbbb-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="9dbbb-122">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="9dbbb-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dbbb-123">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="9dbbb-123">-IpAddress</span></span>
<span data-ttu-id="9dbbb-124">Die IP-Adresse des Integrationslaufzeitknotens.</span><span class="sxs-lookup"><span data-stu-id="9dbbb-124">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="9dbbb-125">-Name</span><span class="sxs-lookup"><span data-stu-id="9dbbb-125">-Name</span></span>
<span data-ttu-id="9dbbb-126">Der Name des Integrations-Runtime-Knotens.</span><span class="sxs-lookup"><span data-stu-id="9dbbb-126">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dbbb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dbbb-127">-ResourceGroupName</span></span>
<span data-ttu-id="9dbbb-128">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="9dbbb-128">Resource group name.</span></span>

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

### <span data-ttu-id="9dbbb-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9dbbb-129">-ResourceId</span></span>
<span data-ttu-id="9dbbb-130">Ressourcenbezeichner der Laufzeit der Synapse-Integration.</span><span class="sxs-lookup"><span data-stu-id="9dbbb-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="9dbbb-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9dbbb-131">-WorkspaceName</span></span>
<span data-ttu-id="9dbbb-132">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="9dbbb-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9dbbb-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9dbbb-133">-WorkspaceObject</span></span>
<span data-ttu-id="9dbbb-134">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="9dbbb-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9dbbb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dbbb-135">CommonParameters</span></span>
<span data-ttu-id="9dbbb-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dbbb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dbbb-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9dbbb-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dbbb-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9dbbb-138">INPUTS</span></span>

### <span data-ttu-id="9dbbb-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9dbbb-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="9dbbb-140">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9dbbb-140">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="9dbbb-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9dbbb-141">OUTPUTS</span></span>

### <span data-ttu-id="9dbbb-142">Microsoft.Azure.Commands.Synapse.Models.PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="9dbbb-142">Microsoft.Azure.Commands.Synapse.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="9dbbb-143">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="9dbbb-143">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="9dbbb-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9dbbb-144">NOTES</span></span>

## <span data-ttu-id="9dbbb-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9dbbb-145">RELATED LINKS</span></span>
