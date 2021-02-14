---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
ms.openlocfilehash: 4bd797528b3656364594f28f72d2b9ce2f7fdfaa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163249"
---
# <span data-ttu-id="5ace2-101">Remove-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="5ace2-101">Remove-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="5ace2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ace2-102">SYNOPSIS</span></span>
<span data-ttu-id="5ace2-103">Entfernt das Ziel aus der Zielgruppe.</span><span class="sxs-lookup"><span data-stu-id="5ace2-103">Removes the target from the target group</span></span>

## <span data-ttu-id="5ace2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ace2-104">SYNTAX</span></span>

### <span data-ttu-id="5ace2-105">SqlDatabase (Standard)</span><span class="sxs-lookup"><span data-stu-id="5ace2-105">SqlDatabase (Default)</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ace2-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="5ace2-106">SqlServerOrElasticPool</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>] -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ace2-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="5ace2-107">SqlShardMap</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String> -DatabaseName <String>
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ace2-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="5ace2-108">SqlDatabaseUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ace2-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="5ace2-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ace2-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="5ace2-110">SqlShardMapUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ace2-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5ace2-111">SqlDatabaseUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ace2-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5ace2-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ace2-113">SqlShardMapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5ace2-113">SqlShardMapUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ace2-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5ace2-114">DESCRIPTION</span></span>
<span data-ttu-id="5ace2-115">Das Remove-AzSqlElasticJobTarget cmdlet entfernt eine Zielressource in eine Zielgruppe.</span><span class="sxs-lookup"><span data-stu-id="5ace2-115">The Remove-AzSqlElasticJobTarget cmdlet removes a target resource to a target group</span></span>

## <span data-ttu-id="5ace2-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5ace2-116">EXAMPLES</span></span>

### <span data-ttu-id="5ace2-117">Beispiel 1: Entfernen eines Serverziels</span><span class="sxs-lookup"><span data-stu-id="5ace2-117">Example 1: Remove a server target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="5ace2-118">Beispiel 2: Entfernen eines Datenbankziels</span><span class="sxs-lookup"><span data-stu-id="5ace2-118">Example 2: Remove a database target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="5ace2-119">Beispiel 3: Entfernen eines Ziels für einen Pool</span><span class="sxs-lookup"><span data-stu-id="5ace2-119">Example 3: Remove an elastic pool target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="5ace2-120">Beispiel 4: Entfernen eines Shardzuordnungsziels</span><span class="sxs-lookup"><span data-stu-id="5ace2-120">Example 4: Remove a shard map target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="5ace2-121">Entfernt ein Ziel (Server, Pool, Datenbank und Shardkarte) aus einer Zielgruppe.</span><span class="sxs-lookup"><span data-stu-id="5ace2-121">Removes a target (server, elastic pool, database, and shard map) from a target group</span></span>

## <span data-ttu-id="5ace2-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ace2-122">PARAMETERS</span></span>

### <span data-ttu-id="5ace2-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="5ace2-123">-AgentName</span></span>
<span data-ttu-id="5ace2-124">SQL Sie den Namen des Datenbank-Agents.</span><span class="sxs-lookup"><span data-stu-id="5ace2-124">SQL Database Agent Name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ace2-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="5ace2-125">-AgentServerName</span></span>
<span data-ttu-id="5ace2-126">SQL Datenbank-Agent-Servername.</span><span class="sxs-lookup"><span data-stu-id="5ace2-126">SQL Database Agent Server Name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ace2-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5ace2-127">-DatabaseName</span></span>
<span data-ttu-id="5ace2-128">Name des Datenbankziels</span><span class="sxs-lookup"><span data-stu-id="5ace2-128">Database Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlShardMap, SqlDatabaseUsingParentObject, SqlShardMapUsingParentObject, SqlDatabaseUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ace2-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ace2-129">-DefaultProfile</span></span>
<span data-ttu-id="5ace2-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5ace2-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ace2-131">-PoolName</span><span class="sxs-lookup"><span data-stu-id="5ace2-131">-ElasticPoolName</span></span>
<span data-ttu-id="5ace2-132">Zielname des Poolpools</span><span class="sxs-lookup"><span data-stu-id="5ace2-132">Elastic Pool Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool, SqlServerOrElasticPoolUsingParentObject, SqlServerOrElasticPoolUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ace2-133">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5ace2-133">-ParentObject</span></span>
<span data-ttu-id="5ace2-134">Das Zielgruppenobjekt.</span><span class="sxs-lookup"><span data-stu-id="5ace2-134">The target group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel
Parameter Sets: SqlDatabaseUsingParentObject, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ace2-135">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5ace2-135">-ParentResourceId</span></span>
<span data-ttu-id="5ace2-136">Die Ressourcen-ID der Zielgruppe.</span><span class="sxs-lookup"><span data-stu-id="5ace2-136">The target group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabaseUsingParentResourceId, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ace2-137">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="5ace2-137">-RefreshCredentialName</span></span>
<span data-ttu-id="5ace2-138">Name der Anmeldeinformationen aktualisieren</span><span class="sxs-lookup"><span data-stu-id="5ace2-138">Refresh Credential Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool, SqlShardMap, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ace2-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ace2-139">-ResourceGroupName</span></span>
<span data-ttu-id="5ace2-140">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="5ace2-140">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ace2-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5ace2-141">-ServerName</span></span>
<span data-ttu-id="5ace2-142">Serverzielname</span><span class="sxs-lookup"><span data-stu-id="5ace2-142">Server Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlShardMap, SqlDatabaseUsingParentObject, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject, SqlDatabaseUsingParentResourceId, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ace2-143">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="5ace2-143">-ShardMapName</span></span>
<span data-ttu-id="5ace2-144">Zielname der Shardzuordnung</span><span class="sxs-lookup"><span data-stu-id="5ace2-144">Shard Map Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlShardMap, SqlShardMapUsingParentObject, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ace2-145">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="5ace2-145">-TargetGroupName</span></span>
<span data-ttu-id="5ace2-146">SQL Sie den Namen des Datenbank-Agents.</span><span class="sxs-lookup"><span data-stu-id="5ace2-146">SQL Database Agent Name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ace2-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ace2-147">-Confirm</span></span>
<span data-ttu-id="5ace2-148">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5ace2-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ace2-149">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5ace2-149">-WhatIf</span></span>
<span data-ttu-id="5ace2-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5ace2-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ace2-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5ace2-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ace2-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ace2-152">CommonParameters</span></span>
<span data-ttu-id="5ace2-153">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ace2-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ace2-154">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ace2-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ace2-155">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5ace2-155">INPUTS</span></span>

### <span data-ttu-id="5ace2-156">Microsoft.Azure.Commands.Sql.BenchmarkJobs.Model.AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="5ace2-156">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="5ace2-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5ace2-157">OUTPUTS</span></span>

### <span data-ttu-id="5ace2-158">Microsoft.Azure.Management.Sql.Models.JobTarget</span><span class="sxs-lookup"><span data-stu-id="5ace2-158">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="5ace2-159">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5ace2-159">NOTES</span></span>

## <span data-ttu-id="5ace2-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5ace2-160">RELATED LINKS</span></span>
