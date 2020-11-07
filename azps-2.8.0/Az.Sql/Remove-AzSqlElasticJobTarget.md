---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
ms.openlocfilehash: 5b52a3b7601e98c8ae74866e88c996ab599added
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825947"
---
# <span data-ttu-id="6cf4f-101">Remove-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="6cf4f-101">Remove-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="6cf4f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6cf4f-102">SYNOPSIS</span></span>
<span data-ttu-id="6cf4f-103">Entfernt das Ziel aus der Zielgruppe</span><span class="sxs-lookup"><span data-stu-id="6cf4f-103">Removes the target from the target group</span></span>

## <span data-ttu-id="6cf4f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6cf4f-104">SYNTAX</span></span>

### <span data-ttu-id="6cf4f-105">SQLDatabase (Standard)</span><span class="sxs-lookup"><span data-stu-id="6cf4f-105">SqlDatabase (Default)</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cf4f-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="6cf4f-106">SqlServerOrElasticPool</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>] -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cf4f-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="6cf4f-107">SqlShardMap</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String> -DatabaseName <String>
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6cf4f-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="6cf4f-108">SqlDatabaseUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cf4f-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="6cf4f-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cf4f-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="6cf4f-110">SqlShardMapUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cf4f-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6cf4f-111">SqlDatabaseUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cf4f-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6cf4f-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6cf4f-113">SqlShardMapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6cf4f-113">SqlShardMapUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cf4f-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6cf4f-114">DESCRIPTION</span></span>
<span data-ttu-id="6cf4f-115">Das Remove-AzSqlElasticJobTarget-Cmdlet entfernt eine Zielressource in eine Zielgruppe</span><span class="sxs-lookup"><span data-stu-id="6cf4f-115">The Remove-AzSqlElasticJobTarget cmdlet removes a target resource to a target group</span></span>

## <span data-ttu-id="6cf4f-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6cf4f-116">EXAMPLES</span></span>

### <span data-ttu-id="6cf4f-117">Beispiel 1: Entfernen eines Server Ziels</span><span class="sxs-lookup"><span data-stu-id="6cf4f-117">Example 1 - Remove a server target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="6cf4f-118">Beispiel 2 – Entfernen eines Daten Bank Ziels</span><span class="sxs-lookup"><span data-stu-id="6cf4f-118">Example 2 - Remove a database target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="6cf4f-119">Beispiel 3: Entfernen eines elastischen Pool Ziels</span><span class="sxs-lookup"><span data-stu-id="6cf4f-119">Example 3 - Remove an elastic pool target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="6cf4f-120">Beispiel 4 – Entfernen eines Shard-Karten Ziels</span><span class="sxs-lookup"><span data-stu-id="6cf4f-120">Example 4 - Remove a shard map target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="6cf4f-121">Entfernt ein Ziel (Server, elastischer Pool, Datenbank und Shard-Karte) aus einer Zielgruppe</span><span class="sxs-lookup"><span data-stu-id="6cf4f-121">Removes a target (server, elastic pool, database, and shard map) from a target group</span></span>

## <span data-ttu-id="6cf4f-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="6cf4f-122">PARAMETERS</span></span>

### <span data-ttu-id="6cf4f-123">-Agentname</span><span class="sxs-lookup"><span data-stu-id="6cf4f-123">-AgentName</span></span>
<span data-ttu-id="6cf4f-124">Name des SQL-Datenbankagenten</span><span class="sxs-lookup"><span data-stu-id="6cf4f-124">SQL Database Agent Name.</span></span>

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

### <span data-ttu-id="6cf4f-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="6cf4f-125">-AgentServerName</span></span>
<span data-ttu-id="6cf4f-126">Server Name des SQL-Datenbankagenten</span><span class="sxs-lookup"><span data-stu-id="6cf4f-126">SQL Database Agent Server Name.</span></span>

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

