---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8752766572975ef97094a3915446086c903a7fd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006501"
---
# Get-AzureSqlDatabaseCopy

## Synopsis
Überprüft den Status von Kopier Beziehungen.

## Syntax

### ByServerNameOnly (Standard)
```
Get-AzureSqlDatabaseCopy -ServerName <String> [-DatabaseName <String>] [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByInputObject
```
Get-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByDatabase
```
Get-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureSqlDatabaseCopy** " überprüft den Status einer oder mehrerer aktiver Kopier Beziehungen.
Führen Sie dieses Cmdlet aus, nachdem Sie das Start-AzureSqlDatabaseCopy-oder Stop-AzureSqlDatabaseCopy-Cmdlet ausgeführt haben.
Sie können eine bestimmte Kopier Beziehung, alle Kopier Beziehungen oder eine gefilterte Liste von Kopier Beziehungen überprüfen, beispielsweise alle Kopien auf einem bestimmten Zielserver.
Sie können dieses Cmdlet auf dem Server ausführen, der die Quell-oder Zieldatenbank hostet.

Dieses Cmdlet ist synchron.
Das Cmdlet blockiert die Azure PowerShell-Konsole, bis ein Statusobjekt zurückgegeben wird.

Die Parameter *PartnerServer* und *PartnerDatabase* sind optional.
Wenn Sie keinen der Parameter angeben, gibt dieses Cmdlet eine Tabelle mit Ergebnissen zurück.
Wenn Sie den Status nur für eine bestimmte Datenbank anzeigen möchten, geben Sie beide Parameter an.

## Beispiele

### Beispiel 1: Abrufen des Kopierstatus einer Datenbank
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

Dieser Befehl ruft den Status der Datenbank Orders auf dem Server mit dem Namen lpqd0zbr8y ab.
Der *PartnerServer* -Parameter schränkt diesen Befehl auf den bk0b8kf658-Server ein.

### Beispiel 2: Abrufen des Status aller Kopien auf einem serverGet des Status aller Kopien auf einem Server
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

Dieser Befehl ruft den Status aller aktiven Kopien auf dem Server mit dem Namen lpqd0zbr8y ab.

## Parameter

### -Datenbank
Gibt ein Objekt an, das die Azure SQL-Quelldatenbank darstellt.
Dieses Cmdlet ruft den Kopierstatus der Datenbank ab, die dieser Parameter angibt.

```yaml
Type: Database
Parameter Sets: ByDatabase
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseCopy
Gibt ein Objekt an, das eine Datenbank darstellt.
Dieses Cmdlet ruft den Kopierstatus der Datenbank ab, die dieser Parameter angibt.
Dieser Parameter akzeptiert Pipelineeingaben.

```yaml
Type: DatabaseCopy
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Gibt den Namen der Quelldatenbank an.
Dieses Cmdlet ruft den Kopierstatus der Datenbank ab, die dieser Parameter angibt.

```yaml
Type: String
Parameter Sets: ByServerNameOnly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerDatabase
Gibt den Namen der sekundären Datenbank an.
Wenn diese Datenbank in der sys.dm_database_copies dynamischen Verwaltungsansicht nicht gefunden wird, gibt dieses Cmdlet ein leeres Statusobjekt zurück.

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServer
Gibt den Namen des Servers an, der die Zieldatenbank hostet.
Wenn dieser Server nicht in der sys.dm_database_copies dynamischen Verwaltungsansicht zu finden ist, gibt dieses Cmdlet ein leeres Statusobjekt zurück.

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
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

### -Servername
Gibt den Namen des Servers an, auf dem sich die Datenbankkopie befindet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. WindowsAzure. Commands. SQLDatabase. Model. DatabaseCopy

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database

## Ausgaben

### Microsoft. WindowsAzure. Commands. SQLDatabase. Model. DatabaseCopy

## Notizen
* Authentifizierung: Dieses Cmdlet erfordert zertifikatbasierte Authentifizierung. Ein Beispiel für die Verwendung der zertifikatbasierten Authentifizierung zum Einrichten des aktuellen Abonnements finden Sie unter New-AzureSqlDatabaseServerContext-Cmdlet.

## Verwandte Links

[Azure SQL-Datenbank](https://azure.microsoft.com/en-us/services/sql-database/)

[Vorgänge für Azure SQL-Datenbanken](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Azure SQL-Datenbank-Cmdlets](./Azure.SQLDatabase.md)

[Anfang-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)

[Stopp-AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


