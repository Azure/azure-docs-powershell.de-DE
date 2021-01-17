---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
ms.openlocfilehash: 6304e730e6b3b0a4f8edc0f42fc024852acbfc12
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361471"
---
# <span data-ttu-id="e434c-101">Test-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="e434c-101">Test-AzSynapseSparkPool</span></span>

## <span data-ttu-id="e434c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e434c-102">SYNOPSIS</span></span>
<span data-ttu-id="e434c-103">Sucht nach dem Vorhandensein eines Synapse Analytics Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="e434c-103">Checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="e434c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e434c-104">SYNTAX</span></span>

### <span data-ttu-id="e434c-105">TestByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e434c-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e434c-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e434c-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e434c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e434c-107">DESCRIPTION</span></span>
<span data-ttu-id="e434c-108">Das **Cmdlet "Test-AzSynapseSparkPool"** sucht nach dem Vorhandensein eines Synapse Analytics Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="e434c-108">The **Test-AzSynapseSparkPool** cmdlet checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="e434c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e434c-109">EXAMPLES</span></span>

### <span data-ttu-id="e434c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e434c-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="e434c-111">Dieser Befehl überprüft das Vorhandensein des angegebenen Sparkpools.</span><span class="sxs-lookup"><span data-stu-id="e434c-111">This command checks the existence of the specified Spark pool.</span></span>

## <span data-ttu-id="e434c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e434c-112">PARAMETERS</span></span>

### <span data-ttu-id="e434c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e434c-113">-DefaultProfile</span></span>
<span data-ttu-id="e434c-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e434c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e434c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e434c-115">-Name</span></span>
<span data-ttu-id="e434c-116">Name des Synapse Spark-Pools.</span><span class="sxs-lookup"><span data-stu-id="e434c-116">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="e434c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e434c-117">-ResourceGroupName</span></span>
<span data-ttu-id="e434c-118">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="e434c-118">Resource group name.</span></span>

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

### <span data-ttu-id="e434c-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e434c-119">-WorkspaceName</span></span>
<span data-ttu-id="e434c-120">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="e434c-120">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e434c-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e434c-121">-WorkspaceObject</span></span>
<span data-ttu-id="e434c-122">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="e434c-122">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e434c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e434c-123">CommonParameters</span></span>
<span data-ttu-id="e434c-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e434c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e434c-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e434c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e434c-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e434c-126">INPUTS</span></span>

### <span data-ttu-id="e434c-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e434c-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e434c-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e434c-128">OUTPUTS</span></span>

### <span data-ttu-id="e434c-129">System.Object</span><span class="sxs-lookup"><span data-stu-id="e434c-129">System.Object</span></span>
## <span data-ttu-id="e434c-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e434c-130">NOTES</span></span>

## <span data-ttu-id="e434c-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e434c-131">RELATED LINKS</span></span>
