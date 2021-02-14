---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
ms.openlocfilehash: f7fc860711c5037e6ce6390f9fb7d79ddfa7d6ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163324"
---
# <span data-ttu-id="c4305-101">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="c4305-101">New-AzSqlSyncMember</span></span>

## <span data-ttu-id="c4305-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4305-102">SYNOPSIS</span></span>
<span data-ttu-id="c4305-103">Erstellt ein Azure SQL Database Sync Member.</span><span class="sxs-lookup"><span data-stu-id="c4305-103">Creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="c4305-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c4305-104">SYNTAX</span></span>

### <span data-ttu-id="c4305-105">AzureSqlDatabase (Standard)</span><span class="sxs-lookup"><span data-stu-id="c4305-105">AzureSqlDatabase (Default)</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-UsePrivateLinkConnection] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4305-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="c4305-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-UsePrivateLinkConnection] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4305-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="c4305-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-UsePrivateLinkConnection]
 [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4305-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c4305-108">DESCRIPTION</span></span>
<span data-ttu-id="c4305-109">Das **Cmdlet "New-AzSqlSyncMember"** erstellt ein Azure SQL Database Sync Member.</span><span class="sxs-lookup"><span data-stu-id="c4305-109">The **New-AzSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="c4305-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c4305-110">EXAMPLES</span></span>

### <span data-ttu-id="c4305-111">Beispiel 1: Erstellen eines Synchronisierungsmitglieds für eine Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="c4305-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
-MemberDatabaseType "AzureSqlDatabase" -MemberServerName "memberServer01.full.dns.name" -MemberDatabaseName "memberDatabase01" -MemberDatabaseCredential $credential | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : UnProvisioned
```

<span data-ttu-id="c4305-112">Mit diesem Befehl wird ein Synchronisierungsmmitglied für eine Azure SQL erstellt.</span><span class="sxs-lookup"><span data-stu-id="c4305-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="c4305-113">Beispiel 2: Erstellen eines Synchronisierungsmitglieds für eine lokale SQL Server Datenbank</span><span class="sxs-lookup"><span data-stu-id="c4305-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
-MemberDatabaseType "SqlServerDatabase" -SqlServerDatabaseId "dbId" -syncAgentResourceGroupName "syncAgentResourceGroupName" -syncAgentServerName "syncAgentServerName" 
-syncAgentDatabaseName "syncAgentDatabaseName" -syncAgentName "agentName" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : /subscriptions/{subscriptionId}/resourceGroups/{syncAgentResourceGroupName}/servers/{syncAgentServerName}/syncAgents/{syncAgentId}
SqlServerDatabaseId         : dbId
MemberServerName            : 
MemberDatabaseName          : 
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : UnProvisioned
```

<span data-ttu-id="c4305-114">Mit diesem Befehl wird ein Synchronisierungsm member für eine lokale SQL erstellt.</span><span class="sxs-lookup"><span data-stu-id="c4305-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="c4305-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4305-115">PARAMETERS</span></span>

### <span data-ttu-id="c4305-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c4305-116">-DatabaseName</span></span>
<span data-ttu-id="c4305-117">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="c4305-117">The name of the Azure SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4305-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4305-118">-DefaultProfile</span></span>
<span data-ttu-id="c4305-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c4305-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4305-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="c4305-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="c4305-121">Die Anmeldeinformationen (Benutzername und Kennwort) der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="c4305-121">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4305-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="c4305-122">-MemberDatabaseName</span></span>
<span data-ttu-id="c4305-123">Der Azure SQL Datenbankname der Memberdatenbank.</span><span class="sxs-lookup"><span data-stu-id="c4305-123">The Azure SQL Database name of the member database.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4305-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="c4305-124">-MemberDatabaseType</span></span>
<span data-ttu-id="c4305-125">Der Datenbanktyp der Memberdatenbank.</span><span class="sxs-lookup"><span data-stu-id="c4305-125">The database type of the member database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SqlServerDatabase, AzureSqlDatabase

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4305-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="c4305-126">-MemberServerName</span></span>
<span data-ttu-id="c4305-127">Die Azure SQL Server Der Name der Memberdatenbank.</span><span class="sxs-lookup"><span data-stu-id="c4305-127">The Azure SQL Server Name of the member database.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4305-128">-Name</span><span class="sxs-lookup"><span data-stu-id="c4305-128">-Name</span></span>
<span data-ttu-id="c4305-129">Der Name des Synchronisierungsmitglieds.</span><span class="sxs-lookup"><span data-stu-id="c4305-129">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4305-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4305-130">-ResourceGroupName</span></span>
<span data-ttu-id="c4305-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c4305-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4305-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c4305-132">-ServerName</span></span>
<span data-ttu-id="c4305-133">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c4305-133">The name of the Azure SQL Server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4305-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="c4305-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="c4305-135">Die ID der SQL Serverdatenbank, die vom Synchronisierungs-Agent verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="c4305-135">The id of the SQL server database which is connected by the sync agent.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent, OnPremisesDatabaseSyncAgentResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4305-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="c4305-136">-SyncAgentName</span></span>
<span data-ttu-id="c4305-137">Der Name des Synchronisierungs-Agents.</span><span class="sxs-lookup"><span data-stu-id="c4305-137">The name of the sync agent.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4305-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4305-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="c4305-139">Der Name der Ressourcengruppe, unter der sich der Synchronisierungs-Agent befindet.</span><span class="sxs-lookup"><span data-stu-id="c4305-139">The name of the resource group where the sync agent is under.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4305-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="c4305-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="c4305-141">Die Ressourcen-ID des Synchronisierungs-Agents.</span><span class="sxs-lookup"><span data-stu-id="c4305-141">The resource ID of the sync agent.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4305-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="c4305-142">-SyncAgentServerName</span></span>
<span data-ttu-id="c4305-143">Der Name des Azure-SQL Server, unter dem sich der Synchronisierungs-Agent befindet.</span><span class="sxs-lookup"><span data-stu-id="c4305-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4305-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="c4305-144">-SyncDirection</span></span>
<span data-ttu-id="c4305-145">Die Synchronisierungsrichtung dieses Synchronisierungsmitglieds.</span><span class="sxs-lookup"><span data-stu-id="c4305-145">The sync direction of this sync member.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Bidirectional, OneWayMemberToHub, OneWayHubToMember

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4305-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="c4305-146">-SyncGroupName</span></span>
<span data-ttu-id="c4305-147">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="c4305-147">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4305-148">-SyncMemberAzureDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="c4305-148">-SyncMemberAzureDatabaseResourceId</span></span>
<span data-ttu-id="c4305-149">Die Ressourcen-ID für die Datenbank des Synchronisierungsmitglieds, die verwendet wird, wenn "UsePrivateLinkConnection" auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c4305-149">The resource ID for the sync member database, used if UsePrivateLinkConnection is set to true.</span></span>

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

### <span data-ttu-id="c4305-150">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="c4305-150">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="c4305-151">Verwenden Sie eine private Linkverbindung, wenn Sie eine Verbindung mit diesem Synchronisierungsmitglied herstellen.</span><span class="sxs-lookup"><span data-stu-id="c4305-151">Use a private link connection when connecting to this sync member.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4305-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4305-152">-Confirm</span></span>
<span data-ttu-id="c4305-153">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c4305-153">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4305-154">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c4305-154">-WhatIf</span></span>
<span data-ttu-id="c4305-155">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c4305-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4305-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4305-156">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4305-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4305-157">CommonParameters</span></span>
<span data-ttu-id="c4305-158">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4305-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4305-159">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4305-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4305-160">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c4305-160">INPUTS</span></span>

### <span data-ttu-id="c4305-161">System.String</span><span class="sxs-lookup"><span data-stu-id="c4305-161">System.String</span></span>

## <span data-ttu-id="c4305-162">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c4305-162">OUTPUTS</span></span>

### <span data-ttu-id="c4305-163">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="c4305-163">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="c4305-164">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c4305-164">NOTES</span></span>

## <span data-ttu-id="c4305-165">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c4305-165">RELATED LINKS</span></span>

[<span data-ttu-id="c4305-166">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="c4305-166">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="c4305-167">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="c4305-167">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="c4305-168">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="c4305-168">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

