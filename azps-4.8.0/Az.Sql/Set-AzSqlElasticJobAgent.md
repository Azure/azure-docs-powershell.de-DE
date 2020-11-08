---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
ms.openlocfilehash: 58adbb3b160272007899dc8740e211b6e81a10a4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008826"
---
# <span data-ttu-id="db734-101">Set-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="db734-101">Set-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="db734-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="db734-102">SYNOPSIS</span></span>
<span data-ttu-id="db734-103">Aktualisieren eines elastischen Job-Agents</span><span class="sxs-lookup"><span data-stu-id="db734-103">Updates an elastic job agent</span></span>

## <span data-ttu-id="db734-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="db734-104">SYNTAX</span></span>

### <span data-ttu-id="db734-105">Standardset (Standard)</span><span class="sxs-lookup"><span data-stu-id="db734-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db734-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="db734-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db734-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="db734-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db734-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="db734-108">DESCRIPTION</span></span>
<span data-ttu-id="db734-109">Das Set-AzSqlElasticJobAgent-Cmdlet aktualisiert eine elastische Auftrags-Agents</span><span class="sxs-lookup"><span data-stu-id="db734-109">The Set-AzSqlElasticJobAgent cmdlet updates an Elastic Job agents</span></span>

## <span data-ttu-id="db734-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="db734-110">EXAMPLES</span></span>

### <span data-ttu-id="db734-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="db734-111">Example 1</span></span>
```
PS C:\> Set-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent -Tag @{ Octopus = "Agent" }

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="db734-112">Aktualisieren eines elastischen Job-Agents</span><span class="sxs-lookup"><span data-stu-id="db734-112">Updates an Elastic Job agent</span></span>

## <span data-ttu-id="db734-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="db734-113">PARAMETERS</span></span>

### <span data-ttu-id="db734-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db734-114">-DefaultProfile</span></span>
<span data-ttu-id="db734-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="db734-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db734-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="db734-116">-InputObject</span></span>
<span data-ttu-id="db734-117">Das Eingabeobjekt des Agents</span><span class="sxs-lookup"><span data-stu-id="db734-117">The agent input object</span></span>

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

### <span data-ttu-id="db734-118">-Name</span><span class="sxs-lookup"><span data-stu-id="db734-118">-Name</span></span>
<span data-ttu-id="db734-119">Name des Agents</span><span class="sxs-lookup"><span data-stu-id="db734-119">The agent name</span></span>

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

### <span data-ttu-id="db734-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db734-120">-ResourceGroupName</span></span>
<span data-ttu-id="db734-121">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="db734-121">The resource group name</span></span>

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

### <span data-ttu-id="db734-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="db734-122">-ResourceId</span></span>
<span data-ttu-id="db734-123">Die Agent-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="db734-123">The agent resource id</span></span>

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

### <span data-ttu-id="db734-124">-Servername</span><span class="sxs-lookup"><span data-stu-id="db734-124">-ServerName</span></span>
<span data-ttu-id="db734-125">Der Servername</span><span class="sxs-lookup"><span data-stu-id="db734-125">The server name</span></span>

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

### <span data-ttu-id="db734-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="db734-126">-Tag</span></span>
<span data-ttu-id="db734-127">Die Tags, die dem Azure SQL-Datenbankagenten zugeordnet werden sollen</span><span class="sxs-lookup"><span data-stu-id="db734-127">The tags to associate with the Azure SQL Database Agent</span></span>

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

### <span data-ttu-id="db734-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="db734-128">-Confirm</span></span>
<span data-ttu-id="db734-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="db734-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db734-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db734-130">-WhatIf</span></span>
<span data-ttu-id="db734-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="db734-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db734-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="db734-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db734-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db734-133">CommonParameters</span></span>
<span data-ttu-id="db734-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db734-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db734-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db734-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db734-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="db734-136">INPUTS</span></span>

### <span data-ttu-id="db734-137">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="db734-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="db734-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="db734-138">OUTPUTS</span></span>

### <span data-ttu-id="db734-139">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="db734-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="db734-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="db734-140">NOTES</span></span>

## <span data-ttu-id="db734-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="db734-141">RELATED LINKS</span></span>
