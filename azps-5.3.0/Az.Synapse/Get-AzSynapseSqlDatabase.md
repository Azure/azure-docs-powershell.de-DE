---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlDatabase.md
ms.openlocfilehash: c203e9c80978f50bd7879627b733de2ec0c6cf7e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383885"
---
# <span data-ttu-id="e5aa8-101">Get-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e5aa8-101">Get-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="e5aa8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5aa8-102">SYNOPSIS</span></span>
<span data-ttu-id="e5aa8-103">Ruft eine Synapse Analytics SQL ab.</span><span class="sxs-lookup"><span data-stu-id="e5aa8-103">Gets a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="e5aa8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5aa8-104">SYNTAX</span></span>

### <span data-ttu-id="e5aa8-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e5aa8-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5aa8-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5aa8-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlDatabase [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5aa8-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5aa8-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlDatabase -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5aa8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e5aa8-108">DESCRIPTION</span></span>
<span data-ttu-id="e5aa8-109">[Dieses Feature ist in einer eingeschränkten Vorschau verfügbar und kann anfänglich nur für bestimmte Abonnements verwendet werden.] Das **Cmdlet "Get-AzSynapseSqlDatabase"** ruft Informationen zu einer Azure Synapse Analytics SQL ab.</span><span class="sxs-lookup"><span data-stu-id="e5aa8-109">[This feature is in a limited preview, initially accessible only to certain subscriptions.] The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="e5aa8-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e5aa8-110">EXAMPLES</span></span>

### <span data-ttu-id="e5aa8-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e5aa8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="e5aa8-112">Dieser Befehl ruft alle SQL Datenbanken in einem Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="e5aa8-112">This command gets all SQL databases under a workspace.</span></span>

### <span data-ttu-id="e5aa8-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e5aa8-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="e5aa8-114">Dieser Befehl ruft die SQL Datenbank im Arbeitsbereich "ContosoWorkspace" mit dem Namen "ContosoSqlDatabase" ab.</span><span class="sxs-lookup"><span data-stu-id="e5aa8-114">This command gets the SQL database under workspace ContosoWorkspace with name ContosoSqlDatabase.</span></span>

### <span data-ttu-id="e5aa8-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e5aa8-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlDatabase
```

<span data-ttu-id="e5aa8-116">Dieser Befehl ruft alle SQL Datenbanken in einem Arbeitsbereich über die Pipeline ab.</span><span class="sxs-lookup"><span data-stu-id="e5aa8-116">This command gets all the SQL databases under a workspace through pipeline.</span></span>

### <span data-ttu-id="e5aa8-117">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="e5aa8-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase"
```

<span data-ttu-id="e5aa8-118">Dieser Befehl ruft die SQL Datenbank mit der angegebenen Ressourcen-ID ab.</span><span class="sxs-lookup"><span data-stu-id="e5aa8-118">This command gets the SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="e5aa8-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5aa8-119">PARAMETERS</span></span>

### <span data-ttu-id="e5aa8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5aa8-120">-DefaultProfile</span></span>
<span data-ttu-id="e5aa8-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5aa8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5aa8-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e5aa8-122">-Name</span></span>
<span data-ttu-id="e5aa8-123">Name der Datenbank von Synapse SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e5aa8-123">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="e5aa8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5aa8-124">-ResourceGroupName</span></span>
<span data-ttu-id="e5aa8-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="e5aa8-125">Resource group name.</span></span>

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

### <span data-ttu-id="e5aa8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5aa8-126">-ResourceId</span></span>
<span data-ttu-id="e5aa8-127">Ressourcenbezeichner von Synapse SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e5aa8-127">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="e5aa8-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e5aa8-128">-WorkspaceName</span></span>
<span data-ttu-id="e5aa8-129">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="e5aa8-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e5aa8-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e5aa8-130">-WorkspaceObject</span></span>
<span data-ttu-id="e5aa8-131">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="e5aa8-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e5aa8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5aa8-132">CommonParameters</span></span>
<span data-ttu-id="e5aa8-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5aa8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5aa8-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5aa8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5aa8-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e5aa8-135">INPUTS</span></span>

### <span data-ttu-id="e5aa8-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e5aa8-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e5aa8-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e5aa8-137">OUTPUTS</span></span>

### <span data-ttu-id="e5aa8-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e5aa8-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="e5aa8-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e5aa8-139">NOTES</span></span>

## <span data-ttu-id="e5aa8-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e5aa8-140">RELATED LINKS</span></span>
