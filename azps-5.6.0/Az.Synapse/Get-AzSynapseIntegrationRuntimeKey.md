---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: d00e4c137e3b46e7721534264c9273cde5a9ad3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928432"
---
# <span data-ttu-id="49b00-101">Get-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="49b00-101">Get-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="49b00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49b00-102">SYNOPSIS</span></span>
<span data-ttu-id="49b00-103">Ruft Schlüssel für eine selbst gehostete Integrationslaufzeit ab.</span><span class="sxs-lookup"><span data-stu-id="49b00-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="49b00-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="49b00-104">SYNTAX</span></span>

### <span data-ttu-id="49b00-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="49b00-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49b00-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49b00-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49b00-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="49b00-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="49b00-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49b00-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49b00-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="49b00-109">DESCRIPTION</span></span>
<span data-ttu-id="49b00-110">Das **Get-AzSynapseIntegrationRuntimeKey-Cmdlet** ruft Schlüssel für eine Integrationslaufzeit ab.</span><span class="sxs-lookup"><span data-stu-id="49b00-110">The **Get-AzSynapseIntegrationRuntimeKey** cmdlet gets keys for an integration runtime.</span></span> <span data-ttu-id="49b00-111">Die Schlüssel werden zum Registrieren eines Integrations-Runtime-Knotens verwendet.</span><span class="sxs-lookup"><span data-stu-id="49b00-111">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="49b00-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="49b00-112">EXAMPLES</span></span>

### <span data-ttu-id="49b00-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="49b00-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="49b00-114">Das Cmdlet ruft Schlüssel für eine Integrationslaufzeit namens "test-selfhost-ir" ab.</span><span class="sxs-lookup"><span data-stu-id="49b00-114">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="49b00-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="49b00-115">PARAMETERS</span></span>

### <span data-ttu-id="49b00-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49b00-116">-DefaultProfile</span></span>
<span data-ttu-id="49b00-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="49b00-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49b00-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49b00-118">-InputObject</span></span>
<span data-ttu-id="49b00-119">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="49b00-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="49b00-120">-Name</span><span class="sxs-lookup"><span data-stu-id="49b00-120">-Name</span></span>
<span data-ttu-id="49b00-121">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="49b00-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="49b00-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49b00-122">-ResourceGroupName</span></span>
<span data-ttu-id="49b00-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="49b00-123">Resource group name.</span></span>

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

### <span data-ttu-id="49b00-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49b00-124">-ResourceId</span></span>
<span data-ttu-id="49b00-125">Ressourcenbezeichner der Synapse-Integrations-Runtime.</span><span class="sxs-lookup"><span data-stu-id="49b00-125">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="49b00-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="49b00-126">-WorkspaceName</span></span>
<span data-ttu-id="49b00-127">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="49b00-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="49b00-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="49b00-128">-WorkspaceObject</span></span>
<span data-ttu-id="49b00-129">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="49b00-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="49b00-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49b00-130">CommonParameters</span></span>
<span data-ttu-id="49b00-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49b00-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49b00-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49b00-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49b00-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="49b00-133">INPUTS</span></span>

### <span data-ttu-id="49b00-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="49b00-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="49b00-135">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="49b00-135">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="49b00-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="49b00-136">OUTPUTS</span></span>

### <span data-ttu-id="49b00-137">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="49b00-137">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="49b00-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="49b00-138">NOTES</span></span>

## <span data-ttu-id="49b00-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="49b00-139">RELATED LINKS</span></span>
