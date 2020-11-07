---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
ms.openlocfilehash: 46455cbf411228f008bdc15c27f78715ccea0e89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664663"
---
# New-AzureRmDataMigrationService

## Synopsis
Erstellt eine neue Instanz des Azure-Daten Bank Migrations Diensts.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureRmDataMigrationService -ResourceGroupName <String> -ServiceName <String> -Location <String>
 -Sku <String> -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>]
```

## Beschreibung
Das New-AzureRmDataMigrationService-Cmdlet erstellt eine neue Instanz des Azure-Daten Bank Migrations Diensts. Dieses Cmdlet übernimmt den Namen der vorhandenen Azure-Ressourcengruppe, den eindeutigen Namen für die neue Instanz des zu erstellenden Azure-Daten Bank Migrations Diensts, den Bereich, in dem die Instanz bereitgestellt wird, den Namen der DMS-Worker-SKU sowie den Namen des virtuellen Azure-Subnets, in dem sich der Dienst befinden soll. Es gibt keinen Parameter für den Abonnement Namen, da erwartet wird, dass der Benutzer das Standardabonnement der Azure-Anmeldesitzung angibt oder Get-AzureRmSubscription-Abonnementname "mysubscription" ausführt | Select-AzureRmSubscription, um ein anderes Abonnement auszuwählen.

## Beispiele

### Beispiel 1
```
PS C:\> New-AzureRmDataMigrationService -ResourceGroupName myResourceGroup -ServiceName TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

Das obige Beispiel zeigt, wie Sie eine neue Instanz des Azure Database Migration Service mit dem Namen Test Service in der Region Central US erstellen.


## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### -Standort
Der Speicherort der zu erstellenden Azure Database Migration Service-Instanz, die einem Azure-Bereich entspricht.

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

### -ResourceGroupName
Der Name der Ressourcengruppe.

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

### -ServiceName
Der Name der Azure-Datenbank-Migrationsdienst Instanz.

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

### -SKU
Die SKU für die Azure Database Migration Service-Instanz. Mögliche Werte sind derzeit Basic_1vCore, Basic_2vCores, GeneralPurpose_4vCores

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

### -VirtualSubnetId
Der Name des Subnetzes unter dem angegebenen virtuellen Netzwerk, das für die Azure-Datenbank-Migrationsdienst Instanz verwendet werden soll.

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




## Ausgaben

### Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService


## Notizen

## Verwandte Links

