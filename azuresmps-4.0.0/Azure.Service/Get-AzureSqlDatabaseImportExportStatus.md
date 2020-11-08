---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 4661C479-6E3B-425D-B9D2-B36D7A83130C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3c55ebd22337a8078f3ae495b3901317f4201e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006500"
---
# Get-AzureSqlDatabaseImportExportStatus

## Synopsis
Ruft den Status einer Import-oder Exportanforderung ab.

## Syntax

### ByConnectionInfo
```
Get-AzureSqlDatabaseImportExportStatus -Username <String> -Password <String> -ServerName <String>
 -RequestId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByRequestObject
```
Get-AzureSqlDatabaseImportExportStatus -Request <ImportExportRequest> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureSqlDatabaseImportExportStatus** " Ruft den Status einer Import-oder Exportanforderung ab.
Das Start-AzureSqlDatabaseImport-oder Start-AzureSqlDatabaseExport-Cmdlet initiiert Anforderungen.
Sie können das Request-Objekt mithilfe des *Request* -Parameters angeben, oder Sie können die Anforderung mithilfe des Parameters *Anforderungs* -Nr und der Parameter *username* , *Password* und *Servername* identifizieren.

## Beispiele

### Beispiel 1: Abrufen des Status einer Exportanforderung
```
PS C:\> $ExportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
PS C:\> Get-AzureSqlDatabaseImportExportStatus -Request $ExportRequest
```

Der erste Befehl erstellt eine Exportanforderung und speichert Sie dann in der $ExportRequest-Variablen.

Der zweite Befehl ruft den Status der Exportanforderung ab, die in $ExportRequest gespeichert ist.

## Parameter

### -Kennwort
Gibt das Kennwort an, das zum Herstellen einer Verbindung mit dem Azure SQL-Datenbankserver erforderlich ist.
Sie müssen diesen Parameter angeben, wenn Sie den Parameter *Requestor* angegeben haben.

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
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

### -Anfrage
Gibt ein **ImportExportRequest** -Objekt an.
Verwenden Sie das Cmdlet Start-AzureSqlDatabaseImport oder Start-AzureSqlDatabaseExport, um ein Import-oder Export Anforderungsobjekt zu erhalten.

```yaml
Type: ImportExportRequest
Parameter Sets: ByRequestObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Anforderungs-Nr
Gibt die GUID des Import-oder Exportvorgangs an, für den dieses Cmdlet den Status erhält.
Wenn Sie diesen Parameter angeben, müssen Sie die Parameter *username* , *Password* und *Servername* angeben.

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Servername
Gibt den Namen des Azure SQL-Datenbankservers an.
Sie müssen diesen Parameter angeben, wenn Sie den Parameter *Requestor* angegeben haben.

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Username
Gibt den Benutzernamen an, der für die Verbindung mit dem Azure SQL-Datenbankserver erforderlich ist.
Sie müssen diesen Parameter angeben, wenn Sie den Parameter *Requestor* angegeben haben.

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. DataObjects. StatusInfo

## Notizen

## Verwandte Links

[Azure SQL-Datenbank](https://azure.microsoft.com/en-us/services/sql-database/)

[Abrufen des Status der Import Export Datenbank](https://msdn.microsoft.com/en-us/library/azure/dn781289.aspx)

[Vorgänge für Azure SQL-Datenbanken](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Anfang-AzureSqlDatabaseExport](./Start-AzureSqlDatabaseExport.md)

[Anfang-AzureSqlDatabaseImport](./Start-AzureSqlDatabaseImport.md)


