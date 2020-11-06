---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncMember.md
ms.openlocfilehash: 30a73047282508adc0c2aa0d0d64a61f9f70e71a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502873"
---
# <span data-ttu-id="25bd0-101">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="25bd0-101">Get-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="25bd0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="25bd0-102">SYNOPSIS</span></span>
<span data-ttu-id="25bd0-103">Gibt Informationen zu Azure SQL-Daten Bank Synchronisierungs Mitgliedern zurück.</span><span class="sxs-lookup"><span data-stu-id="25bd0-103">Returns information about Azure SQL Database Sync Members.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25bd0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="25bd0-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncMember [-Name <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="25bd0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25bd0-105">DESCRIPTION</span></span>
<span data-ttu-id="25bd0-106">Das Cmdlet " **Get-AzureRmSqlSyncMember** " gibt Informationen zu einem oder mehreren Azure SQL-Daten Bank Synchronisierungs Mitgliedern zurück.</span><span class="sxs-lookup"><span data-stu-id="25bd0-106">The **Get-AzureRmSqlSyncMember** cmdlet returns information about one or more Azure SQL Database Sync Members.</span></span>
<span data-ttu-id="25bd0-107">Geben Sie den Namen eines Synchronisierungs Mitglieds an, um Informationen nur für dieses Synchronisierungs Mitglied anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="25bd0-107">Specify the name of a sync member to see information for only that sync member.</span></span>

## <span data-ttu-id="25bd0-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="25bd0-108">EXAMPLES</span></span>

### <span data-ttu-id="25bd0-109">Beispiel 1: Abrufen aller Instanzen eines Azure SQL-Synchronisierungs Elements, das einer Synchronisierungsgruppe zugewiesen ist</span><span class="sxs-lookup"><span data-stu-id="25bd0-109">Example 1: Get all instances of Azure SQL Sync Member assigned to a sync group</span></span>
```
PS C:\>Get-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" | Format-List
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

<span data-ttu-id="25bd0-110">Dieser Befehl ruft Informationen zu allen Azure SQL-Daten Bank Synchronisierungs Mitgliedern ab, die der Synchronisierungsgruppe SyncGroup01 zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="25bd0-110">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01.</span></span>

### <span data-ttu-id="25bd0-111">Beispiel 2: Abrufen von Informationen zu einem Azure SQL-Daten Bank Synchronisierungselement</span><span class="sxs-lookup"><span data-stu-id="25bd0-111">Example 2: Get information about an Azure SQL Database Sync Member</span></span>
```
PS C:\>Get-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" | Format-List
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

<span data-ttu-id="25bd0-112">Dieser Befehl ruft Informationen über das Azure SQL-Daten Bank Synchronisierungselement mit dem Namen "SyncMember01" ab.</span><span class="sxs-lookup"><span data-stu-id="25bd0-112">This command gets information about the Azure SQL Database Sync Member with name "SyncMember01"</span></span>

## <span data-ttu-id="25bd0-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="25bd0-113">PARAMETERS</span></span>

### <span data-ttu-id="25bd0-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="25bd0-114">-DatabaseName</span></span>
<span data-ttu-id="25bd0-115">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="25bd0-115">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="25bd0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25bd0-116">-DefaultProfile</span></span>
<span data-ttu-id="25bd0-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="25bd0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25bd0-118">-Name</span><span class="sxs-lookup"><span data-stu-id="25bd0-118">-Name</span></span>
<span data-ttu-id="25bd0-119">Der Name des Synchronisierungs Mitglieds.</span><span class="sxs-lookup"><span data-stu-id="25bd0-119">The sync member name.</span></span>

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

### <span data-ttu-id="25bd0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25bd0-120">-ResourceGroupName</span></span>
<span data-ttu-id="25bd0-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="25bd0-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="25bd0-122">-Servername</span><span class="sxs-lookup"><span data-stu-id="25bd0-122">-ServerName</span></span>
<span data-ttu-id="25bd0-123">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="25bd0-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="25bd0-124">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="25bd0-124">-SyncGroupName</span></span>
<span data-ttu-id="25bd0-125">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="25bd0-125">The sync group name.</span></span>

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

### <span data-ttu-id="25bd0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25bd0-126">CommonParameters</span></span>
<span data-ttu-id="25bd0-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25bd0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25bd0-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25bd0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25bd0-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="25bd0-129">INPUTS</span></span>

### <span data-ttu-id="25bd0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="25bd0-130">System.String</span></span>

## <span data-ttu-id="25bd0-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="25bd0-131">OUTPUTS</span></span>

### <span data-ttu-id="25bd0-132">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="25bd0-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="25bd0-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="25bd0-133">NOTES</span></span>

## <span data-ttu-id="25bd0-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="25bd0-134">RELATED LINKS</span></span>

[<span data-ttu-id="25bd0-135">Neu – AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="25bd0-135">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="25bd0-136">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="25bd0-136">Update-AzureRmSqlSyncMember</span></span>](./Update-AzureRmSqlSyncMember.md)

[<span data-ttu-id="25bd0-137">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="25bd0-137">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)

