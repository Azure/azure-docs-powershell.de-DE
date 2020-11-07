---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
ms.openlocfilehash: a53a982e13b84bb401389e5edb5294ef1d094a49
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846600"
---
# <span data-ttu-id="ced53-101">Set-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="ced53-101">Set-AzSqlElasticJob</span></span>

## <span data-ttu-id="ced53-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ced53-102">SYNOPSIS</span></span>
<span data-ttu-id="ced53-103">Aktualisiert einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="ced53-103">Updates a job</span></span>

## <span data-ttu-id="ced53-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ced53-104">SYNTAX</span></span>

### <span data-ttu-id="ced53-105">Standardset (Standard)</span><span class="sxs-lookup"><span data-stu-id="ced53-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ced53-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="ced53-106">RunOnce</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ced53-107">Regelmäßige</span><span class="sxs-lookup"><span data-stu-id="ced53-107">Recurring</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ced53-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="ced53-108">ObjectSet</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ced53-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="ced53-109">RunOnceUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-RunOnce] [-StartTime <DateTime>]
 [-EndTime <DateTime>] [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ced53-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="ced53-110">RecurringUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ced53-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ced53-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ced53-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ced53-112">RunOnceUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ced53-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ced53-113">RecurringUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ced53-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ced53-114">DESCRIPTION</span></span>
<span data-ttu-id="ced53-115">Das Set-AzSqlElasticJob-Cmdlet aktualisiert einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="ced53-115">The Set-AzSqlElasticJob cmdlet updates a job</span></span>

## <span data-ttu-id="ced53-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ced53-116">EXAMPLES</span></span>

### <span data-ttu-id="ced53-117">Beispiel 1: aktualisiert einen Job, um eine Stunde ab jetzt zu beginnen, und wiederholen Sie alle 1 Stunde.</span><span class="sxs-lookup"><span data-stu-id="ced53-117">Example 1 - Updates a job to start an hour from now and repeat every 1 hour</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Set-AzSqlElasticJob -IntervalType Hour -IntervalCount 1 -StartTime (Get-Date).AddHours(1) -Enable

JobName Version Description StartTime            EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------            -------                ------------ -------- -------
job1    0                   6/1/2018 10:50:15 PM 12/31/9999 11:59:59 AM Recurring    PT1H     True
```

<span data-ttu-id="ced53-118">Aktualisiert einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="ced53-118">Updates a job</span></span>

## <span data-ttu-id="ced53-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="ced53-119">PARAMETERS</span></span>

### <span data-ttu-id="ced53-120">-Agentname</span><span class="sxs-lookup"><span data-stu-id="ced53-120">-AgentName</span></span>
<span data-ttu-id="ced53-121">Name des Agents</span><span class="sxs-lookup"><span data-stu-id="ced53-121">The agent name</span></span>

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

### <span data-ttu-id="ced53-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ced53-122">-DefaultProfile</span></span>
<span data-ttu-id="ced53-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ced53-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ced53-124">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ced53-124">-Description</span></span>
<span data-ttu-id="ced53-125">Die Stellenbeschreibung</span><span class="sxs-lookup"><span data-stu-id="ced53-125">The job description</span></span>

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

### <span data-ttu-id="ced53-126">-Enable</span><span class="sxs-lookup"><span data-stu-id="ced53-126">-Enable</span></span>
<span data-ttu-id="ced53-127">Die Kennzeichnung, die besagt, dass der Kunde diesen Job aktivieren möchte.</span><span class="sxs-lookup"><span data-stu-id="ced53-127">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="ced53-128">-EndTime</span><span class="sxs-lookup"><span data-stu-id="ced53-128">-EndTime</span></span>
<span data-ttu-id="ced53-129">Endzeit des Auftragszeitplans</span><span class="sxs-lookup"><span data-stu-id="ced53-129">The job schedule end time</span></span>

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

### <span data-ttu-id="ced53-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ced53-130">-InputObject</span></span>
<span data-ttu-id="ced53-131">Das Auftragseingabe Objekt</span><span class="sxs-lookup"><span data-stu-id="ced53-131">The job input object</span></span>

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

### <span data-ttu-id="ced53-132">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="ced53-132">-IntervalCount</span></span>
<span data-ttu-id="ced53-133">Die Anzahl der wiederkehrenden Zeit Plan Intervalle</span><span class="sxs-lookup"><span data-stu-id="ced53-133">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="ced53-134">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="ced53-134">-IntervalType</span></span>
<span data-ttu-id="ced53-135">Der Typ des periodischen Zeitplanintervalls-kann Minuten, Stunden, Tag, Woche, Monat sein.</span><span class="sxs-lookup"><span data-stu-id="ced53-135">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="ced53-136">-Name</span><span class="sxs-lookup"><span data-stu-id="ced53-136">-Name</span></span>
<span data-ttu-id="ced53-137">Der Name des Auftrags</span><span class="sxs-lookup"><span data-stu-id="ced53-137">The job name</span></span>

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

### <span data-ttu-id="ced53-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ced53-138">-ResourceGroupName</span></span>
<span data-ttu-id="ced53-139">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="ced53-139">The resource group name</span></span>

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

### <span data-ttu-id="ced53-140">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ced53-140">-ResourceId</span></span>
<span data-ttu-id="ced53-141">Die Projekt Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="ced53-141">The job resource id</span></span>

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

### <span data-ttu-id="ced53-142">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="ced53-142">-RunOnce</span></span>
<span data-ttu-id="ced53-143">Das Flag, um anzugeben, dass Job einmal ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="ced53-143">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="ced53-144">-Servername</span><span class="sxs-lookup"><span data-stu-id="ced53-144">-ServerName</span></span>
<span data-ttu-id="ced53-145">Der Servername</span><span class="sxs-lookup"><span data-stu-id="ced53-145">The server name</span></span>

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

### <span data-ttu-id="ced53-146">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="ced53-146">-StartTime</span></span>
<span data-ttu-id="ced53-147">Die Startzeit des Auftragszeitplans</span><span class="sxs-lookup"><span data-stu-id="ced53-147">The job schedule start time</span></span>

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

### <span data-ttu-id="ced53-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ced53-148">-Confirm</span></span>
<span data-ttu-id="ced53-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ced53-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ced53-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ced53-150">-WhatIf</span></span>
<span data-ttu-id="ced53-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ced53-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ced53-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ced53-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ced53-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ced53-153">CommonParameters</span></span>
<span data-ttu-id="ced53-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ced53-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ced53-155">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ced53-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ced53-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ced53-156">INPUTS</span></span>

### <span data-ttu-id="ced53-157">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="ced53-157">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="ced53-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ced53-158">OUTPUTS</span></span>

### <span data-ttu-id="ced53-159">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="ced53-159">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="ced53-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="ced53-160">NOTES</span></span>

## <span data-ttu-id="ced53-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ced53-161">RELATED LINKS</span></span>
