---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/stop-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
ms.openlocfilehash: ec5ab9706bd459a07c91e7060d3bf6da30f76ed5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173788"
---
# <span data-ttu-id="1fb99-101">Stop-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="1fb99-101">Stop-AzSqlElasticJob</span></span>

## <span data-ttu-id="1fb99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fb99-102">SYNOPSIS</span></span>
<span data-ttu-id="1fb99-103">Beendet einen Auftrag mit der Auftragsausführungs-ID</span><span class="sxs-lookup"><span data-stu-id="1fb99-103">Stops a job given it's job execution id</span></span>

## <span data-ttu-id="1fb99-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1fb99-104">SYNTAX</span></span>

### <span data-ttu-id="1fb99-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1fb99-105">DefaultSet (Default)</span></span>
```
Stop-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1fb99-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="1fb99-106">ObjectSet</span></span>
```
Stop-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobExecutionModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fb99-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1fb99-107">ResourceIdSet</span></span>
```
Stop-AzSqlElasticJob [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fb99-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1fb99-108">DESCRIPTION</span></span>
<span data-ttu-id="1fb99-109">Das Stop-AzSqlElasticJob-Cmdlet beendet die Ausführung eines Auftrags mit einer ausgeführten Ausführung.</span><span class="sxs-lookup"><span data-stu-id="1fb99-109">The Stop-AzSqlElasticJob cmdlet stops a job's with a running execution.</span></span>
<span data-ttu-id="1fb99-110">Gibt den aktuellen Status der Auftragsausführung zurück.</span><span class="sxs-lookup"><span data-stu-id="1fb99-110">Returns the current status of the job execution</span></span>

## <span data-ttu-id="1fb99-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1fb99-111">EXAMPLES</span></span>

### <span data-ttu-id="1fb99-112">Beispiel 1: Beendet einen Auftrag mit ausgeführter Ausführung eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="1fb99-112">Example 1: Stops a job with a running job execution</span></span>
```powershell
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId dab0ebe8-fd52-42e9-bacf-e5f27577039b
$je | Stop-AzSqlElasticJob
JobName JobExecutionId                       Lifecycle                    StartTime            EndTime
------- --------------                       ---------                    ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b WaitingForChildJobExecutions 6/1/2018 10:13:56 PM
```

<span data-ttu-id="1fb99-113">Beendet die Ausführung eines ausgeführten Auftrags und gibt den aktuellen Status zurück.</span><span class="sxs-lookup"><span data-stu-id="1fb99-113">Stops a running job execution and returns it's current status</span></span>

### <span data-ttu-id="1fb99-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1fb99-114">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Stop-AzSqlElasticJob -AgentName agent -JobExecutionId 00000000-0000-0000-0000-000000000000 -JobName job1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="1fb99-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1fb99-115">PARAMETERS</span></span>

### <span data-ttu-id="1fb99-116">-AgentName</span><span class="sxs-lookup"><span data-stu-id="1fb99-116">-AgentName</span></span>
<span data-ttu-id="1fb99-117">Der Agentname</span><span class="sxs-lookup"><span data-stu-id="1fb99-117">The agent name</span></span>

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

### <span data-ttu-id="1fb99-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fb99-118">-DefaultProfile</span></span>
<span data-ttu-id="1fb99-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1fb99-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fb99-120">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="1fb99-120">-JobExecutionId</span></span>
<span data-ttu-id="1fb99-121">Die Auftragsausführungs-ID.</span><span class="sxs-lookup"><span data-stu-id="1fb99-121">The job execution id.</span></span>

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

### <span data-ttu-id="1fb99-122">-JobName</span><span class="sxs-lookup"><span data-stu-id="1fb99-122">-JobName</span></span>
<span data-ttu-id="1fb99-123">Der Name des Auftrags</span><span class="sxs-lookup"><span data-stu-id="1fb99-123">The job name</span></span>

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

### <span data-ttu-id="1fb99-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1fb99-124">-ParentObject</span></span>
<span data-ttu-id="1fb99-125">Das Datenbankobjekt des Agentsteuerelements</span><span class="sxs-lookup"><span data-stu-id="1fb99-125">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="1fb99-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="1fb99-126">-ParentResourceId</span></span>
<span data-ttu-id="1fb99-127">Die Ressourcen-ID für die Ausführung des Auftrags</span><span class="sxs-lookup"><span data-stu-id="1fb99-127">The job execution resource id</span></span>

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

### <span data-ttu-id="1fb99-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fb99-128">-ResourceGroupName</span></span>
<span data-ttu-id="1fb99-129">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="1fb99-129">The resource group name</span></span>

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

### <span data-ttu-id="1fb99-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1fb99-130">-ServerName</span></span>
<span data-ttu-id="1fb99-131">Der Servername</span><span class="sxs-lookup"><span data-stu-id="1fb99-131">The server name</span></span>

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

### <span data-ttu-id="1fb99-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1fb99-132">-Confirm</span></span>
<span data-ttu-id="1fb99-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1fb99-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fb99-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1fb99-134">-WhatIf</span></span>
<span data-ttu-id="1fb99-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1fb99-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fb99-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1fb99-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fb99-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fb99-137">CommonParameters</span></span>
<span data-ttu-id="1fb99-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fb99-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fb99-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1fb99-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fb99-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1fb99-140">INPUTS</span></span>

### <span data-ttu-id="1fb99-141">Microsoft.Azure.Commands.Sql.BenchmarkJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="1fb99-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="1fb99-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1fb99-142">OUTPUTS</span></span>

### <span data-ttu-id="1fb99-143">Microsoft.Azure.Commands.Sql.BenchmarkJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="1fb99-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="1fb99-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1fb99-144">NOTES</span></span>

## <span data-ttu-id="1fb99-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1fb99-145">RELATED LINKS</span></span>
