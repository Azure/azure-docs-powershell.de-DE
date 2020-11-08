---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
ms.openlocfilehash: d07ec757fd5ab589de6234caac23992d6ff320fe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007669"
---
# <span data-ttu-id="e0f62-101">Test-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e0f62-101">Test-AzSynapseSqlPool</span></span>

## <span data-ttu-id="e0f62-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e0f62-102">SYNOPSIS</span></span>
<span data-ttu-id="e0f62-103">Überprüft, ob ein Synapse Analytics SQL-Pool vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e0f62-103">Checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e0f62-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0f62-104">SYNTAX</span></span>

### <span data-ttu-id="e0f62-105">TestByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e0f62-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0f62-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0f62-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0f62-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e0f62-107">DESCRIPTION</span></span>
<span data-ttu-id="e0f62-108">Das Cmdlet **Test-AzSynapseSqlPool** überprüft, ob ein Synapse Analytics SQL-Pool vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e0f62-108">The **Test-AzSynapseSqlPool** cmdlet checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e0f62-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e0f62-109">EXAMPLES</span></span>

### <span data-ttu-id="e0f62-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e0f62-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="e0f62-111">Dieser Befehl überprüft das vorhanden sein des angegebenen SQL-Pools.</span><span class="sxs-lookup"><span data-stu-id="e0f62-111">This command checks the existence of the specified SQL pool.</span></span>

## <span data-ttu-id="e0f62-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0f62-112">PARAMETERS</span></span>

### <span data-ttu-id="e0f62-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0f62-113">-DefaultProfile</span></span>
<span data-ttu-id="e0f62-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e0f62-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0f62-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e0f62-115">-Name</span></span>
<span data-ttu-id="e0f62-116">Name des Synapsen-SQL-Pools.</span><span class="sxs-lookup"><span data-stu-id="e0f62-116">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="e0f62-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0f62-117">-ResourceGroupName</span></span>
<span data-ttu-id="e0f62-118">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e0f62-118">Resource group name.</span></span>

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

### <span data-ttu-id="e0f62-119">-Version</span><span class="sxs-lookup"><span data-stu-id="e0f62-119">-Version</span></span>
<span data-ttu-id="e0f62-120">Version des Synapse SQL-Pools.</span><span class="sxs-lookup"><span data-stu-id="e0f62-120">Version of Synapse SQL pool.</span></span> <span data-ttu-id="e0f62-121">Beispiel: 2 oder 3.</span><span class="sxs-lookup"><span data-stu-id="e0f62-121">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="e0f62-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e0f62-122">-WorkspaceName</span></span>
<span data-ttu-id="e0f62-123">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="e0f62-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e0f62-124">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="e0f62-124">-WorkspaceObject</span></span>
<span data-ttu-id="e0f62-125">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="e0f62-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e0f62-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0f62-126">CommonParameters</span></span>
<span data-ttu-id="e0f62-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0f62-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0f62-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0f62-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0f62-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e0f62-129">INPUTS</span></span>

### <span data-ttu-id="e0f62-130">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e0f62-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e0f62-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e0f62-131">OUTPUTS</span></span>

### <span data-ttu-id="e0f62-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="e0f62-132">System.Object</span></span>
## <span data-ttu-id="e0f62-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="e0f62-133">NOTES</span></span>

## <span data-ttu-id="e0f62-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e0f62-134">RELATED LINKS</span></span>
