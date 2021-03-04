---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/test-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
ms.openlocfilehash: d932a875957f1649976966a9f2e115e93dfea351
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948232"
---
# <span data-ttu-id="108cd-101">Test-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="108cd-101">Test-AzSynapseSqlPool</span></span>

## <span data-ttu-id="108cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="108cd-102">SYNOPSIS</span></span>
<span data-ttu-id="108cd-103">Überprüft, ob ein Synapse Analytics-SQL ist.</span><span class="sxs-lookup"><span data-stu-id="108cd-103">Checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="108cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="108cd-104">SYNTAX</span></span>

### <span data-ttu-id="108cd-105">TestByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="108cd-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="108cd-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="108cd-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="108cd-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="108cd-107">DESCRIPTION</span></span>
<span data-ttu-id="108cd-108">Das **Test-AzSynapseSqlPool-Cmdlet** überprüft, ob ein Synapse Analytics-SQL ist.</span><span class="sxs-lookup"><span data-stu-id="108cd-108">The **Test-AzSynapseSqlPool** cmdlet checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="108cd-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="108cd-109">EXAMPLES</span></span>

### <span data-ttu-id="108cd-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="108cd-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="108cd-111">Mit diesem Befehl wird das Vorhandensein des angegebenen SQL überprüft.</span><span class="sxs-lookup"><span data-stu-id="108cd-111">This command checks the existence of the specified SQL pool.</span></span>

## <span data-ttu-id="108cd-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="108cd-112">PARAMETERS</span></span>

### <span data-ttu-id="108cd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="108cd-113">-DefaultProfile</span></span>
<span data-ttu-id="108cd-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="108cd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="108cd-115">-Name</span><span class="sxs-lookup"><span data-stu-id="108cd-115">-Name</span></span>
<span data-ttu-id="108cd-116">Name des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="108cd-116">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="108cd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="108cd-117">-ResourceGroupName</span></span>
<span data-ttu-id="108cd-118">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="108cd-118">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="108cd-119">-Version</span><span class="sxs-lookup"><span data-stu-id="108cd-119">-Version</span></span>
<span data-ttu-id="108cd-120">Version von Synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="108cd-120">Version of Synapse SQL pool.</span></span> <span data-ttu-id="108cd-121">Beispiel: 2 oder 3.</span><span class="sxs-lookup"><span data-stu-id="108cd-121">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="108cd-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="108cd-122">-WorkspaceName</span></span>
<span data-ttu-id="108cd-123">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="108cd-123">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="108cd-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="108cd-124">-WorkspaceObject</span></span>
<span data-ttu-id="108cd-125">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="108cd-125">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: TestByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="108cd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="108cd-126">CommonParameters</span></span>
<span data-ttu-id="108cd-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="108cd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="108cd-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="108cd-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="108cd-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="108cd-129">INPUTS</span></span>

### <span data-ttu-id="108cd-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="108cd-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="108cd-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="108cd-131">OUTPUTS</span></span>

### <span data-ttu-id="108cd-132">System.Object</span><span class="sxs-lookup"><span data-stu-id="108cd-132">System.Object</span></span>
## <span data-ttu-id="108cd-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="108cd-133">NOTES</span></span>

## <span data-ttu-id="108cd-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="108cd-134">RELATED LINKS</span></span>
