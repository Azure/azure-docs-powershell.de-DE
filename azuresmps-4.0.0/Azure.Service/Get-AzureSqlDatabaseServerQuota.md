---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 6723557D-8052-4BFA-872C-384B1423B3AE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 185ad06375fe9bbd11cb25c26b25704baeaa1dfe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005776"
---
# Get-AzureSqlDatabaseServerQuota

## Synopsis
Ruft Kontingentinformationen für einen Azure SQL-Datenbankserver ab.

## Syntax

### ByConnectionContext
```
Get-AzureSqlDatabaseServerQuota -ConnectionContext <IServerDataServiceContext> [-QuotaName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabaseServerQuota -ServerName <String> [-QuotaName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureSqlDatabaseServerQuota** " Ruft die Kontingentinformationen für eine angegebene Instanz des Azure SQL-Datenbankservers ab.
Geben Sie einen Verbindungskontext oder den Servernamen an.
Wenn Sie keinen Kontingent Namen angeben, ruft dieses Cmdlet alle Kontingentinformationen für den Server ab.

## Beispiele

### Beispiel 1: Abrufen von Informationen zu einem bestimmten Kontingent
```
PS C:\> $QuotaPremium = GetAzureSqlDatabaseServerQuota $Context -QuotaName "Premium_Databases"
```

Dieser Befehl ruft das Kontingent mit dem Namen Premium_Databases aus dem Azure SQL-Datenbankserver ab, der durch die in der $Context-Variable gespeicherte Verbindung angegeben wird.

### Beispiel 2: Abrufen von Informationen für alle Kontingente
```
PS C:\> $QuotaList = GetAzureSqlDatabaseServerQuota $Context
```

Dieser Befehl ruft alle Kontingentwerte vom Server ab, der durch die Verbindungs $Context angegeben wird.

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

### -Kontingentname
Gibt den Namen des Kontingentwerts an, den dieses Cmdlet erhält.

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

## Ausgaben

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. Server. ServerQuota []

## Notizen
* Authentifizierung: Dieses Cmdlet kann entweder die SQL Server-Authentifizierung oder die zertifikatbasierte Authentifizierung verwenden. Beispiele für das Einrichten der Authentifizierung finden Sie unter New-AzureSqlDatabaseServerContext-Cmdlet.

## Verwandte Links

[Azure SQL-Datenbank](https://azure.microsoft.com/en-us/services/sql-database/)

[Vorgänge für Azure SQL-Datenbanken](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Neu – AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)


