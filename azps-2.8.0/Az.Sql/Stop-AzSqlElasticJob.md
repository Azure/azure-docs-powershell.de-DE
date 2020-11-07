---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/stop-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
ms.openlocfilehash: 0b7fc702ad331a2ad51e1adfaf4aefd6ae440259
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826199"
---
# <span data-ttu-id="0a251-101">Stop-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="0a251-101">Stop-AzSqlElasticJob</span></span>

## <span data-ttu-id="0a251-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0a251-102">SYNOPSIS</span></span>
<span data-ttu-id="0a251-103">Beendet einen Auftrag, da er die Auftrags Ausführungs-ID hat.</span><span class="sxs-lookup"><span data-stu-id="0a251-103">Stops a job given it's job execution id</span></span>

## <span data-ttu-id="0a251-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a251-104">SYNTAX</span></span>

### <span data-ttu-id="0a251-105">Standardset (Standard)</span><span class="sxs-lookup"><span data-stu-id="0a251-105">DefaultSet (Default)</span></span>
```
Stop-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a251-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="0a251-106">ObjectSet</span></span>
```
Stop-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobExecutionModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a251-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0a251-107">ResourceIdSet</span></span>
```
Stop-AzSqlElasticJob [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a251-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a251-108">DESCRIPTION</span></span>
<span data-ttu-id="0a251-109">Das Stop-AzSqlElasticJob-Cmdlet beendet einen Auftrag mit einer ausgeführten Ausführung.</span><span class="sxs-lookup"><span data-stu-id="0a251-109">The Stop-AzSqlElasticJob cmdlet stops a job's with a running execution.</span></span>
<span data-ttu-id="0a251-110">Gibt den aktuellen Status der Auftragsausführung zurück.</span><span class="sxs-lookup"><span data-stu-id="0a251-110">Returns the current status of the job execution</span></span>

## <span data-ttu-id="0a251-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0a251-111">EXAMPLES</span></span>

### <span data-ttu-id="0a251-112">Beispiel 1: beendet einen Auftrag mit einer ausgeführten Auftragsausführung</span><span class="sxs-lookup"><span data-stu-id="0a251-112">Example 1 - Stops a job with a running job execution</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId dab0ebe8-fd52-42e9-bacf-e5f27577039b
$je | Stop-AzSqlElasticJob
JobName JobExecutionId                       Lifecycle                    StartTime            EndTime
------- --------------                       ---------                    ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b WaitingForChildJobExecutions 6/1/2018 10:13:56 PM
```

<span data-ttu-id="0a251-113">Beendet die Ausführung eines ausgeführten Auftrags und gibt den aktuellen Status zurück.</span><span class="sxs-lookup"><span data-stu-id="0a251-113">Stops a running job execution and returns it's current status</span></span>

## <span data-ttu-id="0a251-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a251-114">PARAMETERS</span></span>

### <span data-ttu-id="0a251-115">-Agentname</span><span class="sxs-lookup"><span data-stu-id="0a251-115">-AgentName</span></span>
<span data-ttu-id="0a251-116">Name des Agents</span><span class="sxs-lookup"><span data-stu-id="0a251-116">The agent name</span></span>

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

### <span data-ttu-id="0a251-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a251-117">-DefaultProfile</span></span>
<span data-ttu-id="0a251-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0a251-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a251-119">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="0a251-119">-JobExecutionId</span></span>
<span data-ttu-id="0a251-120">Die Auftrags Ausführungs-ID.</span><span class="sxs-lookup"><span data-stu-id="0a251-120">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a251-121">-Jobname</span><span class="sxs-lookup"><span data-stu-id="0a251-121">-JobName</span></span>
<span data-ttu-id="0a251-122">Der Name des Auftrags</span><span class="sxs-lookup"><span data-stu-id="0a251-122">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a251-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0a251-123">-ParentObject</span></span>
<span data-ttu-id="0a251-124">Das Datenbankobjekt des Agent-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="0a251-124">The Agent Control Database Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a251-125">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0a251-125">-ParentResourceId</span></span>
<span data-ttu-id="0a251-126">Die Auftrags Ausführungsressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="0a251-126">The job execution resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a251-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a251-127">-ResourceGroupName</span></span>
<span data-ttu-id="0a251-128">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="0a251-128">The resource group name</span></span>

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

### <span data-ttu-id="0a251-129">-Servername</span><span class="sxs-lookup"><span data-stu-id="0a251-129">-ServerName</span></span>
<span data-ttu-id="0a251-130">Der Servername</span><span class="sxs-lookup"><span data-stu-id="0a251-130">The server name</span></span>

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

### <span data-ttu-id="0a251-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0a251-131">-Confirm</span></span>
<span data-ttu-id="0a251-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0a251-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a251-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a251-133">-WhatIf</span></span>
<span data-ttu-id="0a251-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0a251-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a251-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0a251-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a251-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a251-136">CommonParameters</span></span>
<span data-ttu-id="0a251-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a251-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a251-138">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a251-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a251-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0a251-139">INPUTS</span></span>

### <span data-ttu-id="0a251-140">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="0a251-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="0a251-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0a251-141">OUTPUTS</span></span>

### <span data-ttu-id="0a251-142">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="0a251-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="0a251-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="0a251-143">NOTES</span></span>

## <span data-ttu-id="0a251-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0a251-144">RELATED LINKS</span></span>

## <span data-ttu-id="0a251-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0a251-145">RELATED LINKS</span></span>
