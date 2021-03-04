---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/new-azdatamigrationmongodbdatabasesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
ms.openlocfilehash: cf034b01d0cc7bd707d65cb2ddd90e9567003861
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934187"
---
# <span data-ttu-id="cd8f5-101">New-AzDataMigrationMongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="cd8f5-101">New-AzDataMigrationMongoDbDatabaseSetting</span></span>

## <span data-ttu-id="cd8f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd8f5-102">SYNOPSIS</span></span>
<span data-ttu-id="cd8f5-103">Erstellt eine Datenbankeinstellung für die Migration für die MongoDb-Migration.</span><span class="sxs-lookup"><span data-stu-id="cd8f5-103">Creates database setting for migration for the mongoDb migration</span></span>

## <span data-ttu-id="cd8f5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd8f5-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbDatabaseSetting  -Name <Name> [-RU <RU>] -CollectionSetting <Collections>
```

## <span data-ttu-id="cd8f5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cd8f5-105">DESCRIPTION</span></span>
<span data-ttu-id="cd8f5-106">Das New-AzDataMigrationMongoDbDatabaseSetting-Cmdlet erstellt das Migrationseinstellungsobjekt, das das Durchsatz- und Löschverhalten angibt.</span><span class="sxs-lookup"><span data-stu-id="cd8f5-106">The New-AzDataMigrationMongoDbDatabaseSetting  cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="cd8f5-107">Die Ausgabe ist ein Schlüsselwertpaar mit dem Namen der Sammlung und dem Wert der Einstellung, das beim Aufrufen der Migrationsaufgabe verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="cd8f5-107">The output is a key value pair with name of collection and value of the setting, which can be used in invoking the migration task.</span></span>

## <span data-ttu-id="cd8f5-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cd8f5-108">EXAMPLES</span></span>

### <span data-ttu-id="cd8f5-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cd8f5-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationMongoDbDatabaseSetting  -Name mycollection -RU 1000 -CollectionSetting @($coll1, $coll2)

Name Setting
---- -------
test Microsoft.Azure.Management.DataMigration.Models.MongoDbDatabaseSettings

```

## <span data-ttu-id="cd8f5-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="cd8f5-110">PARAMETERS</span></span>

### <span data-ttu-id="cd8f5-111">-Name</span><span class="sxs-lookup"><span data-stu-id="cd8f5-111">-Name</span></span>
<span data-ttu-id="cd8f5-112">Name der Datenbank</span><span class="sxs-lookup"><span data-stu-id="cd8f5-112">Name of the database</span></span>

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
### <span data-ttu-id="cd8f5-113">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="cd8f5-113">-TargetRequestUnit</span></span>
<span data-ttu-id="cd8f5-114">Der dedizierte Wert für die Anforderungseinheit auf Datenbankebene.</span><span class="sxs-lookup"><span data-stu-id="cd8f5-114">The dedicated database level request unit value.</span></span> <span data-ttu-id="cd8f5-115">Wenn nicht festgelegt, verwendet diese Sammlung die freigegebene Datenbank RU.</span><span class="sxs-lookup"><span data-stu-id="cd8f5-115">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="cd8f5-116">-Sammlungen</span><span class="sxs-lookup"><span data-stu-id="cd8f5-116">-Collections</span></span>
<span data-ttu-id="cd8f5-117">Das Array der MongoDb-Sammlungseinstellungsobjekte, die von einem New-AzureRmDmsMongoDbDatabaseSetting zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cd8f5-117">The array of MongoDb collection setting objects returned by New-AzureRmDmsMongoDbDatabaseSetting call.</span></span>

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

### <span data-ttu-id="cd8f5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd8f5-118">CommonParameters</span></span>
<span data-ttu-id="cd8f5-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd8f5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd8f5-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd8f5-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd8f5-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cd8f5-121">INPUTS</span></span>

### <span data-ttu-id="cd8f5-122">Keine</span><span class="sxs-lookup"><span data-stu-id="cd8f5-122">None</span></span>

## <span data-ttu-id="cd8f5-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cd8f5-123">OUTPUTS</span></span>

### <span data-ttu-id="cd8f5-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="cd8f5-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span></span>

## <span data-ttu-id="cd8f5-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="cd8f5-125">NOTES</span></span>

## <span data-ttu-id="cd8f5-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="cd8f5-126">RELATED LINKS</span></span>
