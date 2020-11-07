---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
ms.openlocfilehash: 5b5837fb0c5fa56e8e8f9887b6d85bfc3a3a559c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825583"
---
# <span data-ttu-id="f2093-101">Get-AzSqlElasticJobExecution</span><span class="sxs-lookup"><span data-stu-id="f2093-101">Get-AzSqlElasticJobExecution</span></span>

## <span data-ttu-id="f2093-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f2093-102">SYNOPSIS</span></span>
<span data-ttu-id="f2093-103">Ruft mindestens eine Auftragsausführung ab</span><span class="sxs-lookup"><span data-stu-id="f2093-103">Gets one or more job executions</span></span>

## <span data-ttu-id="f2093-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2093-104">SYNTAX</span></span>

### <span data-ttu-id="f2093-105">Standardset (Standard)</span><span class="sxs-lookup"><span data-stu-id="f2093-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName <String>] [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2093-106">WithJobExecutionId</span><span class="sxs-lookup"><span data-stu-id="f2093-106">WithJobExecutionId</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 -JobName <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2093-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="f2093-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> [-JobName <String>]
 [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2093-108">WithJobExecutionIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="f2093-108">WithJobExecutionIdUsingParentObject</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> -JobName <String>
 -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2093-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f2093-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> [-JobName <String>] [-Count] <Int32>
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2093-110">WithJobExecutionIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f2093-110">WithJobExecutionIdUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> -JobName <String> -JobExecutionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2093-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2093-111">DESCRIPTION</span></span>
<span data-ttu-id="f2093-112">Das Get-AzSqlElasticJobExecution-Cmdlet ruft mindestens eine Auftragsausführung ab.</span><span class="sxs-lookup"><span data-stu-id="f2093-112">The Get-AzSqlElasticJobExecution cmdlet gets one or more job executions</span></span>

## <span data-ttu-id="f2093-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f2093-113">EXAMPLES</span></span>

### <span data-ttu-id="f2093-114">Beispiel 1 – Ruft eine oder mehrere Auftragsausführungen über alle Aufträge ab</span><span class="sxs-lookup"><span data-stu-id="f2093-114">Example 1 - Gets one or more job executions across all jobs</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b Canceled  6/1/2018 10:13:56 PM 6/1/2018 10:13:59 PM
job1    3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:43 PM 6/1/2018 10:11:47 PM
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

### <span data-ttu-id="f2093-115">Beispiel 2 – ruft mindestens eine Auftragsausführung für einen Auftrag ab</span><span class="sxs-lookup"><span data-stu-id="f2093-115">Example 2 - Gets one or more job executions for a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3 -JobName job2

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

<span data-ttu-id="f2093-116">Ruft mindestens eine Auftragsausführung ab</span><span class="sxs-lookup"><span data-stu-id="f2093-116">Gets one or more job executions</span></span>

## <span data-ttu-id="f2093-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2093-117">PARAMETERS</span></span>

### <span data-ttu-id="f2093-118">-Aktiv</span><span class="sxs-lookup"><span data-stu-id="f2093-118">-Active</span></span>
<span data-ttu-id="f2093-119">Filtern nach Erstellungszeit min</span><span class="sxs-lookup"><span data-stu-id="f2093-119">Filter by create time min</span></span>

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

### <span data-ttu-id="f2093-120">-Agentname</span><span class="sxs-lookup"><span data-stu-id="f2093-120">-AgentName</span></span>
<span data-ttu-id="f2093-121">Der Name des Agents.</span><span class="sxs-lookup"><span data-stu-id="f2093-121">The agent name.</span></span>

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

### <span data-ttu-id="f2093-122">-Anzahl</span><span class="sxs-lookup"><span data-stu-id="f2093-122">-Count</span></span>
<span data-ttu-id="f2093-123">Anzahl gibt die oberste Anzahl der Ausführungen zurück.</span><span class="sxs-lookup"><span data-stu-id="f2093-123">Count returns the top number of executions.</span></span>

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

### <span data-ttu-id="f2093-124">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="f2093-124">-CreateTimeMax</span></span>
<span data-ttu-id="f2093-125">Filtern nach Erstellungszeit min</span><span class="sxs-lookup"><span data-stu-id="f2093-125">Filter by create time min</span></span>

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

### <span data-ttu-id="f2093-126">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="f2093-126">-CreateTimeMin</span></span>
<span data-ttu-id="f2093-127">Filtern nach Erstellungszeit min</span><span class="sxs-lookup"><span data-stu-id="f2093-127">Filter by create time min</span></span>

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

### <span data-ttu-id="f2093-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2093-128">-DefaultProfile</span></span>
<span data-ttu-id="f2093-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f2093-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2093-130">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="f2093-130">-EndTimeMax</span></span>
<span data-ttu-id="f2093-131">Filtern nach Erstellungszeit min</span><span class="sxs-lookup"><span data-stu-id="f2093-131">Filter by create time min</span></span>

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

### <span data-ttu-id="f2093-132">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="f2093-132">-EndTimeMin</span></span>
<span data-ttu-id="f2093-133">Filtern nach Erstellungszeit min</span><span class="sxs-lookup"><span data-stu-id="f2093-133">Filter by create time min</span></span>

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

### <span data-ttu-id="f2093-134">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="f2093-134">-JobExecutionId</span></span>
<span data-ttu-id="f2093-135">Die Auftrags Ausführungs-ID.</span><span class="sxs-lookup"><span data-stu-id="f2093-135">The job execution id.</span></span>

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

### <span data-ttu-id="f2093-136">-Jobname</span><span class="sxs-lookup"><span data-stu-id="f2093-136">-JobName</span></span>
<span data-ttu-id="f2093-137">Der Name des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="f2093-137">The job name.</span></span>

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

### <span data-ttu-id="f2093-138">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f2093-138">-ParentObject</span></span>
<span data-ttu-id="f2093-139">Die Auftrags Ausführungs-ID.</span><span class="sxs-lookup"><span data-stu-id="f2093-139">The job execution id.</span></span>

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

### <span data-ttu-id="f2093-140">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f2093-140">-ParentResourceId</span></span>
<span data-ttu-id="f2093-141">Die Agent-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="f2093-141">The agent resource id.</span></span>

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

### <span data-ttu-id="f2093-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2093-142">-ResourceGroupName</span></span>
<span data-ttu-id="f2093-143">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f2093-143">The resource group name.</span></span>

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

### <span data-ttu-id="f2093-144">-Servername</span><span class="sxs-lookup"><span data-stu-id="f2093-144">-ServerName</span></span>
<span data-ttu-id="f2093-145">Der Servername.</span><span class="sxs-lookup"><span data-stu-id="f2093-145">The server name.</span></span>

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

### <span data-ttu-id="f2093-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2093-146">CommonParameters</span></span>
<span data-ttu-id="f2093-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2093-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2093-148">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2093-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2093-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f2093-149">INPUTS</span></span>

### <span data-ttu-id="f2093-150">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="f2093-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="f2093-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f2093-151">OUTPUTS</span></span>

### <span data-ttu-id="f2093-152">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="f2093-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="f2093-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="f2093-153">NOTES</span></span>

## <span data-ttu-id="f2093-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f2093-154">RELATED LINKS</span></span>
