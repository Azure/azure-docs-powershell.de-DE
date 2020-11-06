---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
ms.openlocfilehash: 61f66a61d14738da034644fc3dfef865c8719181
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481445"
---
# Restore-AzureRmSqlDatabase

## Synopsis
Stellt eine SQL-Datenbank wieder her.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### FromPointInTimeBackup
```
Restore-AzureRmSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <DatabaseEdition>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FromDeletedDatabaseBackup
```
Restore-AzureRmSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <DatabaseEdition>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FromGeoBackup
```
Restore-AzureRmSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <DatabaseEdition>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### FromLongTermRetentionBackup
```
Restore-AzureRmSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <DatabaseEdition>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Restore-AzureRmSqlDatabase** stellt eine SQL-Datenbank aus einer Geo-redundanten Sicherung, einer Sicherung einer gelöschten Datenbank, einer langfristigen Aufbewahrungs Sicherung oder einem Zeitpunkt in einer Livedatenbank wieder her.
Die wiederhergestellte Datenbank wird als neue Datenbank erstellt.

Sie können eine elastische SQL-Datenbank erstellen, indem Sie den *ElasticPoolName* -Parameter auf einen vorhandenen elastischen Pool festlegen.

## Beispiele

### Beispiel 1: Wiederherstellen einer Datenbank ab einem bestimmten Zeitpunkt
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

Der erste Befehl ruft die SQL-Datenbank mit dem Namen database01 ab und speichert Sie dann in der $Database-Variablen.

Der zweite Befehl stellt die Datenbank in $Database aus der angegebenen Point-in-Time-Sicherung in der Datenbank mit dem Namen RestoredDatabase wieder her.

### Beispiel 2: Wiederherstellen einer Datenbank von einem bestimmten Zeitpunkt zu einem elastischen Pool
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

Der erste Befehl ruft die SQL-Datenbank mit dem Namen database01 ab und speichert Sie dann in der $Database-Variablen.

Der zweite Befehl stellt die Datenbank in $Database aus der angegebenen Point-in-Time-Sicherung in der SQL-Datenbank namens RestoredDatabase im elastischen Pool mit dem Namen elasticpool01 wieder her.

### Beispiel 3: Wiederherstellen einer gelöschten Datenbank
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

Der erste Befehl ruft die gelöschte Datenbanksicherung ab, die Sie mithilfe von [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md)wiederherstellen möchten.
Mit dem zweiten Befehl wird die Wiederherstellung aus der gelöschten Datenbanksicherung mit dem Cmdlet [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) gestartet. Wenn der Parameter-PointInTime nicht angegeben wird, wird die Datenbank in der Lösch Zeit wiederhergestellt.

### Beispiel 4: Wiederherstellen einer gelöschten Datenbank in einem elastischen Pool
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

Der erste Befehl ruft die gelöschte Datenbanksicherung ab, die Sie mithilfe von [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md)wiederherstellen möchten.
Mit dem zweiten Befehl wird die Wiederherstellung aus der gelöschten Datenbanksicherung mithilfe von [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md)gestartet. Wenn der Parameter-PointInTime nicht angegeben wird, wird die Datenbank in der Lösch Zeit wiederhergestellt.

### Beispiel 5: Geo-Restore einer Datenbank
```
PS C:\>$GeoBackup = Get-AzureRmSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

Der erste Befehl ruft die Geo-redundante Sicherung für die Datenbank mit dem Namen database01 ab und speichert Sie dann in der $GeoBackup-Variablen.

Der zweite Befehl stellt die Sicherung in $GeoBackup in der SQL-Datenbank mit dem Namen RestoredDatabase wieder her.

## Parameter

### -DeletionDate
Gibt das Löschdatum als **DateTime** -Objekt an.
Verwenden Sie das Get-Date-Cmdlet, um ein **DateTime** -Objekt abzurufen.

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Edition
Gibt die Edition der SQL-Datenbank an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Keine
- Premium
- Grundlegende
- Standard
- Datawarehouse
- Kostenlos

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ElasticPoolName
Gibt den Namen des elastischen Pools an, in dem die SQL-Datenbank abgelegt werden soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FromDeletedDatabaseBackup
Gibt an, dass dieses Cmdlet eine Datenbank aus einer Sicherung einer gelöschten SQL-Datenbank wieder herstellt.
Sie können das Get-AzureRMSqlDeletedDatabaseBackup-Cmdlet verwenden, um die Sicherung einer gelöschten SQL-Datenbank abzurufen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromDeletedDatabaseBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FromGeoBackup
Gibt an, dass dieses Cmdlet eine SQL-Datenbank aus einer Geo-redundanten Sicherung wieder herstellt.
Sie können das Get-AzureRMSqlDatabaseGeoBackup-Cmdlet verwenden, um eine Geo-redundante Sicherung zu erhalten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromGeoBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FromLongTermRetentionBackup
Gibt an, dass dieses Cmdlet eine SQL-Datenbank aus einer langfristigen Aufbewahrungs Sicherung wieder herstellt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromLongTermRetentionBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FromPointInTimeBackup
Gibt an, dass dieses Cmdlet eine SQL-Datenbank aus einer Point-in-Time-Sicherung wieder herstellt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromPointInTimeBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PointInTime
Gibt den Zeitpunkt als **DateTime** -Objekt an, in dem Sie Ihre SQL-Datenbank wiederherstellen möchten.
Verwenden Sie das Cmdlet " **Get-Date** ", um ein **DateTime** -Objekt abzurufen.

Verwenden Sie diesen Parameter zusammen mit dem *FromPointInTimeBackup* -Parameter.

```yaml
Type: System.DateTime
Parameter Sets: FromPointInTimeBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, der das Cmdlet die SQL-Datenbank zuweist.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Resourcen-Nr
Gibt die ID der wiederherzustellenden Ressource an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Servername
Gibt den Namen des SQL-Datenbankservers an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceObjectiveName
Gibt den Namen des Dienst Ziels an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zieldatenbankname
Gibt den Namen der Datenbank an, die wiederhergestellt werden soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel

## Notizen

## Verwandte Links

[Wiederherstellen einer Azure SQL-Datenbank aus einem Ausfall](https://go.microsoft.com/fwlink/?LinkId=746882)

[Wiederherstellen einer Azure SQL-Datenbank aus einem Benutzer Fehler](https://go.microsoft.com/fwlink/?LinkId=746944)

[Get-AzureRmSqlDatabase](./Get-AzureRmSqlDatabase.md)

[Get-AzureRMSqlDatabaseGeoBackup](./Get-AzureRMSqlDatabaseGeoBackup.md)

[Get-AzureRMSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md)

[SQL-Datenbank-Dokumentation](https://docs.microsoft.com/azure/sql-database/)

