---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 63889ce74af1051211a579d1af7cc54be14822f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662431"
---
# Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential

## Synopsis
Synchronisiert Anmeldeinformationen zwischen Integrationslauf Zeit Knoten.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ByIntegrationRuntimeName (Standard)
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### ByResourceId
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### ByIntegrationRuntimeObject
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-WhatIf] [-Confirm]
```

## Beschreibung
Das Cmdlet " **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** " synchronisiert lokale Anmeldeinformationen zwischen Integrationslauf Zeit Knoten, wodurch die Anmeldeinformationen in allen Knoten identisch sind.

## Beispiele

### Beispiel 1: Synchronisieren einer Integration Runtime-Anmeldeinformationen
```
PS C:\> Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

Mit dem Cmdlet werden die Anmeldeinformationen zwischen Integrationslauf Zeit Knoten synchronisiert.

## Parameter

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Datafactoryname
Der Name der Daten Factory.

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.

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

### -Inputobject
Das Integrationslauf Zeit Objekt.

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IntegrationRuntimeName
Der Name der Integrationslaufzeit.

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe.

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Resourcen-Nr
Die Azure-Ressourcen-ID.

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## Eingaben

### System. String
Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime


## Ausgaben

### System. Object

## Notizen

## Verwandte Links
