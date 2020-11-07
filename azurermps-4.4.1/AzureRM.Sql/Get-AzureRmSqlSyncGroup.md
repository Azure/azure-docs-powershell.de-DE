---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroup.md
ms.openlocfilehash: e581f0bd94e58f725055c0dc1a4f1d704b891c86
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662397"
---
# <span data-ttu-id="75af6-101">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="75af6-101">Get-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="75af6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="75af6-102">SYNOPSIS</span></span>
<span data-ttu-id="75af6-103">Gibt Informationen zu Azure SQL-Daten Bank Synchronisierungsgruppen zurück.</span><span class="sxs-lookup"><span data-stu-id="75af6-103">Returns information about Azure SQL Database Sync Groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75af6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="75af6-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncGroup [[-Name] <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75af6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75af6-105">DESCRIPTION</span></span>
<span data-ttu-id="75af6-106">Das Cmdlet " **Get-AzureRmSqlSyncGroup** " gibt Informationen zu mindestens einer Azure SQL-Daten Bank Synchronisierungsgruppe zurück.</span><span class="sxs-lookup"><span data-stu-id="75af6-106">The **Get-AzureRmSqlSyncGroup** cmdlet returns information about one or more Azure SQL Database Sync Groups.</span></span>
<span data-ttu-id="75af6-107">Geben Sie den Namen einer Synchronisierungsgruppe an, um Informationen nur für diese Synchronisierungsgruppe anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="75af6-107">Specify the name of a sync group to see information for only that sync group.</span></span>

## <span data-ttu-id="75af6-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75af6-108">EXAMPLES</span></span>

### <span data-ttu-id="75af6-109">Beispiel 1: Abrufen aller Instanzen einer Azure SQL-Synchronisierungsgruppe, die einer Azure SQL-Datenbank zugewiesen ist</span><span class="sxs-lookup"><span data-stu-id="75af6-109">Example 1: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database</span></span>
```
PS C:\>Get-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Format-List
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

<span data-ttu-id="75af6-110">Dieser Befehl ruft Informationen zu allen Azure SQL-Daten Bank Synchronisierungsgruppen ab, die einer Azure SQL-Datenbank zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="75af6-110">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database.</span></span>

### <span data-ttu-id="75af6-111">Beispiel 2: Abrufen von Informationen zu einer Azure SQL-Daten Bank Synchronisierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="75af6-111">Example 2: Get information about an Azure SQL Database Sync Group</span></span>
```
PS C:\>Get-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" | Format-List
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

<span data-ttu-id="75af6-112">Dieser Befehl ruft Informationen zur Azure SQL-Daten Bank Synchronisierungsgruppe mit dem Namen "SyncGroup01" ab.</span><span class="sxs-lookup"><span data-stu-id="75af6-112">This command gets information about the Azure SQL Database Sync Group with name "SyncGroup01"</span></span>

## <span data-ttu-id="75af6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="75af6-113">PARAMETERS</span></span>

### <span data-ttu-id="75af6-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="75af6-114">-DatabaseName</span></span>
<span data-ttu-id="75af6-115">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="75af6-115">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="75af6-116">-Name</span><span class="sxs-lookup"><span data-stu-id="75af6-116">-Name</span></span>
<span data-ttu-id="75af6-117">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="75af6-117">The sync group name.</span></span>

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

### <span data-ttu-id="75af6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75af6-118">-ResourceGroupName</span></span>
<span data-ttu-id="75af6-119">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="75af6-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="75af6-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="75af6-120">-ServerName</span></span>
<span data-ttu-id="75af6-121">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="75af6-121">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="75af6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75af6-122">-DefaultProfile</span></span>
<span data-ttu-id="75af6-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="75af6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75af6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75af6-124">CommonParameters</span></span>
<span data-ttu-id="75af6-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75af6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75af6-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75af6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75af6-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="75af6-127">INPUTS</span></span>

## <span data-ttu-id="75af6-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="75af6-128">OUTPUTS</span></span>

### <span data-ttu-id="75af6-129">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="75af6-129">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="75af6-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="75af6-130">NOTES</span></span>

## <span data-ttu-id="75af6-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="75af6-131">RELATED LINKS</span></span>

[<span data-ttu-id="75af6-132">Neu – AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="75af6-132">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="75af6-133">Update-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="75af6-133">Update-AzureRmSqlSyncGroup</span></span>](./Update-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="75af6-134">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="75af6-134">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

