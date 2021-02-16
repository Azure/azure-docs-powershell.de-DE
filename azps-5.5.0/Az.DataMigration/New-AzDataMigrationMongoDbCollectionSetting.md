---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: 4e0082d742aff54ba4d4b57d4e148e249ab8ecf7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148129"
---
# <span data-ttu-id="c49b7-101">New-AzDataMigrationMongoDbCollectionSetting</span><span class="sxs-lookup"><span data-stu-id="c49b7-101">New-AzDataMigrationMongoDbCollectionSetting</span></span>

## <span data-ttu-id="c49b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c49b7-102">SYNOPSIS</span></span>
<span data-ttu-id="c49b7-103">Erstellt die Sammlungseinstellung für die Migration entsprechend der MongoDb-Migration.</span><span class="sxs-lookup"><span data-stu-id="c49b7-103">Creates collection setting for migration according for the mongoDb migration</span></span>

## <span data-ttu-id="c49b7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c49b7-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## <span data-ttu-id="c49b7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c49b7-105">DESCRIPTION</span></span>
<span data-ttu-id="c49b7-106">Das New-AzDataMigrationMongoDbCollectionSetting erstellt das Migrationseinstellungsobjekt, das das Durchsatz- und Löschverhalten angibt.</span><span class="sxs-lookup"><span data-stu-id="c49b7-106">The New-AzDataMigrationMongoDbCollectionSetting cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="c49b7-107">Die Ausgabe des Cmdlets ist ein Schlüsselwertpaar mit dem Namen der Sammlung und dem Wert der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="c49b7-107">The output the cmdlet is key value pair with name of the collection, and value of the setting.</span></span> <span data-ttu-id="c49b7-108">Die Ausgabe wird beim Zusammenstellen der Einstellungen auf Datenbankebene für die Migration verwendet.</span><span class="sxs-lookup"><span data-stu-id="c49b7-108">The output is used in assembling the database level settings for migration.</span></span>

## <span data-ttu-id="c49b7-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c49b7-109">EXAMPLES</span></span>

### <span data-ttu-id="c49b7-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c49b7-110">Example 1</span></span>
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

## <span data-ttu-id="c49b7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c49b7-111">PARAMETERS</span></span>

### <span data-ttu-id="c49b7-112">-Name</span><span class="sxs-lookup"><span data-stu-id="c49b7-112">-Name</span></span>
<span data-ttu-id="c49b7-113">Name der Sammlung</span><span class="sxs-lookup"><span data-stu-id="c49b7-113">Name of the collection</span></span>

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

### <span data-ttu-id="c49b7-114">-ShardKey</span><span class="sxs-lookup"><span data-stu-id="c49b7-114">-ShardKey</span></span>
<span data-ttu-id="c49b7-115">Die durch Kommas getrennte Liste der Shardschlüssel.</span><span class="sxs-lookup"><span data-stu-id="c49b7-115">The comma separated list of the shard keys.</span></span> <span data-ttu-id="c49b7-116">Für ein #A0 können Sie die Reihenfolge des Shardschlüssels "ShardKeyName:Order" angeben, wobei "Reihenfolge" 1, -1 oder leer für Hash ist, z. B. "_id,email:-1".</span><span class="sxs-lookup"><span data-stu-id="c49b7-116">For mongoDb target, you can specify shard key order of "ShardKeyName:Order", where order is 1, -1 or empty for hashed, for example "_id,email:-1".</span></span>

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

### <span data-ttu-id="c49b7-117">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="c49b7-117">-TargetRequestUnit</span></span>
<span data-ttu-id="c49b7-118">Der Wert der dedizierten Sammlungsanforderungseinheit.</span><span class="sxs-lookup"><span data-stu-id="c49b7-118">The dedicated collection request unit value.</span></span> <span data-ttu-id="c49b7-119">Ist dies nicht festgelegt, verwendet diese Sammlung die freigegebene Datenbank RU.</span><span class="sxs-lookup"><span data-stu-id="c49b7-119">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="c49b7-120">-CanDelete</span><span class="sxs-lookup"><span data-stu-id="c49b7-120">-CanDelete</span></span>
<span data-ttu-id="c49b7-121">Ob die Zieldaten gelöscht werden sollen, wenn der Schalter festgelegt ist, werden sie bei der Migration bereinigt.</span><span class="sxs-lookup"><span data-stu-id="c49b7-121">Whether the target data is supposed to be deleted, if the switch is set, it will be cleaned up at migration</span></span>

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


### <span data-ttu-id="c49b7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c49b7-122">CommonParameters</span></span>
<span data-ttu-id="c49b7-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c49b7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c49b7-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c49b7-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c49b7-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c49b7-125">INPUTS</span></span>

### <span data-ttu-id="c49b7-126">Keine</span><span class="sxs-lookup"><span data-stu-id="c49b7-126">None</span></span>

## <span data-ttu-id="c49b7-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c49b7-127">OUTPUTS</span></span>

### <span data-ttu-id="c49b7-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span><span class="sxs-lookup"><span data-stu-id="c49b7-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span></span>

## <span data-ttu-id="c49b7-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c49b7-129">NOTES</span></span>

## <span data-ttu-id="c49b7-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c49b7-130">RELATED LINKS</span></span>
