---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqladvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedDataSecurityPolicy.md
ms.openlocfilehash: b0d21c8d59d2a33671fead2e88d402779f99fb7f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383940"
---
# <span data-ttu-id="eabee-101">Get-AzSynapseSqlAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="eabee-101">Get-AzSynapseSqlAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="eabee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eabee-102">SYNOPSIS</span></span>
<span data-ttu-id="eabee-103">Ruft die Erweiterte Datensicherheitsrichtlinie eines Arbeitsbereichs ab.</span><span class="sxs-lookup"><span data-stu-id="eabee-103">Gets Advanced Data Security policy of a workspace.</span></span>

## <span data-ttu-id="eabee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eabee-104">SYNTAX</span></span>

### <span data-ttu-id="eabee-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="eabee-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eabee-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eabee-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eabee-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eabee-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eabee-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eabee-108">DESCRIPTION</span></span>
<span data-ttu-id="eabee-109">Das **Cmdlet "Get-AzSynapseSqlAdvancedDataSecurityPolicy"** ruft die Erweiterte Datensicherheitsrichtlinie eines Arbeitsbereichs ab.</span><span class="sxs-lookup"><span data-stu-id="eabee-109">The **Get-AzSynapseSqlAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a workspace.</span></span>

## <span data-ttu-id="eabee-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="eabee-110">EXAMPLES</span></span>

### <span data-ttu-id="eabee-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="eabee-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedDataSecurityPolicy -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="eabee-112">Dieser Befehl ruft "Advanced Data Security" für den Arbeitsbereich "ContosoWorkspace" ab.</span><span class="sxs-lookup"><span data-stu-id="eabee-112">This command gets Advanced Data Security on the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="eabee-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="eabee-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAdvancedDataSecurityPolicy
```

<span data-ttu-id="eabee-114">Dieser Befehl ruft "Advanced Data Security" für den Arbeitsbereich mit dem Namen "ContosoWorkspace" über die Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="eabee-114">This command gets Advanced Data Security on the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="eabee-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eabee-115">PARAMETERS</span></span>

### <span data-ttu-id="eabee-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eabee-116">-DefaultProfile</span></span>
<span data-ttu-id="eabee-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eabee-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eabee-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eabee-118">-InputObject</span></span>
<span data-ttu-id="eabee-119">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="eabee-119">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eabee-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eabee-120">-ResourceGroupName</span></span>
<span data-ttu-id="eabee-121">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="eabee-121">Resource group name.</span></span>

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

### <span data-ttu-id="eabee-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eabee-122">-ResourceId</span></span>
<span data-ttu-id="eabee-123">Ressourcenbezeichner des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="eabee-123">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="eabee-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="eabee-124">-WorkspaceName</span></span>
<span data-ttu-id="eabee-125">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="eabee-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="eabee-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eabee-126">CommonParameters</span></span>
<span data-ttu-id="eabee-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eabee-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eabee-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eabee-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eabee-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="eabee-129">INPUTS</span></span>

### <span data-ttu-id="eabee-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="eabee-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="eabee-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="eabee-131">OUTPUTS</span></span>

### <span data-ttu-id="eabee-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="eabee-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="eabee-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="eabee-133">NOTES</span></span>

## <span data-ttu-id="eabee-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="eabee-134">RELATED LINKS</span></span>
