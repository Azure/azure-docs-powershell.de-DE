---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
ms.openlocfilehash: 79b26156ae99bfcdd94671649b403b495377af30
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824663"
---
# <span data-ttu-id="8616c-101">Add-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="8616c-101">Add-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="8616c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8616c-102">SYNOPSIS</span></span>
<span data-ttu-id="8616c-103">Hinzufügen eines Auftragsschritts zu einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="8616c-103">Adds a job step to a job</span></span>

## <span data-ttu-id="8616c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8616c-104">SYNTAX</span></span>

### <span data-ttu-id="8616c-105">Standardset (Standard)</span><span class="sxs-lookup"><span data-stu-id="8616c-105">DefaultSet (Default)</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String> -Name <String>
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8616c-106">WithOutputDb</span><span class="sxs-lookup"><span data-stu-id="8616c-106">WithOutputDb</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String> -OutputTableName <String>
 -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8616c-107">WithOutputDbId</span><span class="sxs-lookup"><span data-stu-id="8616c-107">WithOutputDbId</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseResourceId <String> -OutputCredentialName <String> -OutputTableName <String> -Name <String>
 [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8616c-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="8616c-108">ObjectSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8616c-109">WithOutputDbUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="8616c-109">WithOutputDbUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8616c-110">WithOutputDbIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="8616c-110">WithOutputDbIdUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseResourceId <String>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8616c-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8616c-111">ResourceIdSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8616c-112">WithOutputDbUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8616c-112">WithOutputDbUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8616c-113">WithOutputDbIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8616c-113">WithOutputDbIdUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseResourceId <String> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8616c-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8616c-114">DESCRIPTION</span></span>
<span data-ttu-id="8616c-115">Das Add-AzSqlElasticJobStep-Cmdlet fügt einen Auftragsschritt zu einem Auftrag hinzu</span><span class="sxs-lookup"><span data-stu-id="8616c-115">The Add-AzSqlElasticJobStep cmdlet adds a job step to a job</span></span>

## <span data-ttu-id="8616c-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8616c-116">EXAMPLES</span></span>

### <span data-ttu-id="8616c-117">Beispiel 1: Hinzufügen eines Schritts zu einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="8616c-117">Example 1 - Adds a step to a job</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -Name job1
$job | Add-AzSqlElasticJobStep -Name step1 -TargetGroupName tg1 -CredentialName cred1 -CommandText "SELECT 1"

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="8616c-118">Hinzufügen eines Auftragsschritts zu einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="8616c-118">Adds a job step to a job</span></span>

## <span data-ttu-id="8616c-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="8616c-119">PARAMETERS</span></span>

### <span data-ttu-id="8616c-120">-Agentname</span><span class="sxs-lookup"><span data-stu-id="8616c-120">-AgentName</span></span>
<span data-ttu-id="8616c-121">Name des Agents</span><span class="sxs-lookup"><span data-stu-id="8616c-121">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8616c-122">-CommandText</span><span class="sxs-lookup"><span data-stu-id="8616c-122">-CommandText</span></span>
<span data-ttu-id="8616c-123">Der Befehlstext</span><span class="sxs-lookup"><span data-stu-id="8616c-123">The command text</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8616c-124">-Credentialname</span><span class="sxs-lookup"><span data-stu-id="8616c-124">-CredentialName</span></span>
<span data-ttu-id="8616c-125">Der Anmeldeinformationsname</span><span class="sxs-lookup"><span data-stu-id="8616c-125">The credential name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8616c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8616c-126">-DefaultProfile</span></span>
<span data-ttu-id="8616c-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8616c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8616c-128">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="8616c-128">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="8616c-129">Das anfängliche Wiederholungsintervall für Sekunden</span><span class="sxs-lookup"><span data-stu-id="8616c-129">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="8616c-130">-Jobname</span><span class="sxs-lookup"><span data-stu-id="8616c-130">-JobName</span></span>
<span data-ttu-id="8616c-131">Der Name des Auftrags</span><span class="sxs-lookup"><span data-stu-id="8616c-131">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8616c-132">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="8616c-132">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="8616c-133">Das maximale Wiederholungsintervall für Sekunden</span><span class="sxs-lookup"><span data-stu-id="8616c-133">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="8616c-134">-Name</span><span class="sxs-lookup"><span data-stu-id="8616c-134">-Name</span></span>
<span data-ttu-id="8616c-135">Der Name des Auftragsschritts</span><span class="sxs-lookup"><span data-stu-id="8616c-135">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8616c-136">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="8616c-136">-OutputCredentialName</span></span>
<span data-ttu-id="8616c-137">Der Name der Ausgabe Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="8616c-137">The output credential name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8616c-138">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="8616c-138">-OutputDatabaseObject</span></span>
<span data-ttu-id="8616c-139">Das Ausgabedaten Bank Objekt</span><span class="sxs-lookup"><span data-stu-id="8616c-139">The output database object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: WithOutputDb, WithOutputDbUsingParentObject, WithOutputDbUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8616c-140">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="8616c-140">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="8616c-141">Die Ressourcen-ID der Ausgabedatenbank</span><span class="sxs-lookup"><span data-stu-id="8616c-141">The output database resource id</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDbId, WithOutputDbIdUsingParentObject, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8616c-142">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="8616c-142">-OutputSchemaName</span></span>
<span data-ttu-id="8616c-143">Name des Ausgabe Schemas</span><span class="sxs-lookup"><span data-stu-id="8616c-143">The output schema name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8616c-144">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="8616c-144">-OutputTableName</span></span>
<span data-ttu-id="8616c-145">Der Name der Ausgabetabelle</span><span class="sxs-lookup"><span data-stu-id="8616c-145">The output table name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8616c-146">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8616c-146">-ParentObject</span></span>
<span data-ttu-id="8616c-147">Das Auftragsobjekt</span><span class="sxs-lookup"><span data-stu-id="8616c-147">The job object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8616c-148">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8616c-148">-ParentResourceId</span></span>
<span data-ttu-id="8616c-149">Die Projekt Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="8616c-149">The job resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8616c-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8616c-150">-ResourceGroupName</span></span>
<span data-ttu-id="8616c-151">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="8616c-151">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8616c-152">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="8616c-152">-RetryAttempts</span></span>
<span data-ttu-id="8616c-153">Die Wiederholungsversuche</span><span class="sxs-lookup"><span data-stu-id="8616c-153">The retry attempts</span></span>

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

### <span data-ttu-id="8616c-154">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="8616c-154">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="8616c-155">Das Wiederholungsintervall zurück aus Multiplikator</span><span class="sxs-lookup"><span data-stu-id="8616c-155">The retry interval back off multiplier</span></span>

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

### <span data-ttu-id="8616c-156">-Servername</span><span class="sxs-lookup"><span data-stu-id="8616c-156">-ServerName</span></span>
<span data-ttu-id="8616c-157">Der Servername</span><span class="sxs-lookup"><span data-stu-id="8616c-157">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8616c-158">-Schritt-für-Schritt-Nr</span><span class="sxs-lookup"><span data-stu-id="8616c-158">-StepId</span></span>
<span data-ttu-id="8616c-159">Die Schritt-ID</span><span class="sxs-lookup"><span data-stu-id="8616c-159">The step id</span></span>

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

### <span data-ttu-id="8616c-160">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="8616c-160">-TargetGroupName</span></span>
<span data-ttu-id="8616c-161">Der Name der Zielgruppe</span><span class="sxs-lookup"><span data-stu-id="8616c-161">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId, ObjectSet, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, ResourceIdSet, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WithOutputDbUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8616c-162">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="8616c-162">-TimeoutSeconds</span></span>
<span data-ttu-id="8616c-163">Die Sekunden für Timeouts</span><span class="sxs-lookup"><span data-stu-id="8616c-163">The time out seconds</span></span>

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

### <span data-ttu-id="8616c-164">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8616c-164">-Confirm</span></span>
<span data-ttu-id="8616c-165">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8616c-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8616c-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8616c-166">-WhatIf</span></span>
<span data-ttu-id="8616c-167">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8616c-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8616c-168">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8616c-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8616c-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8616c-169">CommonParameters</span></span>
<span data-ttu-id="8616c-170">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8616c-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8616c-171">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8616c-171">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8616c-172">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8616c-172">INPUTS</span></span>

### <span data-ttu-id="8616c-173">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="8616c-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="8616c-174">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8616c-174">OUTPUTS</span></span>

### <span data-ttu-id="8616c-175">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="8616c-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="8616c-176">Notizen</span><span class="sxs-lookup"><span data-stu-id="8616c-176">NOTES</span></span>

## <span data-ttu-id="8616c-177">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8616c-177">RELATED LINKS</span></span>
