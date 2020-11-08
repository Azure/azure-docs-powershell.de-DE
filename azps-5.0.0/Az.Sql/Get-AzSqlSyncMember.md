---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
ms.openlocfilehash: e5bb853d9dd818801298254eac1f120efcc829a4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175873"
---
# <span data-ttu-id="2cfa2-101">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="2cfa2-101">Get-AzSqlSyncMember</span></span>

## <span data-ttu-id="2cfa2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2cfa2-102">SYNOPSIS</span></span>
<span data-ttu-id="2cfa2-103">Gibt Informationen zu Azure SQL-Daten Bank Synchronisierungs Mitgliedern zurück.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-103">Returns information about Azure SQL Database Sync Members.</span></span>

## <span data-ttu-id="2cfa2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2cfa2-104">SYNTAX</span></span>

```
Get-AzSqlSyncMember [-Name <String>] [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cfa2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2cfa2-105">DESCRIPTION</span></span>
<span data-ttu-id="2cfa2-106">Das Cmdlet " **Get-AzSqlSyncMember** " gibt Informationen zu einem oder mehreren Azure SQL-Daten Bank Synchronisierungs Mitgliedern zurück.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-106">The **Get-AzSqlSyncMember** cmdlet returns information about one or more Azure SQL Database Sync Members.</span></span>
<span data-ttu-id="2cfa2-107">Geben Sie den Namen eines Synchronisierungs Mitglieds an, um Informationen nur für dieses Synchronisierungs Mitglied anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-107">Specify the name of a sync member to see information for only that sync member.</span></span>

## <span data-ttu-id="2cfa2-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2cfa2-108">EXAMPLES</span></span>

### <span data-ttu-id="2cfa2-109">Beispiel 1: Abrufen aller Instanzen eines Azure SQL-Synchronisierungs Elements, das einer Synchronisierungsgruppe zugewiesen ist</span><span class="sxs-lookup"><span data-stu-id="2cfa2-109">Example 1: Get all instances of Azure SQL Sync Member assigned to a sync group</span></span>
```
PS C:\> Get-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" | Format-List
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
SyncState                   : Good 

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember02
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      :  
SyncState                   : Good
```

<span data-ttu-id="2cfa2-110">Dieser Befehl ruft Informationen zu allen Azure SQL-Daten Bank Synchronisierungs Mitgliedern ab, die der Synchronisierungsgruppe SyncGroup01 zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-110">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01.</span></span>

### <span data-ttu-id="2cfa2-111">Beispiel 2: Abrufen von Informationen zu einem Azure SQL-Daten Bank Synchronisierungselement</span><span class="sxs-lookup"><span data-stu-id="2cfa2-111">Example 2: Get information about an Azure SQL Database Sync Member</span></span>
```
PS C:\> Get-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" | Format-List
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
SyncState                   : Good
```

<span data-ttu-id="2cfa2-112">Dieser Befehl ruft Informationen über das Azure SQL-Daten Bank Synchronisierungselement mit dem Namen "SyncMember01" ab.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-112">This command gets information about the Azure SQL Database Sync Member with name "SyncMember01"</span></span>

### <span data-ttu-id="2cfa2-113">Beispiel 3: Abrufen aller Instanzen des Azure SQL-Synchronisierungs Elements, das einer Synchronisierungsgruppe mithilfe von Filtern zugewiesen ist</span><span class="sxs-lookup"><span data-stu-id="2cfa2-113">Example 3: Get all instances of Azure SQL Sync Member assigned to a sync group using filtering</span></span>
```
PS C:\> Get-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember*" | Format-List
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
SyncState                   : Good 

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember02
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      :  
SyncState                   : Good
```

<span data-ttu-id="2cfa2-114">Dieser Befehl ruft Informationen zu allen Azure SQL-Daten Bank Synchronisierungs Mitgliedern ab, die der Synchronisierungsgruppen-SyncGroup01 zugeordnet sind, die mit "SyncMember" beginnen.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-114">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01 that start with "SyncMember".</span></span>

## <span data-ttu-id="2cfa2-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="2cfa2-115">PARAMETERS</span></span>

### <span data-ttu-id="2cfa2-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2cfa2-116">-DatabaseName</span></span>
<span data-ttu-id="2cfa2-117">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="2cfa2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cfa2-118">-DefaultProfile</span></span>
<span data-ttu-id="2cfa2-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2cfa2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2cfa2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2cfa2-120">-Name</span></span>
<span data-ttu-id="2cfa2-121">Der Name des Synchronisierungs Mitglieds.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-121">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cfa2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cfa2-122">-ResourceGroupName</span></span>
<span data-ttu-id="2cfa2-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="2cfa2-124">-Servername</span><span class="sxs-lookup"><span data-stu-id="2cfa2-124">-ServerName</span></span>
<span data-ttu-id="2cfa2-125">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="2cfa2-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="2cfa2-126">-SyncGroupName</span></span>
<span data-ttu-id="2cfa2-127">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-127">The sync group name.</span></span>

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

### <span data-ttu-id="2cfa2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cfa2-128">CommonParameters</span></span>
<span data-ttu-id="2cfa2-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cfa2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cfa2-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2cfa2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cfa2-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2cfa2-131">INPUTS</span></span>

### <span data-ttu-id="2cfa2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2cfa2-132">System.String</span></span>

## <span data-ttu-id="2cfa2-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2cfa2-133">OUTPUTS</span></span>

### <span data-ttu-id="2cfa2-134">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="2cfa2-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="2cfa2-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="2cfa2-135">NOTES</span></span>

## <span data-ttu-id="2cfa2-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2cfa2-136">RELATED LINKS</span></span>

[<span data-ttu-id="2cfa2-137">Neu – AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="2cfa2-137">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="2cfa2-138">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="2cfa2-138">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="2cfa2-139">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="2cfa2-139">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

