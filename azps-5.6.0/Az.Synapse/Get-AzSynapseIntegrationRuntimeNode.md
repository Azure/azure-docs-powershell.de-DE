---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: dbd791b3ab77889e8c78279b576b614c4d86b4b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940723"
---
# <span data-ttu-id="6edca-101">Get-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="6edca-101">Get-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="6edca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6edca-102">SYNOPSIS</span></span>
<span data-ttu-id="6edca-103">Ruft Informationen zum Integrations-Runtime-Knoten ab.</span><span class="sxs-lookup"><span data-stu-id="6edca-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="6edca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6edca-104">SYNTAX</span></span>

### <span data-ttu-id="6edca-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6edca-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6edca-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6edca-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6edca-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6edca-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6edca-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6edca-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6edca-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6edca-109">DESCRIPTION</span></span>
<span data-ttu-id="6edca-110">Das **Cmdlet Get-AzSynapseIntegrationRuntimeNode** ruft die Detailinformationen eines Integrations-Runtime-Knotens ab.</span><span class="sxs-lookup"><span data-stu-id="6edca-110">The **Get-AzSynapseIntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="6edca-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6edca-111">EXAMPLES</span></span>

### <span data-ttu-id="6edca-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6edca-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'
```

<span data-ttu-id="6edca-113">Das Cmdlet ruft Informationen des Knotens "Node_1" in der selbst gehosteten Integrations-Runtime "test-selfhost-ir" im Arbeitsbereich ContosoWorkspace ab.</span><span class="sxs-lookup"><span data-stu-id="6edca-113">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="6edca-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6edca-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress
```

<span data-ttu-id="6edca-115">Das Cmdlet ruft Informationen des Knotens "Node_1" in der selbst gehosteten Integrations-Runtime "test-selfhost-ir" im Arbeitsbereich "test-df-eu2" ab, einschließlich der IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="6edca-115">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="6edca-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6edca-116">PARAMETERS</span></span>

### <span data-ttu-id="6edca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6edca-117">-DefaultProfile</span></span>
<span data-ttu-id="6edca-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6edca-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6edca-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6edca-119">-InputObject</span></span>
<span data-ttu-id="6edca-120">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="6edca-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="6edca-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="6edca-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="6edca-122">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="6edca-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="6edca-123">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="6edca-123">-IpAddress</span></span>
<span data-ttu-id="6edca-124">Die IP-Adresse des Integrations-Runtime-Knotens.</span><span class="sxs-lookup"><span data-stu-id="6edca-124">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="6edca-125">-Name</span><span class="sxs-lookup"><span data-stu-id="6edca-125">-Name</span></span>
<span data-ttu-id="6edca-126">Der Name des Integrations-Runtime-Knotens.</span><span class="sxs-lookup"><span data-stu-id="6edca-126">The integration runtime node name.</span></span>

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

### <span data-ttu-id="6edca-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6edca-127">-ResourceGroupName</span></span>
<span data-ttu-id="6edca-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6edca-128">Resource group name.</span></span>

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

### <span data-ttu-id="6edca-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6edca-129">-ResourceId</span></span>
<span data-ttu-id="6edca-130">Ressourcenbezeichner der Synapse-Integrations-Runtime.</span><span class="sxs-lookup"><span data-stu-id="6edca-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="6edca-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6edca-131">-WorkspaceName</span></span>
<span data-ttu-id="6edca-132">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="6edca-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6edca-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6edca-133">-WorkspaceObject</span></span>
<span data-ttu-id="6edca-134">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="6edca-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6edca-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6edca-135">CommonParameters</span></span>
<span data-ttu-id="6edca-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6edca-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6edca-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6edca-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6edca-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6edca-138">INPUTS</span></span>

### <span data-ttu-id="6edca-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6edca-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6edca-140">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6edca-140">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="6edca-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6edca-141">OUTPUTS</span></span>

### <span data-ttu-id="6edca-142">Microsoft.Azure.Commands.Synapse.Models.PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="6edca-142">Microsoft.Azure.Commands.Synapse.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="6edca-143">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="6edca-143">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="6edca-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6edca-144">NOTES</span></span>

## <span data-ttu-id="6edca-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6edca-145">RELATED LINKS</span></span>
