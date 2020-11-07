---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: 98c019c8dedf767fc2b75bb2133f7c545ffd03ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845387"
---
# <span data-ttu-id="f4d65-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="f4d65-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="f4d65-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f4d65-102">SYNOPSIS</span></span>
<span data-ttu-id="f4d65-103">Erstellt einen neuen Auftrag</span><span class="sxs-lookup"><span data-stu-id="f4d65-103">Creates a new job</span></span>

## <span data-ttu-id="f4d65-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4d65-104">SYNTAX</span></span>

### <span data-ttu-id="f4d65-105">Standardset (Standard)</span><span class="sxs-lookup"><span data-stu-id="f4d65-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4d65-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="f4d65-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4d65-107">Regelmäßige</span><span class="sxs-lookup"><span data-stu-id="f4d65-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4d65-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="f4d65-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4d65-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="f4d65-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4d65-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="f4d65-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4d65-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f4d65-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4d65-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f4d65-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4d65-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f4d65-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4d65-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4d65-114">DESCRIPTION</span></span>
<span data-ttu-id="f4d65-115">Das New-AzSqlElasticJob-Cmdlet erstellt einen neuen Auftrag</span><span class="sxs-lookup"><span data-stu-id="f4d65-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="f4d65-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f4d65-116">EXAMPLES</span></span>

### <span data-ttu-id="f4d65-117">Beispiel 1: Erstellen eines neuen Auftrags</span><span class="sxs-lookup"><span data-stu-id="f4d65-117">Example 1 - Creates a new job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="f4d65-118">Erstellt einen neuen Auftrag</span><span class="sxs-lookup"><span data-stu-id="f4d65-118">Creates a new job</span></span>

## <span data-ttu-id="f4d65-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4d65-119">PARAMETERS</span></span>

### <span data-ttu-id="f4d65-120">-Agentname</span><span class="sxs-lookup"><span data-stu-id="f4d65-120">-AgentName</span></span>
<span data-ttu-id="f4d65-121">Name des Agents</span><span class="sxs-lookup"><span data-stu-id="f4d65-121">The agent name</span></span>

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

### <span data-ttu-id="f4d65-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4d65-122">-DefaultProfile</span></span>
<span data-ttu-id="f4d65-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f4d65-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4d65-124">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4d65-124">-Description</span></span>
<span data-ttu-id="f4d65-125">Die Stellenbeschreibung</span><span class="sxs-lookup"><span data-stu-id="f4d65-125">The job description</span></span>

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

### <span data-ttu-id="f4d65-126">-Enable</span><span class="sxs-lookup"><span data-stu-id="f4d65-126">-Enable</span></span>
<span data-ttu-id="f4d65-127">Die Kennzeichnung, die besagt, dass der Kunde diesen Job aktivieren möchte.</span><span class="sxs-lookup"><span data-stu-id="f4d65-127">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="f4d65-128">-EndTime</span><span class="sxs-lookup"><span data-stu-id="f4d65-128">-EndTime</span></span>
<span data-ttu-id="f4d65-129">Endzeit des Auftragszeitplans</span><span class="sxs-lookup"><span data-stu-id="f4d65-129">The job schedule end time</span></span>

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

### <span data-ttu-id="f4d65-130">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="f4d65-130">-IntervalCount</span></span>
<span data-ttu-id="f4d65-131">Die Anzahl der wiederkehrenden Zeit Plan Intervalle</span><span class="sxs-lookup"><span data-stu-id="f4d65-131">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="f4d65-132">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="f4d65-132">-IntervalType</span></span>
<span data-ttu-id="f4d65-133">Der Typ des periodischen Zeitplanintervalls-kann Minuten, Stunden, Tag, Woche, Monat sein.</span><span class="sxs-lookup"><span data-stu-id="f4d65-133">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="f4d65-134">-Name</span><span class="sxs-lookup"><span data-stu-id="f4d65-134">-Name</span></span>
<span data-ttu-id="f4d65-135">Der Name des Auftrags</span><span class="sxs-lookup"><span data-stu-id="f4d65-135">The job name</span></span>

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

### <span data-ttu-id="f4d65-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f4d65-136">-ParentObject</span></span>
<span data-ttu-id="f4d65-137">Das Eingabeobjekt des Agents</span><span class="sxs-lookup"><span data-stu-id="f4d65-137">The agent input object</span></span>

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

### <span data-ttu-id="f4d65-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f4d65-138">-ParentResourceId</span></span>
<span data-ttu-id="f4d65-139">Die Agent-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="f4d65-139">The agent resource id</span></span>

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

### <span data-ttu-id="f4d65-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4d65-140">-ResourceGroupName</span></span>
<span data-ttu-id="f4d65-141">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f4d65-141">The resource group name</span></span>

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

### <span data-ttu-id="f4d65-142">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="f4d65-142">-RunOnce</span></span>
<span data-ttu-id="f4d65-143">Das Flag, um anzugeben, dass Job einmal ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="f4d65-143">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="f4d65-144">-Servername</span><span class="sxs-lookup"><span data-stu-id="f4d65-144">-ServerName</span></span>
<span data-ttu-id="f4d65-145">Der Servername</span><span class="sxs-lookup"><span data-stu-id="f4d65-145">The server name</span></span>

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

### <span data-ttu-id="f4d65-146">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="f4d65-146">-StartTime</span></span>
<span data-ttu-id="f4d65-147">Die Startzeit des Auftragszeitplans</span><span class="sxs-lookup"><span data-stu-id="f4d65-147">The job schedule start time</span></span>

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

### <span data-ttu-id="f4d65-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f4d65-148">-Confirm</span></span>
<span data-ttu-id="f4d65-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f4d65-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4d65-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4d65-150">-WhatIf</span></span>
<span data-ttu-id="f4d65-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f4d65-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4d65-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f4d65-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4d65-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4d65-153">CommonParameters</span></span>
<span data-ttu-id="f4d65-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4d65-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4d65-155">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4d65-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4d65-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f4d65-156">INPUTS</span></span>

### <span data-ttu-id="f4d65-157">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="f4d65-157">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="f4d65-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f4d65-158">OUTPUTS</span></span>

### <span data-ttu-id="f4d65-159">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="f4d65-159">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="f4d65-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="f4d65-160">NOTES</span></span>

## <span data-ttu-id="f4d65-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f4d65-161">RELATED LINKS</span></span>
