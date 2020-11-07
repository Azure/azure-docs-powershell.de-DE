---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: 29ae424807b8648238e2cc855fb90734773e870d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825464"
---
# <span data-ttu-id="0d4f3-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="0d4f3-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="0d4f3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0d4f3-102">SYNOPSIS</span></span>
<span data-ttu-id="0d4f3-103">Erstellt einen neuen Auftrag</span><span class="sxs-lookup"><span data-stu-id="0d4f3-103">Creates a new job</span></span>

## <span data-ttu-id="0d4f3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d4f3-104">SYNTAX</span></span>

### <span data-ttu-id="0d4f3-105">Standardset (Standard)</span><span class="sxs-lookup"><span data-stu-id="0d4f3-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d4f3-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="0d4f3-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d4f3-107">Regelmäßige</span><span class="sxs-lookup"><span data-stu-id="0d4f3-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d4f3-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="0d4f3-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d4f3-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="0d4f3-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d4f3-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="0d4f3-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d4f3-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0d4f3-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d4f3-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0d4f3-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d4f3-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0d4f3-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d4f3-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d4f3-114">DESCRIPTION</span></span>
<span data-ttu-id="0d4f3-115">Das New-AzSqlElasticJob-Cmdlet erstellt einen neuen Auftrag</span><span class="sxs-lookup"><span data-stu-id="0d4f3-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="0d4f3-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d4f3-116">EXAMPLES</span></span>

### <span data-ttu-id="0d4f3-117">Beispiel 1: Erstellen eines neuen Auftrags</span><span class="sxs-lookup"><span data-stu-id="0d4f3-117">Example 1 - Creates a new job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="0d4f3-118">Erstellt einen neuen Auftrag</span><span class="sxs-lookup"><span data-stu-id="0d4f3-118">Creates a new job</span></span>

## <span data-ttu-id="0d4f3-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d4f3-119">PARAMETERS</span></span>

### <span data-ttu-id="0d4f3-120">-Agentname</span><span class="sxs-lookup"><span data-stu-id="0d4f3-120">-AgentName</span></span>
<span data-ttu-id="0d4f3-121">Name des Agents</span><span class="sxs-lookup"><span data-stu-id="0d4f3-121">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d4f3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d4f3-122">-DefaultProfile</span></span>
<span data-ttu-id="0d4f3-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0d4f3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d4f3-124">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d4f3-124">-Description</span></span>
<span data-ttu-id="0d4f3-125">Die Stellenbeschreibung</span><span class="sxs-lookup"><span data-stu-id="0d4f3-125">The job description</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d4f3-126">-Enable</span><span class="sxs-lookup"><span data-stu-id="0d4f3-126">-Enable</span></span>
<span data-ttu-id="0d4f3-127">Die Kennzeichnung, die besagt, dass der Kunde diesen Job aktivieren möchte.</span><span class="sxs-lookup"><span data-stu-id="0d4f3-127">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="0d4f3-128">-EndTime</span><span class="sxs-lookup"><span data-stu-id="0d4f3-128">-EndTime</span></span>
<span data-ttu-id="0d4f3-129">Endzeit des Auftragszeitplans</span><span class="sxs-lookup"><span data-stu-id="0d4f3-129">The job schedule end time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d4f3-130">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="0d4f3-130">-IntervalCount</span></span>
<span data-ttu-id="0d4f3-131">Die Anzahl der wiederkehrenden Zeit Plan Intervalle</span><span class="sxs-lookup"><span data-stu-id="0d4f3-131">The recurring schedule interval count</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d4f3-132">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="0d4f3-132">-IntervalType</span></span>
<span data-ttu-id="0d4f3-133">Der Typ des periodischen Zeitplanintervalls-kann Minuten, Stunden, Tag, Woche, Monat sein.</span><span class="sxs-lookup"><span data-stu-id="0d4f3-133">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

```yaml
Type: System.String
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d4f3-134">-Name</span><span class="sxs-lookup"><span data-stu-id="0d4f3-134">-Name</span></span>
<span data-ttu-id="0d4f3-135">Der Name des Auftrags</span><span class="sxs-lookup"><span data-stu-id="0d4f3-135">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: JobName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d4f3-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0d4f3-136">-ParentObject</span></span>
<span data-ttu-id="0d4f3-137">Das Eingabeobjekt des Agents</span><span class="sxs-lookup"><span data-stu-id="0d4f3-137">The agent input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet, RunOnceUsingParentObject, RecurringUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d4f3-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0d4f3-138">-ParentResourceId</span></span>
<span data-ttu-id="0d4f3-139">Die Agent-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="0d4f3-139">The agent resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, RunOnceUsingParentResourceId, RecurringUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d4f3-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d4f3-140">-ResourceGroupName</span></span>
<span data-ttu-id="0d4f3-141">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="0d4f3-141">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d4f3-142">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="0d4f3-142">-RunOnce</span></span>
<span data-ttu-id="0d4f3-143">Das Flag, um anzugeben, dass Job einmal ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="0d4f3-143">The flag to indicate job will be run once</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RunOnce, RunOnceUsingParentObject, RunOnceUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d4f3-144">-Servername</span><span class="sxs-lookup"><span data-stu-id="0d4f3-144">-ServerName</span></span>
<span data-ttu-id="0d4f3-145">Der Servername</span><span class="sxs-lookup"><span data-stu-id="0d4f3-145">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d4f3-146">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="0d4f3-146">-StartTime</span></span>
<span data-ttu-id="0d4f3-147">Die Startzeit des Auftragszeitplans</span><span class="sxs-lookup"><span data-stu-id="0d4f3-147">The job schedule start time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: RunOnce, Recurring, RunOnceUsingParentObject, RecurringUsingParentObject, RunOnceUsingParentResourceId, RecurringUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d4f3-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0d4f3-148">-Confirm</span></span>
<span data-ttu-id="0d4f3-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0d4f3-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d4f3-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d4f3-150">-WhatIf</span></span>
<span data-ttu-id="0d4f3-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0d4f3-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d4f3-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0d4f3-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d4f3-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d4f3-153">CommonParameters</span></span>
<span data-ttu-id="0d4f3-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d4f3-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d4f3-155">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d4f3-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d4f3-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0d4f3-156">INPUTS</span></span>

### <span data-ttu-id="0d4f3-157">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="0d4f3-157">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="0d4f3-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0d4f3-158">OUTPUTS</span></span>

### <span data-ttu-id="0d4f3-159">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="0d4f3-159">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="0d4f3-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="0d4f3-160">NOTES</span></span>

## <span data-ttu-id="0d4f3-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0d4f3-161">RELATED LINKS</span></span>
