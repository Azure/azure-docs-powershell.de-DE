---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
ms.openlocfilehash: 7e1c03b176974c85802451980df24f5a7fdf9b1d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825859"
---
# <span data-ttu-id="2f74b-101">Set-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="2f74b-101">Set-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="2f74b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2f74b-102">SYNOPSIS</span></span>
<span data-ttu-id="2f74b-103">Aktualisiert einen Auftragsschritt</span><span class="sxs-lookup"><span data-stu-id="2f74b-103">Updates a job step</span></span>

## <span data-ttu-id="2f74b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f74b-104">SYNTAX</span></span>

### <span data-ttu-id="2f74b-105">Standardset (Standard)</span><span class="sxs-lookup"><span data-stu-id="2f74b-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f74b-106">WithRemoveOutput</span><span class="sxs-lookup"><span data-stu-id="2f74b-106">WithRemoveOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-RemoveOutput] [-TargetGroupName <String>] [-CredentialName <String>]
 [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f74b-107">WithAddOutput</span><span class="sxs-lookup"><span data-stu-id="2f74b-107">WithAddOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -OutputDatabaseResourceId <String> [-OutputCredentialName <String>]
 [-OutputTableName <String>] [-OutputSchemaName <String>] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f74b-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="2f74b-108">ObjectSet</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-OutputDatabaseObject <AzureSqlDatabaseModel>] [-OutputCredentialName <String>] [-OutputTableName <String>]
 [-OutputSchemaName <String>] [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f74b-109">WithRemoveOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="2f74b-109">WithRemoveOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> [-RemoveOutput]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f74b-110">WithAddOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="2f74b-110">WithAddOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f74b-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2f74b-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f74b-112">WithRemoveOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2f74b-112">WithRemoveOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-RemoveOutput] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f74b-113">WithAddOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2f74b-113">WithAddOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f74b-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f74b-114">DESCRIPTION</span></span>
<span data-ttu-id="2f74b-115">Das Set-AzSqlElasticJobStep-Cmdlet aktualisiert einen Auftragsschritt</span><span class="sxs-lookup"><span data-stu-id="2f74b-115">The Set-AzSqlElasticJobStep cmdlet updates a job step</span></span>

## <span data-ttu-id="2f74b-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2f74b-116">EXAMPLES</span></span>

### <span data-ttu-id="2f74b-117">Beispiel 1 – aktualisiert die Zielgruppe eines Auftragsschritts für einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="2f74b-117">Example 1 - Updates a job step's target group for a job</span></span>
```
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -TargetGroupName tg2

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg2             cred1                 (43200,10,1,120,2) SELECT 1
```

### <span data-ttu-id="2f74b-118">Beispiel 2 – aktualisiert das T-SQL-Skript eines Auftragsschritts für einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="2f74b-118">Example 2 - Updates a job step's T-SQL script for a job</span></span>
```
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -CommandText "SELECT 2"

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 2
```

<span data-ttu-id="2f74b-119">Aktualisiert einen Auftragsschritt aus einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="2f74b-119">Updates a job step from a job</span></span>

## <span data-ttu-id="2f74b-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f74b-120">PARAMETERS</span></span>

### <span data-ttu-id="2f74b-121">-Agentname</span><span class="sxs-lookup"><span data-stu-id="2f74b-121">-AgentName</span></span>
<span data-ttu-id="2f74b-122">Name des Agents</span><span class="sxs-lookup"><span data-stu-id="2f74b-122">The agent name</span></span>

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

### <span data-ttu-id="2f74b-123">-CommandText</span><span class="sxs-lookup"><span data-stu-id="2f74b-123">-CommandText</span></span>
<span data-ttu-id="2f74b-124">Der Befehlstext</span><span class="sxs-lookup"><span data-stu-id="2f74b-124">The command text</span></span>

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

### <span data-ttu-id="2f74b-125">-Credentialname</span><span class="sxs-lookup"><span data-stu-id="2f74b-125">-CredentialName</span></span>
<span data-ttu-id="2f74b-126">Der Anmeldeinformationsname</span><span class="sxs-lookup"><span data-stu-id="2f74b-126">The credential name</span></span>

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

### <span data-ttu-id="2f74b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f74b-127">-DefaultProfile</span></span>
<span data-ttu-id="2f74b-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2f74b-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f74b-129">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="2f74b-129">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="2f74b-130">Das anfängliche Wiederholungsintervall für Sekunden</span><span class="sxs-lookup"><span data-stu-id="2f74b-130">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="2f74b-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2f74b-131">-InputObject</span></span>
<span data-ttu-id="2f74b-132">Das Auftragsschritt Objekt</span><span class="sxs-lookup"><span data-stu-id="2f74b-132">The job step object</span></span>

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

### <span data-ttu-id="2f74b-133">-Jobname</span><span class="sxs-lookup"><span data-stu-id="2f74b-133">-JobName</span></span>
<span data-ttu-id="2f74b-134">Der Name des Auftrags</span><span class="sxs-lookup"><span data-stu-id="2f74b-134">The job name</span></span>

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

