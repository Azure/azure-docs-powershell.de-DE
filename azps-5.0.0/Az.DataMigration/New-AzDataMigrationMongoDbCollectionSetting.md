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
# New-AzDataMigrationMongoDbCollectionSetting

## Synopsis
Erstellt eine Sammlungs Einstellung für die Migration entsprechend der mongoDb-Migration.

## Syntax

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## Beschreibung
Das New-AzDataMigrationMongoDbCollectionSetting-Cmdlet erstellt das Migrations Einstellungsobjekt, das den Durchsatz und das Löschverhalten angibt.
Die Ausgabe das Cmdlet ist ein Schlüsselwert Paar mit dem Namen der Sammlung und dem Wert der Einstellung. Die Ausgabe wird verwendet, um die Einstellungen auf Datenbankebene für die Migration zusammenzusetzen.

## Beispiele

### Beispiel 1
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

## Parameter

### -Name
Name der Sammlung

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

### -ShardKey
Die durch trennzeichengetrennte Liste der Shard-Schlüssel. Für mongoDb Target können Sie die Shard-Schlüsselreihenfolge für "ShardKeyName: Order" angeben, wobei Reihenfolge 1,-1 oder leer für Hash ist, beispielsweise "_id, e-Mail:-1".

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

### -TargetRequestUnit
Der Wert der dedizierten Sammlungs Anforderungseinheit. Wenn dies nicht der Fall ist, verwendet die Sammlung die freigegebene Datenbank ru.

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

### -CanDelete
Ob die Zieldaten gelöscht werden sollen, wenn der Schalter festgesetzt wird, wird bei der Migration bereinigt

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


### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### Microsoft. Azure. Commands. datamigration. Models. MongoDbCollectionSetting>

## Notizen

## Verwandte Links
