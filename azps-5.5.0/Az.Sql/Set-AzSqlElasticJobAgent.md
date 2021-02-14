---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
ms.openlocfilehash: 58adbb3b160272007899dc8740e211b6e81a10a4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163204"
---
# <span data-ttu-id="62fd0-101">Set-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="62fd0-101">Set-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="62fd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62fd0-102">SYNOPSIS</span></span>
<span data-ttu-id="62fd0-103">Aktualisiert einen Jobsuchenmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="62fd0-103">Updates an elastic job agent</span></span>

## <span data-ttu-id="62fd0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="62fd0-104">SYNTAX</span></span>

### <span data-ttu-id="62fd0-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="62fd0-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62fd0-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="62fd0-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62fd0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="62fd0-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62fd0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="62fd0-108">DESCRIPTION</span></span>
<span data-ttu-id="62fd0-109">Das cmdlet Set-AzSqlElasticJobAgent aktualisiert die Agents eines Jobcenters im Auftrag von "Job".</span><span class="sxs-lookup"><span data-stu-id="62fd0-109">The Set-AzSqlElasticJobAgent cmdlet updates an Elastic Job agents</span></span>

## <span data-ttu-id="62fd0-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="62fd0-110">EXAMPLES</span></span>

### <span data-ttu-id="62fd0-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="62fd0-111">Example 1</span></span>
```
PS C:\> Set-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent -Tag @{ Octopus = "Agent" }

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="62fd0-112">Aktualisiert einen Mitarbeiter für Jobsuchen</span><span class="sxs-lookup"><span data-stu-id="62fd0-112">Updates an Elastic Job agent</span></span>

## <span data-ttu-id="62fd0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62fd0-113">PARAMETERS</span></span>

### <span data-ttu-id="62fd0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62fd0-114">-DefaultProfile</span></span>
<span data-ttu-id="62fd0-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="62fd0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62fd0-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62fd0-116">-InputObject</span></span>
<span data-ttu-id="62fd0-117">Das Agenteingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="62fd0-117">The agent input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62fd0-118">-Name</span><span class="sxs-lookup"><span data-stu-id="62fd0-118">-Name</span></span>
<span data-ttu-id="62fd0-119">Der Agentname</span><span class="sxs-lookup"><span data-stu-id="62fd0-119">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: AgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62fd0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62fd0-120">-ResourceGroupName</span></span>
<span data-ttu-id="62fd0-121">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="62fd0-121">The resource group name</span></span>

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

### <span data-ttu-id="62fd0-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62fd0-122">-ResourceId</span></span>
<span data-ttu-id="62fd0-123">Die Agentressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="62fd0-123">The agent resource id</span></span>

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

### <span data-ttu-id="62fd0-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="62fd0-124">-ServerName</span></span>
<span data-ttu-id="62fd0-125">Der Servername</span><span class="sxs-lookup"><span data-stu-id="62fd0-125">The server name</span></span>

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

### <span data-ttu-id="62fd0-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="62fd0-126">-Tag</span></span>
<span data-ttu-id="62fd0-127">Die Tags, die dem Azure SQL-Datenbank-Agent zugeordnet werden sollen</span><span class="sxs-lookup"><span data-stu-id="62fd0-127">The tags to associate with the Azure SQL Database Agent</span></span>

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

### <span data-ttu-id="62fd0-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62fd0-128">-Confirm</span></span>
<span data-ttu-id="62fd0-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="62fd0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62fd0-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="62fd0-130">-WhatIf</span></span>
<span data-ttu-id="62fd0-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="62fd0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62fd0-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="62fd0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62fd0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62fd0-133">CommonParameters</span></span>
<span data-ttu-id="62fd0-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62fd0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62fd0-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62fd0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62fd0-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="62fd0-136">INPUTS</span></span>

### <span data-ttu-id="62fd0-137">Microsoft.Azure.Commands.Sql.AgentJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="62fd0-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="62fd0-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="62fd0-138">OUTPUTS</span></span>

### <span data-ttu-id="62fd0-139">Microsoft.Azure.Commands.Sql.AgentJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="62fd0-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="62fd0-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="62fd0-140">NOTES</span></span>

## <span data-ttu-id="62fd0-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="62fd0-141">RELATED LINKS</span></span>
