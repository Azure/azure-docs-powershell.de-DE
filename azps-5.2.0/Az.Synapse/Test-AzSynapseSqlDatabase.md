---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
ms.openlocfilehash: e97c10359d00fefa30c783e67c7a3bc64c16a214
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306427"
---
# <span data-ttu-id="b323d-101">Test-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b323d-101">Test-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="b323d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b323d-102">SYNOPSIS</span></span>
<span data-ttu-id="b323d-103">Sucht nach dem Vorhandensein einer Synapse Analytics SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b323d-103">Checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="b323d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b323d-104">SYNTAX</span></span>

### <span data-ttu-id="b323d-105">TestByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b323d-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b323d-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b323d-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b323d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b323d-107">DESCRIPTION</span></span>
<span data-ttu-id="b323d-108">Das **Cmdlet "Test-AzSynapseSqlDatabase"** sucht nach dem Vorhandensein einer Synapse Analytics SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b323d-108">The **Test-AzSynapseSqlDatabase** cmdlet checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="b323d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b323d-109">EXAMPLES</span></span>

### <span data-ttu-id="b323d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b323d-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="b323d-111">Dieser Befehl überprüft das Vorhandensein der angegebenen SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b323d-111">This command checks the existence of the specified SQL database.</span></span>

## <span data-ttu-id="b323d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b323d-112">PARAMETERS</span></span>

### <span data-ttu-id="b323d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b323d-113">-DefaultProfile</span></span>
<span data-ttu-id="b323d-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b323d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b323d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b323d-115">-Name</span></span>
<span data-ttu-id="b323d-116">Name der Datenbank von Synapse SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b323d-116">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="b323d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b323d-117">-ResourceGroupName</span></span>
<span data-ttu-id="b323d-118">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="b323d-118">Resource group name.</span></span>

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

### <span data-ttu-id="b323d-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b323d-119">-WorkspaceName</span></span>
<span data-ttu-id="b323d-120">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="b323d-120">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b323d-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b323d-121">-WorkspaceObject</span></span>
<span data-ttu-id="b323d-122">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="b323d-122">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b323d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b323d-123">CommonParameters</span></span>
<span data-ttu-id="b323d-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b323d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b323d-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b323d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b323d-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b323d-126">INPUTS</span></span>

### <span data-ttu-id="b323d-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b323d-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b323d-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b323d-128">OUTPUTS</span></span>

### <span data-ttu-id="b323d-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b323d-129">System.Boolean</span></span>

## <span data-ttu-id="b323d-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b323d-130">NOTES</span></span>

## <span data-ttu-id="b323d-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b323d-131">RELATED LINKS</span></span>
