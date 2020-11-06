---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationsqlserversqldbselecteddb
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSqlServerSqlDbSelectedDB.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSqlServerSqlDbSelectedDB.md
ms.openlocfilehash: 1be43b5d08011a71ec093df2f93c63dd04c6004d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482985"
---
# <span data-ttu-id="93bfc-101">New-AzureRmDataMigrationSqlServerSqlDbSelectedDB</span><span class="sxs-lookup"><span data-stu-id="93bfc-101">New-AzureRmDataMigrationSqlServerSqlDbSelectedDB</span></span>

## <span data-ttu-id="93bfc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="93bfc-102">SYNOPSIS</span></span>
<span data-ttu-id="93bfc-103">Erstellt ein MigrateSqlServerSqlDbDatabaseInput-Objekt, das Informationen zu Quell-und Zieldatenbanken für die Migration enthält.</span><span class="sxs-lookup"><span data-stu-id="93bfc-103">Creates a MigrateSqlServerSqlDbDatabaseInput object that contains information about source and target databases for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93bfc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="93bfc-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationSqlServerSqlDbSelectedDB [-Id <String>] [-Name <String>] [-TargetDatabaseName <String>]
 [-MakeSourceDbReadOnly] [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="93bfc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93bfc-105">DESCRIPTION</span></span>
<span data-ttu-id="93bfc-106">Das New-AzureRmDataMigrationSqlServerSqlDbSelectedDB-Cmdlet erstellt ein MigrateSqlServerSqlDbDatabaseInput-Objekt, das Informationen zu Quell-und Zieldatenbanken sowie zu den Tabellenzuordnungen für die Migration enthält.</span><span class="sxs-lookup"><span data-stu-id="93bfc-106">The New-AzureRmDataMigrationSqlServerSqlDbSelectedDB cmdlet creates a MigrateSqlServerSqlDbDatabaseInput object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="93bfc-107">Dieses Cmdlet kann mit dem New-AzureRmDataMigrationTask-Cmdlet als Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="93bfc-107">This cmdlet can be used as a parameter with the New-AzureRmDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="93bfc-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="93bfc-108">EXAMPLES</span></span>

### <span data-ttu-id="93bfc-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="93bfc-109">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationSqlServerSqlDbSelectedDB  -Name AdventuerWorks2016 -TargetDatabaseName AdventureWorks2016
 -MakeSourceDbReadOnly -TableMap $tableMap
```

<span data-ttu-id="93bfc-110">Im obigen Beispiel wird MigrateSqlServerSqlDbDatabaseInput-Objekt zum Migrieren der **AdventureWorks2016** -Datenbank zu einer SQL Azure-Datenbank mit demselben Namen erstellt.</span><span class="sxs-lookup"><span data-stu-id="93bfc-110">The above example creates MigrateSqlServerSqlDbDatabaseInput object for migrating the **AdventureWorks2016** database to a SQL Azure database with the same name.</span></span>

## <span data-ttu-id="93bfc-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="93bfc-111">PARAMETERS</span></span>

### <span data-ttu-id="93bfc-112">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="93bfc-112">-Confirm</span></span>
<span data-ttu-id="93bfc-113">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="93bfc-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93bfc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93bfc-114">-DefaultProfile</span></span>
<span data-ttu-id="93bfc-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="93bfc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93bfc-116">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="93bfc-116">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="93bfc-117">Vor der Migration die Datenbank auf ReadOnly setzen</span><span class="sxs-lookup"><span data-stu-id="93bfc-117">Set Database to readonly before migration</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93bfc-118">-Name</span><span class="sxs-lookup"><span data-stu-id="93bfc-118">-Name</span></span>
<span data-ttu-id="93bfc-119">Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="93bfc-119">The name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93bfc-120">-TableMap</span><span class="sxs-lookup"><span data-stu-id="93bfc-120">-TableMap</span></span>
<span data-ttu-id="93bfc-121">Zuordnung von Quell-zu Zieltabellen</span><span class="sxs-lookup"><span data-stu-id="93bfc-121">mapping of source to target tables</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93bfc-122">-Zieldatenbankname</span><span class="sxs-lookup"><span data-stu-id="93bfc-122">-TargetDatabaseName</span></span>
<span data-ttu-id="93bfc-123">Der Name der Zieldatenbank.</span><span class="sxs-lookup"><span data-stu-id="93bfc-123">The name of the target Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="93bfc-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="93bfc-124">INPUTS</span></span>

### <span data-ttu-id="93bfc-125">Keine</span><span class="sxs-lookup"><span data-stu-id="93bfc-125">None</span></span>


## <span data-ttu-id="93bfc-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="93bfc-126">OUTPUTS</span></span>

### <span data-ttu-id="93bfc-127">Microsoft. Azure. Management. datamigration. Models. MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="93bfc-127">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>


## <span data-ttu-id="93bfc-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="93bfc-128">NOTES</span></span>

## <span data-ttu-id="93bfc-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="93bfc-129">RELATED LINKS</span></span>


