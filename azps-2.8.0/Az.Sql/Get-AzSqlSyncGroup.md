---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
ms.openlocfilehash: fdee39766c7793b4d326077e5c18e0328a5e4c4c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825500"
---
# <span data-ttu-id="6274c-101">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="6274c-101">Get-AzSqlSyncGroup</span></span>

## <span data-ttu-id="6274c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6274c-102">SYNOPSIS</span></span>
<span data-ttu-id="6274c-103">Gibt Informationen zu Azure SQL-Daten Bank Synchronisierungsgruppen zurück.</span><span class="sxs-lookup"><span data-stu-id="6274c-103">Returns information about Azure SQL Database Sync Groups.</span></span>

## <span data-ttu-id="6274c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6274c-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroup [[-Name] <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6274c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6274c-105">DESCRIPTION</span></span>
<span data-ttu-id="6274c-106">Das Cmdlet " **Get-AzSqlSyncGroup** " gibt Informationen zu mindestens einer Azure SQL-Daten Bank Synchronisierungsgruppe zurück.</span><span class="sxs-lookup"><span data-stu-id="6274c-106">The **Get-AzSqlSyncGroup** cmdlet returns information about one or more Azure SQL Database Sync Groups.</span></span>
<span data-ttu-id="6274c-107">Geben Sie den Namen einer Synchronisierungsgruppe an, um Informationen nur für diese Synchronisierungsgruppe anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6274c-107">Specify the name of a sync group to see information for only that sync group.</span></span>

## <span data-ttu-id="6274c-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6274c-108">EXAMPLES</span></span>

### <span data-ttu-id="6274c-109">Beispiel 1: Abrufen aller Instanzen einer Azure SQL-Synchronisierungsgruppe, die einer Azure SQL-Datenbank zugewiesen ist</span><span class="sxs-lookup"><span data-stu-id="6274c-109">Example 1: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database</span></span>
```
PS C:\>Get-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :  

ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="6274c-110">Dieser Befehl ruft Informationen zu allen Azure SQL-Daten Bank Synchronisierungsgruppen ab, die einer Azure SQL-Datenbank zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="6274c-110">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database.</span></span>

### <span data-ttu-id="6274c-111">Beispiel 2: Abrufen von Informationen zu einer Azure SQL-Daten Bank Synchronisierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="6274c-111">Example 2: Get information about an Azure SQL Database Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="6274c-112">Dieser Befehl ruft Informationen zur Azure SQL-Daten Bank Synchronisierungsgruppe mit dem Namen "SyncGroup01" ab.</span><span class="sxs-lookup"><span data-stu-id="6274c-112">This command gets information about the Azure SQL Database Sync Group with name "SyncGroup01"</span></span>

### <span data-ttu-id="6274c-113">Beispiel 3: Abrufen aller Instanzen einer Azure SQL-Synchronisierungsgruppe, die einer Azure SQL-Datenbank mithilfe von Filtern zugewiesen ist</span><span class="sxs-lookup"><span data-stu-id="6274c-113">Example 3: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database using filtering</span></span>
```
PS C:\>Get-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup*" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :  

ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="6274c-114">Dieser Befehl ruft Informationen zu allen Azure SQL-Daten Bank Synchronisierungsgruppen ab, die einer Azure SQL-Datenbank zugewiesen sind, die mit "SyncGroup" beginnen.</span><span class="sxs-lookup"><span data-stu-id="6274c-114">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database that start with "SyncGroup".</span></span>

## <span data-ttu-id="6274c-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="6274c-115">PARAMETERS</span></span>

### <span data-ttu-id="6274c-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6274c-116">-DatabaseName</span></span>
<span data-ttu-id="6274c-117">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="6274c-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="6274c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6274c-118">-DefaultProfile</span></span>
<span data-ttu-id="6274c-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6274c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6274c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6274c-120">-Name</span></span>
<span data-ttu-id="6274c-121">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="6274c-121">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="6274c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6274c-122">-ResourceGroupName</span></span>
<span data-ttu-id="6274c-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6274c-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="6274c-124">-Servername</span><span class="sxs-lookup"><span data-stu-id="6274c-124">-ServerName</span></span>
<span data-ttu-id="6274c-125">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6274c-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="6274c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6274c-126">CommonParameters</span></span>
<span data-ttu-id="6274c-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6274c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6274c-128">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6274c-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6274c-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6274c-129">INPUTS</span></span>

### <span data-ttu-id="6274c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6274c-130">System.String</span></span>

## <span data-ttu-id="6274c-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6274c-131">OUTPUTS</span></span>

### <span data-ttu-id="6274c-132">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="6274c-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="6274c-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="6274c-133">NOTES</span></span>

## <span data-ttu-id="6274c-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6274c-134">RELATED LINKS</span></span>

[<span data-ttu-id="6274c-135">Neu – AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="6274c-135">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="6274c-136">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="6274c-136">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="6274c-137">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="6274c-137">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

