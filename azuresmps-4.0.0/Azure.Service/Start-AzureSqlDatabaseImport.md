---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5EE936CA-DD9A-4BC6-B835-E22AE633B46D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bc7c8f39f1bdbd35cfffeb59b3b4f184f30845e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005633"
---
# Start-AzureSqlDatabaseImport

## Synopsis
Startet einen Importvorgang aus dem BLOB-Speicher in eine Azure SQL-Datenbank.

## Syntax

### ByContainerObject
```
Start-AzureSqlDatabaseImport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContainer <AzureStorageContainer> -DatabaseName <String> -BlobName <String>
 [-Edition <DatabaseEdition>] [-DatabaseMaxSize <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByContainerName
```
Start-AzureSqlDatabaseImport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContext <IStorageContext> -StorageContainerName <String> -DatabaseName <String> -BlobName <String>
 [-Edition <DatabaseEdition>] [-DatabaseMaxSize <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Start-AzureSqlDatabaseImport** startet einen Importvorgang aus Azure BLOB Storage in eine Azure SQL-Datenbank.
Wenn die Datenbank nicht vorhanden ist, wird Sie von diesem Cmdlet mithilfe der von Ihnen angegebenen Größen-und Editions Werte erstellt.
Der Vorgang erfordert einen Datenbankserver-Verbindungskontext.
Verwenden Sie das Get-AzureSqlDatabaseImportExportStatus-Cmdlet, um den Status des Importvorgangs abzurufen.

## Beispiele

### Beispiel 1: Importieren einer Datenbank
```
PS C:\>$Credential = Get-Credential
PS C:\> $SqlContext = New-AzureSqlDatabaseServerContext -ServerName $ServerName -Credentials $Credential
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName $StorageName -StorageAccountKey $StorageKey
PS C:\> $Container = Get-AzureStorageContainer -Name $ContainerName -Context $StorageContext
PS C:\> $ImportRequest = Start-AzureSqlDatabaseImport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
```

In diesem Beispiel wird ein Importvorgang aus dem BLOB-Speicher in der $BlobName Variablen in die Azure SQL-Datenbank namens DatabaseName initiiert.

## Parameter

### -Blobname
Gibt den Namen des Azure BLOB-Speichers an, aus dem dieses Cmdlet die Datenbank importiert.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseMaxSize
Gibt die maximale Größe für die Datenbank in Gigabyte an.
Wenn die Datenbank nicht vorhanden ist, wird Sie von diesem Cmdlet basierend auf dieser maximalen Größe erstellt.
Die akzeptablen Werte unterscheiden sich je nach Edition.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseName
Gibt einen Namen für die Datenbank an.
Wenn die Datenbank nicht vorhanden ist, wird Sie von diesem Cmdlet erstellt, und der Name, den dieser Parameter angibt, wird zugewiesen.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Edition
Gibt die Edition der Datenbank an.
Wenn die Datenbank nicht vorhanden ist, wird Sie von diesem Cmdlet als diese Edition erstellt.
Gültige Werte sind: 

- Keine
- Web 
- Business 
- Grundlegende
- Standard
- Premium

Der Standardwert ist Web.

```yaml
Type: DatabaseEdition
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

### -SqlConnection
Gibt den Verbindungskontext eines Servers an, der die Datenbank enthält.

```yaml
Type: ISqlServerConnectionInformation
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageContainer
Gibt den Speichercontainer an, der das BLOB enthält, aus dem dieses Cmdlet eine Datenbank importiert.

```yaml
Type: AzureStorageContainer
Parameter Sets: ByContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageContainerName
Gibt den Namen des BLOB-Speichercontainers an.

```yaml
Type: String
Parameter Sets: ByContainerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Storagecontext
Gibt den Kontext des BLOB-Speichercontainers an.

```yaml
Type: IStorageContext
Parameter Sets: ByContainerName
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

### Microsoft. WindowsAzure. Commands. SQLDatabase. Services. ImportExportRequest

## Notizen

## Verwandte Links

[Azure SQL-Datenbank](https://azure.microsoft.com/en-us/services/sql-database/)

[Datenbank importieren](https://msdn.microsoft.com/en-us/library/azure/dn781284.aspx)

[Vorgänge für Azure SQL-Datenbanken](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabaseImportExportStatus](./Get-AzureSqlDatabaseImportExportStatus.md)

[Anfang-AzureSqlDatabaseExport](./Start-AzureSqlDatabaseExport.md)


