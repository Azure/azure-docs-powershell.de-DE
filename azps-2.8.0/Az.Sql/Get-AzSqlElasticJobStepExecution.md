---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobstepexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
ms.openlocfilehash: 74d3eca33de166ea7bd4a7b22a9c74145770b4a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825784"
---
# <span data-ttu-id="21a07-101">Get-AzSqlElasticJobStepExecution</span><span class="sxs-lookup"><span data-stu-id="21a07-101">Get-AzSqlElasticJobStepExecution</span></span>

## <span data-ttu-id="21a07-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="21a07-102">SYNOPSIS</span></span>
<span data-ttu-id="21a07-103">Ruft mindestens eine Auftragsschritt Ausführung ab</span><span class="sxs-lookup"><span data-stu-id="21a07-103">Gets one or more job step executions</span></span>

## <span data-ttu-id="21a07-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="21a07-104">SYNTAX</span></span>

### <span data-ttu-id="21a07-105">Standardset (Standard)</span><span class="sxs-lookup"><span data-stu-id="21a07-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="21a07-106">WithJobStepName</span><span class="sxs-lookup"><span data-stu-id="21a07-106">WithJobStepName</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -StepName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="21a07-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="21a07-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21a07-108">WithJobStepNameUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="21a07-108">WithJobStepNameUsingParentObject</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21a07-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="21a07-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21a07-110">WithJobStepNameUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="21a07-110">WithJobStepNameUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21a07-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="21a07-111">DESCRIPTION</span></span>
<span data-ttu-id="21a07-112">Das Get-AzSqlElasticJobStepExecution-Cmdlet ruft einen oder mehrere Auftragsschritt Ausführungen aus einer Auftragsausführung ab.</span><span class="sxs-lookup"><span data-stu-id="21a07-112">The Get-AzSqlElasticJobStepExecution cmdlet gets one or more job step executions from a job execution</span></span>

## <span data-ttu-id="21a07-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="21a07-113">EXAMPLES</span></span>

### <span data-ttu-id="21a07-114">Beispiel 1 – Ruft einen oder mehrere Auftragsschritt Ausführungen aus einer Auftragsausführung ab</span><span class="sxs-lookup"><span data-stu-id="21a07-114">Example 1 - Gets one or more job step executions from a job executions</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="21a07-115">Beispiel 2 – Ruft einen oder mehrere Auftragsschritt Ausführungen aus einer Auftragsausführung ab, wobei nach Schrittname gefiltert wird</span><span class="sxs-lookup"><span data-stu-id="21a07-115">Example 2 - Gets one or more job step executions from a job execution, filtering by step name</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution -StepName step1

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

<span data-ttu-id="21a07-116">Ruft mindestens eine Auftragsschritt Ausführung ab</span><span class="sxs-lookup"><span data-stu-id="21a07-116">Gets one or more job step executions</span></span>

## <span data-ttu-id="21a07-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="21a07-117">PARAMETERS</span></span>

### <span data-ttu-id="21a07-118">-Aktiv</span><span class="sxs-lookup"><span data-stu-id="21a07-118">-Active</span></span>
<span data-ttu-id="21a07-119">Kennzeichnen, um nach aktiven Ausführungen zu filtern.</span><span class="sxs-lookup"><span data-stu-id="21a07-119">Flag to filter by active executions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21a07-120">-Agentname</span><span class="sxs-lookup"><span data-stu-id="21a07-120">-AgentName</span></span>
<span data-ttu-id="21a07-121">Der Name des Agents.</span><span class="sxs-lookup"><span data-stu-id="21a07-121">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21a07-122">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="21a07-122">-CreateTimeMax</span></span>
<span data-ttu-id="21a07-123">Filtern nach Erstellungszeit Max</span><span class="sxs-lookup"><span data-stu-id="21a07-123">Filter by create time max</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21a07-124">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="21a07-124">-CreateTimeMin</span></span>
<span data-ttu-id="21a07-125">Filtern nach Erstellungszeit min</span><span class="sxs-lookup"><span data-stu-id="21a07-125">Filter by create time min</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21a07-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21a07-126">-DefaultProfile</span></span>
<span data-ttu-id="21a07-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="21a07-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21a07-128">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="21a07-128">-EndTimeMax</span></span>
<span data-ttu-id="21a07-129">Nach Beendigungszeit Max Filtern</span><span class="sxs-lookup"><span data-stu-id="21a07-129">Filter by end time max.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21a07-130">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="21a07-130">-EndTimeMin</span></span>
<span data-ttu-id="21a07-131">Filtern nach Endzeit min.</span><span class="sxs-lookup"><span data-stu-id="21a07-131">Filter by end time min.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21a07-132">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="21a07-132">-JobExecutionId</span></span>
<span data-ttu-id="21a07-133">Die Auftrags Ausführungs-ID.</span><span class="sxs-lookup"><span data-stu-id="21a07-133">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21a07-134">-Jobname</span><span class="sxs-lookup"><span data-stu-id="21a07-134">-JobName</span></span>
<span data-ttu-id="21a07-135">Der Name des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="21a07-135">The job name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21a07-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="21a07-136">-ParentObject</span></span>
<span data-ttu-id="21a07-137">Das Agent-Objekt.</span><span class="sxs-lookup"><span data-stu-id="21a07-137">The agent object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel
Parameter Sets: ObjectSet, WithJobStepNameUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21a07-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="21a07-138">-ParentResourceId</span></span>
<span data-ttu-id="21a07-139">Die Ressourcen-ID des Auftrags Ausführungs Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="21a07-139">The job execution resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithJobStepNameUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21a07-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21a07-140">-ResourceGroupName</span></span>
<span data-ttu-id="21a07-141">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="21a07-141">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21a07-142">-Servername</span><span class="sxs-lookup"><span data-stu-id="21a07-142">-ServerName</span></span>
<span data-ttu-id="21a07-143">Der Servername.</span><span class="sxs-lookup"><span data-stu-id="21a07-143">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21a07-144">-Stepname</span><span class="sxs-lookup"><span data-stu-id="21a07-144">-StepName</span></span>
<span data-ttu-id="21a07-145">Der Name des Auftragsschritts.</span><span class="sxs-lookup"><span data-stu-id="21a07-145">The job step name.</span></span>

```yaml
Type: System.String
Parameter Sets: WithJobStepName, WithJobStepNameUsingParentObject, WithJobStepNameUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21a07-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21a07-146">CommonParameters</span></span>
<span data-ttu-id="21a07-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21a07-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21a07-148">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21a07-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21a07-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="21a07-149">INPUTS</span></span>

### <span data-ttu-id="21a07-150">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="21a07-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="21a07-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="21a07-151">OUTPUTS</span></span>

### <span data-ttu-id="21a07-152">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="21a07-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="21a07-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="21a07-153">NOTES</span></span>

## <span data-ttu-id="21a07-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="21a07-154">RELATED LINKS</span></span>
