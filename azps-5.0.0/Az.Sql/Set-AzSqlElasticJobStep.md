---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
ms.openlocfilehash: 4f6f0471224799e818f9db29e5be5a4c49f9c45e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302986"
---
# <span data-ttu-id="2bd1c-101">Set-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="2bd1c-101">Set-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="2bd1c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2bd1c-102">SYNOPSIS</span></span>
<span data-ttu-id="2bd1c-103">Aktualisiert einen Auftragsschritt</span><span class="sxs-lookup"><span data-stu-id="2bd1c-103">Updates a job step</span></span>

## <span data-ttu-id="2bd1c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bd1c-104">SYNTAX</span></span>

### <span data-ttu-id="2bd1c-105">Standardset (Standard)</span><span class="sxs-lookup"><span data-stu-id="2bd1c-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bd1c-106">WithRemoveOutput</span><span class="sxs-lookup"><span data-stu-id="2bd1c-106">WithRemoveOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-RemoveOutput] [-TargetGroupName <String>] [-CredentialName <String>]
 [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2bd1c-107">WithAddOutput</span><span class="sxs-lookup"><span data-stu-id="2bd1c-107">WithAddOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -OutputDatabaseResourceId <String> [-OutputCredentialName <String>]
 [-OutputTableName <String>] [-OutputSchemaName <String>] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2bd1c-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="2bd1c-108">ObjectSet</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-OutputDatabaseObject <AzureSqlDatabaseModel>] [-OutputCredentialName <String>] [-OutputTableName <String>]
 [-OutputSchemaName <String>] [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bd1c-109">WithRemoveOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="2bd1c-109">WithRemoveOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> [-RemoveOutput]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bd1c-110">WithAddOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="2bd1c-110">WithAddOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bd1c-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2bd1c-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bd1c-112">WithRemoveOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2bd1c-112">WithRemoveOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-RemoveOutput] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2bd1c-113">WithAddOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2bd1c-113">WithAddOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bd1c-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2bd1c-114">DESCRIPTION</span></span>
<span data-ttu-id="2bd1c-115">Das Set-AzSqlElasticJobStep-Cmdlet aktualisiert einen Auftragsschritt</span><span class="sxs-lookup"><span data-stu-id="2bd1c-115">The Set-AzSqlElasticJobStep cmdlet updates a job step</span></span>

## <span data-ttu-id="2bd1c-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2bd1c-116">EXAMPLES</span></span>

### <span data-ttu-id="2bd1c-117">Beispiel 1: Aktualisieren der Zielgruppe eines Auftragsschritts für einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="2bd1c-117">Example 1: Updates a job step's target group for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -TargetGroupName tg2

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg2             cred1                 (43200,10,1,120,2) SELECT 1
```

### <span data-ttu-id="2bd1c-118">Beispiel 2: aktualisiert das T-SQL-Skript eines Auftragsschritts für einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="2bd1c-118">Example 2: Updates a job step's T-SQL script for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -CommandText "SELECT 2"

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 2
```

<span data-ttu-id="2bd1c-119">Aktualisiert einen Auftragsschritt aus einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="2bd1c-119">Updates a job step from a job</span></span>

### <span data-ttu-id="2bd1c-120">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="2bd1c-120">Example 3</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJobStep -AgentName agent -CommandText 'SELECT 2' -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="2bd1c-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="2bd1c-121">PARAMETERS</span></span>

### <span data-ttu-id="2bd1c-122">-Agentname</span><span class="sxs-lookup"><span data-stu-id="2bd1c-122">-AgentName</span></span>
<span data-ttu-id="2bd1c-123">Name des Agents</span><span class="sxs-lookup"><span data-stu-id="2bd1c-123">The agent name</span></span>

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

### <span data-ttu-id="2bd1c-124">-CommandText</span><span class="sxs-lookup"><span data-stu-id="2bd1c-124">-CommandText</span></span>
<span data-ttu-id="2bd1c-125">Der Befehlstext</span><span class="sxs-lookup"><span data-stu-id="2bd1c-125">The command text</span></span>

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

### <span data-ttu-id="2bd1c-126">-Credentialname</span><span class="sxs-lookup"><span data-stu-id="2bd1c-126">-CredentialName</span></span>
<span data-ttu-id="2bd1c-127">Der Anmeldeinformationsname</span><span class="sxs-lookup"><span data-stu-id="2bd1c-127">The credential name</span></span>

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

### <span data-ttu-id="2bd1c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bd1c-128">-DefaultProfile</span></span>
<span data-ttu-id="2bd1c-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bd1c-130">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="2bd1c-130">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="2bd1c-131">Das anfängliche Wiederholungsintervall für Sekunden</span><span class="sxs-lookup"><span data-stu-id="2bd1c-131">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="2bd1c-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2bd1c-132">-InputObject</span></span>
<span data-ttu-id="2bd1c-133">Das Auftragsschritt Objekt</span><span class="sxs-lookup"><span data-stu-id="2bd1c-133">The job step object</span></span>

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

### <span data-ttu-id="2bd1c-134">-Jobname</span><span class="sxs-lookup"><span data-stu-id="2bd1c-134">-JobName</span></span>
<span data-ttu-id="2bd1c-135">Der Name des Auftrags</span><span class="sxs-lookup"><span data-stu-id="2bd1c-135">The job name</span></span>

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

