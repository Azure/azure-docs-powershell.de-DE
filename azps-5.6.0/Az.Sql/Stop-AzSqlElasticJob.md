---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/stop-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
ms.openlocfilehash: 1279366f07ce071e223aea1f7cc048403b9b4379
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939371"
---
# <span data-ttu-id="2b871-101">Stop-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="2b871-101">Stop-AzSqlElasticJob</span></span>

## <span data-ttu-id="2b871-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b871-102">SYNOPSIS</span></span>
<span data-ttu-id="2b871-103">Beendet einen Auftrag mit der Auftragsausführungs-ID</span><span class="sxs-lookup"><span data-stu-id="2b871-103">Stops a job given it's job execution id</span></span>

## <span data-ttu-id="2b871-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2b871-104">SYNTAX</span></span>

### <span data-ttu-id="2b871-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2b871-105">DefaultSet (Default)</span></span>
```
Stop-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b871-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="2b871-106">ObjectSet</span></span>
```
Stop-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobExecutionModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b871-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2b871-107">ResourceIdSet</span></span>
```
Stop-AzSqlElasticJob [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b871-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2b871-108">DESCRIPTION</span></span>
<span data-ttu-id="2b871-109">Das Stop-AzSqlElasticJob-Cmdlet beendet die Ausführung eines Auftrags mit einer ausgeführten Ausführung.</span><span class="sxs-lookup"><span data-stu-id="2b871-109">The Stop-AzSqlElasticJob cmdlet stops a job's with a running execution.</span></span>
<span data-ttu-id="2b871-110">Gibt den aktuellen Status der Auftragsausführung zurück.</span><span class="sxs-lookup"><span data-stu-id="2b871-110">Returns the current status of the job execution</span></span>

## <span data-ttu-id="2b871-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2b871-111">EXAMPLES</span></span>

### <span data-ttu-id="2b871-112">Beispiel 1: Stoppt einen Auftrag mit ausgeführter Auftragsausführung</span><span class="sxs-lookup"><span data-stu-id="2b871-112">Example 1: Stops a job with a running job execution</span></span>
```powershell
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId dab0ebe8-fd52-42e9-bacf-e5f27577039b
$je | Stop-AzSqlElasticJob
JobName JobExecutionId                       Lifecycle                    StartTime            EndTime
------- --------------                       ---------                    ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b WaitingForChildJobExecutions 6/1/2018 10:13:56 PM
```

<span data-ttu-id="2b871-113">Beendet die Ausführung eines ausgeführten Auftrags und gibt den aktuellen Status zurück.</span><span class="sxs-lookup"><span data-stu-id="2b871-113">Stops a running job execution and returns it's current status</span></span>

### <span data-ttu-id="2b871-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2b871-114">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Stop-AzSqlElasticJob -AgentName agent -JobExecutionId 00000000-0000-0000-0000-000000000000 -JobName job1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="2b871-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2b871-115">PARAMETERS</span></span>

### <span data-ttu-id="2b871-116">-AgentName</span><span class="sxs-lookup"><span data-stu-id="2b871-116">-AgentName</span></span>
<span data-ttu-id="2b871-117">Der Agentname</span><span class="sxs-lookup"><span data-stu-id="2b871-117">The agent name</span></span>

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

### <span data-ttu-id="2b871-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b871-118">-DefaultProfile</span></span>
<span data-ttu-id="2b871-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2b871-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b871-120">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="2b871-120">-JobExecutionId</span></span>
<span data-ttu-id="2b871-121">Die Auftragsausführungs-ID.</span><span class="sxs-lookup"><span data-stu-id="2b871-121">The job execution id.</span></span>

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

### <span data-ttu-id="2b871-122">-JobName</span><span class="sxs-lookup"><span data-stu-id="2b871-122">-JobName</span></span>
<span data-ttu-id="2b871-123">Der Auftragsname</span><span class="sxs-lookup"><span data-stu-id="2b871-123">The job name</span></span>

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

### <span data-ttu-id="2b871-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2b871-124">-ParentObject</span></span>
<span data-ttu-id="2b871-125">Das Datenbankobjekt "Agentsteuerelement"</span><span class="sxs-lookup"><span data-stu-id="2b871-125">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="2b871-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2b871-126">-ParentResourceId</span></span>
<span data-ttu-id="2b871-127">Ressourcen-ID für die Auftragsausführung</span><span class="sxs-lookup"><span data-stu-id="2b871-127">The job execution resource id</span></span>

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

### <span data-ttu-id="2b871-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b871-128">-ResourceGroupName</span></span>
<span data-ttu-id="2b871-129">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="2b871-129">The resource group name</span></span>

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

### <span data-ttu-id="2b871-130">-Servername</span><span class="sxs-lookup"><span data-stu-id="2b871-130">-ServerName</span></span>
<span data-ttu-id="2b871-131">Der Servername</span><span class="sxs-lookup"><span data-stu-id="2b871-131">The server name</span></span>

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

### <span data-ttu-id="2b871-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2b871-132">-Confirm</span></span>
<span data-ttu-id="2b871-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2b871-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b871-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b871-134">-WhatIf</span></span>
<span data-ttu-id="2b871-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2b871-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b871-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2b871-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b871-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b871-137">CommonParameters</span></span>
<span data-ttu-id="2b871-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b871-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b871-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b871-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b871-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2b871-140">INPUTS</span></span>

### <span data-ttu-id="2b871-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="2b871-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="2b871-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2b871-142">OUTPUTS</span></span>

### <span data-ttu-id="2b871-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="2b871-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="2b871-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2b871-144">NOTES</span></span>

## <span data-ttu-id="2b871-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2b871-145">RELATED LINKS</span></span>
