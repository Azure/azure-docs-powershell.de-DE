---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
ms.openlocfilehash: 1352ef72ffc6fd757b4019e217ecb439495ebb44
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179602"
---
# <span data-ttu-id="d5cf3-101">Remove-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="d5cf3-101">Remove-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="d5cf3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d5cf3-102">SYNOPSIS</span></span>
<span data-ttu-id="d5cf3-103">Entfernt den elastischen Job-Agent</span><span class="sxs-lookup"><span data-stu-id="d5cf3-103">Removes the elastic job agent</span></span>

## <span data-ttu-id="d5cf3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5cf3-104">SYNTAX</span></span>

### <span data-ttu-id="d5cf3-105">Standardset (Standard)</span><span class="sxs-lookup"><span data-stu-id="d5cf3-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5cf3-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="d5cf3-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5cf3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d5cf3-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5cf3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d5cf3-108">DESCRIPTION</span></span>
<span data-ttu-id="d5cf3-109">Das Remove-AzSqlElasticJobAgent-Cmdlet entfernt einen elastischen Auftrags-Agent</span><span class="sxs-lookup"><span data-stu-id="d5cf3-109">The Remove-AzSqlElasticJobAgent cmdlet removes an Elastic Job agent</span></span>

## <span data-ttu-id="d5cf3-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d5cf3-110">EXAMPLES</span></span>

### <span data-ttu-id="d5cf3-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d5cf3-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="d5cf3-112">Entfernt einen elastischen Job-Agent</span><span class="sxs-lookup"><span data-stu-id="d5cf3-112">Removes an Elastic Job agent</span></span>

## <span data-ttu-id="d5cf3-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5cf3-113">PARAMETERS</span></span>

### <span data-ttu-id="d5cf3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5cf3-114">-DefaultProfile</span></span>
<span data-ttu-id="d5cf3-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d5cf3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5cf3-116">-Force</span><span class="sxs-lookup"><span data-stu-id="d5cf3-116">-Force</span></span>
<span data-ttu-id="d5cf3-117">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="d5cf3-117">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5cf3-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d5cf3-118">-InputObject</span></span>
<span data-ttu-id="d5cf3-119">Das Agent-Objekt</span><span class="sxs-lookup"><span data-stu-id="d5cf3-119">The agent object</span></span>

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

### <span data-ttu-id="d5cf3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d5cf3-120">-Name</span></span>
<span data-ttu-id="d5cf3-121">Name des Agents</span><span class="sxs-lookup"><span data-stu-id="d5cf3-121">The agent name</span></span>

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

### <span data-ttu-id="d5cf3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5cf3-122">-ResourceGroupName</span></span>
<span data-ttu-id="d5cf3-123">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="d5cf3-123">The resource group name</span></span>

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

### <span data-ttu-id="d5cf3-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d5cf3-124">-ResourceId</span></span>
<span data-ttu-id="d5cf3-125">Die Agent-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="d5cf3-125">The agent resource id</span></span>

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

### <span data-ttu-id="d5cf3-126">-Servername</span><span class="sxs-lookup"><span data-stu-id="d5cf3-126">-ServerName</span></span>
<span data-ttu-id="d5cf3-127">Der Servername</span><span class="sxs-lookup"><span data-stu-id="d5cf3-127">The server name</span></span>

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

### <span data-ttu-id="d5cf3-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d5cf3-128">-Confirm</span></span>
<span data-ttu-id="d5cf3-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d5cf3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5cf3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5cf3-130">-WhatIf</span></span>
<span data-ttu-id="d5cf3-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5cf3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5cf3-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d5cf3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5cf3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5cf3-133">CommonParameters</span></span>
<span data-ttu-id="d5cf3-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5cf3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5cf3-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5cf3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5cf3-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d5cf3-136">INPUTS</span></span>

### <span data-ttu-id="d5cf3-137">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="d5cf3-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="d5cf3-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d5cf3-138">OUTPUTS</span></span>

### <span data-ttu-id="d5cf3-139">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="d5cf3-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="d5cf3-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="d5cf3-140">NOTES</span></span>

## <span data-ttu-id="d5cf3-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d5cf3-141">RELATED LINKS</span></span>
