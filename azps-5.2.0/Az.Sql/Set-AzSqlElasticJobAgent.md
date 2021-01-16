---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
ms.openlocfilehash: 58adbb3b160272007899dc8740e211b6e81a10a4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98300459"
---
# <span data-ttu-id="de6b4-101">Set-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="de6b4-101">Set-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="de6b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de6b4-102">SYNOPSIS</span></span>
<span data-ttu-id="de6b4-103">Aktualisiert einen Jobsuchenmitarbeiter</span><span class="sxs-lookup"><span data-stu-id="de6b4-103">Updates an elastic job agent</span></span>

## <span data-ttu-id="de6b4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de6b4-104">SYNTAX</span></span>

### <span data-ttu-id="de6b4-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="de6b4-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de6b4-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="de6b4-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de6b4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="de6b4-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de6b4-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="de6b4-108">DESCRIPTION</span></span>
<span data-ttu-id="de6b4-109">Das cmdlet Set-AzSqlElasticJobAgent aktualisiert die Agents eines Jobcenters im Auftrag von "Job".</span><span class="sxs-lookup"><span data-stu-id="de6b4-109">The Set-AzSqlElasticJobAgent cmdlet updates an Elastic Job agents</span></span>

## <span data-ttu-id="de6b4-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="de6b4-110">EXAMPLES</span></span>

### <span data-ttu-id="de6b4-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="de6b4-111">Example 1</span></span>
```
PS C:\> Set-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent -Tag @{ Octopus = "Agent" }

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="de6b4-112">Aktualisiert einen Mitarbeiter für Jobsuchen</span><span class="sxs-lookup"><span data-stu-id="de6b4-112">Updates an Elastic Job agent</span></span>

## <span data-ttu-id="de6b4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de6b4-113">PARAMETERS</span></span>

### <span data-ttu-id="de6b4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de6b4-114">-DefaultProfile</span></span>
<span data-ttu-id="de6b4-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="de6b4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de6b4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de6b4-116">-InputObject</span></span>
<span data-ttu-id="de6b4-117">Das Agenteingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="de6b4-117">The agent input object</span></span>

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

### <span data-ttu-id="de6b4-118">-Name</span><span class="sxs-lookup"><span data-stu-id="de6b4-118">-Name</span></span>
<span data-ttu-id="de6b4-119">Der Name des Agents</span><span class="sxs-lookup"><span data-stu-id="de6b4-119">The agent name</span></span>

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

### <span data-ttu-id="de6b4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de6b4-120">-ResourceGroupName</span></span>
<span data-ttu-id="de6b4-121">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="de6b4-121">The resource group name</span></span>

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

### <span data-ttu-id="de6b4-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de6b4-122">-ResourceId</span></span>
<span data-ttu-id="de6b4-123">Die Agentressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="de6b4-123">The agent resource id</span></span>

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

### <span data-ttu-id="de6b4-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="de6b4-124">-ServerName</span></span>
<span data-ttu-id="de6b4-125">Der Servername</span><span class="sxs-lookup"><span data-stu-id="de6b4-125">The server name</span></span>

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

### <span data-ttu-id="de6b4-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="de6b4-126">-Tag</span></span>
<span data-ttu-id="de6b4-127">Die Tags, die dem Azure SQL-Datenbank-Agent zugeordnet werden sollen</span><span class="sxs-lookup"><span data-stu-id="de6b4-127">The tags to associate with the Azure SQL Database Agent</span></span>

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

### <span data-ttu-id="de6b4-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de6b4-128">-Confirm</span></span>
<span data-ttu-id="de6b4-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="de6b4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de6b4-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="de6b4-130">-WhatIf</span></span>
<span data-ttu-id="de6b4-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="de6b4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de6b4-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="de6b4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de6b4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de6b4-133">CommonParameters</span></span>
<span data-ttu-id="de6b4-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de6b4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de6b4-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de6b4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de6b4-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="de6b4-136">INPUTS</span></span>

### <span data-ttu-id="de6b4-137">Microsoft.Azure.Commands.Sql.AgentJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="de6b4-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="de6b4-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="de6b4-138">OUTPUTS</span></span>

### <span data-ttu-id="de6b4-139">Microsoft.Azure.Commands.Sql.AgentJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="de6b4-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="de6b4-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="de6b4-140">NOTES</span></span>

## <span data-ttu-id="de6b4-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="de6b4-141">RELATED LINKS</span></span>
