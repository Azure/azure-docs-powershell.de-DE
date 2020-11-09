---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/new-azdatamigrationmongodbdatabasesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
ms.openlocfilehash: 9ae50501306dfa1a76fa4966113ac2e9b681f6c5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297645"
---
# <span data-ttu-id="35dcc-101">New-AzDataMigrationMongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="35dcc-101">New-AzDataMigrationMongoDbDatabaseSetting</span></span>

## <span data-ttu-id="35dcc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="35dcc-102">SYNOPSIS</span></span>
<span data-ttu-id="35dcc-103">Erstellt eine Datenbankeinstellung für die Migration für die mongoDb-Migration</span><span class="sxs-lookup"><span data-stu-id="35dcc-103">Creates database setting for migration for the mongoDb migration</span></span>

## <span data-ttu-id="35dcc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="35dcc-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbDatabaseSetting  -Name <Name> [-RU <RU>] -CollectionSetting <Collections>
```

## <span data-ttu-id="35dcc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="35dcc-105">DESCRIPTION</span></span>
<span data-ttu-id="35dcc-106">Das New-AzDataMigrationMongoDbDatabaseSetting-Cmdlet erstellt das Migrations Einstellungsobjekt, das den Durchsatz und das Löschverhalten angibt.</span><span class="sxs-lookup"><span data-stu-id="35dcc-106">The New-AzDataMigrationMongoDbDatabaseSetting  cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="35dcc-107">Die Ausgabe ist ein Schlüsselwert Paar mit dem Namen der Sammlung und dem Wert der Einstellung, der beim Aufrufen der Migrationsaufgabe verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="35dcc-107">The output is a key value pair with name of collection and value of the setting, which can be used in invoking the migration task.</span></span>

## <span data-ttu-id="35dcc-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="35dcc-108">EXAMPLES</span></span>

### <span data-ttu-id="35dcc-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="35dcc-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationMongoDbDatabaseSetting  -Name mycollection -RU 1000 -CollectionSetting @($coll1, $coll2)

Name Setting
---- -------
test Microsoft.Azure.Management.DataMigration.Models.MongoDbDatabaseSettings

```

## <span data-ttu-id="35dcc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="35dcc-110">PARAMETERS</span></span>

### <span data-ttu-id="35dcc-111">-Name</span><span class="sxs-lookup"><span data-stu-id="35dcc-111">-Name</span></span>
<span data-ttu-id="35dcc-112">Name der Datenbank</span><span class="sxs-lookup"><span data-stu-id="35dcc-112">Name of the database</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="35dcc-113">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="35dcc-113">-TargetRequestUnit</span></span>
<span data-ttu-id="35dcc-114">Der dedizierte Wert der Anforderungseinheit auf Datenbankebene</span><span class="sxs-lookup"><span data-stu-id="35dcc-114">The dedicated database level request unit value.</span></span> <span data-ttu-id="35dcc-115">Wenn dies nicht der Fall ist, verwendet die Sammlung die freigegebene Datenbank ru.</span><span class="sxs-lookup"><span data-stu-id="35dcc-115">If not set, that collection uses shared database RU.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: RU

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35dcc-116">-Sammlungen</span><span class="sxs-lookup"><span data-stu-id="35dcc-116">-Collections</span></span>
<span data-ttu-id="35dcc-117">Das Array der MongoDB-Sammlungs Einstellungsobjekte, die von New-AzureRmDmsMongoDbDatabaseSetting Aufruf zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="35dcc-117">The array of MongoDb collection setting objects returned by New-AzureRmDmsMongoDbDatabaseSetting call.</span></span>

```yaml
Type: System.Collections.Generic.KeyValuePair<string, MongoDbCollectionSettings>[]
Parameter Sets: (All)
Aliases: colls

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35dcc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35dcc-118">CommonParameters</span></span>
<span data-ttu-id="35dcc-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35dcc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35dcc-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35dcc-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35dcc-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="35dcc-121">INPUTS</span></span>

### <span data-ttu-id="35dcc-122">Keine</span><span class="sxs-lookup"><span data-stu-id="35dcc-122">None</span></span>

## <span data-ttu-id="35dcc-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="35dcc-123">OUTPUTS</span></span>

### <span data-ttu-id="35dcc-124">Microsoft. Azure. Commands. datamigration. Models. MongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="35dcc-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span></span>

## <span data-ttu-id="35dcc-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="35dcc-125">NOTES</span></span>

## <span data-ttu-id="35dcc-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="35dcc-126">RELATED LINKS</span></span>
