---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F63769D6-9A31-4A67-972A-1E0428853C86
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88f61718e363a630b70519590025a6da80364aeb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005629"
---
# Start-AzureSqlDatabaseRecovery

## Synopsis
Initiiert eine Wiederherstellungsanforderung für eine Datenbank.

## Syntax

### BySourceDatabaseName
```
Start-AzureSqlDatabaseRecovery -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceDatabaseObject
```
Start-AzureSqlDatabaseRecovery -SourceDatabase <RecoverableDatabase> [-TargetServerName <String>]
 [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Start-AzureSqlDatabaseRecovery** initiiert eine Wiederherstellungsanforderung für eine Live-oder gelöschte Datenbank.
Dieses Cmdlet unterstützt die grundlegende Wiederherstellung, die die letzte bekanntermaßen verfügbare Sicherung für die Datenbank verwendet.
Beim Wiederherstellungsvorgang wird eine neue Datenbank erstellt.
Wenn Sie eine Livedatenbank auf demselben Server wiederherstellen, müssen Sie einen anderen Namen für die neue Datenbank angeben.

Wenn Sie eine Point-in-Time-Wiederherstellung für eine Datenbank ausführen möchten, verwenden Sie stattdessen das Cmdlet **Start-AzureSqlDatabaseRestore** .

## Beispiele

### Beispiel 1: Wiederherstellen einer als Objekt angegebenen Datenbank
```
PS C:\> $Database = Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored"
```

Der erste Befehl ruft ein Datenbankobjekt mit dem Cmdlet **Get-AzureSqlRecoverableDatabase** ab.
Der Befehl speichert das Objekt in der $Database Variablen.

Mit dem zweiten Befehl wird die in $Database gespeicherte Datenbank erneut hergestellt.

### Beispiel 2: Wiederherstellen einer durch den Namen angegebenen Datenbank
```
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored"
```

Mit diesem Befehl wird eine Datenbank mit dem Datenbanknamen wiederhergestellt.

## Parameter

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

### -SourceDatabase
Gibt das Database-Objekt an, das die Datenbank darstellt, die von diesem Cmdlet erneut hergestellt wird.

```yaml
Type: RecoverableDatabase
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceDatabaseName
Gibt den Namen der Datenbank an, die von diesem Cmdlet erneut hergestellt wird.

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceServerName
Gibt den Namen des Servers an, auf dem die Quelldatenbank Live ausgeführt wird, oder auf dem die Quelldatenbank ausgeführt wurde, bevor Sie gelöscht wurde.

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Zieldatenbankname
Gibt den Namen der wiederhergestellten Datenbank an.
Wenn die Quelldatenbank weiterhin aktiv ist, müssen Sie einen Namen angeben, der vom Quelldaten Banknamen abweicht, um ihn auf demselben Server wiederherstellen zu können.

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

### -TargetServerName
Gibt den Namen des Servers an, für den eine Datenbank wiederhergestellt werden soll.
Sie können eine Datenbank auf demselben Server oder auf einem anderen Server wiederherstellen.

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

### Microsoft. WindowsAzure. Management. SQL. Models. RecoverableDatabase

## Ausgaben

### Microsoft. WindowsAzure. Management. SQL. Models. RecoverDatabaseOperation

## Notizen
* Sie müssen dieses Cmdlet mithilfe der zertifikatbasierten Authentifizierung ausführen. Führen Sie die folgenden Befehle auf dem Computer aus, auf dem Sie dieses Cmdlet ausführen: 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## Verwandte Links

[Azure SQL-Datenbank](https://azure.microsoft.com/en-us/services/sql-database/)

[Erstellen einer Daten Bank Wiederherstellungsanforderung](https://msdn.microsoft.com/en-us/library/dn800986.aspx)

[Geo-Replikation in Azure SQL-Datenbank](https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/)

[Vorgänge für Azure SQL-Datenbanken](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlRecoverableDatabase](./Get-AzureSqlRecoverableDatabase.md)

[Anfang-AzureSqlDatabaseRestore](./Start-AzureSqlDatabaseRestore.md)