### <span data-ttu-id="2bd1c-136">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="2bd1c-136">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="2bd1c-137">Das maximale Wiederholungsintervall für Sekunden</span><span class="sxs-lookup"><span data-stu-id="2bd1c-137">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="2bd1c-138">-Name</span><span class="sxs-lookup"><span data-stu-id="2bd1c-138">-Name</span></span>
<span data-ttu-id="2bd1c-139">Der Schrittname</span><span class="sxs-lookup"><span data-stu-id="2bd1c-139">The step name</span></span>

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

### <span data-ttu-id="2bd1c-140">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="2bd1c-140">-OutputCredentialName</span></span>
<span data-ttu-id="2bd1c-141">Der Name der Ausgabe Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="2bd1c-141">The output credential name</span></span>

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

### <span data-ttu-id="2bd1c-142">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="2bd1c-142">-OutputDatabaseObject</span></span>
<span data-ttu-id="2bd1c-143">Das Ausgabedaten Bank Objekt</span><span class="sxs-lookup"><span data-stu-id="2bd1c-143">The output database object</span></span>

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

### <span data-ttu-id="2bd1c-144">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="2bd1c-144">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="2bd1c-145">Die Ressourcen-ID der Ausgabedatenbank</span><span class="sxs-lookup"><span data-stu-id="2bd1c-145">The output database resource id</span></span>

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

### <span data-ttu-id="2bd1c-146">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="2bd1c-146">-OutputSchemaName</span></span>
<span data-ttu-id="2bd1c-147">Name des Ausgabe Schemas</span><span class="sxs-lookup"><span data-stu-id="2bd1c-147">The output schema name</span></span>

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

### <span data-ttu-id="2bd1c-148">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="2bd1c-148">-OutputTableName</span></span>
<span data-ttu-id="2bd1c-149">Der Name der Ausgabetabelle</span><span class="sxs-lookup"><span data-stu-id="2bd1c-149">The output table name</span></span>

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

### <span data-ttu-id="2bd1c-150">-RemoveOutput</span><span class="sxs-lookup"><span data-stu-id="2bd1c-150">-RemoveOutput</span></span>
<span data-ttu-id="2bd1c-151">Das Flag, um anzugeben, ob die Ausgabe entfernt werden soll</span><span class="sxs-lookup"><span data-stu-id="2bd1c-151">The flag to indicate whether to remove output</span></span>

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

### <span data-ttu-id="2bd1c-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bd1c-152">-ResourceGroupName</span></span>
<span data-ttu-id="2bd1c-153">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="2bd1c-153">The resource group name</span></span>

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

### <span data-ttu-id="2bd1c-154">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2bd1c-154">-ResourceId</span></span>
<span data-ttu-id="2bd1c-155">Die Ressourcen-ID des Auftragsschritts</span><span class="sxs-lookup"><span data-stu-id="2bd1c-155">The job step resource id</span></span>

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

### <span data-ttu-id="2bd1c-156">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="2bd1c-156">-RetryAttempts</span></span>
<span data-ttu-id="2bd1c-157">Der Retry-versucht</span><span class="sxs-lookup"><span data-stu-id="2bd1c-157">The retry attemps</span></span>

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

### <span data-ttu-id="2bd1c-158">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="2bd1c-158">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="2bd1c-159">Das Wiederholungsintervall Backoff-Multiplikator</span><span class="sxs-lookup"><span data-stu-id="2bd1c-159">The retry interval backoff multiplier</span></span>

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

### <span data-ttu-id="2bd1c-160">-Servername</span><span class="sxs-lookup"><span data-stu-id="2bd1c-160">-ServerName</span></span>
<span data-ttu-id="2bd1c-161">Der Servername</span><span class="sxs-lookup"><span data-stu-id="2bd1c-161">The server name</span></span>

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

### <span data-ttu-id="2bd1c-162">-Schritt-für-Schritt-Nr</span><span class="sxs-lookup"><span data-stu-id="2bd1c-162">-StepId</span></span>
<span data-ttu-id="2bd1c-163">Der Schritt-ID-Text</span><span class="sxs-lookup"><span data-stu-id="2bd1c-163">The step id text</span></span>

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

### <span data-ttu-id="2bd1c-164">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="2bd1c-164">-TargetGroupName</span></span>
<span data-ttu-id="2bd1c-165">Der Name der Zielgruppe</span><span class="sxs-lookup"><span data-stu-id="2bd1c-165">The target group name</span></span>

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

### <span data-ttu-id="2bd1c-166">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="2bd1c-166">-TimeoutSeconds</span></span>
<span data-ttu-id="2bd1c-167">Die Timeout Sekunden</span><span class="sxs-lookup"><span data-stu-id="2bd1c-167">The timeout seconds</span></span>

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

### <span data-ttu-id="2bd1c-168">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2bd1c-168">-Confirm</span></span>
<span data-ttu-id="2bd1c-169">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bd1c-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bd1c-170">-WhatIf</span></span>
<span data-ttu-id="2bd1c-171">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bd1c-172">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bd1c-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bd1c-173">CommonParameters</span></span>
<span data-ttu-id="2bd1c-174">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bd1c-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bd1c-175">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2bd1c-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bd1c-176">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2bd1c-176">INPUTS</span></span>

### <span data-ttu-id="2bd1c-177">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="2bd1c-177">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="2bd1c-178">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2bd1c-178">OUTPUTS</span></span>

### <span data-ttu-id="2bd1c-179">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="2bd1c-179">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="2bd1c-180">Notizen</span><span class="sxs-lookup"><span data-stu-id="2bd1c-180">NOTES</span></span>

## <span data-ttu-id="2bd1c-181">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2bd1c-181">RELATED LINKS</span></span>
