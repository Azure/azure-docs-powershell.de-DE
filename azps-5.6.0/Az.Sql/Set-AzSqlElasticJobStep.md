---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/set-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
ms.openlocfilehash: ec2f9174cc0ca8781b56784836a4583b0568128e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933395"
---
# <span data-ttu-id="9167f-101">Set-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="9167f-101">Set-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="9167f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9167f-102">SYNOPSIS</span></span>
<span data-ttu-id="9167f-103">Aktualisiert einen Auftragsschritt</span><span class="sxs-lookup"><span data-stu-id="9167f-103">Updates a job step</span></span>

## <span data-ttu-id="9167f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9167f-104">SYNTAX</span></span>

### <span data-ttu-id="9167f-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9167f-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9167f-106">WithRemoveOutput</span><span class="sxs-lookup"><span data-stu-id="9167f-106">WithRemoveOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-RemoveOutput] [-TargetGroupName <String>] [-CredentialName <String>]
 [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9167f-107">WithAddOutput</span><span class="sxs-lookup"><span data-stu-id="9167f-107">WithAddOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -OutputDatabaseResourceId <String> [-OutputCredentialName <String>]
 [-OutputTableName <String>] [-OutputSchemaName <String>] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9167f-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="9167f-108">ObjectSet</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-OutputDatabaseObject <AzureSqlDatabaseModel>] [-OutputCredentialName <String>] [-OutputTableName <String>]
 [-OutputSchemaName <String>] [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9167f-109">WithRemoveOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="9167f-109">WithRemoveOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> [-RemoveOutput]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9167f-110">WithAddOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="9167f-110">WithAddOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9167f-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9167f-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9167f-112">WithRemoveOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9167f-112">WithRemoveOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-RemoveOutput] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9167f-113">WithAddOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9167f-113">WithAddOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9167f-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9167f-114">DESCRIPTION</span></span>
<span data-ttu-id="9167f-115">Das Set-AzSqlElasticJobStep cmdlet aktualisiert einen Auftragsschritt</span><span class="sxs-lookup"><span data-stu-id="9167f-115">The Set-AzSqlElasticJobStep cmdlet updates a job step</span></span>

## <span data-ttu-id="9167f-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9167f-116">EXAMPLES</span></span>

### <span data-ttu-id="9167f-117">Beispiel 1: Aktualisiert die Zielgruppe eines Auftragsschritts für einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="9167f-117">Example 1: Updates a job step's target group for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -TargetGroupName tg2

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg2             cred1                 (43200,10,1,120,2) SELECT 1
```

### <span data-ttu-id="9167f-118">Beispiel 2: Aktualisiert das T-SQL eines Auftragsschritts für einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="9167f-118">Example 2: Updates a job step's T-SQL script for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -CommandText "SELECT 2"

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 2
```

<span data-ttu-id="9167f-119">Aktualisiert einen Auftragsschritt aus einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="9167f-119">Updates a job step from a job</span></span>

### <span data-ttu-id="9167f-120">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="9167f-120">Example 3</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJobStep -AgentName agent -CommandText 'SELECT 2' -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="9167f-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9167f-121">PARAMETERS</span></span>

### <span data-ttu-id="9167f-122">-AgentName</span><span class="sxs-lookup"><span data-stu-id="9167f-122">-AgentName</span></span>
<span data-ttu-id="9167f-123">Der Agentname</span><span class="sxs-lookup"><span data-stu-id="9167f-123">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9167f-124">-CommandText</span><span class="sxs-lookup"><span data-stu-id="9167f-124">-CommandText</span></span>
<span data-ttu-id="9167f-125">Der Befehlstext</span><span class="sxs-lookup"><span data-stu-id="9167f-125">The command text</span></span>

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

### <span data-ttu-id="9167f-126">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="9167f-126">-CredentialName</span></span>
<span data-ttu-id="9167f-127">Der Name der Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="9167f-127">The credential name</span></span>

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

### <span data-ttu-id="9167f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9167f-128">-DefaultProfile</span></span>
<span data-ttu-id="9167f-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9167f-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9167f-130">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="9167f-130">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="9167f-131">Die ersten Sekunden des Wiederholungsintervalls</span><span class="sxs-lookup"><span data-stu-id="9167f-131">The initial retry interval seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9167f-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9167f-132">-InputObject</span></span>
<span data-ttu-id="9167f-133">Das Auftragsschrittobjekt</span><span class="sxs-lookup"><span data-stu-id="9167f-133">The job step object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel
Parameter Sets: ObjectSet, WithRemoveOutputUsingParentObject, WithAddOutputUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9167f-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="9167f-134">-JobName</span></span>
<span data-ttu-id="9167f-135">Der Auftragsname</span><span class="sxs-lookup"><span data-stu-id="9167f-135">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9167f-136">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="9167f-136">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="9167f-137">Das maximale Wiederholungsintervall (Sekunden)</span><span class="sxs-lookup"><span data-stu-id="9167f-137">The maximum retry interval seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9167f-138">-Name</span><span class="sxs-lookup"><span data-stu-id="9167f-138">-Name</span></span>
<span data-ttu-id="9167f-139">Der Schrittname</span><span class="sxs-lookup"><span data-stu-id="9167f-139">The step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9167f-140">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="9167f-140">-OutputCredentialName</span></span>
<span data-ttu-id="9167f-141">Der Name der Ausgabeanmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="9167f-141">The output credential name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithAddOutput, ObjectSet, WithAddOutputUsingParentObject, ResourceIdSet, WithAddOutputUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9167f-142">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="9167f-142">-OutputDatabaseObject</span></span>
<span data-ttu-id="9167f-143">Das Ausgabedatenbankobjekt</span><span class="sxs-lookup"><span data-stu-id="9167f-143">The output database object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9167f-144">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="9167f-144">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="9167f-145">Die Ressourcen-ID der Ausgabedatenbank</span><span class="sxs-lookup"><span data-stu-id="9167f-145">The output database resource id</span></span>

