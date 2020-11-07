---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
ms.openlocfilehash: 502e64ba553f20983bd437fea40d5247cf04548f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651467"
---
# <span data-ttu-id="5cdd9-101">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="5cdd9-101">New-AzDataMigrationSelectedDBObject</span></span>

## <span data-ttu-id="5cdd9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5cdd9-102">SYNOPSIS</span></span>
<span data-ttu-id="5cdd9-103">Erstellt ein Datenbankeingabe Objekt, das Informationen zu Quell-und Zieldatenbanken für die Migration enthält.</span><span class="sxs-lookup"><span data-stu-id="5cdd9-103">Creates a database input object that contains information about source and target databases for migration.</span></span>

## <span data-ttu-id="5cdd9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5cdd9-104">SYNTAX</span></span>

### <span data-ttu-id="5cdd9-105">MigrateSqlServerSqlDb (Standard)</span><span class="sxs-lookup"><span data-stu-id="5cdd9-105">MigrateSqlServerSqlDb (Default)</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDb] [-MakeSourceDbReadOnly]
 [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5cdd9-106">MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="5cdd9-106">MigrateSqlServerSqlDbMi</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDbMi] [-BackupFileShare <FileShare>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5cdd9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5cdd9-107">DESCRIPTION</span></span>
<span data-ttu-id="5cdd9-108">Mit dem New-AzDataMigrationSelectedDB-Cmdlet wird ein DatenbankInfo-Objekt erstellt, das Informationen zu Quell-und Zieldatenbanken sowie zu den Tabellenzuordnungen für die Migration enthält.</span><span class="sxs-lookup"><span data-stu-id="5cdd9-108">The New-AzDataMigrationSelectedDB cmdlet creates a database info object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="5cdd9-109">Dieses Cmdlet kann mit dem New-AzDataMigrationTask-Cmdlet als Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5cdd9-109">This cmdlet can be used as a parameter with the New-AzDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="5cdd9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5cdd9-110">EXAMPLES</span></span>

### <span data-ttu-id="5cdd9-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5cdd9-111">Example 1</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDb -Name "HR" -TargetDatabaseName "HR_PSTEST" -TableMap $tableMap

Name TargetDatabaseName MakeSourceDbReadOnly TableMap
---- ------------------ -------------------- --------
HR   HR_PSTEST                         False {[HR.COUNTRIES, HR.COUNTRIES]}
```

### <span data-ttu-id="5cdd9-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5cdd9-112">Example 2</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDbMi -Name "HR" -TargetDatabaseName "HR_PSTEST" -BackupFileShare $backupFileShare

Name RestoreDatabaseName BackupFileShare
---- ------------------- ---------------
HR   HRTest              Microsoft.Azure.Management.DataMigration.Models.FileShare
```

## <span data-ttu-id="5cdd9-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="5cdd9-113">PARAMETERS</span></span>

### <span data-ttu-id="5cdd9-114">-BackupFileShare</span><span class="sxs-lookup"><span data-stu-id="5cdd9-114">-BackupFileShare</span></span>
<span data-ttu-id="5cdd9-115">Dateifreigabe, bei der die Quellserver-Datenbankdateien für diese Datenbank gesichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5cdd9-115">File share where the source server database files for this database should be backed up.</span></span>
<span data-ttu-id="5cdd9-116">Verwenden Sie diese Einstellung, um Dateifreigabeinformationen für jede Datenbank zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="5cdd9-116">Use this setting to override file share information for each database.</span></span>
<span data-ttu-id="5cdd9-117">Verwenden Sie den vollqualifizierten Domänennamen für den Server.</span><span class="sxs-lookup"><span data-stu-id="5cdd9-117">Use fully qualified domain name for the server.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.FileShare
Parameter Sets: MigrateSqlServerSqlDbMi
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5cdd9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cdd9-118">-DefaultProfile</span></span>
<span data-ttu-id="5cdd9-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5cdd9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cdd9-120">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="5cdd9-120">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="5cdd9-121">Vor der Migration die Datenbank auf ReadOnly setzen</span><span class="sxs-lookup"><span data-stu-id="5cdd9-121">Set Database to readonly before migration</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cdd9-122">-MigrateSqlServerSqlDb</span><span class="sxs-lookup"><span data-stu-id="5cdd9-122">-MigrateSqlServerSqlDb</span></span>
<span data-ttu-id="5cdd9-123">Setzen Sie den Migrationstyp auf SQL Server auf SQL DB-Migration.</span><span class="sxs-lookup"><span data-stu-id="5cdd9-123">Set migration type to SQL Server to SQL DB Migration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cdd9-124">-MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="5cdd9-124">-MigrateSqlServerSqlDbMi</span></span>
<span data-ttu-id="5cdd9-125">Setzen Sie den Migrationstyp auf SQL Server auf SQL DB Mi-Migration.</span><span class="sxs-lookup"><span data-stu-id="5cdd9-125">Set migration type to SQL Server to SQL DB MI Migration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDbMi
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cdd9-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="5cdd9-126">-SourceDatabaseName</span></span>
<span data-ttu-id="5cdd9-127">Der Name der Quelldatenbank.</span><span class="sxs-lookup"><span data-stu-id="5cdd9-127">The name of the source database.</span></span>

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

### <span data-ttu-id="5cdd9-128">-TableMap</span><span class="sxs-lookup"><span data-stu-id="5cdd9-128">-TableMap</span></span>
<span data-ttu-id="5cdd9-129">Zuordnung von Quell-zu Zieltabellen</span><span class="sxs-lookup"><span data-stu-id="5cdd9-129">mapping of source to target tables</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cdd9-130">-Zieldatenbankname</span><span class="sxs-lookup"><span data-stu-id="5cdd9-130">-TargetDatabaseName</span></span>
<span data-ttu-id="5cdd9-131">Der Name der Zieldatenbank.</span><span class="sxs-lookup"><span data-stu-id="5cdd9-131">The name of the target database.</span></span>

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

### <span data-ttu-id="5cdd9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cdd9-132">CommonParameters</span></span>
<span data-ttu-id="5cdd9-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cdd9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cdd9-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cdd9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cdd9-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5cdd9-135">INPUTS</span></span>

### <span data-ttu-id="5cdd9-136">Microsoft. Azure. Management. datamigration. Models. FileShare</span><span class="sxs-lookup"><span data-stu-id="5cdd9-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span></span>

## <span data-ttu-id="5cdd9-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5cdd9-137">OUTPUTS</span></span>

### <span data-ttu-id="5cdd9-138">Microsoft. Azure. Management. datamigration. Models. MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="5cdd9-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="5cdd9-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="5cdd9-139">NOTES</span></span>

## <span data-ttu-id="5cdd9-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5cdd9-140">RELATED LINKS</span></span>
