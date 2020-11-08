---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 383F36F3-3F52-4FC3-99F7-831096E6037D
online version: ''
schema: 2.0.0
ms.openlocfilehash: ff7c7cd50b06a4110b6af12611f3d91eaedfd227
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005632"
---
# Start-AzureSqlDatabaseRestore

## Synopsis
Führt eine Point-in-Time-Wiederherstellung einer Datenbank durch.

## Syntax

### BySourceDatabaseObject
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>] -SourceDatabase <Database>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceRestorableDroppedDatabaseObject
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>]
 -SourceRestorableDroppedDatabase <RestorableDroppedDatabase> [-TargetServerName <String>]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceDatabaseName
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceRestorableDroppedDatabaseName
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 -SourceDatabaseDeletionDate <DateTime> [-TargetServerName <String>] [-RestorableDropped]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Start-AzureSqlDatabaseRestore** führt eine Point-in-Time-Wiederherstellung einer Basic-, Standard-oder Premium-Datenbank durch.
Azure SQL-Datenbank speichert grundlegende Datenbanksicherungen 7 Tage, Standard für 14 Tage und Premium für 35 Tage.
Beim Wiederherstellungsvorgang wird eine neue Datenbank erstellt.
Wenn die Quelldatenbank nicht gelöscht wird, muss der *sourcedatabasename* -und der *Zieldatenbankname* -Parameter unterschiedliche Werte aufweisen.

Azure SQL-Datenbank unterstützt derzeit keine serverübergreifende Wiederherstellung.
Die Namen der Quell-und Zielserver müssen identisch sein.

## Beispiele

### Beispiel 1: Wiederherstellen einer als Objekt angegebenen Datenbank bis zu einem bestimmten Zeitpunkt
```
PS C:\> $Database = Get-AzureSqlDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

Der erste Befehl ruft ein Datenbankobjekt für die Datenbank mit dem Namen Database17 auf dem Server mit dem Namen SERVER01 ab und speichert es dann in der $Database-Variablen.

Mit dem zweiten Befehl wird die Datenbank zu einem bestimmten Zeitpunkt wiederhergestellt.
Der Befehl gibt den Namen für die neue Datenbank an.

### Beispiel 2: Wiederherstellen einer vom Namen angegebenen Datenbank zu einem bestimmten Zeitpunkt
```
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

Mit diesem Befehl wird die Datenbank mit dem Namen Database17 zu einem bestimmten Zeitpunkt wiederhergestellt.
Der Befehl gibt den Namen für die neue Datenbank an.

### Beispiel 3: Wiederherstellen einer gelöschten Datenbank, die als Objekt auf einen Zeitpunkt festgelegt ist
```
PS C:\> $Database = Get-AzureSqlDatabase -RestorableDropped -ServerName "Server01" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceRestorableDroppedDatabase $Database -TargetDatabaseName "DroppedDatabaseRestored"
```

Der erste Befehl ruft ein Datenbankobjekt für die Datenbank mit dem Namen Database01 auf dem Server mit dem Namen SERVER01 ab.
Der Befehl gibt den *RestorableDropped* -Parameter an.
Aus diesem Grund erhält das Cmdlet eine wiederherstellbare gelöschte Datenbank zum angegebenen Wiederherstellungspunkt.
Der Befehl speichert das Datenbankobjekt in der $Database Variablen.

Der zweite Befehl stellt die von $Database angegebene gelöschte Datenbank wieder her.
Der Befehl gibt den Namen für die neue Datenbank an.

## Parameter

### -PointInTime
Gibt den Wiederherstellungspunkt an, auf den die Datenbank wiederhergestellt werden soll.
Nach Abschluss des Wiederherstellungsvorgangs wird die Datenbank in dem Zustand wiederhergestellt, in dem Sie sich zu dem Datum und der Uhrzeit befand, zu dem dieser Parameter angegeben wurde.
Bei einer Livedatenbank, die auf die aktuelle Uhrzeit und für eine gelöschte Datenbank eingestellt ist, verwendet dieses Cmdlet standardmäßig den Zeitpunkt, zu dem die Datenbank gelöscht wurde.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest.
Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestorableDropped
Gibt an, dass dieses Cmdlet eine wiederherstellbare gelöschte Datenbank wieder herstellt.

```yaml
Type: SwitchParameter
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceDatabase
Gibt den Namen der Datenbank an, die von diesem Cmdlet wiederhergestellt wird.

```yaml
Type: Database
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceDatabaseDeletionDate
Gibt das Datum und die Uhrzeit an, zu dem die Datenbank gelöscht wurde.
Sie müssen Millisekunden einbeziehen, wenn Sie die Zeit angeben, die mit der tatsächlichen Lösch Zeit der Datenbank übereinstimmen soll.

```yaml
Type: DateTime
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceDatabaseName
Gibt den Namen der Livedatenbank an, die von diesem Cmdlet wiederhergestellt wird.

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceRestorableDroppedDatabase
Gibt ein Objekt an, das die wiederherstellbare gelöschte Datenbank darstellt, die von diesem Cmdlet wiederhergestellt wird.
Verwenden Sie zum Abrufen eines **RestorableDroppedDatabase** -Objekts das Get-AzureSqlDatabase-Cmdlet, und geben Sie den *RestorableDropped* -Parameter an.

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceServerName
Gibt den Namen des Servers an, auf dem die Quelldatenbank Live ausgeführt wird, oder auf dem die Quelldatenbank ausgeführt wurde, bevor Sie gelöscht wurde.

```yaml
Type: String
Parameter Sets: BySourceDatabaseObject, BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Zieldatenbankname
Gibt den Namen der neuen Datenbank an, die vom Wiederherstellungsvorgang erstellt wird.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetServerName
Gibt den Namen des Servers an, auf dem dieses Cmdlet die Datenbank wieder herstellt.

Azure SQL-Datenbank unterstützt derzeit keine serverübergreifende Wiederherstellung.
Die Namen der Quell-und Zielserver müssen identisch sein.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. RestorableDroppedDatabase

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database

## Ausgaben

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. RestoreDatabaseOperation

## Notizen
* Sie müssen dieses Cmdlet mithilfe der zertifikatbasierten Authentifizierung ausführen. Führen Sie die folgenden Befehle auf dem Computer aus, auf dem dieses Cmdlet ausgeführt wird: 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## Verwandte Links

[Azure SQL-Datenbank](https://azure.microsoft.com/en-us/services/sql-database/)

[Erstellen einer Daten Bank Wiederherstellungsanforderung](https://msdn.microsoft.com/en-us/library/dn509571.aspx)

[Vorgänge für Azure SQL-Datenbanken](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)


