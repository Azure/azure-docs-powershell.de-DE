---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: e6853c3b4fa32a10e93ee281aab0b97755403671
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290663"
---
# <span data-ttu-id="4259e-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="4259e-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="4259e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4259e-102">SYNOPSIS</span></span>
<span data-ttu-id="4259e-103">Erstellt einen neuen Auftrag</span><span class="sxs-lookup"><span data-stu-id="4259e-103">Creates a new job</span></span>

## <span data-ttu-id="4259e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4259e-104">SYNTAX</span></span>

### <span data-ttu-id="4259e-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4259e-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4259e-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="4259e-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4259e-107">Recurring</span><span class="sxs-lookup"><span data-stu-id="4259e-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4259e-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="4259e-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4259e-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="4259e-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4259e-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="4259e-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4259e-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4259e-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4259e-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4259e-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4259e-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4259e-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4259e-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4259e-114">DESCRIPTION</span></span>
<span data-ttu-id="4259e-115">Das New-AzSqlElasticJob erstellt einen neuen Auftrag</span><span class="sxs-lookup"><span data-stu-id="4259e-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="4259e-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4259e-116">EXAMPLES</span></span>

### <span data-ttu-id="4259e-117">Beispiel 1: Erstellt einen neuen Auftrag</span><span class="sxs-lookup"><span data-stu-id="4259e-117">Example 1: Creates a new job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="4259e-118">Erstellt einen neuen Auftrag</span><span class="sxs-lookup"><span data-stu-id="4259e-118">Creates a new job</span></span>

### <span data-ttu-id="4259e-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4259e-119">Example 2</span></span>

<span data-ttu-id="4259e-120">Erstellt einen neuen Auftrag.</span><span class="sxs-lookup"><span data-stu-id="4259e-120">Creates a new job.</span></span> <span data-ttu-id="4259e-121">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="4259e-121">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticJob -Name job1 -RunOnce
```

## <span data-ttu-id="4259e-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4259e-122">PARAMETERS</span></span>

### <span data-ttu-id="4259e-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="4259e-123">-AgentName</span></span>
<span data-ttu-id="4259e-124">Der Agentname</span><span class="sxs-lookup"><span data-stu-id="4259e-124">The agent name</span></span>

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

### <span data-ttu-id="4259e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4259e-125">-DefaultProfile</span></span>
<span data-ttu-id="4259e-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4259e-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4259e-127">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4259e-127">-Description</span></span>
<span data-ttu-id="4259e-128">Stellenbeschreibung</span><span class="sxs-lookup"><span data-stu-id="4259e-128">The job description</span></span>

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

### <span data-ttu-id="4259e-129">-Enable</span><span class="sxs-lookup"><span data-stu-id="4259e-129">-Enable</span></span>
<span data-ttu-id="4259e-130">Das Kennzeichen, mit dem angegeben wird, dass der Kunde diesen Auftrag aktivieren möchte.</span><span class="sxs-lookup"><span data-stu-id="4259e-130">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="4259e-131">-EndTime</span><span class="sxs-lookup"><span data-stu-id="4259e-131">-EndTime</span></span>
<span data-ttu-id="4259e-132">Die Endzeit des Auftragsplans</span><span class="sxs-lookup"><span data-stu-id="4259e-132">The job schedule end time</span></span>

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

### <span data-ttu-id="4259e-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="4259e-133">-IntervalCount</span></span>
<span data-ttu-id="4259e-134">Die Anzahl der Periodenintervalle</span><span class="sxs-lookup"><span data-stu-id="4259e-134">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="4259e-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="4259e-135">-IntervalType</span></span>
<span data-ttu-id="4259e-136">Der Intervalltyp "Terminserie" – Kann "Minute", "Stunde", "Tag", "Woche", "Monat" sein.</span><span class="sxs-lookup"><span data-stu-id="4259e-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="4259e-137">-Name</span><span class="sxs-lookup"><span data-stu-id="4259e-137">-Name</span></span>
<span data-ttu-id="4259e-138">Der Name des Auftrags</span><span class="sxs-lookup"><span data-stu-id="4259e-138">The job name</span></span>

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

### <span data-ttu-id="4259e-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4259e-139">-ParentObject</span></span>
<span data-ttu-id="4259e-140">Das Agenteingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="4259e-140">The agent input object</span></span>

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

### <span data-ttu-id="4259e-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4259e-141">-ParentResourceId</span></span>
<span data-ttu-id="4259e-142">Die Agentressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="4259e-142">The agent resource id</span></span>

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

### <span data-ttu-id="4259e-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4259e-143">-ResourceGroupName</span></span>
<span data-ttu-id="4259e-144">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="4259e-144">The resource group name</span></span>

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

### <span data-ttu-id="4259e-145">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="4259e-145">-RunOnce</span></span>
<span data-ttu-id="4259e-146">Das Kennzeichen zur Angabe, dass der Auftrag einmal ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="4259e-146">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="4259e-147">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4259e-147">-ServerName</span></span>
<span data-ttu-id="4259e-148">Der Servername</span><span class="sxs-lookup"><span data-stu-id="4259e-148">The server name</span></span>

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

### <span data-ttu-id="4259e-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4259e-149">-StartTime</span></span>
<span data-ttu-id="4259e-150">Startzeit des Auftragsplans</span><span class="sxs-lookup"><span data-stu-id="4259e-150">The job schedule start time</span></span>

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

### <span data-ttu-id="4259e-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4259e-151">-Confirm</span></span>
<span data-ttu-id="4259e-152">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4259e-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4259e-153">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4259e-153">-WhatIf</span></span>
<span data-ttu-id="4259e-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4259e-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4259e-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4259e-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4259e-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4259e-156">CommonParameters</span></span>
<span data-ttu-id="4259e-157">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4259e-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4259e-158">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4259e-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4259e-159">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4259e-159">INPUTS</span></span>

### <span data-ttu-id="4259e-160">Microsoft.Azure.Commands.Sql.AgentJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="4259e-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="4259e-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4259e-161">OUTPUTS</span></span>

### <span data-ttu-id="4259e-162">Microsoft.Azure.Commands.Sql.BenchmarkJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="4259e-162">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="4259e-163">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4259e-163">NOTES</span></span>

## <span data-ttu-id="4259e-164">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4259e-164">RELATED LINKS</span></span>
