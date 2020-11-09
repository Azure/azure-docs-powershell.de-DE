---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: 4e0082d742aff54ba4d4b57d4e148e249ab8ecf7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297646"
---
# <span data-ttu-id="fb125-101">New-AzDataMigrationMongoDbCollectionSetting</span><span class="sxs-lookup"><span data-stu-id="fb125-101">New-AzDataMigrationMongoDbCollectionSetting</span></span>

## <span data-ttu-id="fb125-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fb125-102">SYNOPSIS</span></span>
<span data-ttu-id="fb125-103">Erstellt eine Sammlungs Einstellung für die Migration entsprechend der mongoDb-Migration.</span><span class="sxs-lookup"><span data-stu-id="fb125-103">Creates collection setting for migration according for the mongoDb migration</span></span>

## <span data-ttu-id="fb125-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb125-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## <span data-ttu-id="fb125-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb125-105">DESCRIPTION</span></span>
<span data-ttu-id="fb125-106">Das New-AzDataMigrationMongoDbCollectionSetting-Cmdlet erstellt das Migrations Einstellungsobjekt, das den Durchsatz und das Löschverhalten angibt.</span><span class="sxs-lookup"><span data-stu-id="fb125-106">The New-AzDataMigrationMongoDbCollectionSetting cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="fb125-107">Die Ausgabe das Cmdlet ist ein Schlüsselwert Paar mit dem Namen der Sammlung und dem Wert der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="fb125-107">The output the cmdlet is key value pair with name of the collection, and value of the setting.</span></span> <span data-ttu-id="fb125-108">Die Ausgabe wird verwendet, um die Einstellungen auf Datenbankebene für die Migration zusammenzusetzen.</span><span class="sxs-lookup"><span data-stu-id="fb125-108">The output is used in assembling the database level settings for migration.</span></span>

## <span data-ttu-id="fb125-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fb125-109">EXAMPLES</span></span>

### <span data-ttu-id="fb125-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fb125-110">Example 1</span></span>
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

## <span data-ttu-id="fb125-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb125-111">PARAMETERS</span></span>

### <span data-ttu-id="fb125-112">-Name</span><span class="sxs-lookup"><span data-stu-id="fb125-112">-Name</span></span>
<span data-ttu-id="fb125-113">Name der Sammlung</span><span class="sxs-lookup"><span data-stu-id="fb125-113">Name of the collection</span></span>

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

### <span data-ttu-id="fb125-114">-ShardKey</span><span class="sxs-lookup"><span data-stu-id="fb125-114">-ShardKey</span></span>
<span data-ttu-id="fb125-115">Die durch trennzeichengetrennte Liste der Shard-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="fb125-115">The comma separated list of the shard keys.</span></span> <span data-ttu-id="fb125-116">Für mongoDb Target können Sie die Shard-Schlüsselreihenfolge für "ShardKeyName: Order" angeben, wobei Reihenfolge 1,-1 oder leer für Hash ist, beispielsweise "_id, e-Mail:-1".</span><span class="sxs-lookup"><span data-stu-id="fb125-116">For mongoDb target, you can specify shard key order of "ShardKeyName:Order", where order is 1, -1 or empty for hashed, for example "_id,email:-1".</span></span>

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

### <span data-ttu-id="fb125-117">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="fb125-117">-TargetRequestUnit</span></span>
<span data-ttu-id="fb125-118">Der Wert der dedizierten Sammlungs Anforderungseinheit.</span><span class="sxs-lookup"><span data-stu-id="fb125-118">The dedicated collection request unit value.</span></span> <span data-ttu-id="fb125-119">Wenn dies nicht der Fall ist, verwendet die Sammlung die freigegebene Datenbank ru.</span><span class="sxs-lookup"><span data-stu-id="fb125-119">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="fb125-120">-CanDelete</span><span class="sxs-lookup"><span data-stu-id="fb125-120">-CanDelete</span></span>
<span data-ttu-id="fb125-121">Ob die Zieldaten gelöscht werden sollen, wenn der Schalter festgesetzt wird, wird bei der Migration bereinigt</span><span class="sxs-lookup"><span data-stu-id="fb125-121">Whether the target data is supposed to be deleted, if the switch is set, it will be cleaned up at migration</span></span>

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


### <span data-ttu-id="fb125-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb125-122">CommonParameters</span></span>
<span data-ttu-id="fb125-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb125-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb125-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb125-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb125-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fb125-125">INPUTS</span></span>

### <span data-ttu-id="fb125-126">Keine</span><span class="sxs-lookup"><span data-stu-id="fb125-126">None</span></span>

## <span data-ttu-id="fb125-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fb125-127">OUTPUTS</span></span>

### <span data-ttu-id="fb125-128">Microsoft. Azure. Commands. datamigration. Models. MongoDbCollectionSetting></span><span class="sxs-lookup"><span data-stu-id="fb125-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span></span>

## <span data-ttu-id="fb125-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="fb125-129">NOTES</span></span>

## <span data-ttu-id="fb125-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fb125-130">RELATED LINKS</span></span>
