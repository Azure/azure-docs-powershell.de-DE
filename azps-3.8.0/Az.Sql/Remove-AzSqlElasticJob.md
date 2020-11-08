---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJob.md
ms.openlocfilehash: 03f2e9af6b7225fd7622c03347bdea87c63453c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003397"
---
# <span data-ttu-id="6e182-101">Remove-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="6e182-101">Remove-AzSqlElasticJob</span></span>

## <span data-ttu-id="6e182-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6e182-102">SYNOPSIS</span></span>
<span data-ttu-id="6e182-103">Entfernt einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="6e182-103">Removes a job</span></span>

## <span data-ttu-id="6e182-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e182-104">SYNTAX</span></span>

### <span data-ttu-id="6e182-105">Standardset (Standard)</span><span class="sxs-lookup"><span data-stu-id="6e182-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e182-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="6e182-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e182-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6e182-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJob [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e182-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e182-108">DESCRIPTION</span></span>
<span data-ttu-id="6e182-109">Das Remove-AzSqlElasticJob-Cmdlet entfernt einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="6e182-109">The Remove-AzSqlElasticJob cmdlet removes a job</span></span>

## <span data-ttu-id="6e182-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6e182-110">EXAMPLES</span></span>

### <span data-ttu-id="6e182-111">Beispiel 1 – entfernt einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="6e182-111">Example 1 - Removes a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="6e182-112">Entfernt einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="6e182-112">Removes a job</span></span>

## <span data-ttu-id="6e182-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e182-113">PARAMETERS</span></span>

### <span data-ttu-id="6e182-114">-Agentname</span><span class="sxs-lookup"><span data-stu-id="6e182-114">-AgentName</span></span>
<span data-ttu-id="6e182-115">Name des Agents</span><span class="sxs-lookup"><span data-stu-id="6e182-115">The agent name</span></span>

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

### <span data-ttu-id="6e182-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e182-116">-DefaultProfile</span></span>
<span data-ttu-id="6e182-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6e182-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e182-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6e182-118">-Force</span></span>
<span data-ttu-id="6e182-119">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="6e182-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="6e182-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6e182-120">-InputObject</span></span>
<span data-ttu-id="6e182-121">Das Auftragseingabe Objekt</span><span class="sxs-lookup"><span data-stu-id="6e182-121">The job input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e182-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6e182-122">-Name</span></span>
<span data-ttu-id="6e182-123">Der Name des Auftrags</span><span class="sxs-lookup"><span data-stu-id="6e182-123">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: JobName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e182-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e182-124">-ResourceGroupName</span></span>
<span data-ttu-id="6e182-125">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="6e182-125">The resource group name</span></span>

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

### <span data-ttu-id="6e182-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="6e182-126">-ResourceId</span></span>
<span data-ttu-id="6e182-127">Die Agent-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="6e182-127">The agent resource id</span></span>

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

### <span data-ttu-id="6e182-128">-Servername</span><span class="sxs-lookup"><span data-stu-id="6e182-128">-ServerName</span></span>
<span data-ttu-id="6e182-129">Der Servername</span><span class="sxs-lookup"><span data-stu-id="6e182-129">The server name</span></span>

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

### <span data-ttu-id="6e182-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6e182-130">-Confirm</span></span>
<span data-ttu-id="6e182-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6e182-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e182-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e182-132">-WhatIf</span></span>
<span data-ttu-id="6e182-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6e182-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e182-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6e182-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e182-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e182-135">CommonParameters</span></span>
<span data-ttu-id="6e182-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e182-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e182-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e182-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e182-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6e182-138">INPUTS</span></span>

### <span data-ttu-id="6e182-139">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="6e182-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="6e182-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6e182-140">OUTPUTS</span></span>

### <span data-ttu-id="6e182-141">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="6e182-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="6e182-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="6e182-142">NOTES</span></span>

## <span data-ttu-id="6e182-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6e182-143">RELATED LINKS</span></span>
