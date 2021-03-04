---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseintegrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
ms.openlocfilehash: 158d4a54cdbeec0dd8cf756a3c685aede97f5bed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940728"
---
# <span data-ttu-id="a5d36-101">Get-AzSynapseIntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="a5d36-101">Get-AzSynapseIntegrationRuntimeMetric</span></span>

## <span data-ttu-id="a5d36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5d36-102">SYNOPSIS</span></span>
<span data-ttu-id="a5d36-103">Ruft Metrikdaten für eine Integrationslaufzeit ab.</span><span class="sxs-lookup"><span data-stu-id="a5d36-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="a5d36-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5d36-104">SYNTAX</span></span>

### <span data-ttu-id="a5d36-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a5d36-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5d36-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5d36-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5d36-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5d36-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5d36-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5d36-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5d36-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5d36-109">DESCRIPTION</span></span>
<span data-ttu-id="a5d36-110">Das **Get-AzSynapseIntegrationRuntimeMetric-Cmdlet** ruft Metrikdaten zur Integrationslaufzeit in einem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="a5d36-110">The **Get-AzSynapseIntegrationRuntimeMetric** cmdlet gets metric data about integration runtime in a workspace.</span></span>

## <span data-ttu-id="a5d36-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a5d36-111">EXAMPLES</span></span>

### <span data-ttu-id="a5d36-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a5d36-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeMetric -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="a5d36-113">Mit diesem Befehl werden Metrikdaten zur Integrations-Runtime mit dem Namen "test-selfhost-ir" im Arbeitsbereich namens ContosoWorkspace angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a5d36-113">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="a5d36-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a5d36-114">PARAMETERS</span></span>

### <span data-ttu-id="a5d36-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5d36-115">-DefaultProfile</span></span>
<span data-ttu-id="a5d36-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a5d36-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5d36-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5d36-117">-InputObject</span></span>
<span data-ttu-id="a5d36-118">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a5d36-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="a5d36-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a5d36-119">-Name</span></span>
<span data-ttu-id="a5d36-120">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="a5d36-120">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d36-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5d36-121">-ResourceGroupName</span></span>
<span data-ttu-id="a5d36-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a5d36-122">Resource group name.</span></span>

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

### <span data-ttu-id="a5d36-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5d36-123">-ResourceId</span></span>
<span data-ttu-id="a5d36-124">Ressourcenbezeichner der Synapse-Integrations-Runtime.</span><span class="sxs-lookup"><span data-stu-id="a5d36-124">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="a5d36-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a5d36-125">-WorkspaceName</span></span>
<span data-ttu-id="a5d36-126">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="a5d36-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a5d36-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a5d36-127">-WorkspaceObject</span></span>
<span data-ttu-id="a5d36-128">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a5d36-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a5d36-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5d36-129">CommonParameters</span></span>
<span data-ttu-id="a5d36-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5d36-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5d36-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5d36-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5d36-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a5d36-132">INPUTS</span></span>

### <span data-ttu-id="a5d36-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a5d36-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a5d36-134">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a5d36-134">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="a5d36-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a5d36-135">OUTPUTS</span></span>

### <span data-ttu-id="a5d36-136">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="a5d36-136">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="a5d36-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a5d36-137">NOTES</span></span>

## <span data-ttu-id="a5d36-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a5d36-138">RELATED LINKS</span></span>
