---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35e29655e8447644b6c5449309424595e45ca187
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413063"
---
# Start-AzureSqlDatabaseCopy

## SYNOPSIS
Startet einen Kopiervorgang einer Azure SQL-Datenbank.

## SYNTAX

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

## BESCHREIBUNG
Das **Cmdlet "Start-AzureSqlDatabaseCopy"** startet einen einmaligen Kopiervorgang oder einen kontinuierlichen Kopiervorgang einer bestimmten Azure SQL-Datenbank.
Dieses Cmdlet ist keine Transaktion.

Die ursprüngliche Datenbank ist die Quelldatenbank.
Die Kopie ist die sekundäre Oder Zieldatenbank.
Bei einer fortlaufenden Kopie können sich die Quell- und Zieldatenbanken nicht auf demselben Server befinden, und die Server, die als Host für die Quell- und Zieldatenbanken verwendet werden, müssen Teil desselben Abonnements sein.

Wenn Sie den Parameter *"ContinuousCopy" nicht* angeben, erstellt dieses Cmdlet eine einmalkopie der Quelldatenbank.
Wenn die Antwort empfangen wird, kann der Vorgang noch ausgeführt werden.
Sie können den Vorgang mithilfe des cmdlets Get-AzureSqlDatabaseCopy oder Get-AzureSqlDatabaseOperation überwachen.

Wenn Sie *"ContinuousCopy"* angeben, erstellt dieses Cmdlet eine fortlaufende Kopie der Quelldatenbank.
Wenn die Antwort empfangen wird, wird der Vorgang ausgeführt.
Sie können den Vorgang mithilfe von **"Get-AzureSqlDatabaseCopy"** oder **"Get-AzureSqlDatabaseOperation" überwachen.**

Sie können eine fortlaufende Kopie als Online- oder Offlinedatenbank erstellen.
Die fortlaufende Onlinekopie wird zum Konfigurieren von active Geo-Replication für Azure SQL https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ verwendet.
Die fortlaufende Offlinekopie wird verwendet, um Standard-Geo-Replication für Azure SQL zu https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ konfigurieren.

## BEISPIELE

### Beispiel 1: Planen einer fortlaufenden Datenbankkopie
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

Mit diesem Befehl wird eine fortlaufende Kopie der Datenbank mit dem Namen "Orders" auf dem Server mit dem Namen "lpqd0zbr8y" geplant.
Der Befehl erstellt eine Zieldatenbank auf dem Server mit dem Namen bk0b8kf658.

### Beispiel 2: Erstellen einer Einmalkopie auf demselben Server
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

Mit diesem Befehl wird eine Einmalkopie der Datenbank mit dem Namen "Orders" auf dem Server mit dem Namen "lpqd0zbr8y" erstellt.
Mit dem Befehl wird eine Kopie mit dem Namen "OrdersCopy" auf demselben Server erstellt.

### Beispiel 3: Planen einer fortlaufenden Offlinedatenbankkopie
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

Mit diesem Befehl wird eine fortlaufende Kopie der Datenbank mit dem Namen "Orders" auf dem Server mit dem Namen "lpqd0zbr8y" geplant.
Mit diesem Befehl wird eine Offlinezieldatenbank auf dem Server mit dem Namen bk0b8kf658 erstellt.

## PARAMETERS

### -ContinuousCopy
Gibt an, dass die Datenbankkopie eine fortlaufende Kopie (eine Replikatdatenbank) ist.
Kontinuierliches Kopieren wird auf demselben Server nicht unterstützt.
Wenn dieser Parameter nicht angegeben wird, wird eine Einmalkopie ausgeführt.
Bei einer einmal erstellten Kopie müssen sich die Quell- und Partnerdatenbank auf demselben Server befinden.

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

### -Database
Gibt ein Objekt an, das die Azure SQL darstellt.
Dieser Parameter akzeptiert die Pipelineeingabe.

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
Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.

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
Gibt an, dass eine fortlaufende Kopie keine aktive Kopie, sondern eine passive Kopie ist.
Wenn es sich bei der Quelldatenbank um eine Standardeditionsdatenbank handelt, ist dieser Parameter erforderlich.
Wenn dieser Parameter angegeben wird, muss *auch "ContinuousCopy"* angegeben werden.

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
Wenn Sie den Parameter *"ContinuousCopy"* angeben, muss der Wert für *"PartnerDatabase"* mit dem Namen der Quelldatenbank übereinstimmen.
Wenn Sie *"ContinuousCopy" nicht* angeben, müssen Sie einen Namen für die Zieldatenbank angeben, der sich vom Quelldatenbanknamen unterscheiden kann.

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
Dieser Server muss im selben Abonnement wie der Quelldatenbankserver vorhanden sein.

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

### -Profile
Gibt das Azure-Profil an, aus dem dieses Cmdlet liest.
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

### -ServerName
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

### -Confirm
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

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

### -Waswenn
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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database

## AUSGABEN

### Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy

## HINWEISE
* Authentifizierung: Für dieses Cmdlet ist zertifikatbasierte Authentifizierung erforderlich. Ein Beispiel für die Verwendung der zertifikatbasierten Authentifizierung zum Festlegen des aktuellen Abonnements finden Sie unter New-AzureSqlDatabaseServerContext Cmdlet.
* Überwachung: Verwenden Sie das **Cmdlet "Get-AzureSqlDatabaseCopy",** um den Status einer oder mehreren kontinuierlichen Kopierbeziehungen zu überprüfen, die auf dem Server aktiv sind. Verwenden Sie das Cmdlet **"Get-AzureSqlDatabaseOperation",** um den Status der Vorgänge sowohl an der Quelle als auch an dem Ziel der fortlaufenden Kopierbeziehung zu überprüfen.

## LINKS ZU VERWANDTEN THEMEN

[Azure SQL-Datenbank](https://azure.microsoft.com/en-us/services/sql-database/)

[Vorgänge für Azure SQL Datenbanken](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Starten einer Datenbankkopie](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)



[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[Stop-AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


