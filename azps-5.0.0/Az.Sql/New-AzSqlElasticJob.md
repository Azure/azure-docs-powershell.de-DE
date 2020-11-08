---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: e6853c3b4fa32a10e93ee281aab0b97755403671
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176891"
---
# <span data-ttu-id="4aa7c-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="4aa7c-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="4aa7c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4aa7c-102">SYNOPSIS</span></span>
<span data-ttu-id="4aa7c-103">Erstellt einen neuen Auftrag</span><span class="sxs-lookup"><span data-stu-id="4aa7c-103">Creates a new job</span></span>

## <span data-ttu-id="4aa7c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4aa7c-104">SYNTAX</span></span>

### <span data-ttu-id="4aa7c-105">Standardset (Standard)</span><span class="sxs-lookup"><span data-stu-id="4aa7c-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4aa7c-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="4aa7c-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4aa7c-107">Regelmäßige</span><span class="sxs-lookup"><span data-stu-id="4aa7c-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4aa7c-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="4aa7c-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4aa7c-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="4aa7c-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4aa7c-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="4aa7c-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4aa7c-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4aa7c-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4aa7c-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4aa7c-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4aa7c-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4aa7c-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4aa7c-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4aa7c-114">DESCRIPTION</span></span>
<span data-ttu-id="4aa7c-115">Das New-AzSqlElasticJob-Cmdlet erstellt einen neuen Auftrag</span><span class="sxs-lookup"><span data-stu-id="4aa7c-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="4aa7c-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4aa7c-116">EXAMPLES</span></span>

### <span data-ttu-id="4aa7c-117">Beispiel 1: Erstellen eines neuen Auftrags</span><span class="sxs-lookup"><span data-stu-id="4aa7c-117">Example 1: Creates a new job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="4aa7c-118">Erstellt einen neuen Auftrag</span><span class="sxs-lookup"><span data-stu-id="4aa7c-118">Creates a new job</span></span>

### <span data-ttu-id="4aa7c-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4aa7c-119">Example 2</span></span>

<span data-ttu-id="4aa7c-120">Erstellt einen neuen Auftrag.</span><span class="sxs-lookup"><span data-stu-id="4aa7c-120">Creates a new job.</span></span> <span data-ttu-id="4aa7c-121">automatisch</span><span class="sxs-lookup"><span data-stu-id="4aa7c-121">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticJob -Name job1 -RunOnce
```

## <span data-ttu-id="4aa7c-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="4aa7c-122">PARAMETERS</span></span>

### <span data-ttu-id="4aa7c-123">-Agentname</span><span class="sxs-lookup"><span data-stu-id="4aa7c-123">-AgentName</span></span>
<span data-ttu-id="4aa7c-124">Name des Agents</span><span class="sxs-lookup"><span data-stu-id="4aa7c-124">The agent name</span></span>

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

### <span data-ttu-id="4aa7c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aa7c-125">-DefaultProfile</span></span>
<span data-ttu-id="4aa7c-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4aa7c-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4aa7c-127">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4aa7c-127">-Description</span></span>
<span data-ttu-id="4aa7c-128">Die Stellenbeschreibung</span><span class="sxs-lookup"><span data-stu-id="4aa7c-128">The job description</span></span>

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

### <span data-ttu-id="4aa7c-129">-Enable</span><span class="sxs-lookup"><span data-stu-id="4aa7c-129">-Enable</span></span>
<span data-ttu-id="4aa7c-130">Die Kennzeichnung, die besagt, dass der Kunde diesen Job aktivieren möchte.</span><span class="sxs-lookup"><span data-stu-id="4aa7c-130">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="4aa7c-131">-EndTime</span><span class="sxs-lookup"><span data-stu-id="4aa7c-131">-EndTime</span></span>
<span data-ttu-id="4aa7c-132">Endzeit des Auftragszeitplans</span><span class="sxs-lookup"><span data-stu-id="4aa7c-132">The job schedule end time</span></span>

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

### <span data-ttu-id="4aa7c-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="4aa7c-133">-IntervalCount</span></span>
<span data-ttu-id="4aa7c-134">Die Anzahl der wiederkehrenden Zeit Plan Intervalle</span><span class="sxs-lookup"><span data-stu-id="4aa7c-134">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="4aa7c-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="4aa7c-135">-IntervalType</span></span>
<span data-ttu-id="4aa7c-136">Der Typ des periodischen Zeitplanintervalls-kann Minuten, Stunden, Tag, Woche, Monat sein.</span><span class="sxs-lookup"><span data-stu-id="4aa7c-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="4aa7c-137">-Name</span><span class="sxs-lookup"><span data-stu-id="4aa7c-137">-Name</span></span>
<span data-ttu-id="4aa7c-138">Der Name des Auftrags</span><span class="sxs-lookup"><span data-stu-id="4aa7c-138">The job name</span></span>

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

### <span data-ttu-id="4aa7c-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4aa7c-139">-ParentObject</span></span>
<span data-ttu-id="4aa7c-140">Das Eingabeobjekt des Agents</span><span class="sxs-lookup"><span data-stu-id="4aa7c-140">The agent input object</span></span>

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

### <span data-ttu-id="4aa7c-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4aa7c-141">-ParentResourceId</span></span>
<span data-ttu-id="4aa7c-142">Die Agent-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="4aa7c-142">The agent resource id</span></span>

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

### <span data-ttu-id="4aa7c-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4aa7c-143">-ResourceGroupName</span></span>
<span data-ttu-id="4aa7c-144">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="4aa7c-144">The resource group name</span></span>

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

### <span data-ttu-id="4aa7c-145">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="4aa7c-145">-RunOnce</span></span>
<span data-ttu-id="4aa7c-146">Das Flag, um anzugeben, dass Job einmal ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="4aa7c-146">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="4aa7c-147">-Servername</span><span class="sxs-lookup"><span data-stu-id="4aa7c-147">-ServerName</span></span>
<span data-ttu-id="4aa7c-148">Der Servername</span><span class="sxs-lookup"><span data-stu-id="4aa7c-148">The server name</span></span>

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

### <span data-ttu-id="4aa7c-149">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="4aa7c-149">-StartTime</span></span>
<span data-ttu-id="4aa7c-150">Die Startzeit des Auftragszeitplans</span><span class="sxs-lookup"><span data-stu-id="4aa7c-150">The job schedule start time</span></span>

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

### <span data-ttu-id="4aa7c-151">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4aa7c-151">-Confirm</span></span>
<span data-ttu-id="4aa7c-152">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4aa7c-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4aa7c-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4aa7c-153">-WhatIf</span></span>
<span data-ttu-id="4aa7c-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4aa7c-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4aa7c-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4aa7c-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4aa7c-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aa7c-156">CommonParameters</span></span>
<span data-ttu-id="4aa7c-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4aa7c-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aa7c-158">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4aa7c-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aa7c-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4aa7c-159">INPUTS</span></span>

### <span data-ttu-id="4aa7c-160">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="4aa7c-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="4aa7c-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4aa7c-161">OUTPUTS</span></span>

### <span data-ttu-id="4aa7c-162">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="4aa7c-162">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="4aa7c-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="4aa7c-163">NOTES</span></span>

## <span data-ttu-id="4aa7c-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4aa7c-164">RELATED LINKS</span></span>
