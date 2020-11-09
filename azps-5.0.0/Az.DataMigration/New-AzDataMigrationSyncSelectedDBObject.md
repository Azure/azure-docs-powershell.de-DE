---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationSyncSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
ms.openlocfilehash: d045e25c754dc852bed127b4361d3d7eb584022b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297604"
---
# <span data-ttu-id="2741c-101">New-AzDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="2741c-101">New-AzDataMigrationSyncSelectedDBObject</span></span>

## <span data-ttu-id="2741c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2741c-102">SYNOPSIS</span></span>
<span data-ttu-id="2741c-103">Erstellt ein spezifisches DatenbankInfo Objekt für das Synchronisierungsszenario, das für eine Migrationsaufgabe verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2741c-103">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

## <span data-ttu-id="2741c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2741c-104">SYNTAX</span></span>

```
New-AzDataMigrationSyncSelectedDBObject -TargetDatabaseName <String> -SchemaName <String> -TableMap <Hashtable>
 [-MigrationSetting <Hashtable>] [-SourceSetting <Hashtable>] [-TargetSetting <Hashtable>]
 -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2741c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2741c-105">DESCRIPTION</span></span>

<span data-ttu-id="2741c-106">Das New-AzDataMigrationSyncSelectedDB-Cmdlet erstellt ein für das Synchronisierungsszenario spezifisches Daten Bank Informationsobjekt, das Informationen zu Quell-und Zieldatenbanken enthält.</span><span class="sxs-lookup"><span data-stu-id="2741c-106">The New-AzDataMigrationSyncSelectedDB cmdlet creates a database info object specific to the sync scenario which contains information about source and target databases.</span></span>

## <span data-ttu-id="2741c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2741c-107">EXAMPLES</span></span>

### <span data-ttu-id="2741c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2741c-108">Example 1</span></span>
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

<span data-ttu-id="2741c-109">In diesem Beispiel wird ein Datenbankmetadaten-Objekt erstellt, das die Migrationseinstellungen für $DatabaseName zu Daten Bank $DatabaseName beschreibt.</span><span class="sxs-lookup"><span data-stu-id="2741c-109">This example creates a database metadata object describing the migrating settings for $DatabaseName to database $DatabaseName.</span></span>  

## <span data-ttu-id="2741c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2741c-110">PARAMETERS</span></span>

### <span data-ttu-id="2741c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2741c-111">-DefaultProfile</span></span>
<span data-ttu-id="2741c-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2741c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2741c-113">-MigrationSetting</span><span class="sxs-lookup"><span data-stu-id="2741c-113">-MigrationSetting</span></span>
<span data-ttu-id="2741c-114">Migrationseinstellungen, die das Migrationsverhalten optimieren</span><span class="sxs-lookup"><span data-stu-id="2741c-114">Migration settings which tune the migration behavior</span></span>

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

### <span data-ttu-id="2741c-115">-Schemaname</span><span class="sxs-lookup"><span data-stu-id="2741c-115">-SchemaName</span></span>
<span data-ttu-id="2741c-116">Zu migrierender Schema Name</span><span class="sxs-lookup"><span data-stu-id="2741c-116">Schema name to be migrated</span></span>

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

### <span data-ttu-id="2741c-117">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="2741c-117">-SourceDatabaseName</span></span>
<span data-ttu-id="2741c-118">Der Name der Quelldatenbank.</span><span class="sxs-lookup"><span data-stu-id="2741c-118">The name of the source database.</span></span>

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

### <span data-ttu-id="2741c-119">-SourceSetting</span><span class="sxs-lookup"><span data-stu-id="2741c-119">-SourceSetting</span></span>
<span data-ttu-id="2741c-120">Quelleinstellungen zum Optimieren des Migrations Verhaltens von Quellendpunkt</span><span class="sxs-lookup"><span data-stu-id="2741c-120">Source settings to tune source endpoint migration behavior</span></span>

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

### <span data-ttu-id="2741c-121">-TableMap</span><span class="sxs-lookup"><span data-stu-id="2741c-121">-TableMap</span></span>
<span data-ttu-id="2741c-122">Zuordnung von Quell-zu Zieltabellen</span><span class="sxs-lookup"><span data-stu-id="2741c-122">Mapping of source to target tables</span></span>

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

### <span data-ttu-id="2741c-123">-Zieldatenbankname</span><span class="sxs-lookup"><span data-stu-id="2741c-123">-TargetDatabaseName</span></span>
<span data-ttu-id="2741c-124">Der Name der Zieldatenbank</span><span class="sxs-lookup"><span data-stu-id="2741c-124">The name of the target database</span></span>

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

### <span data-ttu-id="2741c-125">-TargetSetting</span><span class="sxs-lookup"><span data-stu-id="2741c-125">-TargetSetting</span></span>
<span data-ttu-id="2741c-126">Zieleinstellungen zum Optimieren des Migrations Verhaltens von Zielendpunkt</span><span class="sxs-lookup"><span data-stu-id="2741c-126">Target settings to tune target endpoint migration behavior</span></span>

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

### <span data-ttu-id="2741c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2741c-127">CommonParameters</span></span>
<span data-ttu-id="2741c-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2741c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2741c-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2741c-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2741c-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2741c-130">INPUTS</span></span>

### <span data-ttu-id="2741c-131">Keine</span><span class="sxs-lookup"><span data-stu-id="2741c-131">None</span></span>

## <span data-ttu-id="2741c-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2741c-132">OUTPUTS</span></span>

### <span data-ttu-id="2741c-133">Microsoft. Azure. Management. datamigration. Models. MigrateSqlServerSqlDbSyncTaskInput</span><span class="sxs-lookup"><span data-stu-id="2741c-133">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbSyncTaskInput</span></span>

## <span data-ttu-id="2741c-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="2741c-134">NOTES</span></span>

## <span data-ttu-id="2741c-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2741c-135">RELATED LINKS</span></span>
