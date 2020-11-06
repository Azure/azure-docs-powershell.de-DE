---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncSchema.md
ms.openlocfilehash: ef66de2b12cf0ea723540c392a296d2d1c482505
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478874"
---
# <span data-ttu-id="9d8e8-101">Get-AzureRmSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="9d8e8-101">Get-AzureRmSqlSyncSchema</span></span>

## <span data-ttu-id="9d8e8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9d8e8-102">SYNOPSIS</span></span>
<span data-ttu-id="9d8e8-103">Gibt Informationen zum Synchronisierungs Schema einer Mitgliedsdatenbank oder einer Hub-Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="9d8e8-103">Returns information about the sync schema of a member database or a hub database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d8e8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d8e8-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d8e8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d8e8-105">DESCRIPTION</span></span>
<span data-ttu-id="9d8e8-106">Das Cmdlet " **Get-AzureRmSqlSyncSchema** " gibt Informationen zum Synchronisierungs Schema einer Mitgliedsdatenbank oder einer Hub-Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="9d8e8-106">The **Get-AzureRmSqlSyncSchema** cmdlet returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="9d8e8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9d8e8-107">EXAMPLES</span></span>

### <span data-ttu-id="9d8e8-108">Beispiel 1,1: Abrufen des Synchronisierungsschemas für eine Hub-Datenbank</span><span class="sxs-lookup"><span data-stu-id="9d8e8-108">Example 1.1: Get the sync schema for a hub database</span></span>
```
PS C:\>Get-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
Tables                     LastUpdateTime
------                     --------------
{dbo.Table_1, dbo.Table_2} 6/13/2017 10:03:44 AM
```

<span data-ttu-id="9d8e8-109">Dieser Befehl ruft das Synchronisierungs Schema für die Hub-Datenbank in der syncGroup01-Synchronisierungsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="9d8e8-109">This command gets the sync schema for the hub database in the sync group syncGroup01.</span></span>

### <span data-ttu-id="9d8e8-110">Beispiel 1,2: Abrufen des Synchronisierungsschemas für eine Hub-Datenbank und Erweitern von Tabellen</span><span class="sxs-lookup"><span data-stu-id="9d8e8-110">Example 1.2: Get the sync schema for a hub database, and expand Tables</span></span>
```
PS C:\>Get-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"  | select -ExpandProperty Tables
Columns    : {column1, column2}
ErrorId    : Schema_TableHasNoPrimaryKey
HasError   : True
Name       : dbo.Table_1
QuotedName : [dbo].[Table_1]

Columns    : {column2, column4}
ErrorId    : Schema_TableHasNoPrimaryKey
HasError   : True
Name       : dbo.Table_2
QuotedName : [dbo].[Table_2]
```

<span data-ttu-id="9d8e8-111">Dieser Befehl ruft das Synchronisierungs Schema für die Hub-Datenbank in der Synchronisierungsgruppe syncGroup01 und Expand Tables-Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="9d8e8-111">This command gets the sync schema for the hub database in the sync group syncGroup01 and expand Tables property.</span></span>

### <span data-ttu-id="9d8e8-112">Beispiel 2: Abrufen des Synchronisierungsschemas für eine Mitgliedsdatenbank</span><span class="sxs-lookup"><span data-stu-id="9d8e8-112">Example 2: Get the sync schema for a member database</span></span>
```
PS C:\>Get-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
The schema payload is the same as Example 1.
```

<span data-ttu-id="9d8e8-113">Dieser Befehl ruft das Synchronisierungs Schema für die Mitgliedsdatenbank im Synchronisierungs Member syncMember01 ab.</span><span class="sxs-lookup"><span data-stu-id="9d8e8-113">This command gets the sync schema for the member database in the sync member syncMember01.</span></span>

## <span data-ttu-id="9d8e8-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d8e8-114">PARAMETERS</span></span>

### <span data-ttu-id="9d8e8-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9d8e8-115">-DatabaseName</span></span>
<span data-ttu-id="9d8e8-116">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="9d8e8-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="9d8e8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d8e8-117">-ResourceGroupName</span></span>
<span data-ttu-id="9d8e8-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9d8e8-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="9d8e8-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="9d8e8-119">-ServerName</span></span>
<span data-ttu-id="9d8e8-120">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9d8e8-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="9d8e8-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="9d8e8-121">-SyncGroupName</span></span>
<span data-ttu-id="9d8e8-122">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9d8e8-122">The sync group name.</span></span>

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

### <span data-ttu-id="9d8e8-123">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="9d8e8-123">-SyncMemberName</span></span>
<span data-ttu-id="9d8e8-124">Der Name des Synchronisierungs Mitglieds.</span><span class="sxs-lookup"><span data-stu-id="9d8e8-124">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d8e8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d8e8-125">-DefaultProfile</span></span>
<span data-ttu-id="9d8e8-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9d8e8-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d8e8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d8e8-127">CommonParameters</span></span>
<span data-ttu-id="9d8e8-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d8e8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d8e8-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d8e8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d8e8-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9d8e8-130">INPUTS</span></span>

## <span data-ttu-id="9d8e8-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9d8e8-131">OUTPUTS</span></span>

### <span data-ttu-id="9d8e8-132">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncFullSchemaModel</span><span class="sxs-lookup"><span data-stu-id="9d8e8-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span></span>

### <span data-ttu-id="9d8e8-133">Tabellen: Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncFullSchemaTableModel</span><span class="sxs-lookup"><span data-stu-id="9d8e8-133">Tables: Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaTableModel</span></span>

### <span data-ttu-id="9d8e8-134">Columns: Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncFullSchemaColumnModel</span><span class="sxs-lookup"><span data-stu-id="9d8e8-134">Columns: Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaColumnModel</span></span>

## <span data-ttu-id="9d8e8-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="9d8e8-135">NOTES</span></span>

## <span data-ttu-id="9d8e8-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9d8e8-136">RELATED LINKS</span></span>

