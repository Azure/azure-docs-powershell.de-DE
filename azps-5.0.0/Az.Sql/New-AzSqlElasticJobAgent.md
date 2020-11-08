---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
ms.openlocfilehash: f00c2e9cb7b9d0d35efdf99a6f81f24488dd8387
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176882"
---
# <span data-ttu-id="a47bf-101">New-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="a47bf-101">New-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="a47bf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a47bf-102">SYNOPSIS</span></span>
<span data-ttu-id="a47bf-103">Erstellt einen neuen elastischen Job-Agent</span><span class="sxs-lookup"><span data-stu-id="a47bf-103">Creates a new elastic job agent</span></span>

## <span data-ttu-id="a47bf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a47bf-104">SYNTAX</span></span>

### <span data-ttu-id="a47bf-105">Standardset (Standard)</span><span class="sxs-lookup"><span data-stu-id="a47bf-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-Name] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a47bf-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="a47bf-106">ObjectSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseObject] <AzureSqlDatabaseModel> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a47bf-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a47bf-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseResourceId] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a47bf-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a47bf-108">DESCRIPTION</span></span>
<span data-ttu-id="a47bf-109">Das New-AzSqlElasticJobAgent-Cmdlet erstellt einen neuen elastischen Auftrags-Agent</span><span class="sxs-lookup"><span data-stu-id="a47bf-109">The New-AzSqlElasticJobAgent cmdlet creates a new Elastic Job agent</span></span>

## <span data-ttu-id="a47bf-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a47bf-110">EXAMPLES</span></span>

### <span data-ttu-id="a47bf-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a47bf-111">Example 1</span></span>
```
PS C:\> New-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -DatabaseName jobdb -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="a47bf-112">Erstellt einen neuen elastischen Job-Agent</span><span class="sxs-lookup"><span data-stu-id="a47bf-112">Creates a new Elastic Job agent</span></span>

## <span data-ttu-id="a47bf-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a47bf-113">PARAMETERS</span></span>

### <span data-ttu-id="a47bf-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a47bf-114">-DatabaseName</span></span>
<span data-ttu-id="a47bf-115">Der Datenbankname</span><span class="sxs-lookup"><span data-stu-id="a47bf-115">The database name</span></span>

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

### <span data-ttu-id="a47bf-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="a47bf-116">-DatabaseObject</span></span>
<span data-ttu-id="a47bf-117">Das Datenbankobjekt des Agent-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="a47bf-117">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="a47bf-118">-DatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="a47bf-118">-DatabaseResourceId</span></span>
<span data-ttu-id="a47bf-119">Die Ressourcen-ID des Agent-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="a47bf-119">The Agent Control Database Resource Id</span></span>

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

### <span data-ttu-id="a47bf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a47bf-120">-DefaultProfile</span></span>
<span data-ttu-id="a47bf-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a47bf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a47bf-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a47bf-122">-Name</span></span>
<span data-ttu-id="a47bf-123">Name des Agents</span><span class="sxs-lookup"><span data-stu-id="a47bf-123">The Agent Name</span></span>

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

### <span data-ttu-id="a47bf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a47bf-124">-ResourceGroupName</span></span>
<span data-ttu-id="a47bf-125">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="a47bf-125">The resource group name</span></span>

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

### <span data-ttu-id="a47bf-126">-Servername</span><span class="sxs-lookup"><span data-stu-id="a47bf-126">-ServerName</span></span>
<span data-ttu-id="a47bf-127">Der Servername</span><span class="sxs-lookup"><span data-stu-id="a47bf-127">The server name</span></span>

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

### <span data-ttu-id="a47bf-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="a47bf-128">-Tag</span></span>
<span data-ttu-id="a47bf-129">Die Agenten-Tags</span><span class="sxs-lookup"><span data-stu-id="a47bf-129">The Agent Tags</span></span>

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

### <span data-ttu-id="a47bf-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a47bf-130">-Confirm</span></span>
<span data-ttu-id="a47bf-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a47bf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a47bf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a47bf-132">-WhatIf</span></span>
<span data-ttu-id="a47bf-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a47bf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a47bf-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a47bf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a47bf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a47bf-135">CommonParameters</span></span>
<span data-ttu-id="a47bf-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a47bf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a47bf-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a47bf-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a47bf-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a47bf-138">INPUTS</span></span>

### <span data-ttu-id="a47bf-139">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a47bf-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="a47bf-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a47bf-140">OUTPUTS</span></span>

### <span data-ttu-id="a47bf-141">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="a47bf-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="a47bf-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="a47bf-142">NOTES</span></span>

## <span data-ttu-id="a47bf-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a47bf-143">RELATED LINKS</span></span>
