---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationSyncSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
ms.openlocfilehash: d045e25c754dc852bed127b4361d3d7eb584022b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148105"
---
# <span data-ttu-id="4ae7a-101">New-AzDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="4ae7a-101">New-AzDataMigrationSyncSelectedDBObject</span></span>

## <span data-ttu-id="4ae7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ae7a-102">SYNOPSIS</span></span>
<span data-ttu-id="4ae7a-103">Erstellt ein Datenbankinformationsobjekt speziell für das Synchronisierungsszenario, das für eine Migrationsaufgabe verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4ae7a-103">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

## <span data-ttu-id="4ae7a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ae7a-104">SYNTAX</span></span>

```
New-AzDataMigrationSyncSelectedDBObject -TargetDatabaseName <String> -SchemaName <String> -TableMap <Hashtable>
 [-MigrationSetting <Hashtable>] [-SourceSetting <Hashtable>] [-TargetSetting <Hashtable>]
 -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ae7a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ae7a-105">DESCRIPTION</span></span>

<span data-ttu-id="4ae7a-106">Das New-AzDataMigrationSyncSelectedDB erstellt ein spezielles Datenbankinformationsobjekt für das Synchronisierungsszenario, das Informationen zu Quell- und Zieldatenbanken enthält.</span><span class="sxs-lookup"><span data-stu-id="4ae7a-106">The New-AzDataMigrationSyncSelectedDB cmdlet creates a database info object specific to the sync scenario which contains information about source and target databases.</span></span>

## <span data-ttu-id="4ae7a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4ae7a-107">EXAMPLES</span></span>

### <span data-ttu-id="4ae7a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4ae7a-108">Example 1</span></span>
```
PS C:\> $tableMap = New-Object 'system.collections.hashtable'
    $tableMap.Add("dbo.TestTable1", "dbo.TestTable1")
    $tableMap.Add("dbo.TestTable2","dbo.TestTable2")

    $selectedDbs = New-AzDmsSyncSelectedDBObject 
        -TargetDatabaseName DatabaseName `
        -SchemaName dbo `
        -TableMap $tableMap `
        -SourceDatabaseName DatabaseName
```

<span data-ttu-id="4ae7a-109">In diesem Beispiel wird ein Datenbankmetadatenobjekt erstellt, das die Migration von Einstellungen für $DatabaseName Datenbank $DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="4ae7a-109">This example creates a database metadata object describing the migrating settings for $DatabaseName to database $DatabaseName.</span></span>  

## <span data-ttu-id="4ae7a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ae7a-110">PARAMETERS</span></span>

### <span data-ttu-id="4ae7a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ae7a-111">-DefaultProfile</span></span>
<span data-ttu-id="4ae7a-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4ae7a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ae7a-113">-MigrationSetting</span><span class="sxs-lookup"><span data-stu-id="4ae7a-113">-MigrationSetting</span></span>
<span data-ttu-id="4ae7a-114">Migrationseinstellungen, die das Migrationsverhalten optimieren</span><span class="sxs-lookup"><span data-stu-id="4ae7a-114">Migration settings which tune the migration behavior</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ae7a-115">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="4ae7a-115">-SchemaName</span></span>
<span data-ttu-id="4ae7a-116">Zu migrierende Schemaname</span><span class="sxs-lookup"><span data-stu-id="4ae7a-116">Schema name to be migrated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ae7a-117">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="4ae7a-117">-SourceDatabaseName</span></span>
<span data-ttu-id="4ae7a-118">Der Name der Quelldatenbank.</span><span class="sxs-lookup"><span data-stu-id="4ae7a-118">The name of the source database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ae7a-119">-SourceSetting</span><span class="sxs-lookup"><span data-stu-id="4ae7a-119">-SourceSetting</span></span>
<span data-ttu-id="4ae7a-120">Quelleinstellungen zum Optimieren des Migrationsverhaltens des Quellendpunkts</span><span class="sxs-lookup"><span data-stu-id="4ae7a-120">Source settings to tune source endpoint migration behavior</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ae7a-121">-TableMap</span><span class="sxs-lookup"><span data-stu-id="4ae7a-121">-TableMap</span></span>
<span data-ttu-id="4ae7a-122">Zuordnung von Quelle zu Zieltabellen</span><span class="sxs-lookup"><span data-stu-id="4ae7a-122">Mapping of source to target tables</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ae7a-123">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="4ae7a-123">-TargetDatabaseName</span></span>
<span data-ttu-id="4ae7a-124">Der Name der Zieldatenbank</span><span class="sxs-lookup"><span data-stu-id="4ae7a-124">The name of the target database</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ae7a-125">-TargetSetting</span><span class="sxs-lookup"><span data-stu-id="4ae7a-125">-TargetSetting</span></span>
<span data-ttu-id="4ae7a-126">Zieleinstellungen zum Optimieren des Migrationsverhaltens des Zielendpunkts</span><span class="sxs-lookup"><span data-stu-id="4ae7a-126">Target settings to tune target endpoint migration behavior</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ae7a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ae7a-127">CommonParameters</span></span>
<span data-ttu-id="4ae7a-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ae7a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ae7a-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ae7a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ae7a-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4ae7a-130">INPUTS</span></span>

### <span data-ttu-id="4ae7a-131">Keine</span><span class="sxs-lookup"><span data-stu-id="4ae7a-131">None</span></span>

## <span data-ttu-id="4ae7a-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4ae7a-132">OUTPUTS</span></span>

### <span data-ttu-id="4ae7a-133">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbSyncTaskInput</span><span class="sxs-lookup"><span data-stu-id="4ae7a-133">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbSyncTaskInput</span></span>

## <span data-ttu-id="4ae7a-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4ae7a-134">NOTES</span></span>

## <span data-ttu-id="4ae7a-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4ae7a-135">RELATED LINKS</span></span>
