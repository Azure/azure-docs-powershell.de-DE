---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
ms.openlocfilehash: 53bd1b1cd1c2f7ba87df8cb5c27f1b2380db04af
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179797"
---
# <span data-ttu-id="fb6a0-101">Set-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="fb6a0-101">Set-AzSqlElasticJob</span></span>

## <span data-ttu-id="fb6a0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fb6a0-102">SYNOPSIS</span></span>
<span data-ttu-id="fb6a0-103">Aktualisiert einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="fb6a0-103">Updates a job</span></span>

## <span data-ttu-id="fb6a0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb6a0-104">SYNTAX</span></span>

### <span data-ttu-id="fb6a0-105">Standardset (Standard)</span><span class="sxs-lookup"><span data-stu-id="fb6a0-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb6a0-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="fb6a0-106">RunOnce</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb6a0-107">Regelmäßige</span><span class="sxs-lookup"><span data-stu-id="fb6a0-107">Recurring</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb6a0-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="fb6a0-108">ObjectSet</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb6a0-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="fb6a0-109">RunOnceUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-RunOnce] [-StartTime <DateTime>]
 [-EndTime <DateTime>] [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb6a0-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="fb6a0-110">RecurringUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb6a0-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fb6a0-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb6a0-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fb6a0-112">RunOnceUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb6a0-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fb6a0-113">RecurringUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb6a0-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb6a0-114">DESCRIPTION</span></span>
<span data-ttu-id="fb6a0-115">Das Set-AzSqlElasticJob-Cmdlet aktualisiert einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="fb6a0-115">The Set-AzSqlElasticJob cmdlet updates a job</span></span>

## <span data-ttu-id="fb6a0-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fb6a0-116">EXAMPLES</span></span>

### <span data-ttu-id="fb6a0-117">Beispiel 1: aktualisiert einen Job, um eine Stunde ab jetzt zu beginnen, und wiederholen Sie alle 1 Stunde.</span><span class="sxs-lookup"><span data-stu-id="fb6a0-117">Example 1: Updates a job to start an hour from now and repeat every 1 hour</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Set-AzSqlElasticJob -IntervalType Hour -IntervalCount 1 -StartTime (Get-Date).AddHours(1) -Enable

JobName Version Description StartTime            EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------            -------                ------------ -------- -------
job1    0                   6/1/2018 10:50:15 PM 12/31/9999 11:59:59 AM Recurring    PT1H     True
```

<span data-ttu-id="fb6a0-118">Aktualisiert einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="fb6a0-118">Updates a job</span></span>

### <span data-ttu-id="fb6a0-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fb6a0-119">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJob -AgentName agent -Enable -IntervalCount 1 -IntervalType Hour -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1 -StartTime '9/16/2016 11:31:12'
```

## <span data-ttu-id="fb6a0-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb6a0-120">PARAMETERS</span></span>

### <span data-ttu-id="fb6a0-121">-Agentname</span><span class="sxs-lookup"><span data-stu-id="fb6a0-121">-AgentName</span></span>
<span data-ttu-id="fb6a0-122">Name des Agents</span><span class="sxs-lookup"><span data-stu-id="fb6a0-122">The agent name</span></span>

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

### <span data-ttu-id="fb6a0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb6a0-123">-DefaultProfile</span></span>
<span data-ttu-id="fb6a0-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fb6a0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb6a0-125">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb6a0-125">-Description</span></span>
<span data-ttu-id="fb6a0-126">Die Stellenbeschreibung</span><span class="sxs-lookup"><span data-stu-id="fb6a0-126">The job description</span></span>

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

### <span data-ttu-id="fb6a0-127">-Enable</span><span class="sxs-lookup"><span data-stu-id="fb6a0-127">-Enable</span></span>
<span data-ttu-id="fb6a0-128">Die Kennzeichnung, die besagt, dass der Kunde diesen Job aktivieren möchte.</span><span class="sxs-lookup"><span data-stu-id="fb6a0-128">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="fb6a0-129">-EndTime</span><span class="sxs-lookup"><span data-stu-id="fb6a0-129">-EndTime</span></span>
<span data-ttu-id="fb6a0-130">Endzeit des Auftragszeitplans</span><span class="sxs-lookup"><span data-stu-id="fb6a0-130">The job schedule end time</span></span>

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

### <span data-ttu-id="fb6a0-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fb6a0-131">-InputObject</span></span>
<span data-ttu-id="fb6a0-132">Das Auftragseingabe Objekt</span><span class="sxs-lookup"><span data-stu-id="fb6a0-132">The job input object</span></span>

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

### <span data-ttu-id="fb6a0-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="fb6a0-133">-IntervalCount</span></span>
<span data-ttu-id="fb6a0-134">Die Anzahl der wiederkehrenden Zeit Plan Intervalle</span><span class="sxs-lookup"><span data-stu-id="fb6a0-134">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="fb6a0-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="fb6a0-135">-IntervalType</span></span>
<span data-ttu-id="fb6a0-136">Der Typ des periodischen Zeitplanintervalls-kann Minuten, Stunden, Tag, Woche, Monat sein.</span><span class="sxs-lookup"><span data-stu-id="fb6a0-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="fb6a0-137">-Name</span><span class="sxs-lookup"><span data-stu-id="fb6a0-137">-Name</span></span>
<span data-ttu-id="fb6a0-138">Der Name des Auftrags</span><span class="sxs-lookup"><span data-stu-id="fb6a0-138">The job name</span></span>

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

### <span data-ttu-id="fb6a0-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb6a0-139">-ResourceGroupName</span></span>
<span data-ttu-id="fb6a0-140">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="fb6a0-140">The resource group name</span></span>

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

### <span data-ttu-id="fb6a0-141">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="fb6a0-141">-ResourceId</span></span>
<span data-ttu-id="fb6a0-142">Die Projekt Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="fb6a0-142">The job resource id</span></span>

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

### <span data-ttu-id="fb6a0-143">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="fb6a0-143">-RunOnce</span></span>
<span data-ttu-id="fb6a0-144">Das Flag, um anzugeben, dass Job einmal ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="fb6a0-144">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="fb6a0-145">-Servername</span><span class="sxs-lookup"><span data-stu-id="fb6a0-145">-ServerName</span></span>
<span data-ttu-id="fb6a0-146">Der Servername</span><span class="sxs-lookup"><span data-stu-id="fb6a0-146">The server name</span></span>

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

### <span data-ttu-id="fb6a0-147">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="fb6a0-147">-StartTime</span></span>
<span data-ttu-id="fb6a0-148">Die Startzeit des Auftragszeitplans</span><span class="sxs-lookup"><span data-stu-id="fb6a0-148">The job schedule start time</span></span>

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

### <span data-ttu-id="fb6a0-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fb6a0-149">-Confirm</span></span>
<span data-ttu-id="fb6a0-150">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fb6a0-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb6a0-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb6a0-151">-WhatIf</span></span>
<span data-ttu-id="fb6a0-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fb6a0-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb6a0-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fb6a0-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb6a0-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb6a0-154">CommonParameters</span></span>
<span data-ttu-id="fb6a0-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb6a0-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb6a0-156">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb6a0-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb6a0-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fb6a0-157">INPUTS</span></span>

### <span data-ttu-id="fb6a0-158">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="fb6a0-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="fb6a0-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fb6a0-159">OUTPUTS</span></span>

### <span data-ttu-id="fb6a0-160">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="fb6a0-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="fb6a0-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="fb6a0-161">NOTES</span></span>

## <span data-ttu-id="fb6a0-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fb6a0-162">RELATED LINKS</span></span>
