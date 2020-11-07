---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
ms.openlocfilehash: 0e4557f44d3219b55edc0bd31464033e9000c772
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845319"
---
# <span data-ttu-id="3c0f2-101">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="3c0f2-101">New-AzDataMigrationSelectedDBObject</span></span>

## <span data-ttu-id="3c0f2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3c0f2-102">SYNOPSIS</span></span>
<span data-ttu-id="3c0f2-103">Erstellt ein Datenbankeingabe Objekt, das Informationen zu Quell-und Zieldatenbanken für die Migration enthält.</span><span class="sxs-lookup"><span data-stu-id="3c0f2-103">Creates a database input object that contains information about source and target databases for migration.</span></span>

## <span data-ttu-id="3c0f2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c0f2-104">SYNTAX</span></span>

### <span data-ttu-id="3c0f2-105">MigrateSqlServerSqlDb (Standard)</span><span class="sxs-lookup"><span data-stu-id="3c0f2-105">MigrateSqlServerSqlDb (Default)</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDb] [-MakeSourceDbReadOnly]
 [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c0f2-106">MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="3c0f2-106">MigrateSqlServerSqlDbMi</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDbMi] [-BackupFileShare <FileShare>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c0f2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3c0f2-107">DESCRIPTION</span></span>
<span data-ttu-id="3c0f2-108">Mit dem New-AzDataMigrationSelectedDB-Cmdlet wird ein DatenbankInfo-Objekt erstellt, das Informationen zu Quell-und Zieldatenbanken sowie zu den Tabellenzuordnungen für die Migration enthält.</span><span class="sxs-lookup"><span data-stu-id="3c0f2-108">The New-AzDataMigrationSelectedDB cmdlet creates a database info object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="3c0f2-109">Dieses Cmdlet kann mit dem New-AzDataMigrationTask-Cmdlet als Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3c0f2-109">This cmdlet can be used as a parameter with the New-AzDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="3c0f2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3c0f2-110">EXAMPLES</span></span>

### <span data-ttu-id="3c0f2-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3c0f2-111">Example 1</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDb -Name "HR" -TargetDatabaseName "HR_PSTEST" -TableMap $tableMap

Name TargetDatabaseName MakeSourceDbReadOnly TableMap
---- ------------------ -------------------- --------
HR   HR_PSTEST                         False {[HR.COUNTRIES, HR.COUNTRIES]}
```

### <span data-ttu-id="3c0f2-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3c0f2-112">Example 2</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDbMi -Name "HR" -TargetDatabaseName "HR_PSTEST" -BackupFileShare $backupFileShare

Name RestoreDatabaseName BackupFileShare
---- ------------------- ---------------
HR   HRTest              Microsoft.Azure.Management.DataMigration.Models.FileShare
```

## <span data-ttu-id="3c0f2-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c0f2-113">PARAMETERS</span></span>

### <span data-ttu-id="3c0f2-114">-BackupFileShare</span><span class="sxs-lookup"><span data-stu-id="3c0f2-114">-BackupFileShare</span></span>
<span data-ttu-id="3c0f2-115">Dateifreigabe, bei der die Quellserver-Datenbankdateien für diese Datenbank gesichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3c0f2-115">File share where the source server database files for this database should be backed up.</span></span>
<span data-ttu-id="3c0f2-116">Verwenden Sie diese Einstellung, um Dateifreigabeinformationen für jede Datenbank zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="3c0f2-116">Use this setting to override file share information for each database.</span></span>
<span data-ttu-id="3c0f2-117">Verwenden Sie den vollqualifizierten Domänennamen für den Server.</span><span class="sxs-lookup"><span data-stu-id="3c0f2-117">Use fully qualified domain name for the server.</span></span>

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

### <span data-ttu-id="3c0f2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c0f2-118">-DefaultProfile</span></span>
<span data-ttu-id="3c0f2-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3c0f2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c0f2-120">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="3c0f2-120">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="3c0f2-121">Vor der Migration die Datenbank auf ReadOnly setzen</span><span class="sxs-lookup"><span data-stu-id="3c0f2-121">Set Database to readonly before migration</span></span>

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

### <span data-ttu-id="3c0f2-122">-MigrateSqlServerSqlDb</span><span class="sxs-lookup"><span data-stu-id="3c0f2-122">-MigrateSqlServerSqlDb</span></span>
<span data-ttu-id="3c0f2-123">Setzen Sie den Migrationstyp auf SQL Server auf SQL DB-Migration.</span><span class="sxs-lookup"><span data-stu-id="3c0f2-123">Set migration type to SQL Server to SQL DB Migration.</span></span>

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

### <span data-ttu-id="3c0f2-124">-MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="3c0f2-124">-MigrateSqlServerSqlDbMi</span></span>
<span data-ttu-id="3c0f2-125">Setzen Sie den Migrationstyp auf SQL Server auf SQL DB Mi-Migration.</span><span class="sxs-lookup"><span data-stu-id="3c0f2-125">Set migration type to SQL Server to SQL DB MI Migration.</span></span>

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

### <span data-ttu-id="3c0f2-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="3c0f2-126">-SourceDatabaseName</span></span>
<span data-ttu-id="3c0f2-127">Der Name der Quelldatenbank.</span><span class="sxs-lookup"><span data-stu-id="3c0f2-127">The name of the source database.</span></span>

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

### <span data-ttu-id="3c0f2-128">-TableMap</span><span class="sxs-lookup"><span data-stu-id="3c0f2-128">-TableMap</span></span>
<span data-ttu-id="3c0f2-129">Zuordnung von Quell-zu Zieltabellen</span><span class="sxs-lookup"><span data-stu-id="3c0f2-129">mapping of source to target tables</span></span>

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

### <span data-ttu-id="3c0f2-130">-Zieldatenbankname</span><span class="sxs-lookup"><span data-stu-id="3c0f2-130">-TargetDatabaseName</span></span>
<span data-ttu-id="3c0f2-131">Der Name der Zieldatenbank.</span><span class="sxs-lookup"><span data-stu-id="3c0f2-131">The name of the target database.</span></span>

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

### <span data-ttu-id="3c0f2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c0f2-132">CommonParameters</span></span>
<span data-ttu-id="3c0f2-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c0f2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c0f2-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c0f2-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c0f2-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3c0f2-135">INPUTS</span></span>

### <span data-ttu-id="3c0f2-136">Microsoft. Azure. Management. datamigration. Models. FileShare</span><span class="sxs-lookup"><span data-stu-id="3c0f2-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span></span>

## <span data-ttu-id="3c0f2-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3c0f2-137">OUTPUTS</span></span>

### <span data-ttu-id="3c0f2-138">Microsoft. Azure. Management. datamigration. Models. MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="3c0f2-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="3c0f2-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="3c0f2-139">NOTES</span></span>

## <span data-ttu-id="3c0f2-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3c0f2-140">RELATED LINKS</span></span>
