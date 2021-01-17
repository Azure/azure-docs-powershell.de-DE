---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobstepexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
ms.openlocfilehash: 03c4a6dede1f60e782bbfecdec1fb18894b2ca15
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471747"
---
# <span data-ttu-id="12e44-101">Get-AzSqlElasticJobStepExecution</span><span class="sxs-lookup"><span data-stu-id="12e44-101">Get-AzSqlElasticJobStepExecution</span></span>

## <span data-ttu-id="12e44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12e44-102">SYNOPSIS</span></span>
<span data-ttu-id="12e44-103">Ruft eine oder mehrere Ausführungsschritte ab</span><span class="sxs-lookup"><span data-stu-id="12e44-103">Gets one or more job step executions</span></span>

## <span data-ttu-id="12e44-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12e44-104">SYNTAX</span></span>

### <span data-ttu-id="12e44-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="12e44-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12e44-106">WithJobStepName</span><span class="sxs-lookup"><span data-stu-id="12e44-106">WithJobStepName</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -StepName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12e44-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="12e44-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12e44-108">WithJobStepNameUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="12e44-108">WithJobStepNameUsingParentObject</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12e44-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="12e44-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12e44-110">WithJobStepNameUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="12e44-110">WithJobStepNameUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12e44-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="12e44-111">DESCRIPTION</span></span>
<span data-ttu-id="12e44-112">Das Get-AzSqlElasticJobStepExecution cmdlet ruft eine oder mehrere Ausführungen von Auftragsschritten aus einer Auftragsausführung ab.</span><span class="sxs-lookup"><span data-stu-id="12e44-112">The Get-AzSqlElasticJobStepExecution cmdlet gets one or more job step executions from a job execution</span></span>

## <span data-ttu-id="12e44-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="12e44-113">EXAMPLES</span></span>

### <span data-ttu-id="12e44-114">Beispiel 1: Ruft eine oder mehrere Ausführungsschritte eines Auftrags ab.</span><span class="sxs-lookup"><span data-stu-id="12e44-114">Example 1 - Gets one or more job step executions from a job executions</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="12e44-115">Beispiel 2: Ruft eine oder mehrere Ausführungen von Auftragsschritten aus der Ausführung eines Auftrags ab und filtert nach Schrittname.</span><span class="sxs-lookup"><span data-stu-id="12e44-115">Example 2 - Gets one or more job step executions from a job execution, filtering by step name</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution -StepName step1

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

<span data-ttu-id="12e44-116">Ruft eine oder mehrere Ausführungen von Auftragsschritten ab</span><span class="sxs-lookup"><span data-stu-id="12e44-116">Gets one or more job step executions</span></span>

## <span data-ttu-id="12e44-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12e44-117">PARAMETERS</span></span>

### <span data-ttu-id="12e44-118">-Aktiv</span><span class="sxs-lookup"><span data-stu-id="12e44-118">-Active</span></span>
<span data-ttu-id="12e44-119">Zum Filtern nach aktiven Ausführungen kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="12e44-119">Flag to filter by active executions.</span></span>

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

### <span data-ttu-id="12e44-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="12e44-120">-AgentName</span></span>
<span data-ttu-id="12e44-121">Der Agentname.</span><span class="sxs-lookup"><span data-stu-id="12e44-121">The agent name.</span></span>

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

### <span data-ttu-id="12e44-122">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="12e44-122">-CreateTimeMax</span></span>
<span data-ttu-id="12e44-123">Maximale Zeit nach Erstellungszeit filtern</span><span class="sxs-lookup"><span data-stu-id="12e44-123">Filter by create time max</span></span>

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

### <span data-ttu-id="12e44-124">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="12e44-124">-CreateTimeMin</span></span>
<span data-ttu-id="12e44-125">Filtern nach "Mindestzeit erstellen"</span><span class="sxs-lookup"><span data-stu-id="12e44-125">Filter by create time min</span></span>

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

### <span data-ttu-id="12e44-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12e44-126">-DefaultProfile</span></span>
<span data-ttu-id="12e44-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="12e44-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12e44-128">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="12e44-128">-EndTimeMax</span></span>
<span data-ttu-id="12e44-129">Filter nach Endzeit max.</span><span class="sxs-lookup"><span data-stu-id="12e44-129">Filter by end time max.</span></span>

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

### <span data-ttu-id="12e44-130">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="12e44-130">-EndTimeMin</span></span>
<span data-ttu-id="12e44-131">Filtern nach Endzeit min.</span><span class="sxs-lookup"><span data-stu-id="12e44-131">Filter by end time min.</span></span>

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

### <span data-ttu-id="12e44-132">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="12e44-132">-JobExecutionId</span></span>
<span data-ttu-id="12e44-133">Die Auftragsausführungs-ID.</span><span class="sxs-lookup"><span data-stu-id="12e44-133">The job execution id.</span></span>

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

### <span data-ttu-id="12e44-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="12e44-134">-JobName</span></span>
<span data-ttu-id="12e44-135">Der Name des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="12e44-135">The job name.</span></span>

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

### <span data-ttu-id="12e44-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="12e44-136">-ParentObject</span></span>
<span data-ttu-id="12e44-137">Das Agentobjekt.</span><span class="sxs-lookup"><span data-stu-id="12e44-137">The agent object.</span></span>

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

### <span data-ttu-id="12e44-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="12e44-138">-ParentResourceId</span></span>
<span data-ttu-id="12e44-139">Die Ressourcen-ID für die Ausführung des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="12e44-139">The job execution resource id.</span></span>

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

### <span data-ttu-id="12e44-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12e44-140">-ResourceGroupName</span></span>
<span data-ttu-id="12e44-141">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="12e44-141">The resource group name.</span></span>

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

### <span data-ttu-id="12e44-142">-ServerName</span><span class="sxs-lookup"><span data-stu-id="12e44-142">-ServerName</span></span>
<span data-ttu-id="12e44-143">Der Servername.</span><span class="sxs-lookup"><span data-stu-id="12e44-143">The server name.</span></span>

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

### <span data-ttu-id="12e44-144">-StepName</span><span class="sxs-lookup"><span data-stu-id="12e44-144">-StepName</span></span>
<span data-ttu-id="12e44-145">Der Name des Auftragsschritts.</span><span class="sxs-lookup"><span data-stu-id="12e44-145">The job step name.</span></span>

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

### <span data-ttu-id="12e44-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e44-146">CommonParameters</span></span>
<span data-ttu-id="12e44-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12e44-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e44-148">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12e44-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e44-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="12e44-149">INPUTS</span></span>

### <span data-ttu-id="12e44-150">Microsoft.Azure.Commands.Sql.BenchmarkJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="12e44-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="12e44-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="12e44-151">OUTPUTS</span></span>

### <span data-ttu-id="12e44-152">Microsoft.Azure.Commands.Sql.BenchmarkJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="12e44-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="12e44-153">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="12e44-153">NOTES</span></span>

## <span data-ttu-id="12e44-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="12e44-154">RELATED LINKS</span></span>
