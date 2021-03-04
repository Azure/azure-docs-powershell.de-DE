---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncSchema.md
ms.openlocfilehash: e32f693b5f0bfc114f3ac40a4fc5761ec3a3ca70
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943283"
---
# <span data-ttu-id="f145b-101">Get-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="f145b-101">Get-AzSqlSyncSchema</span></span>

## <span data-ttu-id="f145b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f145b-102">SYNOPSIS</span></span>
<span data-ttu-id="f145b-103">Gibt Informationen zum Synchronisierungsschema einer Memberdatenbank oder Hubdatenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="f145b-103">Returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="f145b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f145b-104">SYNTAX</span></span>

```
Get-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f145b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f145b-105">DESCRIPTION</span></span>
<span data-ttu-id="f145b-106">Das **Get-AzSqlSyncSchema-Cmdlet** gibt Informationen zum Synchronisierungsschema einer Memberdatenbank oder Hubdatenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="f145b-106">The **Get-AzSqlSyncSchema** cmdlet returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="f145b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f145b-107">EXAMPLES</span></span>

### <span data-ttu-id="f145b-108">Beispiel 1: Erhalten des Synchronisierungsschemas für eine Hubdatenbank</span><span class="sxs-lookup"><span data-stu-id="f145b-108">Example 1: Get the sync schema for a hub database</span></span>
```powershell
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
Tables                     LastUpdateTime
------                     --------------
{dbo.Table_1, dbo.Table_2} 6/13/2017 10:03:44 AM
```

<span data-ttu-id="f145b-109">Dieser Befehl ruft das Synchronisierungsschema für die Hubdatenbank in der Synchronisierungsgruppe syncGroup01 ab.</span><span class="sxs-lookup"><span data-stu-id="f145b-109">This command gets the sync schema for the hub database in the sync group syncGroup01.</span></span>

### <span data-ttu-id="f145b-110">Beispiel 2: Holen Sie sich das Synchronisierungsschema für eine Hubdatenbank, und erweitern Sie Tabellen</span><span class="sxs-lookup"><span data-stu-id="f145b-110">Example 2: Get the sync schema for a hub database, and expand Tables</span></span>
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

<span data-ttu-id="f145b-111">Dieser Befehl ruft das Synchronisierungsschema für die Hubdatenbank in der Synchronisierungsgruppe syncGroup01 ab, und erweitern Sie die Eigenschaft Tabellen.</span><span class="sxs-lookup"><span data-stu-id="f145b-111">This command gets the sync schema for the hub database in the sync group syncGroup01 and expand Tables property.</span></span>

### <span data-ttu-id="f145b-112">Beispiel 3: Erhalten des Synchronisierungsschemas für eine Memberdatenbank</span><span class="sxs-lookup"><span data-stu-id="f145b-112">Example 3: Get the sync schema for a member database</span></span>
```powershell
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
The schema payload is the same as Example 1.
```

<span data-ttu-id="f145b-113">Dieser Befehl ruft das Synchronisierungsschema für die Memberdatenbank im Synchronisierungsmitglied syncMember01 ab.</span><span class="sxs-lookup"><span data-stu-id="f145b-113">This command gets the sync schema for the member database in the sync member syncMember01.</span></span>

## <span data-ttu-id="f145b-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f145b-114">PARAMETERS</span></span>

### <span data-ttu-id="f145b-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f145b-115">-DatabaseName</span></span>
<span data-ttu-id="f145b-116">Der Name der Azure SQL Datenbank.</span><span class="sxs-lookup"><span data-stu-id="f145b-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="f145b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f145b-117">-DefaultProfile</span></span>
<span data-ttu-id="f145b-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f145b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f145b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f145b-119">-ResourceGroupName</span></span>
<span data-ttu-id="f145b-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f145b-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="f145b-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="f145b-121">-ServerName</span></span>
<span data-ttu-id="f145b-122">Der Name der Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f145b-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="f145b-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="f145b-123">-SyncGroupName</span></span>
<span data-ttu-id="f145b-124">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f145b-124">The sync group name.</span></span>

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

### <span data-ttu-id="f145b-125">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="f145b-125">-SyncMemberName</span></span>
<span data-ttu-id="f145b-126">Der Name des Synchronisierungsmitglieds.</span><span class="sxs-lookup"><span data-stu-id="f145b-126">The sync member name.</span></span>

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

### <span data-ttu-id="f145b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f145b-127">CommonParameters</span></span>
<span data-ttu-id="f145b-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f145b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f145b-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f145b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f145b-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f145b-130">INPUTS</span></span>

### <span data-ttu-id="f145b-131">System.String</span><span class="sxs-lookup"><span data-stu-id="f145b-131">System.String</span></span>

## <span data-ttu-id="f145b-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f145b-132">OUTPUTS</span></span>

### <span data-ttu-id="f145b-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span><span class="sxs-lookup"><span data-stu-id="f145b-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span></span>

## <span data-ttu-id="f145b-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f145b-134">NOTES</span></span>

## <span data-ttu-id="f145b-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f145b-135">RELATED LINKS</span></span>
