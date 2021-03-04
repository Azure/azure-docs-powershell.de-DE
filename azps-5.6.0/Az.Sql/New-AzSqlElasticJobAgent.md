---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/new-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
ms.openlocfilehash: ca23ba63e2f92fa14c97957a2b21b38d91e453ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933624"
---
# <span data-ttu-id="f92de-101">New-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="f92de-101">New-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="f92de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f92de-102">SYNOPSIS</span></span>
<span data-ttu-id="f92de-103">Erstellt einen neuen flexiblen Job-Agent</span><span class="sxs-lookup"><span data-stu-id="f92de-103">Creates a new elastic job agent</span></span>

## <span data-ttu-id="f92de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f92de-104">SYNTAX</span></span>

### <span data-ttu-id="f92de-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f92de-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-Name] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f92de-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="f92de-106">ObjectSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseObject] <AzureSqlDatabaseModel> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f92de-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f92de-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseResourceId] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f92de-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f92de-108">DESCRIPTION</span></span>
<span data-ttu-id="f92de-109">Das New-AzSqlElasticJobAgent cmdlet erstellt einen neuen "Flexiblen Auftrag"-Agent.</span><span class="sxs-lookup"><span data-stu-id="f92de-109">The New-AzSqlElasticJobAgent cmdlet creates a new Elastic Job agent</span></span>

## <span data-ttu-id="f92de-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f92de-110">EXAMPLES</span></span>

### <span data-ttu-id="f92de-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f92de-111">Example 1</span></span>
```
PS C:\> New-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -DatabaseName jobdb -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="f92de-112">Erstellt einen neuen Mitarbeiter für einen flexiblen Auftrag</span><span class="sxs-lookup"><span data-stu-id="f92de-112">Creates a new Elastic Job agent</span></span>

## <span data-ttu-id="f92de-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f92de-113">PARAMETERS</span></span>

### <span data-ttu-id="f92de-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f92de-114">-DatabaseName</span></span>
<span data-ttu-id="f92de-115">Der Datenbankname</span><span class="sxs-lookup"><span data-stu-id="f92de-115">The database name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f92de-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="f92de-116">-DatabaseObject</span></span>
<span data-ttu-id="f92de-117">Das Datenbankobjekt "Agentsteuerelement"</span><span class="sxs-lookup"><span data-stu-id="f92de-117">The Agent Control Database Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f92de-118">-DatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="f92de-118">-DatabaseResourceId</span></span>
<span data-ttu-id="f92de-119">Die Ressourcen-ID der Agentsteuerelementdatenbank</span><span class="sxs-lookup"><span data-stu-id="f92de-119">The Agent Control Database Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f92de-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f92de-120">-DefaultProfile</span></span>
<span data-ttu-id="f92de-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f92de-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f92de-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f92de-122">-Name</span></span>
<span data-ttu-id="f92de-123">Der Agentname</span><span class="sxs-lookup"><span data-stu-id="f92de-123">The Agent Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AgentName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f92de-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f92de-124">-ResourceGroupName</span></span>
<span data-ttu-id="f92de-125">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f92de-125">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f92de-126">-Servername</span><span class="sxs-lookup"><span data-stu-id="f92de-126">-ServerName</span></span>
<span data-ttu-id="f92de-127">Der Servername</span><span class="sxs-lookup"><span data-stu-id="f92de-127">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f92de-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="f92de-128">-Tag</span></span>
<span data-ttu-id="f92de-129">Die Agenttags</span><span class="sxs-lookup"><span data-stu-id="f92de-129">The Agent Tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f92de-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f92de-130">-Confirm</span></span>
<span data-ttu-id="f92de-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f92de-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f92de-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f92de-132">-WhatIf</span></span>
<span data-ttu-id="f92de-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f92de-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f92de-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f92de-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f92de-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f92de-135">CommonParameters</span></span>
<span data-ttu-id="f92de-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f92de-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f92de-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f92de-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f92de-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f92de-138">INPUTS</span></span>

### <span data-ttu-id="f92de-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="f92de-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="f92de-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f92de-140">OUTPUTS</span></span>

### <span data-ttu-id="f92de-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="f92de-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="f92de-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f92de-142">NOTES</span></span>

## <span data-ttu-id="f92de-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f92de-143">RELATED LINKS</span></span>
