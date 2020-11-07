---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncSchema.md
ms.openlocfilehash: 7e6e060b2ad9e05a0a2789202e74f093f0366749
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826035"
---
# <span data-ttu-id="7de46-101">Get-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="7de46-101">Get-AzSqlSyncSchema</span></span>

## <span data-ttu-id="7de46-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7de46-102">SYNOPSIS</span></span>
<span data-ttu-id="7de46-103">Gibt Informationen zum Synchronisierungs Schema einer Mitgliedsdatenbank oder einer Hub-Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="7de46-103">Returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="7de46-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7de46-104">SYNTAX</span></span>

```
Get-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7de46-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7de46-105">DESCRIPTION</span></span>
<span data-ttu-id="7de46-106">Das Cmdlet " **Get-AzSqlSyncSchema** " gibt Informationen zum Synchronisierungs Schema einer Mitgliedsdatenbank oder einer Hub-Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="7de46-106">The **Get-AzSqlSyncSchema** cmdlet returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="7de46-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7de46-107">EXAMPLES</span></span>

### <span data-ttu-id="7de46-108">Beispiel 1,1: Abrufen des Synchronisierungsschemas für eine Hub-Datenbank</span><span class="sxs-lookup"><span data-stu-id="7de46-108">Example 1.1: Get the sync schema for a hub database</span></span>
```
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
Tables                     LastUpdateTime
------                     --------------
{dbo.Table_1, dbo.Table_2} 6/13/2017 10:03:44 AM
```

<span data-ttu-id="7de46-109">Dieser Befehl ruft das Synchronisierungs Schema für die Hub-Datenbank in der syncGroup01-Synchronisierungsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="7de46-109">This command gets the sync schema for the hub database in the sync group syncGroup01.</span></span>

### <span data-ttu-id="7de46-110">Beispiel 1,2: Abrufen des Synchronisierungsschemas für eine Hub-Datenbank und Erweitern von Tabellen</span><span class="sxs-lookup"><span data-stu-id="7de46-110">Example 1.2: Get the sync schema for a hub database, and expand Tables</span></span>
```
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"  | select -ExpandProperty Tables
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

<span data-ttu-id="7de46-111">Dieser Befehl ruft das Synchronisierungs Schema für die Hub-Datenbank in der Synchronisierungsgruppe syncGroup01 und Expand Tables-Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="7de46-111">This command gets the sync schema for the hub database in the sync group syncGroup01 and expand Tables property.</span></span>

### <span data-ttu-id="7de46-112">Beispiel 2: Abrufen des Synchronisierungsschemas für eine Mitgliedsdatenbank</span><span class="sxs-lookup"><span data-stu-id="7de46-112">Example 2: Get the sync schema for a member database</span></span>
```
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
The schema payload is the same as Example 1.
```

<span data-ttu-id="7de46-113">Dieser Befehl ruft das Synchronisierungs Schema für die Mitgliedsdatenbank im Synchronisierungs Member syncMember01 ab.</span><span class="sxs-lookup"><span data-stu-id="7de46-113">This command gets the sync schema for the member database in the sync member syncMember01.</span></span>

## <span data-ttu-id="7de46-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="7de46-114">PARAMETERS</span></span>

### <span data-ttu-id="7de46-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7de46-115">-DatabaseName</span></span>
<span data-ttu-id="7de46-116">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="7de46-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="7de46-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7de46-117">-DefaultProfile</span></span>
<span data-ttu-id="7de46-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7de46-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7de46-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7de46-119">-ResourceGroupName</span></span>
<span data-ttu-id="7de46-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7de46-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="7de46-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="7de46-121">-ServerName</span></span>
<span data-ttu-id="7de46-122">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7de46-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="7de46-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="7de46-123">-SyncGroupName</span></span>
<span data-ttu-id="7de46-124">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="7de46-124">The sync group name.</span></span>

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

### <span data-ttu-id="7de46-125">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="7de46-125">-SyncMemberName</span></span>
<span data-ttu-id="7de46-126">Der Name des Synchronisierungs Mitglieds.</span><span class="sxs-lookup"><span data-stu-id="7de46-126">The sync member name.</span></span>

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

### <span data-ttu-id="7de46-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7de46-127">CommonParameters</span></span>
<span data-ttu-id="7de46-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7de46-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7de46-129">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7de46-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7de46-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7de46-130">INPUTS</span></span>

### <span data-ttu-id="7de46-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7de46-131">System.String</span></span>

## <span data-ttu-id="7de46-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7de46-132">OUTPUTS</span></span>

### <span data-ttu-id="7de46-133">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncFullSchemaModel</span><span class="sxs-lookup"><span data-stu-id="7de46-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span></span>

## <span data-ttu-id="7de46-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="7de46-134">NOTES</span></span>

## <span data-ttu-id="7de46-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7de46-135">RELATED LINKS</span></span>
