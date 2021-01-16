---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
ms.openlocfilehash: d117ef9685a235528cb91c82a148ff0dddb2d96c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364354"
---
# <span data-ttu-id="be46a-101">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="be46a-101">Get-AzSqlSyncGroup</span></span>

## <span data-ttu-id="be46a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be46a-102">SYNOPSIS</span></span>
<span data-ttu-id="be46a-103">Gibt Informationen zu Azure SQL Datenbanksynchronisierungsgruppen zurück.</span><span class="sxs-lookup"><span data-stu-id="be46a-103">Returns information about Azure SQL Database Sync Groups.</span></span>

## <span data-ttu-id="be46a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="be46a-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroup [[-Name] <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be46a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="be46a-105">DESCRIPTION</span></span>
<span data-ttu-id="be46a-106">Das **Cmdlet "Get-AzSqlSyncGroup"** gibt Informationen zu einer oder mehreren Azure SQL Database Sync Groups zurück.</span><span class="sxs-lookup"><span data-stu-id="be46a-106">The **Get-AzSqlSyncGroup** cmdlet returns information about one or more Azure SQL Database Sync Groups.</span></span>
<span data-ttu-id="be46a-107">Geben Sie den Namen einer Synchronisierungsgruppe an, um nur Informationen für diese Synchronisierungsgruppe zu sehen.</span><span class="sxs-lookup"><span data-stu-id="be46a-107">Specify the name of a sync group to see information for only that sync group.</span></span>

## <span data-ttu-id="be46a-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="be46a-108">EXAMPLES</span></span>

### <span data-ttu-id="be46a-109">Beispiel 1: Alle Instanzen von Azure SQL-Synchronisierungsgruppe, die einer Azure SQL werden</span><span class="sxs-lookup"><span data-stu-id="be46a-109">Example 1: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database</span></span>
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

<span data-ttu-id="be46a-110">Dieser Befehl ruft Informationen zu allen Azure SQL-Datenbanksynchronisierungsgruppen ab, die einer Azure SQL werden.</span><span class="sxs-lookup"><span data-stu-id="be46a-110">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database.</span></span>

### <span data-ttu-id="be46a-111">Beispiel 2: Informationen zu einer Azure SQL Database Sync Group</span><span class="sxs-lookup"><span data-stu-id="be46a-111">Example 2: Get information about an Azure SQL Database Sync Group</span></span>
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

<span data-ttu-id="be46a-112">Dieser Befehl ruft Informationen zur Azure SQL-Datenbanksynchronisierungsgruppe mit dem Namen "SyncGroup01" ab.</span><span class="sxs-lookup"><span data-stu-id="be46a-112">This command gets information about the Azure SQL Database Sync Group with name "SyncGroup01"</span></span>

### <span data-ttu-id="be46a-113">Beispiel 3: Erhalten aller Instanzen von Azure SQL-Synchronisierungsgruppe, die einer Azure SQL mithilfe von Filtern zugewiesen wurden</span><span class="sxs-lookup"><span data-stu-id="be46a-113">Example 3: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database using filtering</span></span>
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

<span data-ttu-id="be46a-114">Dieser Befehl ruft Informationen zu allen Azure SQL-Datenbanksynchronisierungsgruppen ab, die einer Azure SQL-Datenbank zugewiesen sind und mit "Synchronisierungsgruppe" beginnen.</span><span class="sxs-lookup"><span data-stu-id="be46a-114">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database that start with "SyncGroup".</span></span>

## <span data-ttu-id="be46a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be46a-115">PARAMETERS</span></span>

### <span data-ttu-id="be46a-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="be46a-116">-DatabaseName</span></span>
<span data-ttu-id="be46a-117">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="be46a-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="be46a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be46a-118">-DefaultProfile</span></span>
<span data-ttu-id="be46a-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="be46a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be46a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="be46a-120">-Name</span></span>
<span data-ttu-id="be46a-121">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="be46a-121">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be46a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be46a-122">-ResourceGroupName</span></span>
<span data-ttu-id="be46a-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="be46a-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="be46a-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="be46a-124">-ServerName</span></span>
<span data-ttu-id="be46a-125">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="be46a-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="be46a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be46a-126">CommonParameters</span></span>
<span data-ttu-id="be46a-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be46a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be46a-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be46a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be46a-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="be46a-129">INPUTS</span></span>

### <span data-ttu-id="be46a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="be46a-130">System.String</span></span>

## <span data-ttu-id="be46a-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="be46a-131">OUTPUTS</span></span>

### <span data-ttu-id="be46a-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="be46a-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="be46a-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="be46a-133">NOTES</span></span>

## <span data-ttu-id="be46a-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="be46a-134">RELATED LINKS</span></span>

[<span data-ttu-id="be46a-135">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="be46a-135">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="be46a-136">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="be46a-136">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="be46a-137">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="be46a-137">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

