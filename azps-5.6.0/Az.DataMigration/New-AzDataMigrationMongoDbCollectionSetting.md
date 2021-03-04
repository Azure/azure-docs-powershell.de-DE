---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: 817a4c8469d1d3652dade426857f88f9249f82b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925899"
---
# <span data-ttu-id="76058-101">New-AzDataMigrationMongoDbCollectionSetting</span><span class="sxs-lookup"><span data-stu-id="76058-101">New-AzDataMigrationMongoDbCollectionSetting</span></span>

## <span data-ttu-id="76058-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76058-102">SYNOPSIS</span></span>
<span data-ttu-id="76058-103">Erstellt die Sammlungseinstellung für die Migration gemäß der MongoDb-Migration.</span><span class="sxs-lookup"><span data-stu-id="76058-103">Creates collection setting for migration according for the mongoDb migration</span></span>

## <span data-ttu-id="76058-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76058-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## <span data-ttu-id="76058-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="76058-105">DESCRIPTION</span></span>
<span data-ttu-id="76058-106">Das New-AzDataMigrationMongoDbCollectionSetting-Cmdlet erstellt das Migrationseinstellungsobjekt, das das Durchsatz- und Löschverhalten angibt.</span><span class="sxs-lookup"><span data-stu-id="76058-106">The New-AzDataMigrationMongoDbCollectionSetting cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="76058-107">Die Ausgabe des Cmdlets ist ein Schlüsselwertpaar mit dem Namen der Auflistung und dem Wert der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="76058-107">The output the cmdlet is key value pair with name of the collection, and value of the setting.</span></span> <span data-ttu-id="76058-108">Die Ausgabe wird zum Zusammenstellen der Einstellungen auf Datenbankebene für die Migration verwendet.</span><span class="sxs-lookup"><span data-stu-id="76058-108">The output is used in assembling the database level settings for migration.</span></span>

## <span data-ttu-id="76058-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="76058-109">EXAMPLES</span></span>

### <span data-ttu-id="76058-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="76058-110">Example 1</span></span>
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

## <span data-ttu-id="76058-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="76058-111">PARAMETERS</span></span>

### <span data-ttu-id="76058-112">-Name</span><span class="sxs-lookup"><span data-stu-id="76058-112">-Name</span></span>
<span data-ttu-id="76058-113">Name der Sammlung</span><span class="sxs-lookup"><span data-stu-id="76058-113">Name of the collection</span></span>

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

### <span data-ttu-id="76058-114">-ShardKey</span><span class="sxs-lookup"><span data-stu-id="76058-114">-ShardKey</span></span>
<span data-ttu-id="76058-115">Die durch Kommas getrennte Liste der Shardschlüssel.</span><span class="sxs-lookup"><span data-stu-id="76058-115">The comma separated list of the shard keys.</span></span> <span data-ttu-id="76058-116">Für das Ziel "mongoDb" können Sie die Shardschlüsselreihenfolge "ShardKeyName:Order" angeben, wobei die Reihenfolge für hashed 1, -1 oder leer ist, z. B. "_id,email:-1".</span><span class="sxs-lookup"><span data-stu-id="76058-116">For mongoDb target, you can specify shard key order of "ShardKeyName:Order", where order is 1, -1 or empty for hashed, for example "_id,email:-1".</span></span>

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

### <span data-ttu-id="76058-117">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="76058-117">-TargetRequestUnit</span></span>
<span data-ttu-id="76058-118">Der Wert der dedizierten Sammlungsanforderungseinheit.</span><span class="sxs-lookup"><span data-stu-id="76058-118">The dedicated collection request unit value.</span></span> <span data-ttu-id="76058-119">Wenn nicht festgelegt, verwendet diese Sammlung die freigegebene Datenbank RU.</span><span class="sxs-lookup"><span data-stu-id="76058-119">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="76058-120">-CanDelete</span><span class="sxs-lookup"><span data-stu-id="76058-120">-CanDelete</span></span>
<span data-ttu-id="76058-121">Unabhängig davon, ob die Zieldaten gelöscht werden sollen, wenn der Schalter festgelegt ist, werden sie bei der Migration bereinigt.</span><span class="sxs-lookup"><span data-stu-id="76058-121">Whether the target data is supposed to be deleted, if the switch is set, it will be cleaned up at migration</span></span>

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


### <span data-ttu-id="76058-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76058-122">CommonParameters</span></span>
<span data-ttu-id="76058-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76058-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76058-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76058-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76058-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="76058-125">INPUTS</span></span>

### <span data-ttu-id="76058-126">Keine</span><span class="sxs-lookup"><span data-stu-id="76058-126">None</span></span>

## <span data-ttu-id="76058-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="76058-127">OUTPUTS</span></span>

### <span data-ttu-id="76058-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span><span class="sxs-lookup"><span data-stu-id="76058-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span></span>

## <span data-ttu-id="76058-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="76058-129">NOTES</span></span>

## <span data-ttu-id="76058-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="76058-130">RELATED LINKS</span></span>
