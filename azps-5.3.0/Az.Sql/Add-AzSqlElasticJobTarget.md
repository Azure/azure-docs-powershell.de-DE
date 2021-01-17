---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
ms.openlocfilehash: cdf50079a08a4ac021e78e210ae574aa978674fe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375583"
---
# <span data-ttu-id="70219-101">Add-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="70219-101">Add-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="70219-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70219-102">SYNOPSIS</span></span>
<span data-ttu-id="70219-103">Fügt einer Zielgruppe ein Ziel hinzu.</span><span class="sxs-lookup"><span data-stu-id="70219-103">Adds a target to a target group</span></span>

## <span data-ttu-id="70219-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70219-104">SYNTAX</span></span>

### <span data-ttu-id="70219-105">SqlDatabase (Standard)</span><span class="sxs-lookup"><span data-stu-id="70219-105">SqlDatabase (Default)</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70219-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="70219-106">SqlServerOrElasticPool</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70219-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="70219-107">SqlShardMap</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70219-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="70219-108">SqlDatabaseUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70219-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="70219-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70219-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="70219-110">SqlShardMapUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70219-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="70219-111">SqlDatabaseUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70219-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="70219-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70219-113">SqlShardMapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="70219-113">SqlShardMapUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70219-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="70219-114">DESCRIPTION</span></span>
<span data-ttu-id="70219-115">Das Add-AzSqlElasticJobTarget Cmdlet fügt einer Zielgruppe eine Zielressource hinzu.</span><span class="sxs-lookup"><span data-stu-id="70219-115">The Add-AzSqlElasticJobTarget cmdlet adds a target resource to a target group</span></span>

## <span data-ttu-id="70219-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="70219-116">EXAMPLES</span></span>

### <span data-ttu-id="70219-117">Beispiel 1: Hinzufügen eines Serverziels</span><span class="sxs-lookup"><span data-stu-id="70219-117">Example 1: Add a server target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="70219-118">Beispiel 2: Hinzufügen eines Datenbankziels</span><span class="sxs-lookup"><span data-stu-id="70219-118">Example 2: Add a database target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="70219-119">Beispiel 3: Hinzufügen eines Ziels für einen Pool</span><span class="sxs-lookup"><span data-stu-id="70219-119">Example 3: Add an elastic pool target</span></span>
```powershell
PS C:\> $tg | Add-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="70219-120">Beispiel 4: Hinzufügen eines Shardzuordnungsziels</span><span class="sxs-lookup"><span data-stu-id="70219-120">Example 4: Add a shard map target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="70219-121">Fügt einer Zielgruppe ein Ziel (Server, Pool, Datenbank und Shardkarte) hinzu.</span><span class="sxs-lookup"><span data-stu-id="70219-121">Adds a target (server, elastic pool, database, and shard map) to a target group</span></span>

## <span data-ttu-id="70219-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70219-122">PARAMETERS</span></span>

### <span data-ttu-id="70219-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="70219-123">-AgentName</span></span>
<span data-ttu-id="70219-124">Der Agentname.</span><span class="sxs-lookup"><span data-stu-id="70219-124">The agent name.</span></span>

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

### <span data-ttu-id="70219-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="70219-125">-AgentServerName</span></span>
<span data-ttu-id="70219-126">Der Servername.</span><span class="sxs-lookup"><span data-stu-id="70219-126">The server name.</span></span>

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

### <span data-ttu-id="70219-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="70219-127">-DatabaseName</span></span>
<span data-ttu-id="70219-128">Name des Datenbankziels</span><span class="sxs-lookup"><span data-stu-id="70219-128">Database Target Name</span></span>

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

### <span data-ttu-id="70219-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70219-129">-DefaultProfile</span></span>
<span data-ttu-id="70219-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="70219-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70219-131">-PoolName</span><span class="sxs-lookup"><span data-stu-id="70219-131">-ElasticPoolName</span></span>
<span data-ttu-id="70219-132">Zielname des Poolpools</span><span class="sxs-lookup"><span data-stu-id="70219-132">Elastic Pool Target Name</span></span>

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

### <span data-ttu-id="70219-133">-Exclude</span><span class="sxs-lookup"><span data-stu-id="70219-133">-Exclude</span></span>
<span data-ttu-id="70219-134">Schließt ein Ziel aus.</span><span class="sxs-lookup"><span data-stu-id="70219-134">Excludes a target.</span></span>

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

### <span data-ttu-id="70219-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="70219-135">-ParentObject</span></span>
<span data-ttu-id="70219-136">Das Zielgruppenobjekt.</span><span class="sxs-lookup"><span data-stu-id="70219-136">The target group object.</span></span>

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

### <span data-ttu-id="70219-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="70219-137">-ParentResourceId</span></span>
<span data-ttu-id="70219-138">Die Ressourcen-ID der Zielgruppe.</span><span class="sxs-lookup"><span data-stu-id="70219-138">The target group resource id.</span></span>

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

### <span data-ttu-id="70219-139">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="70219-139">-RefreshCredentialName</span></span>
<span data-ttu-id="70219-140">Name der Anmeldeinformationen aktualisieren</span><span class="sxs-lookup"><span data-stu-id="70219-140">Refresh Credential Name</span></span>

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

### <span data-ttu-id="70219-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70219-141">-ResourceGroupName</span></span>
<span data-ttu-id="70219-142">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="70219-142">Resource Group Name</span></span>

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

### <span data-ttu-id="70219-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="70219-143">-ServerName</span></span>
<span data-ttu-id="70219-144">Serverzielname</span><span class="sxs-lookup"><span data-stu-id="70219-144">Server Target Name</span></span>

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

### <span data-ttu-id="70219-145">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="70219-145">-ShardMapName</span></span>
<span data-ttu-id="70219-146">Zielname der Shardzuordnung</span><span class="sxs-lookup"><span data-stu-id="70219-146">Shard Map Target Name</span></span>

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

### <span data-ttu-id="70219-147">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="70219-147">-TargetGroupName</span></span>
<span data-ttu-id="70219-148">Der Name der Zielgruppe.</span><span class="sxs-lookup"><span data-stu-id="70219-148">The target group name.</span></span>

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

### <span data-ttu-id="70219-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70219-149">-Confirm</span></span>
<span data-ttu-id="70219-150">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="70219-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70219-151">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="70219-151">-WhatIf</span></span>
<span data-ttu-id="70219-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="70219-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70219-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="70219-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70219-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70219-154">CommonParameters</span></span>
<span data-ttu-id="70219-155">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70219-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70219-156">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70219-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70219-157">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="70219-157">INPUTS</span></span>

### <span data-ttu-id="70219-158">Microsoft.Azure.Commands.Sql.BenchmarkJobs.Model.AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="70219-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="70219-159">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="70219-159">OUTPUTS</span></span>

### <span data-ttu-id="70219-160">Microsoft.Azure.Management.Sql.Models.JobTarget</span><span class="sxs-lookup"><span data-stu-id="70219-160">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="70219-161">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="70219-161">NOTES</span></span>

## <span data-ttu-id="70219-162">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="70219-162">RELATED LINKS</span></span>
