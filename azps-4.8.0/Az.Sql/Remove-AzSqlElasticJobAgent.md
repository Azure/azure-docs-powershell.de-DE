---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
ms.openlocfilehash: 1352ef72ffc6fd757b4019e217ecb439495ebb44
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166020"
---
# <span data-ttu-id="2faf4-101">Remove-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="2faf4-101">Remove-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="2faf4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2faf4-102">SYNOPSIS</span></span>
<span data-ttu-id="2faf4-103">Entfernt den elastischen Job-Agent</span><span class="sxs-lookup"><span data-stu-id="2faf4-103">Removes the elastic job agent</span></span>

## <span data-ttu-id="2faf4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2faf4-104">SYNTAX</span></span>

### <span data-ttu-id="2faf4-105">Standardset (Standard)</span><span class="sxs-lookup"><span data-stu-id="2faf4-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2faf4-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="2faf4-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2faf4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2faf4-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2faf4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2faf4-108">DESCRIPTION</span></span>
<span data-ttu-id="2faf4-109">Das Remove-AzSqlElasticJobAgent-Cmdlet entfernt einen elastischen Auftrags-Agent</span><span class="sxs-lookup"><span data-stu-id="2faf4-109">The Remove-AzSqlElasticJobAgent cmdlet removes an Elastic Job agent</span></span>

## <span data-ttu-id="2faf4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2faf4-110">EXAMPLES</span></span>

### <span data-ttu-id="2faf4-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2faf4-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="2faf4-112">Entfernt einen elastischen Job-Agent</span><span class="sxs-lookup"><span data-stu-id="2faf4-112">Removes an Elastic Job agent</span></span>

## <span data-ttu-id="2faf4-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="2faf4-113">PARAMETERS</span></span>

### <span data-ttu-id="2faf4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2faf4-114">-DefaultProfile</span></span>
<span data-ttu-id="2faf4-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2faf4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2faf4-116">-Force</span><span class="sxs-lookup"><span data-stu-id="2faf4-116">-Force</span></span>
<span data-ttu-id="2faf4-117">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="2faf4-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="2faf4-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2faf4-118">-InputObject</span></span>
<span data-ttu-id="2faf4-119">Das Agent-Objekt</span><span class="sxs-lookup"><span data-stu-id="2faf4-119">The agent object</span></span>

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

### <span data-ttu-id="2faf4-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2faf4-120">-Name</span></span>
<span data-ttu-id="2faf4-121">Name des Agents</span><span class="sxs-lookup"><span data-stu-id="2faf4-121">The agent name</span></span>

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

### <span data-ttu-id="2faf4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2faf4-122">-ResourceGroupName</span></span>
<span data-ttu-id="2faf4-123">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="2faf4-123">The resource group name</span></span>

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

### <span data-ttu-id="2faf4-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2faf4-124">-ResourceId</span></span>
<span data-ttu-id="2faf4-125">Die Agent-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="2faf4-125">The agent resource id</span></span>

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

### <span data-ttu-id="2faf4-126">-Servername</span><span class="sxs-lookup"><span data-stu-id="2faf4-126">-ServerName</span></span>
<span data-ttu-id="2faf4-127">Der Servername</span><span class="sxs-lookup"><span data-stu-id="2faf4-127">The server name</span></span>

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

### <span data-ttu-id="2faf4-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2faf4-128">-Confirm</span></span>
<span data-ttu-id="2faf4-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2faf4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2faf4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2faf4-130">-WhatIf</span></span>
<span data-ttu-id="2faf4-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2faf4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2faf4-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2faf4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2faf4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2faf4-133">CommonParameters</span></span>
<span data-ttu-id="2faf4-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2faf4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2faf4-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2faf4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2faf4-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2faf4-136">INPUTS</span></span>

### <span data-ttu-id="2faf4-137">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="2faf4-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="2faf4-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2faf4-138">OUTPUTS</span></span>

### <span data-ttu-id="2faf4-139">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="2faf4-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="2faf4-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="2faf4-140">NOTES</span></span>

## <span data-ttu-id="2faf4-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2faf4-141">RELATED LINKS</span></span>
