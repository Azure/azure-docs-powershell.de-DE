---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
ms.openlocfilehash: cdf50079a08a4ac021e78e210ae574aa978674fe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175413"
---
# <span data-ttu-id="ad992-101">Add-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="ad992-101">Add-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="ad992-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ad992-102">SYNOPSIS</span></span>
<span data-ttu-id="ad992-103">Hinzufügen eines Ziels zu einer Zielgruppe</span><span class="sxs-lookup"><span data-stu-id="ad992-103">Adds a target to a target group</span></span>

## <span data-ttu-id="ad992-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad992-104">SYNTAX</span></span>

### <span data-ttu-id="ad992-105">SQLDatabase (Standard)</span><span class="sxs-lookup"><span data-stu-id="ad992-105">SqlDatabase (Default)</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad992-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="ad992-106">SqlServerOrElasticPool</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ad992-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="ad992-107">SqlShardMap</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad992-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="ad992-108">SqlDatabaseUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad992-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="ad992-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad992-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="ad992-110">SqlShardMapUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad992-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ad992-111">SqlDatabaseUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad992-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ad992-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad992-113">SqlShardMapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ad992-113">SqlShardMapUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad992-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad992-114">DESCRIPTION</span></span>
<span data-ttu-id="ad992-115">Das Add-AzSqlElasticJobTarget-Cmdlet fügt eine Zielressource zu einer Zielgruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="ad992-115">The Add-AzSqlElasticJobTarget cmdlet adds a target resource to a target group</span></span>

## <span data-ttu-id="ad992-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad992-116">EXAMPLES</span></span>

### <span data-ttu-id="ad992-117">Beispiel 1: Hinzufügen eines Server Ziels</span><span class="sxs-lookup"><span data-stu-id="ad992-117">Example 1: Add a server target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="ad992-118">Beispiel 2: Hinzufügen eines Daten Bank Ziels</span><span class="sxs-lookup"><span data-stu-id="ad992-118">Example 2: Add a database target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="ad992-119">Beispiel 3: Hinzufügen eines elastischen Pool Ziels</span><span class="sxs-lookup"><span data-stu-id="ad992-119">Example 3: Add an elastic pool target</span></span>
```powershell
PS C:\> $tg | Add-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="ad992-120">Beispiel 4: Hinzufügen eines Shard-Karten Ziels</span><span class="sxs-lookup"><span data-stu-id="ad992-120">Example 4: Add a shard map target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="ad992-121">Fügt einer Zielgruppe ein Ziel (Server, elastischer Pool, Datenbank und Shard-Karte) hinzu.</span><span class="sxs-lookup"><span data-stu-id="ad992-121">Adds a target (server, elastic pool, database, and shard map) to a target group</span></span>

## <span data-ttu-id="ad992-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad992-122">PARAMETERS</span></span>

### <span data-ttu-id="ad992-123">-Agentname</span><span class="sxs-lookup"><span data-stu-id="ad992-123">-AgentName</span></span>
<span data-ttu-id="ad992-124">Der Name des Agents.</span><span class="sxs-lookup"><span data-stu-id="ad992-124">The agent name.</span></span>

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

### <span data-ttu-id="ad992-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="ad992-125">-AgentServerName</span></span>
<span data-ttu-id="ad992-126">Der Servername.</span><span class="sxs-lookup"><span data-stu-id="ad992-126">The server name.</span></span>

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

### <span data-ttu-id="ad992-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ad992-127">-DatabaseName</span></span>
<span data-ttu-id="ad992-128">Name des Daten Bank Ziels</span><span class="sxs-lookup"><span data-stu-id="ad992-128">Database Target Name</span></span>

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

### <span data-ttu-id="ad992-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad992-129">-DefaultProfile</span></span>
<span data-ttu-id="ad992-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ad992-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad992-131">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="ad992-131">-ElasticPoolName</span></span>
<span data-ttu-id="ad992-132">Zielname des elastischen Pools</span><span class="sxs-lookup"><span data-stu-id="ad992-132">Elastic Pool Target Name</span></span>

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

### <span data-ttu-id="ad992-133">-Ausschließen</span><span class="sxs-lookup"><span data-stu-id="ad992-133">-Exclude</span></span>
<span data-ttu-id="ad992-134">Schließt ein Ziel aus.</span><span class="sxs-lookup"><span data-stu-id="ad992-134">Excludes a target.</span></span>

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

### <span data-ttu-id="ad992-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ad992-135">-ParentObject</span></span>
<span data-ttu-id="ad992-136">Das Zielgruppen Objekt.</span><span class="sxs-lookup"><span data-stu-id="ad992-136">The target group object.</span></span>

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

### <span data-ttu-id="ad992-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ad992-137">-ParentResourceId</span></span>
<span data-ttu-id="ad992-138">Die Ressourcen-ID der Zielgruppe.</span><span class="sxs-lookup"><span data-stu-id="ad992-138">The target group resource id.</span></span>

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

### <span data-ttu-id="ad992-139">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="ad992-139">-RefreshCredentialName</span></span>
<span data-ttu-id="ad992-140">Anmelde Informations Name aktualisieren</span><span class="sxs-lookup"><span data-stu-id="ad992-140">Refresh Credential Name</span></span>

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

### <span data-ttu-id="ad992-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad992-141">-ResourceGroupName</span></span>
<span data-ttu-id="ad992-142">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="ad992-142">Resource Group Name</span></span>

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

### <span data-ttu-id="ad992-143">-Servername</span><span class="sxs-lookup"><span data-stu-id="ad992-143">-ServerName</span></span>
<span data-ttu-id="ad992-144">Name des Server Ziels</span><span class="sxs-lookup"><span data-stu-id="ad992-144">Server Target Name</span></span>

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

### <span data-ttu-id="ad992-145">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="ad992-145">-ShardMapName</span></span>
<span data-ttu-id="ad992-146">Name des Splitter Karten-Ziels</span><span class="sxs-lookup"><span data-stu-id="ad992-146">Shard Map Target Name</span></span>

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

### <span data-ttu-id="ad992-147">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="ad992-147">-TargetGroupName</span></span>
<span data-ttu-id="ad992-148">Der Name der Zielgruppe.</span><span class="sxs-lookup"><span data-stu-id="ad992-148">The target group name.</span></span>

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

### <span data-ttu-id="ad992-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ad992-149">-Confirm</span></span>
<span data-ttu-id="ad992-150">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ad992-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad992-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad992-151">-WhatIf</span></span>
<span data-ttu-id="ad992-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ad992-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad992-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ad992-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad992-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad992-154">CommonParameters</span></span>
<span data-ttu-id="ad992-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad992-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad992-156">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad992-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad992-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ad992-157">INPUTS</span></span>

### <span data-ttu-id="ad992-158">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="ad992-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="ad992-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ad992-159">OUTPUTS</span></span>

### <span data-ttu-id="ad992-160">Microsoft. Azure. Management. SQL. Models. JobTarget</span><span class="sxs-lookup"><span data-stu-id="ad992-160">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="ad992-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="ad992-161">NOTES</span></span>

## <span data-ttu-id="ad992-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ad992-162">RELATED LINKS</span></span>
