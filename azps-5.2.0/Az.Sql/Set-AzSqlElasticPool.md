---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: cb76e0ff789f89079772d7f718c3f16c9c01d707
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296356"
---
# Set-AzSqlElasticPool

## SYNOPSIS
Ändert die Eigenschaften eines Datenbankpools in Azure SQL Datenbank.

## SYNTAX

### DtuBasedPool (Standard)
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### VcoreBasedPool
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Set-AzSqlElasticPool"** legt Eigenschaften für einen Pool in Azure SQL fest. Mit diesem Cmdlet können die eDTUs pro Pool *(Dtu),* die maximale Speichergröße pro Pool *(StorageMB),* die maximalen eDTUs pro Datenbank *(DatabaseDtuMax)* und die minimalen eDTUs pro Datenbank *(DatabaseDtuMin)* geändert werden.
Für mehrere Parameter *("-Dtu", "-DatabaseDtuMin" und "-DatabaseDtuMax")* muss der Festgelegte Wert aus der Liste der gültigen Werte für diesen Parameter erstellt werden. Beispielsweise kann "-DatabaseDtuMax" für einen Standardmäßigen 100 eDTU-Pool nur auf 10, 20, 50 oder 100 festgelegt werden.  Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größenpool in [Poolschwimmen.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)

## BEISPIELE

### Beispiel 1: Ändern der Eigenschaften für einen Pool mit Pool
```powershell
PS C:\>Set-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Dtu 1000 -DatabaseDtuMax 100 -DatabaseDtuMin 20
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/Server01/elasticPools/ElasticPool01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
ElasticPoolName   : ElasticPool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 200
DatabaseDtuMax    : 100
DatabaseDtuMin    : 20
StorageMB         : 204800
Tags              :
```

Mit diesem Befehl werden die Eigenschaften für einen Pool mit dem Namen "poolpool01" geändert. Mit dem Befehl wird die Anzahl der DTUs für den Pool für den Pool auf 1000 und die kleinsten und maximalen DTUs bestimmt.

### Beispiel 2: Ändern der maximalen Speichergröße eines Pool im Pool
```powershell
PS C:\>Set-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -StorageMB 2097152
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/Server01/elasticPools/ElasticPool01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
ElasticPoolName   : ElasticPool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Premium
Dtu               : 200
DatabaseDtuMax    : 100
DatabaseDtuMin    : 20
StorageMB         : 2097152
Tags              :
```

Mit diesem Befehl werden die Eigenschaften für einen Pool mit dem Namen "poolpool01" geändert. Mit dem Befehl wird der maximale Speicher für einen Pool mit Pool und Pool auf 2 TB begrenzt.

### Beispiel 3

Ändert die Eigenschaften eines Datenbankpools in Azure SQL Datenbank. (automatisch generiert)

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticPool -Dtu 1000 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01'
```

## PARAMETERS

### -AsJob
Ausführen des Cmdlets im Hintergrund

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputeGeneration
Die zuzuordnende Rechengenerierung.

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases: Family

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseDtuMax
Gibt die maximale Anzahl von DTUs an, die jede einzelne Datenbank im Pool nutzen kann.
Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größenpool in [Poolschwimmen.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)
Die Standardwerte für verschiedene Editionen sind wie folgt:
- Standard.  5 DTUs
- Standard. 100 DTUs
- Premium. 125 DTUs

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseDtuMin
Gibt die Mindestanzahl von DTUs an, die der Pool für alle Datenbanken im Pool garantiert.
Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größenpool in [Poolschwimmen.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)
Der Standardwert ist null (0).

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseVCoreMax
Die maximale VCore-Zahl, die jede SqlAzure-Datenbank im Pool verbrauchen kann.

```yaml
Type: System.Double
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseVCoreMin
Die minimale VCore-Zahl, die jede SqlAzure-Datenbank im Pool verbrauchen kann.

```yaml
Type: System.Double
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Dtu
Gibt die Gesamtzahl der freigegebenen DTUs für den Pool des Pools an.
Details dazu, welche Werte gültig sind, finden Sie in der Tabelle für Ihren speziellen Größenpool in [Poolschwimmen.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)
Die Standardwerte für verschiedene Editionen sind wie folgt:
- Standard. 100 DTUs
- Standard. 100 DTUs
- Premium. 125 DTUs

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Edition
Gibt die Edition der Azure SQL Datenbank für den Pool an. Sie können die Edition nicht ändern. Die zulässigen Werte für diesen Parameter sind:
- Keine
- Standard
- Standard
- Premium
- DataWarehouse
- Kostenlos
- Strecken
- GeneralPurpose
- BusinessCritical

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolName
Gibt den Namen des Poolpools an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LicenseType
Der Lizenztyp für die Azure Sql-Datenbank.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, der der Pool "Pool" zugeordnet ist.

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

### -ServerName
Gibt den Namen des Servers an, auf dem sich der Pool befindet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageMB
Gibt die Speichergrenze in Megabyte für den Pool an. Weitere Informationen finden Sie im New-AzSqlElasticPool Cmdlet.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tags
Gibt ein Wörterbuch mit Schlüssel-Wert-Paaren an, das dieses Cmdlet dem Pool des Pool in Form einer Hashtabelle zu ordnet. Zum Beispiel: `@{key0="value0";"key 1"=$null;key2="value2"}`

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VCore
Die Gesamtzahl der freigegebenen Vcore für den Sql Azure-Pool".

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ZoneRedundant
Die Zonenredundanz, die dem Azure Sql-Pool (Pool für Sql-Pool) zugeordnet werden soll

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Sql.Pool.Model.AzureSqlElasticPoolModel

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzSqlElasticPool](./Get-AzSqlElasticPool.md)

[Get-AzSqlElasticPoolActivity](./Get-AzSqlElasticPoolActivity.md)

[Get-AzSqlElasticPoolDatabase](./Get-AzSqlElasticPoolDatabase.md)

[New-AzSqlElasticPool](./New-AzSqlElasticPool.md)

[SQL Datenbankdokumentation](https://docs.microsoft.com/azure/sql-database/)
