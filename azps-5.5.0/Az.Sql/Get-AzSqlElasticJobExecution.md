---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
ms.openlocfilehash: d5583e5d7c0984b36679517859cc5a109b808a1a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165809"
---
# <span data-ttu-id="33392-101">Get-AzSqlElasticJobExecution</span><span class="sxs-lookup"><span data-stu-id="33392-101">Get-AzSqlElasticJobExecution</span></span>

## <span data-ttu-id="33392-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33392-102">SYNOPSIS</span></span>
<span data-ttu-id="33392-103">Ruft eine oder mehrere Auftragsausführungen ab</span><span class="sxs-lookup"><span data-stu-id="33392-103">Gets one or more job executions</span></span>

## <span data-ttu-id="33392-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="33392-104">SYNTAX</span></span>

### <span data-ttu-id="33392-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="33392-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName <String>] [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="33392-106">WithJobExecutionId</span><span class="sxs-lookup"><span data-stu-id="33392-106">WithJobExecutionId</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 -JobName <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33392-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="33392-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> [-JobName <String>]
 [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33392-108">WithJobExecutionIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="33392-108">WithJobExecutionIdUsingParentObject</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> -JobName <String>
 -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33392-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="33392-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> [-JobName <String>] [-Count] <Int32>
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33392-110">WithJobExecutionIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="33392-110">WithJobExecutionIdUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> -JobName <String> -JobExecutionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33392-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="33392-111">DESCRIPTION</span></span>
<span data-ttu-id="33392-112">Das Get-AzSqlElasticJobExecution-Cmdlet ruft eine oder mehrere Auftragsausführungen ab.</span><span class="sxs-lookup"><span data-stu-id="33392-112">The Get-AzSqlElasticJobExecution cmdlet gets one or more job executions</span></span>

## <span data-ttu-id="33392-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="33392-113">EXAMPLES</span></span>

### <span data-ttu-id="33392-114">Beispiel 1: Ruft eine oder mehrere Auftragsausführungen für alle Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="33392-114">Example 1: Gets one or more job executions across all jobs</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b Canceled  6/1/2018 10:13:56 PM 6/1/2018 10:13:59 PM
job1    3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:43 PM 6/1/2018 10:11:47 PM
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

### <span data-ttu-id="33392-115">Beispiel 2: Ruft eine oder mehrere Auftragsausführungen für einen Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="33392-115">Example 2: Gets one or more job executions for a job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3 -JobName job2

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

<span data-ttu-id="33392-116">Ruft eine oder mehrere Auftragsausführungen ab</span><span class="sxs-lookup"><span data-stu-id="33392-116">Gets one or more job executions</span></span>

### <span data-ttu-id="33392-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="33392-117">Example 3</span></span>

<span data-ttu-id="33392-118">Ruft eine oder mehrere Auftragsausführungen ab.</span><span class="sxs-lookup"><span data-stu-id="33392-118">Gets one or more job executions.</span></span> <span data-ttu-id="33392-119">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="33392-119">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlElasticJobExecution -JobExecutionId 00000000-0000-0000-0000-000000000000 -JobName job1
```

## <span data-ttu-id="33392-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33392-120">PARAMETERS</span></span>

### <span data-ttu-id="33392-121">-Aktiv</span><span class="sxs-lookup"><span data-stu-id="33392-121">-Active</span></span>
<span data-ttu-id="33392-122">Filtern nach "Mindestzeit erstellen"</span><span class="sxs-lookup"><span data-stu-id="33392-122">Filter by create time min</span></span>

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

### <span data-ttu-id="33392-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="33392-123">-AgentName</span></span>
<span data-ttu-id="33392-124">Der Agentname.</span><span class="sxs-lookup"><span data-stu-id="33392-124">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobExecutionId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33392-125">-Count</span><span class="sxs-lookup"><span data-stu-id="33392-125">-Count</span></span>
<span data-ttu-id="33392-126">"Count" gibt die oberste Anzahl von Ausführungsausführungen zurück.</span><span class="sxs-lookup"><span data-stu-id="33392-126">Count returns the top number of executions.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33392-127">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="33392-127">-CreateTimeMax</span></span>
<span data-ttu-id="33392-128">Filtern nach "Mindestzeit erstellen"</span><span class="sxs-lookup"><span data-stu-id="33392-128">Filter by create time min</span></span>

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

### <span data-ttu-id="33392-129">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="33392-129">-CreateTimeMin</span></span>
<span data-ttu-id="33392-130">Filtern nach "Mindestzeit erstellen"</span><span class="sxs-lookup"><span data-stu-id="33392-130">Filter by create time min</span></span>

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

### <span data-ttu-id="33392-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33392-131">-DefaultProfile</span></span>
<span data-ttu-id="33392-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="33392-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33392-133">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="33392-133">-EndTimeMax</span></span>
<span data-ttu-id="33392-134">Filtern nach "Mindestzeit erstellen"</span><span class="sxs-lookup"><span data-stu-id="33392-134">Filter by create time min</span></span>

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

### <span data-ttu-id="33392-135">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="33392-135">-EndTimeMin</span></span>
<span data-ttu-id="33392-136">Filtern nach "Mindestzeit erstellen"</span><span class="sxs-lookup"><span data-stu-id="33392-136">Filter by create time min</span></span>

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

### <span data-ttu-id="33392-137">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="33392-137">-JobExecutionId</span></span>
<span data-ttu-id="33392-138">Die Auftragsausführungs-ID.</span><span class="sxs-lookup"><span data-stu-id="33392-138">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: WithJobExecutionId, WithJobExecutionIdUsingParentObject, WithJobExecutionIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33392-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="33392-139">-JobName</span></span>
<span data-ttu-id="33392-140">Der Name des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="33392-140">The job name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WithJobExecutionId, WithJobExecutionIdUsingParentObject, WithJobExecutionIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33392-141">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="33392-141">-ParentObject</span></span>
<span data-ttu-id="33392-142">Die Auftragsausführungs-ID.</span><span class="sxs-lookup"><span data-stu-id="33392-142">The job execution id.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet, WithJobExecutionIdUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33392-143">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="33392-143">-ParentResourceId</span></span>
<span data-ttu-id="33392-144">Die Agentressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="33392-144">The agent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithJobExecutionIdUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33392-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33392-145">-ResourceGroupName</span></span>
<span data-ttu-id="33392-146">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="33392-146">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobExecutionId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33392-147">-ServerName</span><span class="sxs-lookup"><span data-stu-id="33392-147">-ServerName</span></span>
<span data-ttu-id="33392-148">Der Servername.</span><span class="sxs-lookup"><span data-stu-id="33392-148">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobExecutionId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33392-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33392-149">CommonParameters</span></span>
<span data-ttu-id="33392-150">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33392-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33392-151">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33392-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33392-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="33392-152">INPUTS</span></span>

### <span data-ttu-id="33392-153">Microsoft.Azure.Commands.Sql.AgentJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="33392-153">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="33392-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="33392-154">OUTPUTS</span></span>

### <span data-ttu-id="33392-155">Microsoft.Azure.Commands.Sql.BenchmarkJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="33392-155">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="33392-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="33392-156">NOTES</span></span>

## <span data-ttu-id="33392-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="33392-157">RELATED LINKS</span></span>
