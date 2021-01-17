---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
ms.openlocfilehash: 0b6700d11b017f00f10328afae2cc6638087f216
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460019"
---
# <span data-ttu-id="befb5-101">Get-AzSynapseIntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="befb5-101">Get-AzSynapseIntegrationRuntimeMetric</span></span>

## <span data-ttu-id="befb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="befb5-102">SYNOPSIS</span></span>
<span data-ttu-id="befb5-103">Ruft metrische Daten für eine Integrationslaufzeit ab.</span><span class="sxs-lookup"><span data-stu-id="befb5-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="befb5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="befb5-104">SYNTAX</span></span>

### <span data-ttu-id="befb5-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="befb5-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="befb5-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="befb5-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="befb5-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="befb5-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="befb5-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="befb5-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="befb5-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="befb5-109">DESCRIPTION</span></span>
<span data-ttu-id="befb5-110">Das **Cmdlet "Get-AzSynapseIntegrationRuntimeMetric"** ruft metrische Daten zur Integrationslaufzeit in einem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="befb5-110">The **Get-AzSynapseIntegrationRuntimeMetric** cmdlet gets metric data about integration runtime in a workspace.</span></span>

## <span data-ttu-id="befb5-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="befb5-111">EXAMPLES</span></span>

### <span data-ttu-id="befb5-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="befb5-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeMetric -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="befb5-113">Dieser Befehl zeigt metrische Daten zur Integrationslaufzeit mit dem Namen "test-selfhost-ir" im Arbeitsbereich "ContosoWorkspace" an.</span><span class="sxs-lookup"><span data-stu-id="befb5-113">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="befb5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="befb5-114">PARAMETERS</span></span>

### <span data-ttu-id="befb5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="befb5-115">-DefaultProfile</span></span>
<span data-ttu-id="befb5-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="befb5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="befb5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="befb5-117">-InputObject</span></span>
<span data-ttu-id="befb5-118">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="befb5-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="befb5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="befb5-119">-Name</span></span>
<span data-ttu-id="befb5-120">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="befb5-120">The integration runtime name.</span></span>

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

### <span data-ttu-id="befb5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="befb5-121">-ResourceGroupName</span></span>
<span data-ttu-id="befb5-122">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="befb5-122">Resource group name.</span></span>

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

### <span data-ttu-id="befb5-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="befb5-123">-ResourceId</span></span>
<span data-ttu-id="befb5-124">Ressourcenbezeichner der Synapse-Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="befb5-124">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="befb5-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="befb5-125">-WorkspaceName</span></span>
<span data-ttu-id="befb5-126">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="befb5-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="befb5-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="befb5-127">-WorkspaceObject</span></span>
<span data-ttu-id="befb5-128">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="befb5-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="befb5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="befb5-129">CommonParameters</span></span>
<span data-ttu-id="befb5-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="befb5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="befb5-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="befb5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="befb5-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="befb5-132">INPUTS</span></span>

### <span data-ttu-id="befb5-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="befb5-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="befb5-134">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="befb5-134">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="befb5-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="befb5-135">OUTPUTS</span></span>

### <span data-ttu-id="befb5-136">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="befb5-136">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="befb5-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="befb5-137">NOTES</span></span>

## <span data-ttu-id="befb5-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="befb5-138">RELATED LINKS</span></span>
