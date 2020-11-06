---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/get-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationService.md
ms.openlocfilehash: cac57ff34d925d553c25d97facd81dba017a25c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498965"
---
# Get-AzureRmDataMigrationService

## Synopsis
Ruft die Eigenschaften ab, die einer Instanz des Azure Database Migration Service zugeordnet sind. 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ResourceGroupSet (Standard)
```
Get-AzureRmDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
```

### ResourceIdParameterSet
```
Get-AzureRmDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
```

### ServiceNameGroupSet
```
Get-AzureRmDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>]
```
## Beschreibung
Das Get-AzureRmDataMigrationService-Cmdlet ruft die Eigenschaften ab, die einer Instanz des Azure Database-Migrations Diensts zugeordnet sind, basierend auf dem Dienstnamen und dem Namen der Azure-Ressourcengruppe als Eingabeparameter. 

## Beispiele

### Beispiel 1
```
PS C:\> Get-AzureRmDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

Im obigen Beispiel werden die Eigenschaften der Azure Database Migration Service-Instanz mit dem Namen Test Service abgerufen. 

### Beispiel 2
```
PS C:\> Get-AzureRmDataMigrationService -ResourceGroupName testResourceGroup 
```

Im obigen Beispiel werden Azure Database Migration Services in der Ressourcengruppe namens testResourceGroup abgerufen. 

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

### -Name
Name des Daten Migrations Diensts.

```yaml
Type: String
Parameter Sets: ServiceNameGroupSet
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe.

```yaml
Type: String
Parameter Sets: ResourceGroupSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServiceNameGroupSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Resourcen-Nr
DataMigrationService-Ressourcen-ID.

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## Eingaben

### System. String


## Ausgaben

### System. Collections. Generic. IList ' 1 [[Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService, Microsoft. Azure. Commands. datamigration, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]


## Notizen

## Verwandte Links