```yaml
Type: System.String
Parameter Sets: WithAddOutput, WithAddOutputUsingParentObject, WithAddOutputUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9167f-146">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="9167f-146">-OutputSchemaName</span></span>
<span data-ttu-id="9167f-147">Der Name des Ausgabeschemas</span><span class="sxs-lookup"><span data-stu-id="9167f-147">The output schema name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithAddOutput, ObjectSet, WithAddOutputUsingParentObject, ResourceIdSet, WithAddOutputUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9167f-148">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="9167f-148">-OutputTableName</span></span>
<span data-ttu-id="9167f-149">Der Name der Ausgabetabelle</span><span class="sxs-lookup"><span data-stu-id="9167f-149">The output table name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithAddOutput, ObjectSet, WithAddOutputUsingParentObject, ResourceIdSet, WithAddOutputUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9167f-150">-RemoveOutput</span><span class="sxs-lookup"><span data-stu-id="9167f-150">-RemoveOutput</span></span>
<span data-ttu-id="9167f-151">Das Flag, das angibt, ob die Ausgabe entfernt werden soll</span><span class="sxs-lookup"><span data-stu-id="9167f-151">The flag to indicate whether to remove output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WithRemoveOutput, WithRemoveOutputUsingParentObject, WithRemoveOutputUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9167f-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9167f-152">-ResourceGroupName</span></span>
<span data-ttu-id="9167f-153">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="9167f-153">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9167f-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9167f-154">-ResourceId</span></span>
<span data-ttu-id="9167f-155">Ressourcen-ID des Auftragsschritts</span><span class="sxs-lookup"><span data-stu-id="9167f-155">The job step resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithRemoveOutputUsingParentResourceId, WithAddOutputUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9167f-156">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="9167f-156">-RetryAttempts</span></span>
<span data-ttu-id="9167f-157">Die Wiederholungsversuche</span><span class="sxs-lookup"><span data-stu-id="9167f-157">The retry attemps</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9167f-158">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="9167f-158">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="9167f-159">Der Wiederholungsintervall-Backoff-Multiplikator</span><span class="sxs-lookup"><span data-stu-id="9167f-159">The retry interval backoff multiplier</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9167f-160">-Servername</span><span class="sxs-lookup"><span data-stu-id="9167f-160">-ServerName</span></span>
<span data-ttu-id="9167f-161">Der Servername</span><span class="sxs-lookup"><span data-stu-id="9167f-161">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9167f-162">-StepId</span><span class="sxs-lookup"><span data-stu-id="9167f-162">-StepId</span></span>
<span data-ttu-id="9167f-163">Der Schritt-ID-Text</span><span class="sxs-lookup"><span data-stu-id="9167f-163">The step id text</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9167f-164">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="9167f-164">-TargetGroupName</span></span>
<span data-ttu-id="9167f-165">Der Name der Zielgruppe</span><span class="sxs-lookup"><span data-stu-id="9167f-165">The target group name</span></span>

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

### <span data-ttu-id="9167f-166">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="9167f-166">-TimeoutSeconds</span></span>
<span data-ttu-id="9167f-167">Die Timeoutsekunden</span><span class="sxs-lookup"><span data-stu-id="9167f-167">The timeout seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9167f-168">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9167f-168">-Confirm</span></span>
<span data-ttu-id="9167f-169">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9167f-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9167f-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9167f-170">-WhatIf</span></span>
<span data-ttu-id="9167f-171">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9167f-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9167f-172">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9167f-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9167f-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9167f-173">CommonParameters</span></span>
<span data-ttu-id="9167f-174">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9167f-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9167f-175">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9167f-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9167f-176">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9167f-176">INPUTS</span></span>

### <span data-ttu-id="9167f-177">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="9167f-177">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="9167f-178">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9167f-178">OUTPUTS</span></span>

### <span data-ttu-id="9167f-179">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="9167f-179">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="9167f-180">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9167f-180">NOTES</span></span>

## <span data-ttu-id="9167f-181">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9167f-181">RELATED LINKS</span></span>
