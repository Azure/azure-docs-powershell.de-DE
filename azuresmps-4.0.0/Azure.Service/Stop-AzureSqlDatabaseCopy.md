---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7716587787515221a6e016436a6e3d030c1ab0eb
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405617"
---
# Stop-AzureSqlDatabaseCopy

## SYNOPSIS
Beendet eine fortlaufende Kopierbeziehung.

## SYNTAX

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

## BESCHREIBUNG
Das **Cmdlet "Stop-AzureSqlDatabaseCopy"** beendet eine fortlaufende Kopierbeziehung.
Dieses Cmdlet stoppt die Datenbewegung zwischen der Quelldatenbank und der sekundären oder Zieldatenbank und ändert dann den Zustand der sekundären Datenbank in eine eigenständige Onlinedatenbank.

Es gibt zwei Möglichkeiten, eine fortlaufende Kopierbeziehung zu beenden: Beendigung oder geplante Beendigung und erzwungene Beendigung mit möglichem Datenverlust.
Auf dem Server, der die Quelldatenbank hostet, können Sie dieses Cmdlet im Beendigungs- oder Beendigungsmodus ausführen.
Auf dem Server, der die sekundäre Datenbank hostet, müssen Sie den Modus für erzwungene Beendigung verwenden.

Eine geplante Beendigung wartet, bis alle für die Quelldatenbank vorgesehenen Transaktionen zum Zeitpunkt der Ausführung des Cmdlets in der sekundären Datenbank repliziert wurden.
Bei einer erzwungenen Beendigung wird nicht auf die Replikation noch ausstehender gebundener Transaktionen gewartet, und es kann zu einem möglichen Datenverlust in der sekundären Datenbank kommen.

Während der Replikationsstatus AUSSTEHEND ist, kann eine fortlaufende Kopierbeziehung nur durch eine erzwungene Beendigung erfolgreich beendet werden.
Wenn der Replikationsstatus "AUSSTEHEND" ist, wird eine nicht erzwungene Beendigung nicht unterstützt.

## BEISPIELE

### Beispiel 1: Beenden einer fortlaufenden Kopierbeziehung
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

Dieser Befehl beendet die fortlaufende Kopierbeziehung der Datenbank "Orders" auf dem Server mit dem Namen "lpqd0zbr8y".
Der Server mit dem Namen bk0b8kf658 hostet die sekundäre Datenbank.

### Beispiel 2: Zcibly terminate a continuous copy relationship
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

Der erste Befehl ruft die Datenbankkopiebeziehung für die Datenbank mit dem Namen "Orders" auf dem Server mit dem Namen "lpqd0zbr8y" ab.

Der zweite Befehl beendet eine fortlaufende Kopierbeziehung vom Server, der die sekundäre Datenbank hostet.

## PARAMETERS

### -Database
Gibt ein Objekt an, das die Azure SQL darstellt.
Dieses Cmdlet beendet die fortlaufende Kopierbeziehung der Datenbank, die mit diesem Parameter angegeben wird.

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
Dieses Cmdlet beendet die fortlaufende Kopierbeziehung der Datenbank, die mit diesem Parameter angegeben wird.
Dieser Parameter akzeptiert die Pipelineeingabe.

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
Dieses Cmdlet beendet die fortlaufende Kopierbeziehung der Datenbank, die mit diesem Parameter angegeben wird.

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
Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.

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
Gibt an, dass dieses Cmdlet eine erzwungene Beendigung der fortlaufenden Kopierbeziehung bewirkt.
Eine erzwungene Beendigung kann zu Datenverlust führen.
Um dieses Cmdlet auf einem Server ausführen zu können, der die Zieldatenbank hostet, müssen Sie diesen Parameter angeben.
Wenn Sie dieses Cmdlet auf einem Server ausführen möchten, der die Quelldatenbank hostet, müssen Sie diesen Parameter angeben, wenn die sekundäre Datenbank nicht verfügbar ist.

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
Wenn Sie einen Namen angeben, muss er mit dem Namen der Quelldatenbank übereinstimmen.

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

### -Profile
Gibt das Azure-Profil an, aus dem dieses Cmdlet liest.
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

### -ServerName
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

### -Confirm
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

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

### -Waswenn
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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy

### Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database

## AUSGABEN

### Keine

## HINWEISE
* Authentifizierung: Für dieses Cmdlet ist zertifikatbasierte Authentifizierung erforderlich. Ein Beispiel für die Verwendung der zertifikatbasierten Authentifizierung zum Festlegen des aktuellen Abonnements finden Sie im **Cmdlet "New-AzureSqlDatabaseServerContext".**
* Einschränkungen: Auf dem Server, der die sekundäre Datenbank hostet, wird nur eine erzwungene Beendigung unterstützt.
* Auswirkungen einer Beendigung auf die ehemalige sekundäre Datenbank: Nach der Beendigung wird die sekundäre Datenbank zu einer unabhängigen Datenbank. Wenn das Starting für die sekundäre Datenbank bereits abgeschlossen ist, ist diese Datenbank nach dem Beenden für den Vollzugriff geöffnet. Wenn es sich bei der Quelldatenbank um eine Datenbank mit Lese-/Schreibzugriff handelt, wird aus der früheren sekundären Datenbank auch eine Datenbank mit Lese-/Schreibzugriff.

  Wenn das Startprojekt zurzeit ausgeführt wird, wird das Startprojekt abgebrochen, und die frühere sekundäre Datenbank wird auf dem Server, auf dem sich die sekundäre Datenbank befindet, nie angezeigt.

* Sie können für die Quelldatenbank den schreibgeschützten Modus festlegen. Dadurch wird sichergestellt, dass Quelldatenbanken und sekundäre Datenbanken nach dem Beenden synchronisiert werden, und es wird sichergestellt, dass während der Beendigung keine Transaktionen gebunden werden. Nachdem die Beendigung abgeschlossen ist, legen Sie die Quelle wieder auf den Lese-/Schreibmodus zurück. Optional können Sie auch die frühere sekundäre Datenbank auf den Lese-/Schreibmodus festlegen.
* Überwachung: Verwenden Sie das Cmdlet **"Get-AzureSqlDatabaseOperation",** um den Status der Vorgänge sowohl an der Quelle als auch am Ziel der fortlaufenden Kopierbeziehung zu überprüfen.

## LINKS ZU VERWANDTEN THEMEN

[Azure SQL-Datenbank](https://azure.microsoft.com/en-us/services/sql-database/)

[Vorgänge für Azure SQL Datenbanken](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Beenden der Datenbankkopie](https://msdn.microsoft.com/en-us/library/dn509573.aspx)



[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[Start-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)


