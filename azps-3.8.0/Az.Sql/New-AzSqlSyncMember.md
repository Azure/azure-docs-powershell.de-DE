---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
ms.openlocfilehash: 1decf3d7b179123a116bb570199840118115313f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845803"
---
# <span data-ttu-id="f58e6-101">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f58e6-101">New-AzSqlSyncMember</span></span>

## <span data-ttu-id="f58e6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f58e6-102">SYNOPSIS</span></span>
<span data-ttu-id="f58e6-103">Erstellt ein Azure SQL-Daten Bank Synchronisierungs Mitglied.</span><span class="sxs-lookup"><span data-stu-id="f58e6-103">Creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="f58e6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f58e6-104">SYNTAX</span></span>

### <span data-ttu-id="f58e6-105">AzureSqlDatabase (Standard)</span><span class="sxs-lookup"><span data-stu-id="f58e6-105">AzureSqlDatabase (Default)</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f58e6-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="f58e6-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f58e6-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="f58e6-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f58e6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f58e6-108">DESCRIPTION</span></span>
<span data-ttu-id="f58e6-109">Mit dem Cmdlet **New-AzSqlSyncMember** wird ein Azure SQL-Daten Bank Synchronisierungselement erstellt.</span><span class="sxs-lookup"><span data-stu-id="f58e6-109">The **New-AzSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="f58e6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f58e6-110">EXAMPLES</span></span>

### <span data-ttu-id="f58e6-111">Beispiel 1: Erstellen Sie einen Synchronisierungs Member für eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="f58e6-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
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

<span data-ttu-id="f58e6-112">Dieser Befehl erstellt einen Synchronisierungs Member für eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="f58e6-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="f58e6-113">Beispiel 2: Erstellen eines Synchronisierungs Mitglieds für eine lokale SQL Server-Datenbank</span><span class="sxs-lookup"><span data-stu-id="f58e6-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
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

<span data-ttu-id="f58e6-114">Mit diesem Befehl wird ein Synchronisierungselement für eine lokale SQL-Datenbank erstellt.</span><span class="sxs-lookup"><span data-stu-id="f58e6-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="f58e6-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="f58e6-115">PARAMETERS</span></span>

### <span data-ttu-id="f58e6-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f58e6-116">-DatabaseName</span></span>
<span data-ttu-id="f58e6-117">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="f58e6-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="f58e6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f58e6-118">-DefaultProfile</span></span>
<span data-ttu-id="f58e6-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f58e6-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f58e6-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="f58e6-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="f58e6-121">Die Anmeldeinformationen (Benutzername und Kennwort) der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="f58e6-121">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="f58e6-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="f58e6-122">-MemberDatabaseName</span></span>
<span data-ttu-id="f58e6-123">Der Azure SQL-Datenbankname der Mitgliedsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="f58e6-123">The Azure SQL Database name of the member database.</span></span>

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

### <span data-ttu-id="f58e6-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="f58e6-124">-MemberDatabaseType</span></span>
<span data-ttu-id="f58e6-125">Der Datenbanktyp der Mitgliedsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="f58e6-125">The database type of the member database.</span></span>

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

### <span data-ttu-id="f58e6-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="f58e6-126">-MemberServerName</span></span>
<span data-ttu-id="f58e6-127">Der Azure SQL Server-Name der Mitgliedsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="f58e6-127">The Azure SQL Server Name of the member database.</span></span>

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

### <span data-ttu-id="f58e6-128">-Name</span><span class="sxs-lookup"><span data-stu-id="f58e6-128">-Name</span></span>
<span data-ttu-id="f58e6-129">Der Name des Synchronisierungs Mitglieds.</span><span class="sxs-lookup"><span data-stu-id="f58e6-129">The sync member name.</span></span>

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

### <span data-ttu-id="f58e6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f58e6-130">-ResourceGroupName</span></span>
<span data-ttu-id="f58e6-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f58e6-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="f58e6-132">-Servername</span><span class="sxs-lookup"><span data-stu-id="f58e6-132">-ServerName</span></span>
<span data-ttu-id="f58e6-133">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f58e6-133">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="f58e6-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="f58e6-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="f58e6-135">Die ID der SQL Server-Datenbank, die vom Synchronisierungs-Agent verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="f58e6-135">The id of the SQL server database which is connected by the sync agent.</span></span>

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

### <span data-ttu-id="f58e6-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="f58e6-136">-SyncAgentName</span></span>
<span data-ttu-id="f58e6-137">Der Name des Synchronisierungs-Agents.</span><span class="sxs-lookup"><span data-stu-id="f58e6-137">The name of the sync agent.</span></span>

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

### <span data-ttu-id="f58e6-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f58e6-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="f58e6-139">Der Name der Ressourcengruppe, unter der sich der Synchronisierungs-Agent befindet.</span><span class="sxs-lookup"><span data-stu-id="f58e6-139">The name of the resource group where the sync agent is under.</span></span>

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

### <span data-ttu-id="f58e6-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="f58e6-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="f58e6-141">Die Ressourcen-ID des Synchronisierungs-Agents.</span><span class="sxs-lookup"><span data-stu-id="f58e6-141">The resource ID of the sync agent.</span></span>

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

### <span data-ttu-id="f58e6-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="f58e6-142">-SyncAgentServerName</span></span>
<span data-ttu-id="f58e6-143">Der Name des Azure SQL-Servers, unter dem sich der Synchronisierungs-Agent befindet.</span><span class="sxs-lookup"><span data-stu-id="f58e6-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

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

### <span data-ttu-id="f58e6-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="f58e6-144">-SyncDirection</span></span>
<span data-ttu-id="f58e6-145">Die Synchronisierungsrichtung dieses Synchronisierungs Elements.</span><span class="sxs-lookup"><span data-stu-id="f58e6-145">The sync direction of this sync member.</span></span>

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

### <span data-ttu-id="f58e6-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="f58e6-146">-SyncGroupName</span></span>
<span data-ttu-id="f58e6-147">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f58e6-147">The sync group name.</span></span>

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

### <span data-ttu-id="f58e6-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f58e6-148">-Confirm</span></span>
<span data-ttu-id="f58e6-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f58e6-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f58e6-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f58e6-150">-WhatIf</span></span>
<span data-ttu-id="f58e6-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f58e6-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f58e6-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f58e6-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f58e6-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f58e6-153">CommonParameters</span></span>
<span data-ttu-id="f58e6-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f58e6-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f58e6-155">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f58e6-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f58e6-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f58e6-156">INPUTS</span></span>

### <span data-ttu-id="f58e6-157">System. String</span><span class="sxs-lookup"><span data-stu-id="f58e6-157">System.String</span></span>

## <span data-ttu-id="f58e6-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f58e6-158">OUTPUTS</span></span>

### <span data-ttu-id="f58e6-159">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="f58e6-159">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="f58e6-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="f58e6-160">NOTES</span></span>

## <span data-ttu-id="f58e6-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f58e6-161">RELATED LINKS</span></span>

[<span data-ttu-id="f58e6-162">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f58e6-162">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="f58e6-163">Satz-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f58e6-163">Set-AzSqlSyncMember</span></span>](./Set-AzSqlSyncMember.md)

[<span data-ttu-id="f58e6-164">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="f58e6-164">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

