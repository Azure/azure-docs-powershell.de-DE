---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
ms.openlocfilehash: 04f182cb410e77a9ca61aa6f80da14c08e517406
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825743"
---
# <span data-ttu-id="f8914-101">Set-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="f8914-101">Set-AzSqlElasticJob</span></span>

## <span data-ttu-id="f8914-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f8914-102">SYNOPSIS</span></span>
<span data-ttu-id="f8914-103">Aktualisiert einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="f8914-103">Updates a job</span></span>

## <span data-ttu-id="f8914-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8914-104">SYNTAX</span></span>

### <span data-ttu-id="f8914-105">Standardset (Standard)</span><span class="sxs-lookup"><span data-stu-id="f8914-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8914-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="f8914-106">RunOnce</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8914-107">Regelmäßige</span><span class="sxs-lookup"><span data-stu-id="f8914-107">Recurring</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8914-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="f8914-108">ObjectSet</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f8914-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="f8914-109">RunOnceUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-RunOnce] [-StartTime <DateTime>]
 [-EndTime <DateTime>] [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8914-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="f8914-110">RecurringUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8914-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f8914-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8914-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f8914-112">RunOnceUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8914-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f8914-113">RecurringUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8914-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f8914-114">DESCRIPTION</span></span>
<span data-ttu-id="f8914-115">Das Set-AzSqlElasticJob-Cmdlet aktualisiert einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="f8914-115">The Set-AzSqlElasticJob cmdlet updates a job</span></span>

## <span data-ttu-id="f8914-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f8914-116">EXAMPLES</span></span>

### <span data-ttu-id="f8914-117">Beispiel 1: aktualisiert einen Job, um eine Stunde ab jetzt zu beginnen, und wiederholen Sie alle 1 Stunde.</span><span class="sxs-lookup"><span data-stu-id="f8914-117">Example 1 - Updates a job to start an hour from now and repeat every 1 hour</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Set-AzSqlElasticJob -IntervalType Hour -IntervalCount 1 -StartTime (Get-Date).AddHours(1) -Enable

JobName Version Description StartTime            EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------            -------                ------------ -------- -------
job1    0                   6/1/2018 10:50:15 PM 12/31/9999 11:59:59 AM Recurring    PT1H     True
```

<span data-ttu-id="f8914-118">Aktualisiert einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="f8914-118">Updates a job</span></span>

## <span data-ttu-id="f8914-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8914-119">PARAMETERS</span></span>

### <span data-ttu-id="f8914-120">-Agentname</span><span class="sxs-lookup"><span data-stu-id="f8914-120">-AgentName</span></span>
<span data-ttu-id="f8914-121">Name des Agents</span><span class="sxs-lookup"><span data-stu-id="f8914-121">The agent name</span></span>

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

### <span data-ttu-id="f8914-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8914-122">-DefaultProfile</span></span>
<span data-ttu-id="f8914-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f8914-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8914-124">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f8914-124">-Description</span></span>
<span data-ttu-id="f8914-125">Die Stellenbeschreibung</span><span class="sxs-lookup"><span data-stu-id="f8914-125">The job description</span></span>

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

### <span data-ttu-id="f8914-126">-Enable</span><span class="sxs-lookup"><span data-stu-id="f8914-126">-Enable</span></span>
<span data-ttu-id="f8914-127">Die Kennzeichnung, die besagt, dass der Kunde diesen Job aktivieren möchte.</span><span class="sxs-lookup"><span data-stu-id="f8914-127">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="f8914-128">-EndTime</span><span class="sxs-lookup"><span data-stu-id="f8914-128">-EndTime</span></span>
<span data-ttu-id="f8914-129">Endzeit des Auftragszeitplans</span><span class="sxs-lookup"><span data-stu-id="f8914-129">The job schedule end time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8914-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f8914-130">-InputObject</span></span>
<span data-ttu-id="f8914-131">Das Auftragseingabe Objekt</span><span class="sxs-lookup"><span data-stu-id="f8914-131">The job input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, RunOnceUsingParentObject, RecurringUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8914-132">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="f8914-132">-IntervalCount</span></span>
<span data-ttu-id="f8914-133">Die Anzahl der wiederkehrenden Zeit Plan Intervalle</span><span class="sxs-lookup"><span data-stu-id="f8914-133">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="f8914-134">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="f8914-134">-IntervalType</span></span>
<span data-ttu-id="f8914-135">Der Typ des periodischen Zeitplanintervalls-kann Minuten, Stunden, Tag, Woche, Monat sein.</span><span class="sxs-lookup"><span data-stu-id="f8914-135">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="f8914-136">-Name</span><span class="sxs-lookup"><span data-stu-id="f8914-136">-Name</span></span>
<span data-ttu-id="f8914-137">Der Name des Auftrags</span><span class="sxs-lookup"><span data-stu-id="f8914-137">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases: JobName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8914-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8914-138">-ResourceGroupName</span></span>
<span data-ttu-id="f8914-139">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f8914-139">The resource group name</span></span>

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

### <span data-ttu-id="f8914-140">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f8914-140">-ResourceId</span></span>
<span data-ttu-id="f8914-141">Die Projekt Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="f8914-141">The job resource id</span></span>

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

### <span data-ttu-id="f8914-142">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="f8914-142">-RunOnce</span></span>
<span data-ttu-id="f8914-143">Das Flag, um anzugeben, dass Job einmal ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="f8914-143">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="f8914-144">-Servername</span><span class="sxs-lookup"><span data-stu-id="f8914-144">-ServerName</span></span>
<span data-ttu-id="f8914-145">Der Servername</span><span class="sxs-lookup"><span data-stu-id="f8914-145">The server name</span></span>

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

### <span data-ttu-id="f8914-146">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="f8914-146">-StartTime</span></span>
<span data-ttu-id="f8914-147">Die Startzeit des Auftragszeitplans</span><span class="sxs-lookup"><span data-stu-id="f8914-147">The job schedule start time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8914-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f8914-148">-Confirm</span></span>
<span data-ttu-id="f8914-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f8914-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8914-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8914-150">-WhatIf</span></span>
<span data-ttu-id="f8914-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f8914-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8914-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8914-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8914-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8914-153">CommonParameters</span></span>
<span data-ttu-id="f8914-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8914-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8914-155">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8914-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8914-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f8914-156">INPUTS</span></span>

### <span data-ttu-id="f8914-157">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="f8914-157">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="f8914-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f8914-158">OUTPUTS</span></span>

### <span data-ttu-id="f8914-159">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="f8914-159">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="f8914-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="f8914-160">NOTES</span></span>

## <span data-ttu-id="f8914-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f8914-161">RELATED LINKS</span></span>
