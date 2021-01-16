---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncSchema.md
ms.openlocfilehash: 7dc07f1064837b710c246e4aafb4ceb008019e4e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291833"
---
# <span data-ttu-id="1573a-101">Get-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="1573a-101">Get-AzSqlSyncSchema</span></span>

## <span data-ttu-id="1573a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1573a-102">SYNOPSIS</span></span>
<span data-ttu-id="1573a-103">Gibt Informationen zum Synchronisierungsschema einer Memberdatenbank oder Hubdatenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="1573a-103">Returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="1573a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1573a-104">SYNTAX</span></span>

```
Get-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1573a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1573a-105">DESCRIPTION</span></span>
<span data-ttu-id="1573a-106">Das **Cmdlet "Get-AzSqlSyncSchema"** gibt Informationen zum Synchronisierungsschema einer Memberdatenbank oder Hubdatenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="1573a-106">The **Get-AzSqlSyncSchema** cmdlet returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="1573a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1573a-107">EXAMPLES</span></span>

### <span data-ttu-id="1573a-108">Beispiel 1: Erhalten des Synchronisierungsschemas für eine Hubdatenbank</span><span class="sxs-lookup"><span data-stu-id="1573a-108">Example 1: Get the sync schema for a hub database</span></span>
```powershell
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
Tables                     LastUpdateTime
------                     --------------
{dbo.Table_1, dbo.Table_2} 6/13/2017 10:03:44 AM
```

<span data-ttu-id="1573a-109">Dieser Befehl ruft das Synchronisierungsschema für die Hubdatenbank in der Synchronisierungsgruppe syncGroup01 ab.</span><span class="sxs-lookup"><span data-stu-id="1573a-109">This command gets the sync schema for the hub database in the sync group syncGroup01.</span></span>

### <span data-ttu-id="1573a-110">Beispiel 2: Erhalten des Synchronisierungsschemas für eine Hubdatenbank und Erweitern von Tabellen</span><span class="sxs-lookup"><span data-stu-id="1573a-110">Example 2: Get the sync schema for a hub database, and expand Tables</span></span>
```powershell
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

<span data-ttu-id="1573a-111">Dieser Befehl ruft das Synchronisierungsschema für die Hubdatenbank in der Synchronisierungsgruppe syncGroup01 ab und erweitert die Eigenschaft "Tabellen".</span><span class="sxs-lookup"><span data-stu-id="1573a-111">This command gets the sync schema for the hub database in the sync group syncGroup01 and expand Tables property.</span></span>

### <span data-ttu-id="1573a-112">Beispiel 3: Erhalten des Synchronisierungsschemas für eine Memberdatenbank</span><span class="sxs-lookup"><span data-stu-id="1573a-112">Example 3: Get the sync schema for a member database</span></span>
```powershell
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
The schema payload is the same as Example 1.
```

<span data-ttu-id="1573a-113">Dieser Befehl ruft das Synchronisierungsschema für die Memberdatenbank im Synchronisierungsmember01 ab.</span><span class="sxs-lookup"><span data-stu-id="1573a-113">This command gets the sync schema for the member database in the sync member syncMember01.</span></span>

## <span data-ttu-id="1573a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1573a-114">PARAMETERS</span></span>

### <span data-ttu-id="1573a-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1573a-115">-DatabaseName</span></span>
<span data-ttu-id="1573a-116">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="1573a-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="1573a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1573a-117">-DefaultProfile</span></span>
<span data-ttu-id="1573a-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="1573a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1573a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1573a-119">-ResourceGroupName</span></span>
<span data-ttu-id="1573a-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1573a-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="1573a-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1573a-121">-ServerName</span></span>
<span data-ttu-id="1573a-122">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1573a-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="1573a-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="1573a-123">-SyncGroupName</span></span>
<span data-ttu-id="1573a-124">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="1573a-124">The sync group name.</span></span>

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

### <span data-ttu-id="1573a-125">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="1573a-125">-SyncMemberName</span></span>
<span data-ttu-id="1573a-126">Der Name des Synchronisierungsmitglieds.</span><span class="sxs-lookup"><span data-stu-id="1573a-126">The sync member name.</span></span>

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

### <span data-ttu-id="1573a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1573a-127">CommonParameters</span></span>
<span data-ttu-id="1573a-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1573a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1573a-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1573a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1573a-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1573a-130">INPUTS</span></span>

### <span data-ttu-id="1573a-131">System.String</span><span class="sxs-lookup"><span data-stu-id="1573a-131">System.String</span></span>

## <span data-ttu-id="1573a-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1573a-132">OUTPUTS</span></span>

### <span data-ttu-id="1573a-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span><span class="sxs-lookup"><span data-stu-id="1573a-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span></span>

## <span data-ttu-id="1573a-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1573a-134">NOTES</span></span>

## <span data-ttu-id="1573a-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1573a-135">RELATED LINKS</span></span>
