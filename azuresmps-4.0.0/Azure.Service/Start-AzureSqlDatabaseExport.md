---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 3005E411-9466-4602-8E07-F4EF8804AB2A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22bff485bf49e0ec5f482e1325af661862583605
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005958"
---
# Start-AzureSqlDatabaseExport

## Synopsis
Startet einen Exportvorgang aus einer Azure SQL-Datenbank in den BLOB-Speicher.

## Syntax

### ByContainerObject
```
Start-AzureSqlDatabaseExport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContainer <AzureStorageContainer> -DatabaseName <String> -BlobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByContainerName
```
Start-AzureSqlDatabaseExport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContext <IStorageContext> -StorageContainerName <String> -DatabaseName <String> -BlobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Start-AzureSqlDatabaseExport** startet einen Exportvorgang aus einer Azure SQL-Datenbank in den BLOB-Speicher.
Der Vorgang erfordert einen Datenbankserver-Verbindungskontext.
Verwenden Sie das Get-AzureSqlDatabaseImportExportStatus-Cmdlet, um den Status des Exportvorgangs abzurufen.

## Beispiele

### Beispiel 1: Exportieren einer Datenbank
```
PS C:\>$Credential = Get-Credential
PS C:\> $SqlContext = New-AzureSqlDatabaseServerContext -ServerName $ServerName -Credential $Credential
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName $StorageName -StorageAccountKey $StorageKey
PS C:\> $Container = Get-AzureStorageContainer -Name $ContainerName -Context $StorageContext
PS C:\> $exportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
```

In diesem Beispiel wird ein Exportvorgang aus der Azure SQL-Datenbank initiiert, in dem der in der $DatabaseName-Variable gespeicherte Name des in der $BlobName Variablen gespeicherten BLOB-Speichers gespeichert ist.

## Parameter

### -Blobname
Gibt den Namen des Azure BLOB-Speichers an, in dem dieses Cmdlet die Datenbank exportiert.

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

### -DatabaseName
Gibt den Namen der Datenbank an, aus der mit diesem Cmdlet Daten exportiert werden.

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
Gibt den Speichercontainer an, der das BLOB enthält, in das dieses Cmdlet eine Datenbank exportiert.

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
Gibt den Namen des Speichercontainers an, der das BLOB enthält, in das dieses Cmdlet eine Datenbank exportiert.

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

[Datenbank exportieren](https://msdn.microsoft.com/en-us/library/azure/dn781282.aspx)

[Vorgänge für Azure SQL-Datenbanken](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabaseImportExportStatus](./Get-AzureSqlDatabaseImportExportStatus.md)

[Anfang-AzureSqlDatabaseImport](./Start-AzureSqlDatabaseImport.md)


