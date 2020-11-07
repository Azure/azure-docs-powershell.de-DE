---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationSyncSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
ms.openlocfilehash: d045e25c754dc852bed127b4361d3d7eb584022b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845315"
---
# <span data-ttu-id="a09b9-101">New-AzDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="a09b9-101">New-AzDataMigrationSyncSelectedDBObject</span></span>

## <span data-ttu-id="a09b9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a09b9-102">SYNOPSIS</span></span>
<span data-ttu-id="a09b9-103">Erstellt ein spezifisches DatenbankInfo Objekt für das Synchronisierungsszenario, das für eine Migrationsaufgabe verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a09b9-103">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

## <span data-ttu-id="a09b9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a09b9-104">SYNTAX</span></span>

```
New-AzDataMigrationSyncSelectedDBObject -TargetDatabaseName <String> -SchemaName <String> -TableMap <Hashtable>
 [-MigrationSetting <Hashtable>] [-SourceSetting <Hashtable>] [-TargetSetting <Hashtable>]
 -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a09b9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a09b9-105">DESCRIPTION</span></span>

<span data-ttu-id="a09b9-106">Das New-AzDataMigrationSyncSelectedDB-Cmdlet erstellt ein für das Synchronisierungsszenario spezifisches Daten Bank Informationsobjekt, das Informationen zu Quell-und Zieldatenbanken enthält.</span><span class="sxs-lookup"><span data-stu-id="a09b9-106">The New-AzDataMigrationSyncSelectedDB cmdlet creates a database info object specific to the sync scenario which contains information about source and target databases.</span></span>

## <span data-ttu-id="a09b9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a09b9-107">EXAMPLES</span></span>

### <span data-ttu-id="a09b9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a09b9-108">Example 1</span></span>
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

<span data-ttu-id="a09b9-109">In diesem Beispiel wird ein Datenbankmetadaten-Objekt erstellt, das die Migrationseinstellungen für $DatabaseName zu Daten Bank $DatabaseName beschreibt.</span><span class="sxs-lookup"><span data-stu-id="a09b9-109">This example creates a database metadata object describing the migrating settings for $DatabaseName to database $DatabaseName.</span></span>  

## <span data-ttu-id="a09b9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a09b9-110">PARAMETERS</span></span>

### <span data-ttu-id="a09b9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a09b9-111">-DefaultProfile</span></span>
<span data-ttu-id="a09b9-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a09b9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a09b9-113">-MigrationSetting</span><span class="sxs-lookup"><span data-stu-id="a09b9-113">-MigrationSetting</span></span>
<span data-ttu-id="a09b9-114">Migrationseinstellungen, die das Migrationsverhalten optimieren</span><span class="sxs-lookup"><span data-stu-id="a09b9-114">Migration settings which tune the migration behavior</span></span>

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

### <span data-ttu-id="a09b9-115">-Schemaname</span><span class="sxs-lookup"><span data-stu-id="a09b9-115">-SchemaName</span></span>
<span data-ttu-id="a09b9-116">Zu migrierender Schema Name</span><span class="sxs-lookup"><span data-stu-id="a09b9-116">Schema name to be migrated</span></span>

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

### <span data-ttu-id="a09b9-117">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="a09b9-117">-SourceDatabaseName</span></span>
<span data-ttu-id="a09b9-118">Der Name der Quelldatenbank.</span><span class="sxs-lookup"><span data-stu-id="a09b9-118">The name of the source database.</span></span>

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

### <span data-ttu-id="a09b9-119">-SourceSetting</span><span class="sxs-lookup"><span data-stu-id="a09b9-119">-SourceSetting</span></span>
<span data-ttu-id="a09b9-120">Quelleinstellungen zum Optimieren des Migrations Verhaltens von Quellendpunkt</span><span class="sxs-lookup"><span data-stu-id="a09b9-120">Source settings to tune source endpoint migration behavior</span></span>

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

### <span data-ttu-id="a09b9-121">-TableMap</span><span class="sxs-lookup"><span data-stu-id="a09b9-121">-TableMap</span></span>
<span data-ttu-id="a09b9-122">Zuordnung von Quell-zu Zieltabellen</span><span class="sxs-lookup"><span data-stu-id="a09b9-122">Mapping of source to target tables</span></span>

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

### <span data-ttu-id="a09b9-123">-Zieldatenbankname</span><span class="sxs-lookup"><span data-stu-id="a09b9-123">-TargetDatabaseName</span></span>
<span data-ttu-id="a09b9-124">Der Name der Zieldatenbank</span><span class="sxs-lookup"><span data-stu-id="a09b9-124">The name of the target database</span></span>

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

### <span data-ttu-id="a09b9-125">-TargetSetting</span><span class="sxs-lookup"><span data-stu-id="a09b9-125">-TargetSetting</span></span>
<span data-ttu-id="a09b9-126">Zieleinstellungen zum Optimieren des Migrations Verhaltens von Zielendpunkt</span><span class="sxs-lookup"><span data-stu-id="a09b9-126">Target settings to tune target endpoint migration behavior</span></span>

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

### <span data-ttu-id="a09b9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a09b9-127">CommonParameters</span></span>
<span data-ttu-id="a09b9-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a09b9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a09b9-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a09b9-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a09b9-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a09b9-130">INPUTS</span></span>

### <span data-ttu-id="a09b9-131">Keine</span><span class="sxs-lookup"><span data-stu-id="a09b9-131">None</span></span>

## <span data-ttu-id="a09b9-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a09b9-132">OUTPUTS</span></span>

### <span data-ttu-id="a09b9-133">Microsoft. Azure. Management. datamigration. Models. MigrateSqlServerSqlDbSyncTaskInput</span><span class="sxs-lookup"><span data-stu-id="a09b9-133">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbSyncTaskInput</span></span>

## <span data-ttu-id="a09b9-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="a09b9-134">NOTES</span></span>

## <span data-ttu-id="a09b9-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a09b9-135">RELATED LINKS</span></span>
