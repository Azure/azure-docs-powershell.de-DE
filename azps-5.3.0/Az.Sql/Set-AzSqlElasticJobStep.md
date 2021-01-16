---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
ms.openlocfilehash: 4f6f0471224799e818f9db29e5be5a4c49f9c45e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468092"
---
# <span data-ttu-id="fc5bc-101">Set-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="fc5bc-101">Set-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="fc5bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc5bc-102">SYNOPSIS</span></span>
<span data-ttu-id="fc5bc-103">Aktualisiert einen Auftragsschritt</span><span class="sxs-lookup"><span data-stu-id="fc5bc-103">Updates a job step</span></span>

## <span data-ttu-id="fc5bc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc5bc-104">SYNTAX</span></span>

### <span data-ttu-id="fc5bc-105">DefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fc5bc-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc5bc-106">WithRemoveOutput</span><span class="sxs-lookup"><span data-stu-id="fc5bc-106">WithRemoveOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-RemoveOutput] [-TargetGroupName <String>] [-CredentialName <String>]
 [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc5bc-107">WithAddOutput</span><span class="sxs-lookup"><span data-stu-id="fc5bc-107">WithAddOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -OutputDatabaseResourceId <String> [-OutputCredentialName <String>]
 [-OutputTableName <String>] [-OutputSchemaName <String>] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc5bc-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="fc5bc-108">ObjectSet</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-OutputDatabaseObject <AzureSqlDatabaseModel>] [-OutputCredentialName <String>] [-OutputTableName <String>]
 [-OutputSchemaName <String>] [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc5bc-109">WithRemoveOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="fc5bc-109">WithRemoveOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> [-RemoveOutput]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc5bc-110">WithAddOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="fc5bc-110">WithAddOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc5bc-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fc5bc-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc5bc-112">WithRemoveOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fc5bc-112">WithRemoveOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-RemoveOutput] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc5bc-113">WithAddOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fc5bc-113">WithAddOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc5bc-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fc5bc-114">DESCRIPTION</span></span>
<span data-ttu-id="fc5bc-115">Das Set-AzSqlElasticJobStep aktualisiert einen Auftragsschritt</span><span class="sxs-lookup"><span data-stu-id="fc5bc-115">The Set-AzSqlElasticJobStep cmdlet updates a job step</span></span>

## <span data-ttu-id="fc5bc-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fc5bc-116">EXAMPLES</span></span>

### <span data-ttu-id="fc5bc-117">Beispiel 1: Aktualisiert die Zielgruppe eines Auftragsschritts für einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="fc5bc-117">Example 1: Updates a job step's target group for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -TargetGroupName tg2

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg2             cred1                 (43200,10,1,120,2) SELECT 1
```

### <span data-ttu-id="fc5bc-118">Beispiel 2: Aktualisiert das T-SQL eines Auftragsschritts für einen Auftrag</span><span class="sxs-lookup"><span data-stu-id="fc5bc-118">Example 2: Updates a job step's T-SQL script for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -CommandText "SELECT 2"

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 2
```

<span data-ttu-id="fc5bc-119">Aktualisiert einen Auftragsschritt von einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="fc5bc-119">Updates a job step from a job</span></span>

### <span data-ttu-id="fc5bc-120">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="fc5bc-120">Example 3</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJobStep -AgentName agent -CommandText 'SELECT 2' -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="fc5bc-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc5bc-121">PARAMETERS</span></span>

### <span data-ttu-id="fc5bc-122">-AgentName</span><span class="sxs-lookup"><span data-stu-id="fc5bc-122">-AgentName</span></span>
<span data-ttu-id="fc5bc-123">Der Agentname</span><span class="sxs-lookup"><span data-stu-id="fc5bc-123">The agent name</span></span>

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

### <span data-ttu-id="fc5bc-124">-CommandText</span><span class="sxs-lookup"><span data-stu-id="fc5bc-124">-CommandText</span></span>
<span data-ttu-id="fc5bc-125">Der Befehlstext</span><span class="sxs-lookup"><span data-stu-id="fc5bc-125">The command text</span></span>

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

### <span data-ttu-id="fc5bc-126">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="fc5bc-126">-CredentialName</span></span>
<span data-ttu-id="fc5bc-127">Der Name der Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="fc5bc-127">The credential name</span></span>

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

### <span data-ttu-id="fc5bc-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc5bc-128">-DefaultProfile</span></span>
<span data-ttu-id="fc5bc-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fc5bc-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc5bc-130">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="fc5bc-130">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="fc5bc-131">Die Sekunden für die anfängliche Wiederholungsintervalle</span><span class="sxs-lookup"><span data-stu-id="fc5bc-131">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="fc5bc-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc5bc-132">-InputObject</span></span>
<span data-ttu-id="fc5bc-133">Das Auftragsschrittobjekt</span><span class="sxs-lookup"><span data-stu-id="fc5bc-133">The job step object</span></span>

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

### <span data-ttu-id="fc5bc-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="fc5bc-134">-JobName</span></span>
<span data-ttu-id="fc5bc-135">Der Name des Auftrags</span><span class="sxs-lookup"><span data-stu-id="fc5bc-135">The job name</span></span>

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

### <span data-ttu-id="fc5bc-136">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="fc5bc-136">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="fc5bc-137">Das maximale Wiederholungsintervall in Sekunden</span><span class="sxs-lookup"><span data-stu-id="fc5bc-137">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="fc5bc-138">-Name</span><span class="sxs-lookup"><span data-stu-id="fc5bc-138">-Name</span></span>
<span data-ttu-id="fc5bc-139">Der Schrittname</span><span class="sxs-lookup"><span data-stu-id="fc5bc-139">The step name</span></span>

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

