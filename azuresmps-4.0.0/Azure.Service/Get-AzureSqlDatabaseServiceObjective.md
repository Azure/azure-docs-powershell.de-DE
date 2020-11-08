---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A2C22A8A-EF50-4BE3-82DF-5ED6F69C00CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 457775a74fb7921a3c8b6b5e635bd7df7e704faa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005774"
---
# Get-AzureSqlDatabaseServiceObjective

## Synopsis
Ruft Dienst Ziele für einen Azure SQL-Datenbankserver ab.

## Syntax

### ByConnectionContext (Standard)
```
Get-AzureSqlDatabaseServiceObjective -Context <IServerDataServiceContext>
 [-ServiceObjective <ServiceObjective>] [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabaseServiceObjective -ServerName <String> [-ServiceObjective <ServiceObjective>]
 [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureSqlDatabaseServiceObjective** " ruft Dienst Ziele für einen Azure SQL-Datenbankserver ab.
Dienst Ziele werden als Leistungsstufen bezeichnet.
Wenn Sie kein Dienst Ziel angeben, gibt dieses Cmdlet alle gültigen Dienst Ziele für den angegebenen Server zurück.

Dieses Cmdlet gilt für Basic-, Standard-und Premium-Dienstebenen.

## Beispiele

### Beispiel 1: Abrufen aller Dienst Ziele mithilfe eines Verbindungskontexts
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -Context $Context
```

Dieser Befehl ruft alle Dienst Ziele für den Server ab, die vom Verbindungskontext $Context angegeben werden.

### Beispiel 2: Abrufen aller Dienst Ziele mithilfe eines Server namens
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -ServerName "Server01"
```

Dieser Befehl ruft alle Dienst Ziele für den Server mit dem Namen SERVER01 ab.

## Parameter

### -Context
Gibt den Verbindungskontext eines Servers an.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

### -ServiceObjective
Gibt ein Objekt an, das das Dienst Ziel darstellt, das dieses Cmdlet erhält.
Gültige Werte sind: 

- Standard: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c
- Standard (S0): f1173c43-91bd-4AAA-973c-54e79e15235b
- Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928
- Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7
- * Standard (S3): 789681b8-CA10-4eb0-bdf2-e0b050601b40
- Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d
- Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d
- Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0
- Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446

* Standard (S3) ist Teil des neuesten SQL-Datenbankupdates V12 (Preview).
Weitere Informationen finden Sie unter [Neuerungen in der Azure SQL Database V12 Preview](https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/) ( `https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/` ) in der Azure-Bibliothek.

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ServiceObjectiveName
Gibt den Namen des abzurufenden Dienst Ziels an.
Gültige Werte sind: Basic, S0, S1, S2, S3, P1, P2 und P3.

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

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. ServiceObjective

## Ausgaben

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective\>

## Notizen

## Verwandte Links

[Azure SQL-Datenbank](https://msdn.microsoft.com/library/ee336279.aspx)

[Abrufen des Service Level-Ziels](https://msdn.microsoft.com/en-us/library/azure/dn505709.aspx)

[Vorgänge für Azure SQL-Datenbanken](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Neu – AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)


