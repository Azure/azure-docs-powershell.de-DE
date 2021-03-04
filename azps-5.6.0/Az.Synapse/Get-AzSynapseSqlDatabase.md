---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlDatabase.md
ms.openlocfilehash: 56674f2696e5d7cebdaa9f84072f890c69535223
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950459"
---
# <span data-ttu-id="27c4c-101">Get-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="27c4c-101">Get-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="27c4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27c4c-102">SYNOPSIS</span></span>
<span data-ttu-id="27c4c-103">Ruft eine Synapse Analytics-SQL ab.</span><span class="sxs-lookup"><span data-stu-id="27c4c-103">Gets a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="27c4c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27c4c-104">SYNTAX</span></span>

### <span data-ttu-id="27c4c-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="27c4c-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27c4c-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27c4c-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlDatabase [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27c4c-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="27c4c-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlDatabase -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27c4c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27c4c-108">DESCRIPTION</span></span>
<span data-ttu-id="27c4c-109">[Dieses Feature befindet sich in einer eingeschränkten Vorschau und kann zunächst nur für bestimmte Abonnements verwendet werden.] Das **Get-AzSynapseSqlDatabase-Cmdlet** ruft Informationen zu einer Azure Synapse Analytics-SQL ab.</span><span class="sxs-lookup"><span data-stu-id="27c4c-109">[This feature is in a limited preview, initially accessible only to certain subscriptions.] The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="27c4c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="27c4c-110">EXAMPLES</span></span>

### <span data-ttu-id="27c4c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="27c4c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="27c4c-112">Dieser Befehl ruft alle SQL datenbanken unter einem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="27c4c-112">This command gets all SQL databases under a workspace.</span></span>

### <span data-ttu-id="27c4c-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="27c4c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="27c4c-114">Mit diesem Befehl wird die SQL unter dem Arbeitsbereich ContosoWorkspace mit dem Namen ContosoSqlDatabase ab.</span><span class="sxs-lookup"><span data-stu-id="27c4c-114">This command gets the SQL database under workspace ContosoWorkspace with name ContosoSqlDatabase.</span></span>

### <span data-ttu-id="27c4c-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="27c4c-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlDatabase
```

<span data-ttu-id="27c4c-116">Dieser Befehl ruft alle SQL datenbanken unter einem Arbeitsbereich über die Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="27c4c-116">This command gets all the SQL databases under a workspace through pipeline.</span></span>

### <span data-ttu-id="27c4c-117">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="27c4c-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase"
```

<span data-ttu-id="27c4c-118">Dieser Befehl ruft die SQL mit der angegebenen Ressourcen-ID ab.</span><span class="sxs-lookup"><span data-stu-id="27c4c-118">This command gets the SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="27c4c-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="27c4c-119">PARAMETERS</span></span>

### <span data-ttu-id="27c4c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27c4c-120">-DefaultProfile</span></span>
<span data-ttu-id="27c4c-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="27c4c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27c4c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="27c4c-122">-Name</span></span>
<span data-ttu-id="27c4c-123">Name von Synapse SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="27c4c-123">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27c4c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27c4c-124">-ResourceGroupName</span></span>
<span data-ttu-id="27c4c-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="27c4c-125">Resource group name.</span></span>

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

### <span data-ttu-id="27c4c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27c4c-126">-ResourceId</span></span>
<span data-ttu-id="27c4c-127">Ressourcenbezeichner von Synapse SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="27c4c-127">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="27c4c-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="27c4c-128">-WorkspaceName</span></span>
<span data-ttu-id="27c4c-129">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="27c4c-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="27c4c-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="27c4c-130">-WorkspaceObject</span></span>
<span data-ttu-id="27c4c-131">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="27c4c-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="27c4c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27c4c-132">CommonParameters</span></span>
<span data-ttu-id="27c4c-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27c4c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27c4c-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27c4c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27c4c-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="27c4c-135">INPUTS</span></span>

### <span data-ttu-id="27c4c-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="27c4c-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="27c4c-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="27c4c-137">OUTPUTS</span></span>

### <span data-ttu-id="27c4c-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="27c4c-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="27c4c-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="27c4c-139">NOTES</span></span>

## <span data-ttu-id="27c4c-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="27c4c-140">RELATED LINKS</span></span>
