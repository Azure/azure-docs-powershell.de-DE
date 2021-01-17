---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
ms.openlocfilehash: 0e4557f44d3219b55edc0bd31464033e9000c772
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98304731"
---
# <span data-ttu-id="4faf0-101">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="4faf0-101">New-AzDataMigrationSelectedDBObject</span></span>

## <span data-ttu-id="4faf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4faf0-102">SYNOPSIS</span></span>
<span data-ttu-id="4faf0-103">Erstellt ein Datenbankeingabeobjekt, das Informationen zu Quell- und Zieldatenbanken für die Migration enthält.</span><span class="sxs-lookup"><span data-stu-id="4faf0-103">Creates a database input object that contains information about source and target databases for migration.</span></span>

## <span data-ttu-id="4faf0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4faf0-104">SYNTAX</span></span>

### <span data-ttu-id="4faf0-105">MigrateSqlServerSqlDb (Standard)</span><span class="sxs-lookup"><span data-stu-id="4faf0-105">MigrateSqlServerSqlDb (Default)</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDb] [-MakeSourceDbReadOnly]
 [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4faf0-106">MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="4faf0-106">MigrateSqlServerSqlDbMi</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDbMi] [-BackupFileShare <FileShare>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4faf0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4faf0-107">DESCRIPTION</span></span>
<span data-ttu-id="4faf0-108">Das New-AzDataMigrationSelectedDB erstellt ein Datenbankinformationsobjekt, das Informationen zu Quell- und Zieldatenbanken sowie die Tabellenzuordnungen für die Migration enthält.</span><span class="sxs-lookup"><span data-stu-id="4faf0-108">The New-AzDataMigrationSelectedDB cmdlet creates a database info object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="4faf0-109">Dieses Cmdlet kann als Parameter mit dem cmdlet New-AzDataMigrationTask verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4faf0-109">This cmdlet can be used as a parameter with the New-AzDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="4faf0-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4faf0-110">EXAMPLES</span></span>

### <span data-ttu-id="4faf0-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4faf0-111">Example 1</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDb -Name "HR" -TargetDatabaseName "HR_PSTEST" -TableMap $tableMap

Name TargetDatabaseName MakeSourceDbReadOnly TableMap
---- ------------------ -------------------- --------
HR   HR_PSTEST                         False {[HR.COUNTRIES, HR.COUNTRIES]}
```

### <span data-ttu-id="4faf0-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4faf0-112">Example 2</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDbMi -Name "HR" -TargetDatabaseName "HR_PSTEST" -BackupFileShare $backupFileShare

Name RestoreDatabaseName BackupFileShare
---- ------------------- ---------------
HR   HRTest              Microsoft.Azure.Management.DataMigration.Models.FileShare
```

## <span data-ttu-id="4faf0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4faf0-113">PARAMETERS</span></span>

### <span data-ttu-id="4faf0-114">-BackupFileShare</span><span class="sxs-lookup"><span data-stu-id="4faf0-114">-BackupFileShare</span></span>
<span data-ttu-id="4faf0-115">Dateifreigabe, in der die Quellserverdatenbankdateien für diese Datenbank gesichert werden sollten.</span><span class="sxs-lookup"><span data-stu-id="4faf0-115">File share where the source server database files for this database should be backed up.</span></span>
<span data-ttu-id="4faf0-116">Verwenden Sie diese Einstellung, um Dateifreigabeinformationen für jede Datenbank außer Kraft zu setzen.</span><span class="sxs-lookup"><span data-stu-id="4faf0-116">Use this setting to override file share information for each database.</span></span>
<span data-ttu-id="4faf0-117">Verwenden Sie einen vollqualifizierten Domänennamen für den Server.</span><span class="sxs-lookup"><span data-stu-id="4faf0-117">Use fully qualified domain name for the server.</span></span>

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

### <span data-ttu-id="4faf0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4faf0-118">-DefaultProfile</span></span>
<span data-ttu-id="4faf0-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4faf0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4faf0-120">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="4faf0-120">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="4faf0-121">Festlegen, dass die Datenbank vor der Migration lesbar ist</span><span class="sxs-lookup"><span data-stu-id="4faf0-121">Set Database to readonly before migration</span></span>

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

### <span data-ttu-id="4faf0-122">-MigrateSqlServerSqlDb</span><span class="sxs-lookup"><span data-stu-id="4faf0-122">-MigrateSqlServerSqlDb</span></span>
<span data-ttu-id="4faf0-123">Legen Sie den Migrationstyp SQL Server auf SQL DB Migration.</span><span class="sxs-lookup"><span data-stu-id="4faf0-123">Set migration type to SQL Server to SQL DB Migration.</span></span>

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

### <span data-ttu-id="4faf0-124">-MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="4faf0-124">-MigrateSqlServerSqlDbMi</span></span>
<span data-ttu-id="4faf0-125">Legen Sie den Migrationstyp SQL Server auf SQL DB MI Migration.</span><span class="sxs-lookup"><span data-stu-id="4faf0-125">Set migration type to SQL Server to SQL DB MI Migration.</span></span>

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

### <span data-ttu-id="4faf0-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="4faf0-126">-SourceDatabaseName</span></span>
<span data-ttu-id="4faf0-127">Der Name der Quelldatenbank.</span><span class="sxs-lookup"><span data-stu-id="4faf0-127">The name of the source database.</span></span>

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

### <span data-ttu-id="4faf0-128">-TableMap</span><span class="sxs-lookup"><span data-stu-id="4faf0-128">-TableMap</span></span>
<span data-ttu-id="4faf0-129">Zuordnung von Quelle zu Zieltabellen</span><span class="sxs-lookup"><span data-stu-id="4faf0-129">mapping of source to target tables</span></span>

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

### <span data-ttu-id="4faf0-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="4faf0-130">-TargetDatabaseName</span></span>
<span data-ttu-id="4faf0-131">Der Name der Zieldatenbank.</span><span class="sxs-lookup"><span data-stu-id="4faf0-131">The name of the target database.</span></span>

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

### <span data-ttu-id="4faf0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4faf0-132">CommonParameters</span></span>
<span data-ttu-id="4faf0-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4faf0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4faf0-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4faf0-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4faf0-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4faf0-135">INPUTS</span></span>

### <span data-ttu-id="4faf0-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span><span class="sxs-lookup"><span data-stu-id="4faf0-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span></span>

## <span data-ttu-id="4faf0-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4faf0-137">OUTPUTS</span></span>

### <span data-ttu-id="4faf0-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="4faf0-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="4faf0-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4faf0-139">NOTES</span></span>

## <span data-ttu-id="4faf0-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4faf0-140">RELATED LINKS</span></span>
