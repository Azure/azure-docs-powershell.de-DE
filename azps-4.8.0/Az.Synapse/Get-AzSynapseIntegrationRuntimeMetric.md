---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
ms.openlocfilehash: 0b6700d11b017f00f10328afae2cc6638087f216
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173372"
---
# <span data-ttu-id="3ff3b-101">Get-AzSynapseIntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="3ff3b-101">Get-AzSynapseIntegrationRuntimeMetric</span></span>

## <span data-ttu-id="3ff3b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3ff3b-102">SYNOPSIS</span></span>
<span data-ttu-id="3ff3b-103">Ruft metrische Daten für eine Integrationslaufzeit ab.</span><span class="sxs-lookup"><span data-stu-id="3ff3b-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="3ff3b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ff3b-104">SYNTAX</span></span>

### <span data-ttu-id="3ff3b-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3ff3b-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ff3b-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ff3b-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ff3b-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ff3b-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3ff3b-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ff3b-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ff3b-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3ff3b-109">DESCRIPTION</span></span>
<span data-ttu-id="3ff3b-110">Das Cmdlet " **Get-AzSynapseIntegrationRuntimeMetric** " ruft metrische Daten zur Integrationslaufzeit in einem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="3ff3b-110">The **Get-AzSynapseIntegrationRuntimeMetric** cmdlet gets metric data about integration runtime in a workspace.</span></span>

## <span data-ttu-id="3ff3b-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3ff3b-111">EXAMPLES</span></span>

### <span data-ttu-id="3ff3b-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3ff3b-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeMetric -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="3ff3b-113">Dieser Befehl zeigt metrische Daten zur Integrationslaufzeit mit dem Namen "Test-SelfHost-IR" im Arbeitsbereich mit dem Namen ContosoWorkspace an.</span><span class="sxs-lookup"><span data-stu-id="3ff3b-113">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="3ff3b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ff3b-114">PARAMETERS</span></span>

### <span data-ttu-id="3ff3b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ff3b-115">-DefaultProfile</span></span>
<span data-ttu-id="3ff3b-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3ff3b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ff3b-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3ff3b-117">-InputObject</span></span>
<span data-ttu-id="3ff3b-118">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="3ff3b-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="3ff3b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3ff3b-119">-Name</span></span>
<span data-ttu-id="3ff3b-120">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="3ff3b-120">The integration runtime name.</span></span>

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

### <span data-ttu-id="3ff3b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ff3b-121">-ResourceGroupName</span></span>
<span data-ttu-id="3ff3b-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3ff3b-122">Resource group name.</span></span>

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

### <span data-ttu-id="3ff3b-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3ff3b-123">-ResourceId</span></span>
<span data-ttu-id="3ff3b-124">Ressourcenbezeichner der Synapse-Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="3ff3b-124">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="3ff3b-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3ff3b-125">-WorkspaceName</span></span>
<span data-ttu-id="3ff3b-126">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="3ff3b-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3ff3b-127">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="3ff3b-127">-WorkspaceObject</span></span>
<span data-ttu-id="3ff3b-128">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="3ff3b-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3ff3b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ff3b-129">CommonParameters</span></span>
<span data-ttu-id="3ff3b-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ff3b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ff3b-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ff3b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ff3b-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3ff3b-132">INPUTS</span></span>

### <span data-ttu-id="3ff3b-133">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3ff3b-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="3ff3b-134">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3ff3b-134">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="3ff3b-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3ff3b-135">OUTPUTS</span></span>

### <span data-ttu-id="3ff3b-136">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="3ff3b-136">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="3ff3b-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="3ff3b-137">NOTES</span></span>

## <span data-ttu-id="3ff3b-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3ff3b-138">RELATED LINKS</span></span>
