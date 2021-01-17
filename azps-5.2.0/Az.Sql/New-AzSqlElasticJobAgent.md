---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
ms.openlocfilehash: f00c2e9cb7b9d0d35efdf99a6f81f24488dd8387
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290668"
---
# <span data-ttu-id="bb7a9-101">New-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="bb7a9-101">New-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="bb7a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb7a9-102">SYNOPSIS</span></span>
<span data-ttu-id="bb7a9-103">Erstellt einen neuen Jobcentermitarbeiter</span><span class="sxs-lookup"><span data-stu-id="bb7a9-103">Creates a new elastic job agent</span></span>

## <span data-ttu-id="bb7a9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb7a9-104">SYNTAX</span></span>

### <span data-ttu-id="bb7a9-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bb7a9-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-Name] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb7a9-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="bb7a9-106">ObjectSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseObject] <AzureSqlDatabaseModel> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb7a9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="bb7a9-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseResourceId] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb7a9-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb7a9-108">DESCRIPTION</span></span>
<span data-ttu-id="bb7a9-109">Das cmdlet New-AzSqlElasticJobAgent A0 erstellt einen neuen Agent für Einen Job.</span><span class="sxs-lookup"><span data-stu-id="bb7a9-109">The New-AzSqlElasticJobAgent cmdlet creates a new Elastic Job agent</span></span>

## <span data-ttu-id="bb7a9-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bb7a9-110">EXAMPLES</span></span>

### <span data-ttu-id="bb7a9-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bb7a9-111">Example 1</span></span>
```
PS C:\> New-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -DatabaseName jobdb -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="bb7a9-112">Erstellt einen neuen Mitarbeiter für Jobsuchen</span><span class="sxs-lookup"><span data-stu-id="bb7a9-112">Creates a new Elastic Job agent</span></span>

## <span data-ttu-id="bb7a9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb7a9-113">PARAMETERS</span></span>

### <span data-ttu-id="bb7a9-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bb7a9-114">-DatabaseName</span></span>
<span data-ttu-id="bb7a9-115">Der Datenbankname</span><span class="sxs-lookup"><span data-stu-id="bb7a9-115">The database name</span></span>

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

### <span data-ttu-id="bb7a9-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="bb7a9-116">-DatabaseObject</span></span>
<span data-ttu-id="bb7a9-117">Das Datenbankobjekt des Agentsteuerelements</span><span class="sxs-lookup"><span data-stu-id="bb7a9-117">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="bb7a9-118">-DatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="bb7a9-118">-DatabaseResourceId</span></span>
<span data-ttu-id="bb7a9-119">Die Ressourcen-ID der Agentsteuerung</span><span class="sxs-lookup"><span data-stu-id="bb7a9-119">The Agent Control Database Resource Id</span></span>

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

### <span data-ttu-id="bb7a9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb7a9-120">-DefaultProfile</span></span>
<span data-ttu-id="bb7a9-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bb7a9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb7a9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="bb7a9-122">-Name</span></span>
<span data-ttu-id="bb7a9-123">Der Agentname</span><span class="sxs-lookup"><span data-stu-id="bb7a9-123">The Agent Name</span></span>

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

### <span data-ttu-id="bb7a9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb7a9-124">-ResourceGroupName</span></span>
<span data-ttu-id="bb7a9-125">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="bb7a9-125">The resource group name</span></span>

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

### <span data-ttu-id="bb7a9-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bb7a9-126">-ServerName</span></span>
<span data-ttu-id="bb7a9-127">Der Servername</span><span class="sxs-lookup"><span data-stu-id="bb7a9-127">The server name</span></span>

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

### <span data-ttu-id="bb7a9-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="bb7a9-128">-Tag</span></span>
<span data-ttu-id="bb7a9-129">Die Agenttags</span><span class="sxs-lookup"><span data-stu-id="bb7a9-129">The Agent Tags</span></span>

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

### <span data-ttu-id="bb7a9-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb7a9-130">-Confirm</span></span>
<span data-ttu-id="bb7a9-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bb7a9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb7a9-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="bb7a9-132">-WhatIf</span></span>
<span data-ttu-id="bb7a9-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bb7a9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb7a9-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bb7a9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb7a9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb7a9-135">CommonParameters</span></span>
<span data-ttu-id="bb7a9-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb7a9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb7a9-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb7a9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb7a9-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bb7a9-138">INPUTS</span></span>

### <span data-ttu-id="bb7a9-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="bb7a9-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="bb7a9-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bb7a9-140">OUTPUTS</span></span>

### <span data-ttu-id="bb7a9-141">Microsoft.Azure.Commands.Sql.AgentJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="bb7a9-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="bb7a9-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bb7a9-142">NOTES</span></span>

## <span data-ttu-id="bb7a9-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bb7a9-143">RELATED LINKS</span></span>
