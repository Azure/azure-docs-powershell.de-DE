---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/get-Azsqlelasticjobstepexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
ms.openlocfilehash: 9918c314d239bf822fa789bcab6a9de923b8c2e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943450"
---
# <span data-ttu-id="fd4ce-101">Get-AzSqlElasticJobStepExecution</span><span class="sxs-lookup"><span data-stu-id="fd4ce-101">Get-AzSqlElasticJobStepExecution</span></span>

## <span data-ttu-id="fd4ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd4ce-102">SYNOPSIS</span></span>
<span data-ttu-id="fd4ce-103">Ruft eine oder mehrere Auftragsschrittausführungen ab</span><span class="sxs-lookup"><span data-stu-id="fd4ce-103">Gets one or more job step executions</span></span>

## <span data-ttu-id="fd4ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd4ce-104">SYNTAX</span></span>

### <span data-ttu-id="fd4ce-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fd4ce-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fd4ce-106">WithJobStepName</span><span class="sxs-lookup"><span data-stu-id="fd4ce-106">WithJobStepName</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -StepName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fd4ce-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="fd4ce-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd4ce-108">WithJobStepNameUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="fd4ce-108">WithJobStepNameUsingParentObject</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd4ce-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fd4ce-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd4ce-110">WithJobStepNameUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fd4ce-110">WithJobStepNameUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd4ce-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd4ce-111">DESCRIPTION</span></span>
<span data-ttu-id="fd4ce-112">Das Get-AzSqlElasticJobStepExecution-Cmdlet ruft eine oder mehrere Auftragsschrittausführungen aus einer Auftragsausführung ab.</span><span class="sxs-lookup"><span data-stu-id="fd4ce-112">The Get-AzSqlElasticJobStepExecution cmdlet gets one or more job step executions from a job execution</span></span>

## <span data-ttu-id="fd4ce-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fd4ce-113">EXAMPLES</span></span>

### <span data-ttu-id="fd4ce-114">Beispiel 1 : Ruft eine oder mehrere Auftragsschrittausführungen aus einer Auftragsausführung ab.</span><span class="sxs-lookup"><span data-stu-id="fd4ce-114">Example 1 - Gets one or more job step executions from a job executions</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="fd4ce-115">Beispiel 2: Ruft eine oder mehrere Auftragsschrittausführungen aus einer Auftragsausführung ab und filtert nach Schrittname</span><span class="sxs-lookup"><span data-stu-id="fd4ce-115">Example 2 - Gets one or more job step executions from a job execution, filtering by step name</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution -StepName step1

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

<span data-ttu-id="fd4ce-116">Ruft eine oder mehrere Auftragsschrittausführungen ab</span><span class="sxs-lookup"><span data-stu-id="fd4ce-116">Gets one or more job step executions</span></span>

## <span data-ttu-id="fd4ce-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fd4ce-117">PARAMETERS</span></span>

### <span data-ttu-id="fd4ce-118">-Aktiv</span><span class="sxs-lookup"><span data-stu-id="fd4ce-118">-Active</span></span>
<span data-ttu-id="fd4ce-119">Kennzeichnen Sie, um nach aktiven Ausführungsausführungen zu filtern.</span><span class="sxs-lookup"><span data-stu-id="fd4ce-119">Flag to filter by active executions.</span></span>

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

### <span data-ttu-id="fd4ce-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="fd4ce-120">-AgentName</span></span>
<span data-ttu-id="fd4ce-121">Der Agentname.</span><span class="sxs-lookup"><span data-stu-id="fd4ce-121">The agent name.</span></span>

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

### <span data-ttu-id="fd4ce-122">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="fd4ce-122">-CreateTimeMax</span></span>
<span data-ttu-id="fd4ce-123">Filtern nach maximaler Erstellungszeit</span><span class="sxs-lookup"><span data-stu-id="fd4ce-123">Filter by create time max</span></span>

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

### <span data-ttu-id="fd4ce-124">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="fd4ce-124">-CreateTimeMin</span></span>
<span data-ttu-id="fd4ce-125">Filtern nach Erstellungszeit min</span><span class="sxs-lookup"><span data-stu-id="fd4ce-125">Filter by create time min</span></span>

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

### <span data-ttu-id="fd4ce-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd4ce-126">-DefaultProfile</span></span>
<span data-ttu-id="fd4ce-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd4ce-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd4ce-128">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="fd4ce-128">-EndTimeMax</span></span>
<span data-ttu-id="fd4ce-129">Filtern nach Endzeit max.</span><span class="sxs-lookup"><span data-stu-id="fd4ce-129">Filter by end time max.</span></span>

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

### <span data-ttu-id="fd4ce-130">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="fd4ce-130">-EndTimeMin</span></span>
<span data-ttu-id="fd4ce-131">Filtern nach Endzeit min.</span><span class="sxs-lookup"><span data-stu-id="fd4ce-131">Filter by end time min.</span></span>

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

### <span data-ttu-id="fd4ce-132">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="fd4ce-132">-JobExecutionId</span></span>
<span data-ttu-id="fd4ce-133">Die Auftragsausführungs-ID.</span><span class="sxs-lookup"><span data-stu-id="fd4ce-133">The job execution id.</span></span>

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

### <span data-ttu-id="fd4ce-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="fd4ce-134">-JobName</span></span>
<span data-ttu-id="fd4ce-135">Der Auftragsname.</span><span class="sxs-lookup"><span data-stu-id="fd4ce-135">The job name.</span></span>

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

### <span data-ttu-id="fd4ce-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fd4ce-136">-ParentObject</span></span>
<span data-ttu-id="fd4ce-137">Das Agentobjekt.</span><span class="sxs-lookup"><span data-stu-id="fd4ce-137">The agent object.</span></span>

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

### <span data-ttu-id="fd4ce-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fd4ce-138">-ParentResourceId</span></span>
<span data-ttu-id="fd4ce-139">Die Ressourcen-ID für die Auftragsausführung.</span><span class="sxs-lookup"><span data-stu-id="fd4ce-139">The job execution resource id.</span></span>

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

### <span data-ttu-id="fd4ce-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd4ce-140">-ResourceGroupName</span></span>
<span data-ttu-id="fd4ce-141">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fd4ce-141">The resource group name.</span></span>

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

### <span data-ttu-id="fd4ce-142">-Servername</span><span class="sxs-lookup"><span data-stu-id="fd4ce-142">-ServerName</span></span>
<span data-ttu-id="fd4ce-143">Der Servername.</span><span class="sxs-lookup"><span data-stu-id="fd4ce-143">The server name.</span></span>

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

### <span data-ttu-id="fd4ce-144">-StepName</span><span class="sxs-lookup"><span data-stu-id="fd4ce-144">-StepName</span></span>
<span data-ttu-id="fd4ce-145">Der Name des Auftragsschritts.</span><span class="sxs-lookup"><span data-stu-id="fd4ce-145">The job step name.</span></span>

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

### <span data-ttu-id="fd4ce-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd4ce-146">CommonParameters</span></span>
<span data-ttu-id="fd4ce-147">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd4ce-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd4ce-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd4ce-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd4ce-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fd4ce-149">INPUTS</span></span>

### <span data-ttu-id="fd4ce-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="fd4ce-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="fd4ce-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fd4ce-151">OUTPUTS</span></span>

### <span data-ttu-id="fd4ce-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="fd4ce-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="fd4ce-153">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fd4ce-153">NOTES</span></span>

## <span data-ttu-id="fd4ce-154">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fd4ce-154">RELATED LINKS</span></span>
