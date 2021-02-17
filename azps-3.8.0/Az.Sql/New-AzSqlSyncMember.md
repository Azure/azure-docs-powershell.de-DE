---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
ms.openlocfilehash: 793962db73fd053764a794b64bea8e68edadd73b
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413250"
---
# <span data-ttu-id="d966c-101">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d966c-101">New-AzSqlSyncMember</span></span>

## <span data-ttu-id="d966c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d966c-102">SYNOPSIS</span></span>
<span data-ttu-id="d966c-103">Erstellt ein Azure SQL Database Sync Member.</span><span class="sxs-lookup"><span data-stu-id="d966c-103">Creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="d966c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d966c-104">SYNTAX</span></span>

### <span data-ttu-id="d966c-105">AzureSqlDatabase (Standard)</span><span class="sxs-lookup"><span data-stu-id="d966c-105">AzureSqlDatabase (Default)</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d966c-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="d966c-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d966c-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="d966c-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d966c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d966c-108">DESCRIPTION</span></span>
<span data-ttu-id="d966c-109">Das **Cmdlet "New-AzSqlSyncMember"** erstellt ein Azure SQL Database Sync Member.</span><span class="sxs-lookup"><span data-stu-id="d966c-109">The **New-AzSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="d966c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d966c-110">EXAMPLES</span></span>

### <span data-ttu-id="d966c-111">Beispiel 1: Erstellen eines Synchronisierungsmitglieds für eine Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d966c-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
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

<span data-ttu-id="d966c-112">Mit diesem Befehl wird ein Synchronisierungsmmitglied für eine Azure SQL erstellt.</span><span class="sxs-lookup"><span data-stu-id="d966c-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="d966c-113">Beispiel 2: Erstellen eines Synchronisierungsmitglieds für eine lokale SQL Server Datenbank</span><span class="sxs-lookup"><span data-stu-id="d966c-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
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

<span data-ttu-id="d966c-114">Mit diesem Befehl wird ein Synchronisierungsm member für eine lokale SQL erstellt.</span><span class="sxs-lookup"><span data-stu-id="d966c-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="d966c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d966c-115">PARAMETERS</span></span>

### <span data-ttu-id="d966c-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d966c-116">-DatabaseName</span></span>
<span data-ttu-id="d966c-117">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d966c-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="d966c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d966c-118">-DefaultProfile</span></span>
<span data-ttu-id="d966c-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d966c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d966c-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="d966c-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="d966c-121">Die Anmeldeinformationen (Benutzername und Kennwort) der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d966c-121">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="d966c-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="d966c-122">-MemberDatabaseName</span></span>
<span data-ttu-id="d966c-123">Der Azure SQL Datenbankname der Memberdatenbank.</span><span class="sxs-lookup"><span data-stu-id="d966c-123">The Azure SQL Database name of the member database.</span></span>

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

### <span data-ttu-id="d966c-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="d966c-124">-MemberDatabaseType</span></span>
<span data-ttu-id="d966c-125">Der Datenbanktyp der Memberdatenbank.</span><span class="sxs-lookup"><span data-stu-id="d966c-125">The database type of the member database.</span></span>

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

### <span data-ttu-id="d966c-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="d966c-126">-MemberServerName</span></span>
<span data-ttu-id="d966c-127">Die Azure SQL Server Der Name der Memberdatenbank.</span><span class="sxs-lookup"><span data-stu-id="d966c-127">The Azure SQL Server Name of the member database.</span></span>

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

### <span data-ttu-id="d966c-128">-Name</span><span class="sxs-lookup"><span data-stu-id="d966c-128">-Name</span></span>
<span data-ttu-id="d966c-129">Der Name des Synchronisierungsmitglieds.</span><span class="sxs-lookup"><span data-stu-id="d966c-129">The sync member name.</span></span>

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

### <span data-ttu-id="d966c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d966c-130">-ResourceGroupName</span></span>
<span data-ttu-id="d966c-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d966c-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="d966c-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d966c-132">-ServerName</span></span>
<span data-ttu-id="d966c-133">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d966c-133">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="d966c-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="d966c-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="d966c-135">Die ID der SQL Serverdatenbank, die vom Synchronisierungs-Agent verbunden wird.</span><span class="sxs-lookup"><span data-stu-id="d966c-135">The id of the SQL server database which is connected by the sync agent.</span></span>

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

### <span data-ttu-id="d966c-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="d966c-136">-SyncAgentName</span></span>
<span data-ttu-id="d966c-137">Der Name des Synchronisierungs-Agents.</span><span class="sxs-lookup"><span data-stu-id="d966c-137">The name of the sync agent.</span></span>

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

### <span data-ttu-id="d966c-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d966c-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="d966c-139">Der Name der Ressourcengruppe, unter der sich der Synchronisierungs-Agent befindet.</span><span class="sxs-lookup"><span data-stu-id="d966c-139">The name of the resource group where the sync agent is under.</span></span>

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

### <span data-ttu-id="d966c-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="d966c-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="d966c-141">Die Ressourcen-ID des Synchronisierungs-Agents.</span><span class="sxs-lookup"><span data-stu-id="d966c-141">The resource ID of the sync agent.</span></span>

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

### <span data-ttu-id="d966c-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="d966c-142">-SyncAgentServerName</span></span>
<span data-ttu-id="d966c-143">Der Name des Azure-SQL Server, unter dem sich der Synchronisierungs-Agent befindet.</span><span class="sxs-lookup"><span data-stu-id="d966c-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

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

### <span data-ttu-id="d966c-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="d966c-144">-SyncDirection</span></span>
<span data-ttu-id="d966c-145">Die Synchronisierungsrichtung dieses Synchronisierungsmitglieds.</span><span class="sxs-lookup"><span data-stu-id="d966c-145">The sync direction of this sync member.</span></span>

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

### <span data-ttu-id="d966c-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="d966c-146">-SyncGroupName</span></span>
<span data-ttu-id="d966c-147">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="d966c-147">The sync group name.</span></span>

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

### <span data-ttu-id="d966c-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d966c-148">-Confirm</span></span>
<span data-ttu-id="d966c-149">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d966c-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d966c-150">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d966c-150">-WhatIf</span></span>
<span data-ttu-id="d966c-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d966c-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d966c-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d966c-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d966c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d966c-153">CommonParameters</span></span>
<span data-ttu-id="d966c-154">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d966c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d966c-155">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d966c-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d966c-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d966c-156">INPUTS</span></span>

### <span data-ttu-id="d966c-157">System.String</span><span class="sxs-lookup"><span data-stu-id="d966c-157">System.String</span></span>

## <span data-ttu-id="d966c-158">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d966c-158">OUTPUTS</span></span>

### <span data-ttu-id="d966c-159">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="d966c-159">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="d966c-160">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d966c-160">NOTES</span></span>

## <span data-ttu-id="d966c-161">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d966c-161">RELATED LINKS</span></span>

[<span data-ttu-id="d966c-162">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d966c-162">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)


[<span data-ttu-id="d966c-163">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="d966c-163">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

