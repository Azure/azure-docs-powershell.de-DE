---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 69A26BF3-7FE7-41ED-8C21-C8DC72D09615
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/start-azurermsqlserverupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: 279216ad20783017f091143a7c440873c8e04946
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481946"
---
# Start-AzureRmSqlServerUpgrade

## Synopsis
Startet das Upgrade eines SQL-Datenbankservers.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Start-AzureRmSqlServerUpgrade -ServerVersion <String> [-ScheduleUpgradeAfterUtcDateTime <DateTime>]
 [-DatabaseCollection <RecommendedDatabaseProperties[]>]
 [-ElasticPoolCollection <UpgradeRecommendedElasticPoolProperties[]>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Start-AzureRmSqlServerUpgrade** startet das Upgrade eines Azure SQL-Datenbankservers, Version 11, auf Version 12.
Mithilfe des Get-AzureRmSqlServerUpgrade-Cmdlets können Sie den Fortschritt eines Upgrades überwachen.

## Beispiele

### Beispiel 1: Aktualisieren eines Servers
```
PS C:\>Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0
ResourceGroupName               : ResourceGroup01
ServerName                      : Server01
ServerVersion                   : 12.0
ScheduleUpgradeAfterUtcDateTime : 
DatabaseCollection              :
```

Mit diesem Befehl wird der Server namens SERVER01 aktualisiert, der der Ressourcengruppe TesourceGroup01 zugeordnet ist.

### Beispiel 2: Aktualisieren eines Servers mithilfe von Planungszeit und Daten Bank Empfehlung
```
PS C:\>$ScheduleTime = (Get-Date).AddMinutes(5).ToUniversalTime()
PS C:\> $DatabaseMap = New-Object -TypeName Microsoft.Azure.Management.Sql.Models.RecommendedDatabaseProperties
PS C:\> $DatabaseMap.Name = "contosodb"
PS C:\> $DatabaseMap.TargetEdition = "Standard"
PS C:\> $DatabaseMap.TargetServiceLevelObjective = "S0"
PS C:\> Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0 -ScheduleUpgradeAfterUtcDateTime $ScheduleTime -DatabaseCollection ($DatabaseMap)
```

Der erste Befehl erstellt in Zukunft fünf Minuten mit dem Get-Date-Cmdlet.
Der Befehl speichert das Datum in der Variablen $ScheduleTime.
Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .
Der zweite Befehl erstellt ein **RecommendedDatabaseProperties** -Objekt und speichert dieses Objekt dann in der Variablen $DatabaseMap.
In den nächsten drei Befehlen werden Eigenschaften des Objekts, das in $DatabaseMap gespeichert ist, Werte zugewiesen.
Mit dem letzten Befehl wird der vorhandene Server Server01 auf Version 12,0 aktualisiert.
Der früheste Aktualisierungszeitpunkt ist fünf Minuten nach der Ausführung des Befehls, wie durch die $ScheduleTime-Variable angegeben.
Nach dem Upgrade wird in der Datenbank-contosodb die Standard Edition ausgeführt und der Service Level-Ziel-S0-Wert bereitgestellt.

## Parameter

### -DatabaseCollection
Gibt ein Array von **RecommendedDatabaseProperties** -Objekten an, die dieses Cmdlet für das Server Upgrade verwendet.

```yaml
Type: Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -ElasticPoolCollection
Gibt ein Array von **UpgradeRecommendedElasticPoolProperties** -Objekten an, die für das Server Upgrade verwendet werden sollen.

```yaml
Type: Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.

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

### -ScheduleUpgradeAfterUtcDateTime
Gibt den frühesten Zeitpunkt als **DateTime** -Objekt an, um den Server zu aktualisieren.
Geben Sie einen Wert im ISO8601-Format in koordinierter Weltzeit (Coordinated Universal Time, UTC) an.
Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Servername
Gibt den Namen des Servers an, der vom Cmdlet aktualisiert wird.

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

### -Server Version vom
Gibt die Version an, auf die das Cmdlet den Server aktualisiert.
Der einzige gültige Wert ist 12,0.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. SQL. Serverupgrade. Model. AzureSqlServerUpgradeStartModel

## Notizen

## Verwandte Links

[Get-AzureRmSqlServerUpgrade](./Get-AzureRmSqlServerUpgrade.md)

[Stopp-AzureRmSqlServerUpgrade](./Stop-AzureRmSqlServerUpgrade.md)

[SQL-Datenbank-Dokumentation](https://docs.microsoft.com/azure/sql-database/)


