---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 56026A74-A6DC-47A5-9643-5828C3D0E83B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 32219154f2036ee028b05a369c46be1d8e1def87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006499"
---
# Get-AzureSqlDatabaseOperation

## Synopsis
Ruft den Status von Datenbankvorgängen auf einem Azure-Server ab.

## Syntax

### ByConnectionContext (Standard)
```
Get-AzureSqlDatabaseOperation -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabaseOperation -ServerName <String> [-Database <Database>] [-DatabaseName <String>]
 [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureSqlDatabaseOperation** " Ruft den Status von Datenbankvorgängen auf dem angegebenen Azure-Server ab.
Wenn Sie nur den Parameter *Servername* oder *ConnectionContext* angeben, ruft das Cmdlet alle Datenbankvorgänge für den Server ab.
Wenn Sie auch eine Datenbank mithilfe des *Database* -oder *DatabaseName* -Parameters angeben, ruft dieses Cmdlet alle Vorgänge für die angegebene Datenbank ab.
Wenn Sie eine Vorgangs-GUID und *Servername* oder *ConnectionContext* angeben, ruft das Cmdlet einen einzelnen Datenbankvorgang ab.

## Beispiele

### Beispiel 1: Abrufen des Status aller Datenbankvorgänge für eine Datenbank
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context -DatabaseName "Database17"
```

Dieser Befehl ruft den Status aller Datenbankvorgänge in der Datenbank mit dem Namen Database17 auf dem Server ab, der vom Verbindungskontext $Context angegeben wird.

### Beispiel 2: Abrufen des Status aller Datenbankvorgänge für einen Server
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context
```

Dieser Befehl ruft den Status aller Datenbankvorgänge auf dem Server ab, die vom Verbindungskontext $Context angegeben werden.

## Parameter

### -ConnectionContext
Gibt den Verbindungskontext eines Servers an.

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
Gibt ein Objekt an, das eine Azure SQL-Datenbank darstellt.
Wenn Sie diesen Parameter angeben, müssen Sie den Parameter *Servername* oder *ConnectionContext* angeben.

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

### -DatabaseName
Gibt den Namen einer Datenbank an.
Wenn Sie diesen Parameter angeben, müssen Sie den *Servername* -Parameter oder den *ConnectionContext* -Parameter angeben.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OperationGuid
Gibt die Vorgangs-ID an, die einen bestimmten Datenbankvorgang darstellt, für den dieses Cmdlet den Status erhält.
Sie können Vorgangs-IDs abrufen, indem Sie alle Datenbankvorgänge für eine Azure SQL-Datenbank oder einen Server anfordern.
Wenn Sie diesen Parameter angeben, müssen Sie den *Servername* -Parameter oder den *ConnectionContext* -Parameter angeben.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
Gibt den Namen eines Servers an.

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

### Microsoft. WindowsAzure. Commands. SQLDatabase. Model. SqlDatabaseServerContext

### System. GUID

## Ausgaben

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database. DatabaseOperationResponseList []
Dieses Cmdlet gibt ein Array von **DatabaseOperationResponseList** -Objekten zurück, wenn mehrere Vorgänge abgerufen werden.

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. Database. DatabaseOperationResponse

## Notizen

## Verwandte Links

[Azure SQL-Datenbank](https://msdn.microsoft.com/library/ee336279.aspx)

[Status des Datenbankvorgangs](https://msdn.microsoft.com/en-us/library/azure/dn720371.aspx)

[Vorgänge für Azure SQL-Datenbanken](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[Neu – AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)


