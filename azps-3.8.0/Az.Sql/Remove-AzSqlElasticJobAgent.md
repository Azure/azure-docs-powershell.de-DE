---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
ms.openlocfilehash: 1352ef72ffc6fd757b4019e217ecb439495ebb44
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003396"
---
# <span data-ttu-id="61822-101">Remove-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="61822-101">Remove-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="61822-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="61822-102">SYNOPSIS</span></span>
<span data-ttu-id="61822-103">Entfernt den elastischen Job-Agent</span><span class="sxs-lookup"><span data-stu-id="61822-103">Removes the elastic job agent</span></span>

## <span data-ttu-id="61822-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="61822-104">SYNTAX</span></span>

### <span data-ttu-id="61822-105">Standardset (Standard)</span><span class="sxs-lookup"><span data-stu-id="61822-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61822-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="61822-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61822-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="61822-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61822-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61822-108">DESCRIPTION</span></span>
<span data-ttu-id="61822-109">Das Remove-AzSqlElasticJobAgent-Cmdlet entfernt einen elastischen Auftrags-Agent</span><span class="sxs-lookup"><span data-stu-id="61822-109">The Remove-AzSqlElasticJobAgent cmdlet removes an Elastic Job agent</span></span>

## <span data-ttu-id="61822-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="61822-110">EXAMPLES</span></span>

### <span data-ttu-id="61822-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="61822-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="61822-112">Entfernt einen elastischen Job-Agent</span><span class="sxs-lookup"><span data-stu-id="61822-112">Removes an Elastic Job agent</span></span>

## <span data-ttu-id="61822-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="61822-113">PARAMETERS</span></span>

### <span data-ttu-id="61822-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61822-114">-DefaultProfile</span></span>
<span data-ttu-id="61822-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="61822-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61822-116">-Force</span><span class="sxs-lookup"><span data-stu-id="61822-116">-Force</span></span>
<span data-ttu-id="61822-117">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="61822-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="61822-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="61822-118">-InputObject</span></span>
<span data-ttu-id="61822-119">Das Agent-Objekt</span><span class="sxs-lookup"><span data-stu-id="61822-119">The agent object</span></span>

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

### <span data-ttu-id="61822-120">-Name</span><span class="sxs-lookup"><span data-stu-id="61822-120">-Name</span></span>
<span data-ttu-id="61822-121">Name des Agents</span><span class="sxs-lookup"><span data-stu-id="61822-121">The agent name</span></span>

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

### <span data-ttu-id="61822-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61822-122">-ResourceGroupName</span></span>
<span data-ttu-id="61822-123">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="61822-123">The resource group name</span></span>

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

### <span data-ttu-id="61822-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="61822-124">-ResourceId</span></span>
<span data-ttu-id="61822-125">Die Agent-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="61822-125">The agent resource id</span></span>

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

### <span data-ttu-id="61822-126">-Servername</span><span class="sxs-lookup"><span data-stu-id="61822-126">-ServerName</span></span>
<span data-ttu-id="61822-127">Der Servername</span><span class="sxs-lookup"><span data-stu-id="61822-127">The server name</span></span>

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

### <span data-ttu-id="61822-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="61822-128">-Confirm</span></span>
<span data-ttu-id="61822-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="61822-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61822-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61822-130">-WhatIf</span></span>
<span data-ttu-id="61822-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="61822-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61822-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="61822-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61822-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61822-133">CommonParameters</span></span>
<span data-ttu-id="61822-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61822-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61822-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61822-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61822-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="61822-136">INPUTS</span></span>

### <span data-ttu-id="61822-137">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="61822-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="61822-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="61822-138">OUTPUTS</span></span>

### <span data-ttu-id="61822-139">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="61822-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="61822-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="61822-140">NOTES</span></span>

## <span data-ttu-id="61822-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="61822-141">RELATED LINKS</span></span>