### <span data-ttu-id="fc5bc-140">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="fc5bc-140">-OutputCredentialName</span></span>
<span data-ttu-id="fc5bc-141">Der Name der Anmeldeinformationen für die Ausgabe</span><span class="sxs-lookup"><span data-stu-id="fc5bc-141">The output credential name</span></span>

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

### <span data-ttu-id="fc5bc-142">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="fc5bc-142">-OutputDatabaseObject</span></span>
<span data-ttu-id="fc5bc-143">Das Ausgabedatenbankobjekt</span><span class="sxs-lookup"><span data-stu-id="fc5bc-143">The output database object</span></span>

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

### <span data-ttu-id="fc5bc-144">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="fc5bc-144">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="fc5bc-145">Die Ressourcen-ID der Ausgabedatenbank</span><span class="sxs-lookup"><span data-stu-id="fc5bc-145">The output database resource id</span></span>

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

### <span data-ttu-id="fc5bc-146">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="fc5bc-146">-OutputSchemaName</span></span>
<span data-ttu-id="fc5bc-147">Der Name des Ausgabeschemas</span><span class="sxs-lookup"><span data-stu-id="fc5bc-147">The output schema name</span></span>

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

### <span data-ttu-id="fc5bc-148">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="fc5bc-148">-OutputTableName</span></span>
<span data-ttu-id="fc5bc-149">Der Name der Ausgabetabelle</span><span class="sxs-lookup"><span data-stu-id="fc5bc-149">The output table name</span></span>

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

### <span data-ttu-id="fc5bc-150">-RemoveOutput</span><span class="sxs-lookup"><span data-stu-id="fc5bc-150">-RemoveOutput</span></span>
<span data-ttu-id="fc5bc-151">Das Kennzeichen, mit dem angegeben wird, ob die Ausgabe entfernt werden soll</span><span class="sxs-lookup"><span data-stu-id="fc5bc-151">The flag to indicate whether to remove output</span></span>

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

### <span data-ttu-id="fc5bc-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc5bc-152">-ResourceGroupName</span></span>
<span data-ttu-id="fc5bc-153">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="fc5bc-153">The resource group name</span></span>

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

### <span data-ttu-id="fc5bc-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc5bc-154">-ResourceId</span></span>
<span data-ttu-id="fc5bc-155">Die Ressourcen-ID des Auftragsschritts</span><span class="sxs-lookup"><span data-stu-id="fc5bc-155">The job step resource id</span></span>

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

### <span data-ttu-id="fc5bc-156">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="fc5bc-156">-RetryAttempts</span></span>
<span data-ttu-id="fc5bc-157">Versuchen Sie es erneut mittemps</span><span class="sxs-lookup"><span data-stu-id="fc5bc-157">The retry attemps</span></span>

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

### <span data-ttu-id="fc5bc-158">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="fc5bc-158">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="fc5bc-159">Der Wiederholungsintervall-Backoff-Multiplikator</span><span class="sxs-lookup"><span data-stu-id="fc5bc-159">The retry interval backoff multiplier</span></span>

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

### <span data-ttu-id="fc5bc-160">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fc5bc-160">-ServerName</span></span>
<span data-ttu-id="fc5bc-161">Der Servername</span><span class="sxs-lookup"><span data-stu-id="fc5bc-161">The server name</span></span>

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

### <span data-ttu-id="fc5bc-162">-StepId</span><span class="sxs-lookup"><span data-stu-id="fc5bc-162">-StepId</span></span>
<span data-ttu-id="fc5bc-163">Der Schritt-ID-Text</span><span class="sxs-lookup"><span data-stu-id="fc5bc-163">The step id text</span></span>

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

### <span data-ttu-id="fc5bc-164">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="fc5bc-164">-TargetGroupName</span></span>
<span data-ttu-id="fc5bc-165">Der Name der Zielgruppe</span><span class="sxs-lookup"><span data-stu-id="fc5bc-165">The target group name</span></span>

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

### <span data-ttu-id="fc5bc-166">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="fc5bc-166">-TimeoutSeconds</span></span>
<span data-ttu-id="fc5bc-167">Timeout in Sekunden</span><span class="sxs-lookup"><span data-stu-id="fc5bc-167">The timeout seconds</span></span>

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

### <span data-ttu-id="fc5bc-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc5bc-168">-Confirm</span></span>
<span data-ttu-id="fc5bc-169">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fc5bc-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc5bc-170">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fc5bc-170">-WhatIf</span></span>
<span data-ttu-id="fc5bc-171">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fc5bc-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc5bc-172">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fc5bc-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc5bc-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc5bc-173">CommonParameters</span></span>
<span data-ttu-id="fc5bc-174">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc5bc-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc5bc-175">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc5bc-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc5bc-176">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fc5bc-176">INPUTS</span></span>

### <span data-ttu-id="fc5bc-177">Microsoft.Azure.Commands.Sql.FlexibleJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="fc5bc-177">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="fc5bc-178">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fc5bc-178">OUTPUTS</span></span>

### <span data-ttu-id="fc5bc-179">Microsoft.Azure.Commands.Sql.FlexibleJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="fc5bc-179">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="fc5bc-180">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fc5bc-180">NOTES</span></span>

## <span data-ttu-id="fc5bc-181">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fc5bc-181">RELATED LINKS</span></span>
