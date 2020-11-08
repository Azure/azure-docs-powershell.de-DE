---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 7427A101-9439-45B9-B72E-F8C2DA85E412
online version: ''
schema: 2.0.0
ms.openlocfilehash: c10ae808d105079b9739516bf9eaf316241b1b11
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006504"
---
# Get-AzureSqlDatabase

## Synopsis
Ruft mindestens eine Datenbank ab.

## Syntax

### ByConnectionContext (Standard)
```
Get-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-RestorableDropped] [-RestorableDroppedDatabase <RestorableDroppedDatabase>]
 [-DatabaseDeletionDate <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabase -ServerName <String> [-Database <Database>] [-DatabaseName <String>] [-RestorableDropped]
 [-RestorableDroppedDatabase <RestorableDroppedDatabase>] [-DatabaseDeletionDate <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Get-AzureSqlDatabase können Sie** eine oder mehrere Instanzen einer Azure SQL-Datenbank von einem Azure SQL-Datenbankserver abrufen.
Sie können den Server mit einem Azure SQL-Datenbankserver-Verbindungskontext angeben, den Sie mit dem Cmdlet **New-AzureSqlDatabaseServerContext** erstellen.
Wenn Sie den Azure SQL-Datenbankservernamen angeben, verwendet das Cmdlet die aktuellen Azure-Abonnementinformationen, um die Anforderung für den Zugriff auf den Server zu authentifizieren.

Wenn Sie keine Datenbank angeben, gibt das Cmdlet " **Get-AzureSqlDatabase** " alle Datenbanken vom angegebenen Server zurück.

Abrufen wiederherstellbarer verworfener Datenbanken:

Abrufen wiederherstellbarer verworfener Datenbanken mithilfe des *RestorableDropped* -Parameters.
Verwenden Sie den *RestorableDropped* -Parameter ohne *DatabaseName* und *DatabaseDeletionDate* , um alle wiederherstellbaren verworfenen Datenbanken zurückzugeben.
Wenn Sie eine bestimmte wiederherstellbare gelöschte Datenbank zurückgeben möchten, verwenden Sie den Parameter *RestorableDropped* mit den Parametern *DatabaseName* und *DatabaseDeletionDate* .
Beim Abrufen einer bestimmten wiederherstellbaren gelöschten Datenbank mithilfe des *DatabaseName* -Parameters müssen Sie auch den *DatabaseDeletionDate* -Parameter einbeziehen, und der angegebene *DatabaseDeletionDate* -Wert muss Millisekunden aufweisen, damit er der gewünschten Datenbank entspricht.

Das Cmdlet " **Get-AzureSqlDatabase** " gibt entweder alle wiederherstellbaren gelöschten Datenbanken auf einem Server oder eine bestimmte Datenbank zurück, die sowohl *DatabaseName* als auch *DatabaseDeletionDate* entspricht.
Um wiederherstellbare gelöschte Datenbanken zurückzugeben, die verschiedene Kriterien erfüllen, wie etwa alle wiederherstellbaren verworfenen Datenbanken mit einem bestimmten Namen, müssen Sie alle wiederherstellbaren verworfenen Datenbanken zurückgeben und dann die Ergebnisse auf dem Client filtern.

## Beispiele

### Beispiel 1: Abrufen aller Datenbanken auf einem Server
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

Dieser Befehl ruft alle Datenbanken auf dem Server mit dem Namen lpqd0zbr8y ab.

### Beispiel 2: Abrufen aller wiederherstellbaren verworfenen Datenbanken auf einem Server
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped
```

Dieser Befehl ruft alle wiederherstellbaren verworfenen Datenbanken auf dem Server mit dem Namen lpqd0zbr8y ab.

### Beispiel 3: Abrufen einer Datenbank von einem von einem Verbindungskontext angegebenen Server
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

Dieser Befehl ruft die Datenbank mit dem Namen database01 vom Server ab, der durch den Verbindungskontext $Context angegeben wird.

### Beispiel 4: Speichern eines Datenbankobjekts in einer Variablen
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

Dieser Befehl ruft die Datenbank mit dem Namen database01 vom Server mit dem Namen lpqd0zbr8y ab.
Der Befehl speichert das Datenbankobjekt in der Variablen $Database 01.

### Beispiel 5: Abrufen einer wiederherstellbaren gelöschten Datenbank
```
PS C:\> $DroppedDB = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" -RestorableDropped
```

Dieser Befehl ruft die gelöschte gelöschte Datenbank mit dem Namen database01 ab, die auf 11/9/2012 vom Server mit dem Namen lpqd0zbr8y gelöscht wurde.
Dieser Befehl speichert die Ergebnisse in der $DroppedDB-Variablen.

### Beispiel 6: Abrufen aller wiederherstellbaren gelöschten Datenbanken auf einem Server und Filtern der Ergebnisse
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped | Where-Object {$_.Name -eq "ContactDB"}
```

Dieser Befehl ruft alle wiederherstellbaren gelöschten Datenbanken auf dem Server mit dem Namen lpqd0zbr8y ab und filtert die Ergebnisse dann nur auf die Datenbanken mit dem Namen ContactDB.

## Parameter

### -ConnectionContext
Gibt den Verbindungskontext eines Servers an, von dem eine Datenbank abgerufen werden soll.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Datenbank
Gibt ein Objekt an, das die Datenbank darstellt, die dieses Cmdlet abruft.

```yaml
Type: Database
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseDeletionDate
Gibt das Datum und die Uhrzeit für den Löschvorgang an.
Wenn Sie den *RestorableDropped* -Parameter angeben, geben Sie diesen Parameter an, um eine wiederherstellbare gelöschte Datenbank basierend auf dem Datum und der Uhrzeit des Löschvorgangs abzurufen.

Der *DatabaseDeletionDate* -Parameter muss Millisekunden aufweisen, damit er der Uhrzeit der gewünschten Datenbank entspricht.
Wenn Sie einen Wert ohne Millisekunden angeben, wird die Datenbank nicht gefunden.

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

### -DatabaseName
Gibt den Namen der Datenbank an, die dieses Cmdlet abruft.

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
Gibt an, dass dieses Cmdlet *RestorableDroppedDatabase* -Objekte anstelle von *Daten Bank* Objekten zurückgibt.
Sie können den *DatabaseDeletionDate* -Parameter verwenden, um eine bestimmte zurückgegebene gelöschte Datenbank auszuwählen.

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

### -RestorableDroppedDatabase
Gibt ein Objekt an, das die zurückgegebene gelöschte Datenbank darstellt, die dieses Cmdlet abruft.

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Servername
Gibt den Namen des Servers an, der die Datenbank enthält, die dieses Cmdlet abruft.
Das Cmdlet verwendet das aktuelle Azure-Abonnement für den Zugriff auf den Server.

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. RestorableDroppedDatabase

## Ausgaben

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database\>
Dieses Cmdlet gibt ein *Daten Bank* Objekt zurück, wenn Sie den *RestorableDropped* -Parameter nicht angeben.

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase\>
Dieses Cmdlet gibt ein *RestorableDroppedDatabase* -Objekt zurück, wenn Sie den *RestorableDropped* -Parameter angeben.

## Notizen

## Verwandte Links

[Azure SQL-Datenbank](https://azure.microsoft.com/en-us/services/sql-database/)

[Vorgänge für Azure SQL-Datenbanken](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Neu – AzureSqlDatabase](./New-AzureSqlDatabase.md)

[Neu – AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)

[Remove-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Satz-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