### <span data-ttu-id="2f74b-135">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="2f74b-135">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="2f74b-136">Das maximale Wiederholungsintervall für Sekunden</span><span class="sxs-lookup"><span data-stu-id="2f74b-136">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="2f74b-137">-Name</span><span class="sxs-lookup"><span data-stu-id="2f74b-137">-Name</span></span>
<span data-ttu-id="2f74b-138">Der Schrittname</span><span class="sxs-lookup"><span data-stu-id="2f74b-138">The step name</span></span>

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

### <span data-ttu-id="2f74b-139">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="2f74b-139">-OutputCredentialName</span></span>
<span data-ttu-id="2f74b-140">Der Name der Ausgabe Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="2f74b-140">The output credential name</span></span>

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

### <span data-ttu-id="2f74b-141">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="2f74b-141">-OutputDatabaseObject</span></span>
<span data-ttu-id="2f74b-142">Das Ausgabedaten Bank Objekt</span><span class="sxs-lookup"><span data-stu-id="2f74b-142">The output database object</span></span>

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

### <span data-ttu-id="2f74b-143">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="2f74b-143">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="2f74b-144">Die Ressourcen-ID der Ausgabedatenbank</span><span class="sxs-lookup"><span data-stu-id="2f74b-144">The output database resource id</span></span>

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

### <span data-ttu-id="2f74b-145">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="2f74b-145">-OutputSchemaName</span></span>
<span data-ttu-id="2f74b-146">Name des Ausgabe Schemas</span><span class="sxs-lookup"><span data-stu-id="2f74b-146">The output schema name</span></span>

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

### <span data-ttu-id="2f74b-147">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="2f74b-147">-OutputTableName</span></span>
<span data-ttu-id="2f74b-148">Der Name der Ausgabetabelle</span><span class="sxs-lookup"><span data-stu-id="2f74b-148">The output table name</span></span>

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

### <span data-ttu-id="2f74b-149">-RemoveOutput</span><span class="sxs-lookup"><span data-stu-id="2f74b-149">-RemoveOutput</span></span>
<span data-ttu-id="2f74b-150">Das Flag, um anzugeben, ob die Ausgabe entfernt werden soll</span><span class="sxs-lookup"><span data-stu-id="2f74b-150">The flag to indicate whether to remove output</span></span>

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

### <span data-ttu-id="2f74b-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f74b-151">-ResourceGroupName</span></span>
<span data-ttu-id="2f74b-152">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="2f74b-152">The resource group name</span></span>

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

### <span data-ttu-id="2f74b-153">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2f74b-153">-ResourceId</span></span>
<span data-ttu-id="2f74b-154">Die Ressourcen-ID des Auftragsschritts</span><span class="sxs-lookup"><span data-stu-id="2f74b-154">The job step resource id</span></span>

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

### <span data-ttu-id="2f74b-155">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="2f74b-155">-RetryAttempts</span></span>
<span data-ttu-id="2f74b-156">Der Retry-versucht</span><span class="sxs-lookup"><span data-stu-id="2f74b-156">The retry attemps</span></span>

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

### <span data-ttu-id="2f74b-157">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="2f74b-157">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="2f74b-158">Das Wiederholungsintervall Backoff-Multiplikator</span><span class="sxs-lookup"><span data-stu-id="2f74b-158">The retry interval backoff multiplier</span></span>

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

### <span data-ttu-id="2f74b-159">-Servername</span><span class="sxs-lookup"><span data-stu-id="2f74b-159">-ServerName</span></span>
<span data-ttu-id="2f74b-160">Der Servername</span><span class="sxs-lookup"><span data-stu-id="2f74b-160">The server name</span></span>

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

### <span data-ttu-id="2f74b-161">-Schritt-für-Schritt-Nr</span><span class="sxs-lookup"><span data-stu-id="2f74b-161">-StepId</span></span>
<span data-ttu-id="2f74b-162">Der Schritt-ID-Text</span><span class="sxs-lookup"><span data-stu-id="2f74b-162">The step id text</span></span>

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

### <span data-ttu-id="2f74b-163">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="2f74b-163">-TargetGroupName</span></span>
<span data-ttu-id="2f74b-164">Der Name der Zielgruppe</span><span class="sxs-lookup"><span data-stu-id="2f74b-164">The target group name</span></span>

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

### <span data-ttu-id="2f74b-165">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="2f74b-165">-TimeoutSeconds</span></span>
<span data-ttu-id="2f74b-166">Die Timeout Sekunden</span><span class="sxs-lookup"><span data-stu-id="2f74b-166">The timeout seconds</span></span>

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

### <span data-ttu-id="2f74b-167">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2f74b-167">-Confirm</span></span>
<span data-ttu-id="2f74b-168">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2f74b-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f74b-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f74b-169">-WhatIf</span></span>
<span data-ttu-id="2f74b-170">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2f74b-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f74b-171">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f74b-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f74b-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f74b-172">CommonParameters</span></span>
<span data-ttu-id="2f74b-173">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f74b-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f74b-174">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f74b-174">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f74b-175">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2f74b-175">INPUTS</span></span>

### <span data-ttu-id="2f74b-176">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="2f74b-176">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="2f74b-177">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2f74b-177">OUTPUTS</span></span>

### <span data-ttu-id="2f74b-178">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="2f74b-178">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="2f74b-179">Notizen</span><span class="sxs-lookup"><span data-stu-id="2f74b-179">NOTES</span></span>

## <span data-ttu-id="2f74b-180">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2f74b-180">RELATED LINKS</span></span>
