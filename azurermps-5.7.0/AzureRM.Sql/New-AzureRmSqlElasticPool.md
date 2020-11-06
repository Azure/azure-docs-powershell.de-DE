---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
ms.openlocfilehash: 3d93b0d82a2769acce620ce97141be68c003c281
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498742"
---
# New-AzureRmSqlElasticPool

## Synopsis
Erstellt einen elastischen datenbankpool für eine SQL-Datenbank.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureRmSqlElasticPool -ElasticPoolName <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmSqlElasticPool** erstellt einen elastischen datenbankpool für eine Azure SQL-Datenbank.

Für verschiedene Parameter ( *-DTU,-DatabaseDtuMin und-DatabaseDtuMax* ) ist der festzusetzende Wert aus der Liste gültiger Werte für diesen Parameter erforderlich. Beispiel:-DatabaseDtuMax für einen Standard mäßigen 100-eDTU-Pool kann nur auf 10, 20, 50 oder 100 eingestellt werden.  Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größen Pool in [elastischen Pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool). 

## Beispiele

### Beispiel 1: Erstellen eines elastischen Pools
```
PS C:\>New-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "Standard" -Dtu 400 -DatabaseDtuMin 10 -DatabaseDtuMax 100
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

Dieser Befehl erstellt einen elastischen Pool in der Standard Dienstebene mit dem Namen ElasticPool01. Der Server mit dem Namen Server01, der einer Azure-Ressourcengruppe mit dem Namen ResourceGroup01 zugewiesen ist, hostet den elastischen Pool in. Mit dem Befehl werden die DTU-Eigenschaftswerte für den Pool und die Datenbanken im Pool angegeben.

## Parameter

### -AsJob
Ausführen eines Cmdlets im Hintergrund
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

### -DatabaseDtuMax
Gibt die maximale Anzahl von Datenbankdurchsatz Einheiten (DTUs) an, die eine einzelne Datenbank im Pool nutzen kann.
Die Standardwerte für die verschiedenen Editionen lauten wie folgt:

- Grundlegende. 5 DTUs
- Standard. 100 DTUs
- Premium. 125 DTUs

Informationen dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größen Pool in [elastischen Pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool) . 


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

### -DatabaseDtuMin
Gibt die minimale Anzahl von DTUs an, die der elastische Pool für alle Datenbanken im Pool garantiert.
Der Standardwert ist 0 (null).

Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größen Pool in [elastischen Pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool). 

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

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DTU
Gibt die Gesamtzahl der freigegebenen DTUs für den elastischen Pool an.
Die Standardwerte für die verschiedenen Editionen lauten wie folgt:

- Grundlegende.
100 DTUs
- Standard.
100 DTUs
- Premium.
125 DTUs

Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größen Pool in [elastischen Pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool). 

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

### -Edition
Gibt die Edition der Azure SQL-Datenbank an, die für den elastischen Pool verwendet wird.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Premium
- Grundlegende
- Standard
- Datawarehouse
- Stretch

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ElasticPoolName
Gibt den Namen des von diesem Cmdlet erstellten elastischen Pools an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, der dieses Cmdlet den elastischen Pool zuweist.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Servername
Gibt den Namen des Servers an, der den elastischen Pool hostet.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageMB
Gibt den Speichergrenzwert für den elastischen Pool in Megabyte an. Wenn Sie diesen Parameter nicht angeben, berechnet dieses Cmdlet einen Wert, der vom Wert des *DTU* -Parameters abhängt.

Siehe [eDTU-und Speichergrenzwerte](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) für mögliche Werte.

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

### -Tags
Gibt ein Wörterbuch mit Schlüssel-Wert-Paaren in Form einer Hashtabelle an, die dieses Cmdlet dem elastischen Pool zuordnet. Zum Beispiel:

@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ZoneRedundant
Die Zonen Redundanz, die dem Azure SQL-elastischen Pool zugeordnet werden soll

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

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel

## Notizen

## Verwandte Links

[Get-AzureRmSqlElasticPool](./Get-AzureRmSqlElasticPool.md)

[Get-AzureRmSqlElasticPoolActivity](./Get-AzureRmSqlElasticPoolActivity.md)

[Get-AzureRmSqlElasticPoolDatabase](./Get-AzureRmSqlElasticPoolDatabase.md)

[Remove-AzureRmSqlElasticPool](./Remove-AzureRmSqlElasticPool.md)

[Satz-AzureRmSqlElasticPool](./Set-AzureRmSqlElasticPool.md)

[SQL-Datenbank-Dokumentation](https://docs.microsoft.com/azure/sql-database/)
