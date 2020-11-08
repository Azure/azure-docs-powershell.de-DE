---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc350cdf117ebbf72b023f64895f4c563e73566b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006051"
---
# Start-AzureSqlDatabaseCopy

## Synopsis
Startet einen Kopiervorgang einer Azure SQL-Datenbank.

## Syntax

### ByInputObject
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObjectContinuous
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDatabaseName
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDatabaseNameContinuous
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Start-AzureSqlDatabaseCopy** startet einen einmaligen Kopiervorgang oder einen fortlaufenden Kopiervorgang einer bestimmten Azure SQL-Datenbank.
Dieses Cmdlet ist nicht transaktional.

Die ursprüngliche Datenbank ist die Quelldatenbank.
Die Kopie ist die sekundäre oder Zieldatenbank.
Bei einer fortlaufenden Kopie können sich die Quell-und Zieldatenbanken nicht auf demselben Server befinden, und die Server, die die Quell-und Zieldatenbanken hosten, müssen Teil desselben Abonnements sein.

Wenn Sie den *ContinuousCopy* -Parameter nicht angeben, erstellt dieses Cmdlet eine einmalige Kopie der Quelldatenbank.
Wenn die Antwort empfangen wird, kann der Vorgang weiterhin ausgeführt werden.
Sie können den Vorgang mithilfe des Get-AzureSqlDatabaseCopy-oder Get-AzureSqlDatabaseOperation-Cmdlets überwachen.

Wenn Sie *ContinuousCopy* angeben, erstellt dieses Cmdlet eine fortlaufende Kopie der Quelldatenbank.
Wenn die Antwort empfangen wird, wird der Vorgang ausgeführt.
Sie können den Vorgang mithilfe von **Get-AzureSqlDatabaseCopy** oder **Get-AzureSqlDatabaseOperation** überwachen.

Sie können eine fortlaufende Kopie als Online-oder Offlinedatenbank erstellen.
Die fortlaufende Onlinekopie wird verwendet, um Active Geo-Replication für Azure SQL-Datenbank zu konfigurieren https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ .
Die fortlaufende Offlinekopie wird verwendet, um die Standard Geo-Replication für Azure SQL-Datenbank zu konfigurieren https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ .

## Beispiele

### Beispiel 1: Planen einer fortlaufenden Datenbankkopie
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

Dieser Befehl plant eine fortlaufende Kopie der Datenbank mit dem Namen "Aufträge" auf dem Server mit dem Namen lpqd0zbr8y.
Der Befehl erstellt eine Zieldatenbank auf dem Server mit dem Namen bk0b8kf658.

### Beispiel 2: Erstellen einer einmaligen Kopie auf dem gleichen Server
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

Mit diesem Befehl wird eine einmalige Kopie der Datenbank mit dem Namen "Aufträge" auf dem Server mit dem Namen "lpqd0zbr8y" erstellt.
Der Befehl erstellt eine Kopie mit dem Namen OrdersCopy auf demselben Server.

### Beispiel 3: Planen einer fortlaufenden Offline-Datenbankkopie
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

Dieser Befehl plant eine fortlaufende Kopie der Datenbank mit dem Namen "Aufträge" auf dem Server mit dem Namen lpqd0zbr8y.
Dieser Befehl erstellt eine Offline Zieldatenbank auf dem Server mit dem Namen bk0b8kf658.

## Parameter

### -ContinuousCopy
Gibt an, dass es sich bei der Datenbankkopie um eine fortlaufende Kopie (eine Replikatdatenbank) handelt.
Die fortlaufende Kopie wird nicht innerhalb desselben Servers unterstützt.
Wenn dieser Parameter nicht angegeben wird, wird eine einmalige Kopie ausgeführt.
Bei einer einmaligen Kopie müssen sich die Quell-und Partner Datenbanken auf demselben Server befinden.

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Datenbank
Gibt ein Objekt an, das die Azure SQL-Quelldatenbank darstellt.
Dieser Parameter akzeptiert Pipelineeingaben.

```yaml
Type: Database
Parameter Sets: ByInputObject, ByInputObjectContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Gibt den Namen der Quelldatenbank an.

```yaml
Type: String
Parameter Sets: ByDatabaseName, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.

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

### -OfflineSecondary
Gibt an, dass eine fortlaufende Kopie eine passive Kopie und keine aktive Kopie ist.
Wenn es sich bei der Quelldatenbank um eine Standard Edition-Datenbank handelt, ist dieser Parameter erforderlich.
Wenn dieser Parameter angegeben wird, muss auch *ContinuousCopy* angegeben werden.

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerDatabase
Gibt den Namen der Zieldatenbank an.
Wenn Sie den *ContinuousCopy* -Parameter angeben, muss der Wert für *PartnerDatabase* mit dem Namen der Quelldatenbank übereinstimmen.
Wenn Sie *ContinuousCopy* nicht angeben, müssen Sie einen Namen für die Zieldatenbank angeben, der vom Namen der Quelldatenbank abweichen kann.

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServer
Gibt den Namen des Servers an, der die Zieldatenbank hostet.
Dieser Server muss sich im gleichen Azure-Abonnement wie der Quelldatenbankserver befinden.

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
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
Gibt den Namen des Servers an, auf dem sich die Quelldatenbank befindet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

### Microsoft. WindowsAzure. Commands. SQLDatabase. Model. DatabaseCopy

## Notizen
* Authentifizierung: Dieses Cmdlet erfordert zertifikatbasierte Authentifizierung. Ein Beispiel für die Verwendung der zertifikatbasierten Authentifizierung zum Einrichten des aktuellen Abonnements finden Sie unter New-AzureSqlDatabaseServerContext-Cmdlets.
* Überwachung: Verwenden Sie das Cmdlet " **Get-AzureSqlDatabaseCopy** ", um den Status einer oder mehrerer kontinuierlicher Kopier Beziehungen zu überprüfen, die auf dem Server aktiv sind. Verwenden Sie das Cmdlet **Get-AzureSqlDatabaseOperation** , um den Status der Vorgänge sowohl auf Quelle als auch auf Ziel der fortlaufenden Kopie-Beziehung zu überprüfen.

## Verwandte Links

[Azure SQL-Datenbank](https://azure.microsoft.com/en-us/services/sql-database/)

[Vorgänge für Azure SQL-Datenbanken](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Datenbankkopie starten](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)

[Azure SQL-Datenbank-Cmdlets](./Azure.SQLDatabase.md)

[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[Stopp-AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


