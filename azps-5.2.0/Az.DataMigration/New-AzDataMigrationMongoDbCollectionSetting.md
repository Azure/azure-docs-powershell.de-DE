---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: 4e0082d742aff54ba4d4b57d4e148e249ab8ecf7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302928"
---
# <span data-ttu-id="59228-101">New-AzDataMigrationMongoDbCollectionSetting</span><span class="sxs-lookup"><span data-stu-id="59228-101">New-AzDataMigrationMongoDbCollectionSetting</span></span>

## <span data-ttu-id="59228-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59228-102">SYNOPSIS</span></span>
<span data-ttu-id="59228-103">Erstellt die Sammlungseinstellung für die Migration entsprechend der Migration "mongoDb".</span><span class="sxs-lookup"><span data-stu-id="59228-103">Creates collection setting for migration according for the mongoDb migration</span></span>

## <span data-ttu-id="59228-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59228-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## <span data-ttu-id="59228-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="59228-105">DESCRIPTION</span></span>
<span data-ttu-id="59228-106">Das New-AzDataMigrationMongoDbCollectionSetting erstellt das Migrationseinstellungsobjekt, das das Durchsatz- und Löschverhalten angibt.</span><span class="sxs-lookup"><span data-stu-id="59228-106">The New-AzDataMigrationMongoDbCollectionSetting cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="59228-107">Die Ausgabe des Cmdlets ist ein Schlüsselwertpaar mit dem Namen der Sammlung und dem Wert der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="59228-107">The output the cmdlet is key value pair with name of the collection, and value of the setting.</span></span> <span data-ttu-id="59228-108">Die Ausgabe wird beim Zusammenstellen der Einstellungen auf Datenbankebene für die Migration verwendet.</span><span class="sxs-lookup"><span data-stu-id="59228-108">The output is used in assembling the database level settings for migration.</span></span>

## <span data-ttu-id="59228-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="59228-109">EXAMPLES</span></span>

### <span data-ttu-id="59228-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="59228-110">Example 1</span></span>
```
PS C:\> $x = New-AzDataMigrationMongoDbCollectionSetting -Name myCollection -TargetRequestUnit 1000 -CanDelete -ShardKey "_id:-1,age:1,name"
PS C:\> $x

Name         Setting
----         -------
myCollection Microsoft.Azure.Management.DataMigration.Models.MongoDbCollectionSettings

PS C:\> $x.Setting

CanDelete ShardKey                                                               TargetRUs
--------- --------                                                               ---------
     True Microsoft.Azure.Management.DataMigration.Models.MongoDbShardKeySetting      1000

```

## <span data-ttu-id="59228-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59228-111">PARAMETERS</span></span>

### <span data-ttu-id="59228-112">-Name</span><span class="sxs-lookup"><span data-stu-id="59228-112">-Name</span></span>
<span data-ttu-id="59228-113">Name der Sammlung</span><span class="sxs-lookup"><span data-stu-id="59228-113">Name of the collection</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59228-114">-ShardKey</span><span class="sxs-lookup"><span data-stu-id="59228-114">-ShardKey</span></span>
<span data-ttu-id="59228-115">Die durch Kommas getrennte Liste der Shardschlüssel.</span><span class="sxs-lookup"><span data-stu-id="59228-115">The comma separated list of the shard keys.</span></span> <span data-ttu-id="59228-116">Für ein #A0 können Sie die Reihenfolge des Shardschlüssels "ShardKeyName:Order" angeben, wobei die Reihenfolge 1, -1 oder leer für hashed ist, z. B. "_id,email:-1".</span><span class="sxs-lookup"><span data-stu-id="59228-116">For mongoDb target, you can specify shard key order of "ShardKeyName:Order", where order is 1, -1 or empty for hashed, for example "_id,email:-1".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59228-117">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="59228-117">-TargetRequestUnit</span></span>
<span data-ttu-id="59228-118">Der Wert der dedizierten Sammlungsanforderungseinheit.</span><span class="sxs-lookup"><span data-stu-id="59228-118">The dedicated collection request unit value.</span></span> <span data-ttu-id="59228-119">Ist dies nicht festgelegt, verwendet diese Sammlung die freigegebene Datenbank RU.</span><span class="sxs-lookup"><span data-stu-id="59228-119">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="59228-120">-CanDelete</span><span class="sxs-lookup"><span data-stu-id="59228-120">-CanDelete</span></span>
<span data-ttu-id="59228-121">Ob die Zieldaten gelöscht werden sollen, wenn der Schalter festgelegt ist, werden sie bei der Migration bereinigt.</span><span class="sxs-lookup"><span data-stu-id="59228-121">Whether the target data is supposed to be deleted, if the switch is set, it will be cleaned up at migration</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="59228-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59228-122">CommonParameters</span></span>
<span data-ttu-id="59228-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59228-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59228-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59228-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59228-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="59228-125">INPUTS</span></span>

### <span data-ttu-id="59228-126">Keine</span><span class="sxs-lookup"><span data-stu-id="59228-126">None</span></span>

## <span data-ttu-id="59228-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="59228-127">OUTPUTS</span></span>

### <span data-ttu-id="59228-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span><span class="sxs-lookup"><span data-stu-id="59228-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span></span>

## <span data-ttu-id="59228-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="59228-129">NOTES</span></span>

## <span data-ttu-id="59228-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="59228-130">RELATED LINKS</span></span>
