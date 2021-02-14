---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 08ce91d6d9a942dd20078e0c3b5b537360aac9fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150033"
---
# <span data-ttu-id="a46c4-101">Get-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="a46c4-101">Get-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="a46c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a46c4-102">SYNOPSIS</span></span>
<span data-ttu-id="a46c4-103">Ruft Schlüssel für eine selbst gehostete Integrationslaufzeit ab.</span><span class="sxs-lookup"><span data-stu-id="a46c4-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="a46c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a46c4-104">SYNTAX</span></span>

### <span data-ttu-id="a46c4-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a46c4-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a46c4-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a46c4-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a46c4-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a46c4-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a46c4-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a46c4-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a46c4-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a46c4-109">DESCRIPTION</span></span>
<span data-ttu-id="a46c4-110">Das **Cmdlet "Get-AzSynapseIntegrationRuntimeKey"** ruft Schlüssel für eine Integrationslaufzeit ab.</span><span class="sxs-lookup"><span data-stu-id="a46c4-110">The **Get-AzSynapseIntegrationRuntimeKey** cmdlet gets keys for an integration runtime.</span></span> <span data-ttu-id="a46c4-111">Die Schlüssel werden zum Registrieren eines Integrationslaufzeitknotens verwendet.</span><span class="sxs-lookup"><span data-stu-id="a46c4-111">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="a46c4-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a46c4-112">EXAMPLES</span></span>

### <span data-ttu-id="a46c4-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a46c4-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="a46c4-114">Das Cmdlet ruft Schlüssel für eine Integrationslaufzeit mit dem Namen "test-selfhost-ir" ab.</span><span class="sxs-lookup"><span data-stu-id="a46c4-114">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="a46c4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a46c4-115">PARAMETERS</span></span>

### <span data-ttu-id="a46c4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a46c4-116">-DefaultProfile</span></span>
<span data-ttu-id="a46c4-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a46c4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a46c4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a46c4-118">-InputObject</span></span>
<span data-ttu-id="a46c4-119">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a46c4-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="a46c4-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a46c4-120">-Name</span></span>
<span data-ttu-id="a46c4-121">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="a46c4-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="a46c4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a46c4-122">-ResourceGroupName</span></span>
<span data-ttu-id="a46c4-123">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="a46c4-123">Resource group name.</span></span>

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

### <span data-ttu-id="a46c4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a46c4-124">-ResourceId</span></span>
<span data-ttu-id="a46c4-125">Ressourcenbezeichner der Laufzeit der Synapse-Integration.</span><span class="sxs-lookup"><span data-stu-id="a46c4-125">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="a46c4-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a46c4-126">-WorkspaceName</span></span>
<span data-ttu-id="a46c4-127">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="a46c4-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a46c4-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a46c4-128">-WorkspaceObject</span></span>
<span data-ttu-id="a46c4-129">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a46c4-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a46c4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a46c4-130">CommonParameters</span></span>
<span data-ttu-id="a46c4-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a46c4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a46c4-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a46c4-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a46c4-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a46c4-133">INPUTS</span></span>

### <span data-ttu-id="a46c4-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a46c4-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a46c4-135">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a46c4-135">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="a46c4-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a46c4-136">OUTPUTS</span></span>

### <span data-ttu-id="a46c4-137">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="a46c4-137">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="a46c4-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a46c4-138">NOTES</span></span>

## <span data-ttu-id="a46c4-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a46c4-139">RELATED LINKS</span></span>
