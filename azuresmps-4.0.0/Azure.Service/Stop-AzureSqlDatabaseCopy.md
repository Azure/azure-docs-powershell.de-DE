---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b7674cb5b7abc489dc6aa6d3746f499b9686312
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006609"
---
# Stop-AzureSqlDatabaseCopy

## Synopsis
Beendet eine fortlaufende Kopie-Beziehung.

## Syntax

### ByInputObject
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-ForcedTermination] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDatabase
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByDatabaseName
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Stop-AzureSqlDatabaseCopy** " beendet eine fortlaufende Kopie-Beziehung.
Dieses Cmdlet beendet die Datenverschiebung zwischen der Quelldatenbank und der sekundären oder Zieldatenbank und ändert dann den Zustand der sekundären Datenbank in eine eigenständige Online Datenbank.

Es gibt zwei Möglichkeiten zum Beenden einer fortlaufenden Kopier Beziehung, Kündigung oder geplanter Kündigung sowie zur erzwungenen Kündigung mit einem möglichen Datenverlust.
Auf dem Server, auf dem sich die Quelldatenbank befindet, können Sie dieses Cmdlet im Terminierungs-oder erzwungenen Beendigungsmodus ausführen.
Auf dem Server, auf dem die sekundäre Datenbank gehostet wird, müssen Sie den erzwungenen Beendigungsmodus verwenden.

Eine geplante Terminierung wartet, bis alle zugesicherten Transaktionen in der Quelldatenbank zu dem Zeitpunkt, zu dem Sie das Cmdlet ausführen, in die sekundäre Datenbank repliziert wurden.
Die erzwungene Beendigung wartet nicht auf die Replikation von ausstehenden zugesicherten Transaktionen und kann zu einem möglichen Datenverlust in der sekundären Datenbank führen.

Während der Replikationsstatus aussteht, kann nur erzwungene Beendigung eine fortlaufende Kopie-Beziehung erfolgreich beenden.
Wenn der Replikationsstatus aussteht, wird die nicht erzwungene Kündigung nicht unterstützt.

## Beispiele

### Beispiel 1: Abbrechen einer fortlaufenden Kopie-Beziehung
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

Dieser Befehl beendet die fortlaufende Kopier Beziehung der Datenbank namens Orders auf dem Server mit dem Namen lpqd0zbr8y.
Der Server mit dem Namen bk0b8kf658 hostet die sekundäre Datenbank.

### Beispiel 2: Erzwingen der Beendigung einer fortlaufenden Kopie-Beziehung
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

Der erste Befehl ruft die Datenbank-Kopier Beziehung für die Datenbank mit dem Namen "Orders" auf dem Server mit dem Namen lpqd0zbr8y ab.

Mit dem zweiten Befehl wird zwangsläufig eine fortlaufende Kopier Beziehung vom Server beendet, auf dem die sekundäre Datenbank gehostet wird.

## Parameter

### -Datenbank
Gibt ein Objekt an, das die Azure SQL-Quelldatenbank darstellt.
Dieses Cmdlet beendet die fortlaufende Kopier Beziehung der Datenbank, die dieser Parameter angibt.

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
Dieses Cmdlet beendet die fortlaufende Kopier Beziehung der Datenbank, die dieser Parameter angibt.
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
Gibt den Namen einer Datenbank an.
Dieses Cmdlet beendet die fortlaufende Kopier Beziehung der Datenbank, die dieser Parameter angibt.

```yaml
Type: String
Parameter Sets: ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.

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

### -ForcedTermination
Gibt an, dass dieses Cmdlet die erzwungene Beendigung der kontinuierlichen Kopie-Beziehung verursacht.
Die erzwungene Kündigung kann zu einem Datenverlust führen.
Wenn Sie dieses Cmdlet auf einem Server ausführen möchten, auf dem die Zieldatenbank gehostet wird, müssen Sie diesen Parameter angeben.
Wenn Sie dieses Cmdlet auf einem Server ausführen möchten, auf dem die Quelldatenbank gehostet wird, müssen Sie diesen Parameter angeben, wenn die sekundäre Datenbank nicht verfügbar ist.

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

### -PartnerDatabase
Gibt den Namen der sekundären Datenbank an.
Wenn Sie einen Namen angeben, muss er dem Namen der Quelldatenbank entsprechen.

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServer
Gibt den Namen des Servers an, der die Zieldatenbank hostet.

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
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
Gibt den Namen des Servers an, auf dem sich die Quelldatenbank befindet.

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

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. WindowsAzure. Commands. SQLDatabase. Model. DatabaseCopy

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database

## Ausgaben

### Keine

## Notizen
* Authentifizierung: Dieses Cmdlet erfordert zertifikatbasierte Authentifizierung. Ein Beispiel für die Verwendung der zertifikatbasierten Authentifizierung zum Einrichten des aktuellen Abonnements finden Sie unter dem Cmdlet **New-AzureSqlDatabaseServerContext** .
* Einschränkungen: auf dem Server, auf dem die sekundäre Datenbank gehostet wird, wird nur die erzwungene Beendigung unterstützt.
* Auswirkungen der Kündigung in der ehemaligen sekundären Datenbank: nach der Beendigung wird die sekundäre Datenbank zu einer unabhängigen Datenbank. Wenn das Seeding bereits in der sekundären Datenbank abgeschlossen ist, ist die Datenbank nach Beendigung für den Vollzugriff geöffnet. Wenn es sich bei der Quelldatenbank um eine Datenbank mit Lese-/Schreibzugriff handelt, wird auch die frühere sekundäre Datenbank zu einer Datenbank mit Lese-/Schreibzugriff.

  Wenn das Seeding gerade ausgeführt wird, wird das Seeding abgebrochen, und die frühere sekundäre Datenbank wird auf dem Server, auf dem die sekundäre Datenbank gehostet wird, nie angezeigt.

* Sie können die Quelldatenbank auf schreibgeschützten Modus einstellen. Dadurch wird sichergestellt, dass die Quell-und Sekundär Datenbanken nach der Beendigung synchronisiert werden, und es wird sichergestellt, dass während der Beendigung keine Transaktionen zugesichert werden. Nachdem die Kündigung abgeschlossen ist, stellen Sie die Quelle wieder in den Schreib-und Schreibmodus ein. Optional können Sie auch die frühere sekundäre Datenbank auf den Lese-/Schreibzugriff einstellen.
* Überwachung: Verwenden Sie das Cmdlet **Get-AzureSqlDatabaseOperation** , um den Status der Vorgänge sowohl auf Quelle als auch auf Ziel der fortlaufenden Kopie-Beziehung zu überprüfen.

## Verwandte Links

[Azure SQL-Datenbank](https://azure.microsoft.com/en-us/services/sql-database/)

[Vorgänge für Azure SQL-Datenbanken](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Beenden der Datenbankkopie](https://msdn.microsoft.com/en-us/library/dn509573.aspx)

[Azure SQL-Datenbank-Cmdlets](./Azure.SQLDatabase.md)

[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[Anfang-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)


