---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B3813F54-E5B7-4605-BB1C-67417FDDB076
online version: ''
schema: 2.0.0
ms.openlocfilehash: a3f9817ebe556bc80364d012040387cca72c56c4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006314"
---
# Remove-AzureSqlDatabase

## Synopsis
Löscht eine Azure SQL-Datenbank.

## Syntax

### ByNameWithConnectionContext
```
Remove-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObjectWithConnectionContext
```
Remove-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -Database <Database> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameWithServerName
```
Remove-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObjectWithServerName
```
Remove-AzureSqlDatabase -ServerName <String> -Database <Database> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureSqlDatabase** löscht eine Azure SQL-Datenbank nach dem Server Verbindungskontext oder Servernamen.
Sie können einen Azure SQL-Datenbankserver-Verbindungskontext mithilfe des Cmdlets **New-AzureSqlDatabaseServerContext** erstellen und dann mit diesem Cmdlet verwenden.

Wenn Sie eine Datenbank löschen, indem Sie einen Azure SQL-Datenbankservernamen angeben, verwendet das Cmdlet **Remove-AzureSqlDatabase** den Namen und die aktuellen Azure-Abonnementinformationen, um den Vorgang auszuführen.

## Beispiele

### Beispiel 1: Entfernen einer Datenbank
```
PS C:\> Remove-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

Mit diesem Befehl wird die Datenbank namens database01 aus dem Azure SQL-Datenbankserver-Verbindungskontext $Context entfernt.

### Beispiel 2: Entfernen einer Datenbank mit einem Servernamen
```
PS C:\> Remove-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

Dieser Befehl entfernt die Datenbank mit dem Namen database01 aus dem Azure SQL-Datenbankserver mit dem Namen lpqd0zbr8y.

### Beispiel 3: Entfernen einer Datenbank mithilfe der Pipeline
```
PS C:\> $Database01 | Remove-AzureSqlDatabase -ConnectionContext $Context
PS C:\> $Database01 | Remove-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

In diesem Beispiel wird die alternative Methode zum Übergeben des Datenbankobjekts durch die Pipeline veranschaulicht.

## Parameter

### -ConnectionContext
Gibt den Verbindungskontext eines Servers an, auf dem mit diesem Cmdlet eine Datenbank entfernt wird.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByNameWithConnectionContext, ByObjectWithConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Datenbank
Gibt ein Objekt an, das die von diesem Cmdlet entfernte Datenbank darstellt.

```yaml
Type: Database
Parameter Sets: ByObjectWithConnectionContext, ByObjectWithServerName
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Gibt den Namen der Datenbank an, die von diesem Cmdlet entfernt wird.

```yaml
Type: String
Parameter Sets: ByNameWithConnectionContext, ByNameWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Ermöglicht die Ausführung der Aktion, ohne dass der Benutzer zur Bestätigung aufgefordert wird.

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
Gibt den Namen des Servers an, auf dem dieses Cmdlet die Datenbank löscht.

```yaml
Type: String
Parameter Sets: ByNameWithServerName, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database

## Ausgaben

## Notizen
* Aufgrund des Schweregrads des Vorgangs werden Sie von diesem Cmdlet standardmäßig zur Bestätigung aufgefordert. Um die Bestätigung zu überspringen, geben Sie den Parameter *Force* an.

## Verwandte Links

[Azure SQL-Datenbank](https://azure.microsoft.com/en-us/services/sql-database/)

[Datenbank löschen](https://msdn.microsoft.com/en-us/library/azure/dn505705.aspx)

[Vorgänge für Azure SQL-Datenbanken](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[Neu – AzureSqlDatabase](./New-AzureSqlDatabase.md)

[Neu – AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)

[Satz-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


