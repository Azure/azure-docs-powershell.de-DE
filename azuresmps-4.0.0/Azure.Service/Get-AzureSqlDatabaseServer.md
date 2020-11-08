---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 0ACEDE22-1C2B-4846-A949-710AF6C148D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: d513d6d019c84984923541624063e657e2250b61
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005777"
---
# Get-AzureSqlDatabaseServer

## Synopsis
Ruft Informationen zu Azure SQL-Datenbankservern ab.

## Syntax

```
Get-AzureSqlDatabaseServer [-ServerName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureSqlDatabaseServer** " Ruft Informationen zu den Instanzen des Azure SQL-Datenbankservers im aktuellen Abonnement ab.
Wenn Sie einen Server nach Namen angeben, gibt dieses Cmdlet ein Objekt zurück, das Informationen zu diesem Server enthält.
Andernfalls gibt das Cmdlet Informationen zu allen Servern zurück.

## Beispiele

### Beispiel 1: Abrufen von Informationen zu allen Servern
```
PS C:\> Get-AzureSqlDatabaseServer
```

Dieser Befehl gibt Informationen zu allen Instanzen des Azure SQL-Datenbankservers im aktuellen Abonnement zurück.

### Beispiel 2: Abrufen von Informationen zu einem bestimmten Server
```
PS C:\> Get-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y"
```

Dieser Befehl gibt Informationen zum Server mit dem Namen lpqd0zbr8y zurück.

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

### -Servername
Gibt den Namen des Servers an, den dieses Cmdlet entfernt.
Geben Sie den Servernamen und nicht den vollqualifizierten DNS-Namen an.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. WindowsAzure. Commands. SQLDatabase. Model. SqlDatabaseServerContext

## Ausgaben

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext\>

## Notizen

## Verwandte Links

[Azure SQL-Datenbank](https://azure.microsoft.com/en-us/services/sql-database/)

[Listenserver](https://msdn.microsoft.com/en-us/library/azure/dn505702.aspx)

[Vorgänge für Azure SQL-Datenbanken](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Neu – AzureSqlDatabaseServer](./New-AzureSqlDatabaseServer.md)

[Remove-AzureSqlDatabaseServer](./Remove-AzureSqlDatabaseServer.md)

[Satz-AzureSqlDatabaseServer](./Set-AzureSqlDatabaseServer.md)


