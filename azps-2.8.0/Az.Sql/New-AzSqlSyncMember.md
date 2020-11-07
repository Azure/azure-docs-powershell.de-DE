---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
ms.openlocfilehash: 503f7be9d4d7f595ac8d337568038d7e7e724d1f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825971"
---
# <span data-ttu-id="a2d73-101">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="a2d73-101">New-AzSqlSyncMember</span></span>

## <span data-ttu-id="a2d73-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a2d73-102">SYNOPSIS</span></span>
<span data-ttu-id="a2d73-103">Erstellt ein Azure SQL-Daten Bank Synchronisierungs Mitglied.</span><span class="sxs-lookup"><span data-stu-id="a2d73-103">Creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="a2d73-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2d73-104">SYNTAX</span></span>

### <span data-ttu-id="a2d73-105">AzureSqlDatabase (Standard)</span><span class="sxs-lookup"><span data-stu-id="a2d73-105">AzureSqlDatabase (Default)</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2d73-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="a2d73-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2d73-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="a2d73-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2d73-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a2d73-108">DESCRIPTION</span></span>
<span data-ttu-id="a2d73-109">Mit dem Cmdlet **New-AzSqlSyncMember** wird ein Azure SQL-Daten Bank Synchronisierungselement erstellt.</span><span class="sxs-lookup"><span data-stu-id="a2d73-109">The **New-AzSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="a2d73-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a2d73-110">EXAMPLES</span></span>

### <span data-ttu-id="a2d73-111">Beispiel 1: Erstellen Sie einen Synchronisierungs Member für eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="a2d73-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
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

<span data-ttu-id="a2d73-112">Dieser Befehl erstellt einen Synchronisierungs Member für eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="a2d73-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="a2d73-113">Beispiel 2: Erstellen eines Synchronisierungs Mitglieds für eine lokale SQL Server-Datenbank</span><span class="sxs-lookup"><span data-stu-id="a2d73-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
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

<span data-ttu-id="a2d73-114">Mit diesem Befehl wird ein Synchronisierungselement für eine lokale SQL-Datenbank erstellt.</span><span class="sxs-lookup"><span data-stu-id="a2d73-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="a2d73-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2d73-115">PARAMETERS</span></span>

### <span data-ttu-id="a2d73-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a2d73-116">-DatabaseName</span></span>
<span data-ttu-id="a2d73-117">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="a2d73-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="a2d73-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2d73-118">-DefaultProfile</span></span>
<span data-ttu-id="a2d73-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a2d73-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2d73-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="a2d73-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="a2d73-121">Die Anmeldeinformationen (Benutzername und Kennwort) der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="a2d73-121">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="a2d73-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="a2d73-122">-MemberDatabaseName</span></span>
<span data-ttu-id="a2d73-123">Der Azure SQL-Datenbankname der Mitgliedsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="a2d73-123">The Azure SQL Database name of the member database.</span></span>

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

### <span data-ttu-id="a2d73-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="a2d73-124">-MemberDatabaseType</span></span>
<span data-ttu-id="a2d73-125">Der Datenbanktyp der Mitgliedsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="a2d73-125">The database type of the member database.</span></span>

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

### <span data-ttu-id="a2d73-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="a2d73-126">-MemberServerName</span></span>
<span data-ttu-id="a2d73-127">Der Azure SQL Server-Name der Mitgliedsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="a2d73-127">The Azure SQL Server Name of the member database.</span></span>

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

### <span data-ttu-id="a2d73-128">-Name</span><span class="sxs-lookup"><span data-stu-id="a2d73-128">-Name</span></span>
<span data-ttu-id="a2d73-129">Der Name des Synchronisierungs Mitglieds.</span><span class="sxs-lookup"><span data-stu-id="a2d73-129">The sync member name.</span></span>

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

### <span data-ttu-id="a2d73-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2d73-130">-ResourceGroupName</span></span>
<span data-ttu-id="a2d73-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a2d73-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="a2d73-132">-Servername</span><span class="sxs-lookup"><span data-stu-id="a2d73-132">-ServerName</span></span>
<span data-ttu-id="a2d73-133">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a2d73-133">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="a2d73-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="a2d73-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="a2d73-135">Die ID der SQL Server-Datenbank, die vom Synchronisierungs-Agent verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="a2d73-135">The id of the SQL server database which is connected by the sync agent.</span></span>

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

### <span data-ttu-id="a2d73-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="a2d73-136">-SyncAgentName</span></span>
<span data-ttu-id="a2d73-137">Der Name des Synchronisierungs-Agents.</span><span class="sxs-lookup"><span data-stu-id="a2d73-137">The name of the sync agent.</span></span>

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

### <span data-ttu-id="a2d73-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2d73-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="a2d73-139">Der Name der Ressourcengruppe, unter der sich der Synchronisierungs-Agent befindet.</span><span class="sxs-lookup"><span data-stu-id="a2d73-139">The name of the resource group where the sync agent is under.</span></span>

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

### <span data-ttu-id="a2d73-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="a2d73-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="a2d73-141">Die Ressourcen-ID des Synchronisierungs-Agents.</span><span class="sxs-lookup"><span data-stu-id="a2d73-141">The resource ID of the sync agent.</span></span>

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

### <span data-ttu-id="a2d73-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="a2d73-142">-SyncAgentServerName</span></span>
<span data-ttu-id="a2d73-143">Der Name des Azure SQL-Servers, unter dem sich der Synchronisierungs-Agent befindet.</span><span class="sxs-lookup"><span data-stu-id="a2d73-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

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

### <span data-ttu-id="a2d73-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="a2d73-144">-SyncDirection</span></span>
<span data-ttu-id="a2d73-145">Die Synchronisierungsrichtung dieses Synchronisierungs Elements.</span><span class="sxs-lookup"><span data-stu-id="a2d73-145">The sync direction of this sync member.</span></span>

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

### <span data-ttu-id="a2d73-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="a2d73-146">-SyncGroupName</span></span>
<span data-ttu-id="a2d73-147">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="a2d73-147">The sync group name.</span></span>

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

### <span data-ttu-id="a2d73-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a2d73-148">-Confirm</span></span>
<span data-ttu-id="a2d73-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a2d73-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2d73-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2d73-150">-WhatIf</span></span>
<span data-ttu-id="a2d73-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a2d73-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2d73-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a2d73-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2d73-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2d73-153">CommonParameters</span></span>
<span data-ttu-id="a2d73-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2d73-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2d73-155">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2d73-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2d73-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a2d73-156">INPUTS</span></span>

### <span data-ttu-id="a2d73-157">System. String</span><span class="sxs-lookup"><span data-stu-id="a2d73-157">System.String</span></span>

## <span data-ttu-id="a2d73-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a2d73-158">OUTPUTS</span></span>

### <span data-ttu-id="a2d73-159">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="a2d73-159">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="a2d73-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="a2d73-160">NOTES</span></span>

## <span data-ttu-id="a2d73-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a2d73-161">RELATED LINKS</span></span>

[<span data-ttu-id="a2d73-162">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="a2d73-162">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="a2d73-163">Satz-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="a2d73-163">Set-AzSqlSyncMember</span></span>](./Set-AzSqlSyncMember.md)

[<span data-ttu-id="a2d73-164">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="a2d73-164">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

