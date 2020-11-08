---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 83E8DAD8-151A-408D-819F-274CB813ABDA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6f9a5753fdf4f87afc6baacbe9fc4c33c9be08ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006765"
---
# Get-AzureSqlRecoverableDatabase

## Synopsis
Ruft wiederherstellbare Datenbanken von einem angegebenen Server ab.

## Syntax

### AllDatabasesOnGivenServer (Standard)
```
Get-AzureSqlRecoverableDatabase -ServerName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### GivenDatabaseOnGivenServer
```
Get-AzureSqlRecoverableDatabase -ServerName <String> -DatabaseName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### GivenDatabaseObject
```
Get-AzureSqlRecoverableDatabase -Database <RecoverableDatabase> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureSqlRecoverableDatabase** " ruft wiederherstellbare Datenbanken von einem angegebenen Server ab.
Dieses Cmdlet ruft eine bestimmte wiederherstellbare Datenbank oder alle wiederherstellbaren Datenbanken auf einem Server ab.

## Beispiele

### Beispiel 1: Abrufen aller wiederherstellbaren Datenbanken
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01"
```

Dieser Befehl ruft alle wiederherstellbaren Datenbanken auf dem Server mit dem Namen SERVER01 ab.

### Beispiel 2: Abrufen einer bestimmten wiederherstellbaren Datenbank
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17"
```

Dieser Befehl ruft die Datenbank mit dem Namen Database17 auf dem Server mit dem Namen SERVER01 ab.

## Parameter

### -Datenbank
Gibt ein Objekt an, das die wiederherstellbare Datenbank darstellt, die dieses Cmdlet erhält.

```yaml
Type: RecoverableDatabase
Parameter Sets: GivenDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Gibt den Namen der wiederherstellbaren Datenbank an, die dieses Cmdlet erhält.

```yaml
Type: String
Parameter Sets: GivenDatabaseOnGivenServer
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

### -Servername
Gibt den Namen des Servers an, von dem dieses Cmdlet wiederherstellbare Datenbanken erhält.

```yaml
Type: String
Parameter Sets: AllDatabasesOnGivenServer, GivenDatabaseOnGivenServer
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

### Microsoft. WindowsAzure. Management. SQL. Models. RecoverableDatabase

## Ausgaben

### IEnumerable\<Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase\>

## Notizen
* Sie müssen dieses Cmdlet mithilfe der zertifikatbasierten Authentifizierung ausführen. Führen Sie die folgenden Befehle auf dem Computer aus, auf dem dieses Cmdlet ausgeführt wird: 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## Verwandte Links

[Azure SQL-Datenbank](https://azure.microsoft.com/en-us/services/sql-database/)

[Abrufen einer wiederherstellbaren Datenbank](https://msdn.microsoft.com/en-us/library/azure/dn800985.aspx)

[Vorgänge für Azure SQL-Datenbanken](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Anfang-AzureSqlDatabaseRecovery](./Start-AzureSqlDatabaseRecovery.md)