### <span data-ttu-id="6cf4f-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6cf4f-127">-DatabaseName</span></span>
<span data-ttu-id="6cf4f-128">Name des Daten Bank Ziels</span><span class="sxs-lookup"><span data-stu-id="6cf4f-128">Database Target Name</span></span>

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

### <span data-ttu-id="6cf4f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cf4f-129">-DefaultProfile</span></span>
<span data-ttu-id="6cf4f-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6cf4f-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cf4f-131">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="6cf4f-131">-ElasticPoolName</span></span>
<span data-ttu-id="6cf4f-132">Zielname des elastischen Pools</span><span class="sxs-lookup"><span data-stu-id="6cf4f-132">Elastic Pool Target Name</span></span>

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

### <span data-ttu-id="6cf4f-133">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6cf4f-133">-ParentObject</span></span>
<span data-ttu-id="6cf4f-134">Das Zielgruppen Objekt.</span><span class="sxs-lookup"><span data-stu-id="6cf4f-134">The target group object.</span></span>

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

### <span data-ttu-id="6cf4f-135">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6cf4f-135">-ParentResourceId</span></span>
<span data-ttu-id="6cf4f-136">Die Ressourcen-ID der Zielgruppe.</span><span class="sxs-lookup"><span data-stu-id="6cf4f-136">The target group resource id.</span></span>

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

### <span data-ttu-id="6cf4f-137">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="6cf4f-137">-RefreshCredentialName</span></span>
<span data-ttu-id="6cf4f-138">Anmelde Informations Name aktualisieren</span><span class="sxs-lookup"><span data-stu-id="6cf4f-138">Refresh Credential Name</span></span>

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

### <span data-ttu-id="6cf4f-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cf4f-139">-ResourceGroupName</span></span>
<span data-ttu-id="6cf4f-140">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="6cf4f-140">Resource Group Name</span></span>

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

### <span data-ttu-id="6cf4f-141">-Servername</span><span class="sxs-lookup"><span data-stu-id="6cf4f-141">-ServerName</span></span>
<span data-ttu-id="6cf4f-142">Name des Server Ziels</span><span class="sxs-lookup"><span data-stu-id="6cf4f-142">Server Target Name</span></span>

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

### <span data-ttu-id="6cf4f-143">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="6cf4f-143">-ShardMapName</span></span>
<span data-ttu-id="6cf4f-144">Name des Splitter Karten-Ziels</span><span class="sxs-lookup"><span data-stu-id="6cf4f-144">Shard Map Target Name</span></span>

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

### <span data-ttu-id="6cf4f-145">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="6cf4f-145">-TargetGroupName</span></span>
<span data-ttu-id="6cf4f-146">Name des SQL-Datenbankagenten</span><span class="sxs-lookup"><span data-stu-id="6cf4f-146">SQL Database Agent Name.</span></span>

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

### <span data-ttu-id="6cf4f-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6cf4f-147">-Confirm</span></span>
<span data-ttu-id="6cf4f-148">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6cf4f-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cf4f-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cf4f-149">-WhatIf</span></span>
<span data-ttu-id="6cf4f-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6cf4f-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cf4f-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6cf4f-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cf4f-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cf4f-152">CommonParameters</span></span>
<span data-ttu-id="6cf4f-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cf4f-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cf4f-154">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6cf4f-154">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cf4f-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6cf4f-155">INPUTS</span></span>

### <span data-ttu-id="6cf4f-156">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="6cf4f-156">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="6cf4f-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6cf4f-157">OUTPUTS</span></span>

### <span data-ttu-id="6cf4f-158">Microsoft. Azure. Management. SQL. Models. JobTarget</span><span class="sxs-lookup"><span data-stu-id="6cf4f-158">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="6cf4f-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="6cf4f-159">NOTES</span></span>

## <span data-ttu-id="6cf4f-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6cf4f-160">RELATED LINKS</span></span>
