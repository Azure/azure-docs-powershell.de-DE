---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
ms.openlocfilehash: 53bd1b1cd1c2f7ba87df8cb5c27f1b2380db04af
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307592"
---
# <span data-ttu-id="2f2de-101">Set-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="2f2de-101">Set-AzSqlElasticJob</span></span>

## <span data-ttu-id="2f2de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f2de-102">SYNOPSIS</span></span>
<span data-ttu-id="2f2de-103">Aktualisiert einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="2f2de-103">Updates a job</span></span>

## <span data-ttu-id="2f2de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f2de-104">SYNTAX</span></span>

### <span data-ttu-id="2f2de-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2f2de-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f2de-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="2f2de-106">RunOnce</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f2de-107">Recurring</span><span class="sxs-lookup"><span data-stu-id="2f2de-107">Recurring</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f2de-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="2f2de-108">ObjectSet</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f2de-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="2f2de-109">RunOnceUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-RunOnce] [-StartTime <DateTime>]
 [-EndTime <DateTime>] [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f2de-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="2f2de-110">RecurringUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f2de-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2f2de-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f2de-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2f2de-112">RunOnceUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f2de-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2f2de-113">RecurringUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f2de-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2f2de-114">DESCRIPTION</span></span>
<span data-ttu-id="2f2de-115">Das cmdlet Set-AzSqlElasticJob aktualisiert einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="2f2de-115">The Set-AzSqlElasticJob cmdlet updates a job</span></span>

## <span data-ttu-id="2f2de-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2f2de-116">EXAMPLES</span></span>

### <span data-ttu-id="2f2de-117">Beispiel 1: Aktualisiert einen Auftrag so, dass er ab jetzt eine Stunde beginnt, und wird alle 1 Stunde wiederholt.</span><span class="sxs-lookup"><span data-stu-id="2f2de-117">Example 1: Updates a job to start an hour from now and repeat every 1 hour</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Set-AzSqlElasticJob -IntervalType Hour -IntervalCount 1 -StartTime (Get-Date).AddHours(1) -Enable

JobName Version Description StartTime            EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------            -------                ------------ -------- -------
job1    0                   6/1/2018 10:50:15 PM 12/31/9999 11:59:59 AM Recurring    PT1H     True
```

<span data-ttu-id="2f2de-118">Aktualisiert einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="2f2de-118">Updates a job</span></span>

### <span data-ttu-id="2f2de-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2f2de-119">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJob -AgentName agent -Enable -IntervalCount 1 -IntervalType Hour -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1 -StartTime '9/16/2016 11:31:12'
```

## <span data-ttu-id="2f2de-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f2de-120">PARAMETERS</span></span>

### <span data-ttu-id="2f2de-121">-AgentName</span><span class="sxs-lookup"><span data-stu-id="2f2de-121">-AgentName</span></span>
<span data-ttu-id="2f2de-122">Der Agentname</span><span class="sxs-lookup"><span data-stu-id="2f2de-122">The agent name</span></span>

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

### <span data-ttu-id="2f2de-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f2de-123">-DefaultProfile</span></span>
<span data-ttu-id="2f2de-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2f2de-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f2de-125">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f2de-125">-Description</span></span>
<span data-ttu-id="2f2de-126">Stellenbeschreibung</span><span class="sxs-lookup"><span data-stu-id="2f2de-126">The job description</span></span>

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

### <span data-ttu-id="2f2de-127">-Enable</span><span class="sxs-lookup"><span data-stu-id="2f2de-127">-Enable</span></span>
<span data-ttu-id="2f2de-128">Das Kennzeichen, mit dem angegeben wird, dass der Kunde diesen Auftrag aktivieren möchte.</span><span class="sxs-lookup"><span data-stu-id="2f2de-128">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="2f2de-129">-EndTime</span><span class="sxs-lookup"><span data-stu-id="2f2de-129">-EndTime</span></span>
<span data-ttu-id="2f2de-130">Die Endzeit des Auftragsplans</span><span class="sxs-lookup"><span data-stu-id="2f2de-130">The job schedule end time</span></span>

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

### <span data-ttu-id="2f2de-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f2de-131">-InputObject</span></span>
<span data-ttu-id="2f2de-132">Das Auftragseingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="2f2de-132">The job input object</span></span>

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

### <span data-ttu-id="2f2de-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="2f2de-133">-IntervalCount</span></span>
<span data-ttu-id="2f2de-134">Die Anzahl der Periodenintervalle</span><span class="sxs-lookup"><span data-stu-id="2f2de-134">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="2f2de-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="2f2de-135">-IntervalType</span></span>
<span data-ttu-id="2f2de-136">Der Intervalltyp "Terminserie" – Kann "Minute", "Stunde", "Tag", "Woche", "Monat" sein.</span><span class="sxs-lookup"><span data-stu-id="2f2de-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="2f2de-137">-Name</span><span class="sxs-lookup"><span data-stu-id="2f2de-137">-Name</span></span>
<span data-ttu-id="2f2de-138">Der Name des Auftrags</span><span class="sxs-lookup"><span data-stu-id="2f2de-138">The job name</span></span>

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

### <span data-ttu-id="2f2de-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f2de-139">-ResourceGroupName</span></span>
<span data-ttu-id="2f2de-140">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="2f2de-140">The resource group name</span></span>

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

### <span data-ttu-id="2f2de-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f2de-141">-ResourceId</span></span>
<span data-ttu-id="2f2de-142">Die Auftragsressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="2f2de-142">The job resource id</span></span>

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

### <span data-ttu-id="2f2de-143">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="2f2de-143">-RunOnce</span></span>
<span data-ttu-id="2f2de-144">Das Kennzeichen zur Angabe, dass der Auftrag einmal ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="2f2de-144">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="2f2de-145">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2f2de-145">-ServerName</span></span>
<span data-ttu-id="2f2de-146">Der Servername</span><span class="sxs-lookup"><span data-stu-id="2f2de-146">The server name</span></span>

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

### <span data-ttu-id="2f2de-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2f2de-147">-StartTime</span></span>
<span data-ttu-id="2f2de-148">Startzeit des Auftragsplans</span><span class="sxs-lookup"><span data-stu-id="2f2de-148">The job schedule start time</span></span>

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

### <span data-ttu-id="2f2de-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f2de-149">-Confirm</span></span>
<span data-ttu-id="2f2de-150">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2f2de-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f2de-151">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2f2de-151">-WhatIf</span></span>
<span data-ttu-id="2f2de-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2f2de-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f2de-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f2de-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f2de-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f2de-154">CommonParameters</span></span>
<span data-ttu-id="2f2de-155">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f2de-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f2de-156">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f2de-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f2de-157">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2f2de-157">INPUTS</span></span>

### <span data-ttu-id="2f2de-158">Microsoft.Azure.Commands.Sql.FlexibleJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="2f2de-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="2f2de-159">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2f2de-159">OUTPUTS</span></span>

### <span data-ttu-id="2f2de-160">Microsoft.Azure.Commands.Sql.FlexibleJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="2f2de-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="2f2de-161">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2f2de-161">NOTES</span></span>

## <span data-ttu-id="2f2de-162">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2f2de-162">RELATED LINKS</span></span>
