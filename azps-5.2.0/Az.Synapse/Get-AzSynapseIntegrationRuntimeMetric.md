---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
ms.openlocfilehash: 0b6700d11b017f00f10328afae2cc6638087f216
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297353"
---
# <span data-ttu-id="20f39-101">Get-AzSynapseIntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="20f39-101">Get-AzSynapseIntegrationRuntimeMetric</span></span>

## <span data-ttu-id="20f39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20f39-102">SYNOPSIS</span></span>
<span data-ttu-id="20f39-103">Ruft metrische Daten für eine Integrationslaufzeit ab.</span><span class="sxs-lookup"><span data-stu-id="20f39-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="20f39-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20f39-104">SYNTAX</span></span>

### <span data-ttu-id="20f39-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="20f39-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20f39-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="20f39-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20f39-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="20f39-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="20f39-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="20f39-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20f39-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="20f39-109">DESCRIPTION</span></span>
<span data-ttu-id="20f39-110">Das **Cmdlet "Get-AzSynapseIntegrationRuntimeMetric"** ruft metrische Daten zur Integrationslaufzeit in einem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="20f39-110">The **Get-AzSynapseIntegrationRuntimeMetric** cmdlet gets metric data about integration runtime in a workspace.</span></span>

## <span data-ttu-id="20f39-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="20f39-111">EXAMPLES</span></span>

### <span data-ttu-id="20f39-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="20f39-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeMetric -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="20f39-113">Dieser Befehl zeigt metrische Daten zur Integrationslaufzeit mit dem Namen "test-selfhost-ir" im Arbeitsbereich "ContosoWorkspace" an.</span><span class="sxs-lookup"><span data-stu-id="20f39-113">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="20f39-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20f39-114">PARAMETERS</span></span>

### <span data-ttu-id="20f39-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20f39-115">-DefaultProfile</span></span>
<span data-ttu-id="20f39-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="20f39-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20f39-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20f39-117">-InputObject</span></span>
<span data-ttu-id="20f39-118">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="20f39-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="20f39-119">-Name</span><span class="sxs-lookup"><span data-stu-id="20f39-119">-Name</span></span>
<span data-ttu-id="20f39-120">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="20f39-120">The integration runtime name.</span></span>

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

### <span data-ttu-id="20f39-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20f39-121">-ResourceGroupName</span></span>
<span data-ttu-id="20f39-122">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="20f39-122">Resource group name.</span></span>

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

### <span data-ttu-id="20f39-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20f39-123">-ResourceId</span></span>
<span data-ttu-id="20f39-124">Ressourcenbezeichner der Laufzeit der Synapse-Integration.</span><span class="sxs-lookup"><span data-stu-id="20f39-124">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="20f39-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="20f39-125">-WorkspaceName</span></span>
<span data-ttu-id="20f39-126">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="20f39-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="20f39-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="20f39-127">-WorkspaceObject</span></span>
<span data-ttu-id="20f39-128">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="20f39-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="20f39-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20f39-129">CommonParameters</span></span>
<span data-ttu-id="20f39-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20f39-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20f39-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20f39-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20f39-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="20f39-132">INPUTS</span></span>

### <span data-ttu-id="20f39-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="20f39-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="20f39-134">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="20f39-134">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="20f39-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="20f39-135">OUTPUTS</span></span>

### <span data-ttu-id="20f39-136">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="20f39-136">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="20f39-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="20f39-137">NOTES</span></span>

## <span data-ttu-id="20f39-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="20f39-138">RELATED LINKS</span></span>
