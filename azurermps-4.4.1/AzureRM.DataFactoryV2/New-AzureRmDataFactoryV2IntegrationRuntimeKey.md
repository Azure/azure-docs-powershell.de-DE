---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 166bae99bebbc5a1b1c25ffc79faa3a1f7254bbc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662432"
---
# New-AzureRmDataFactoryV2IntegrationRuntimeKey

## Synopsis
Generieren Sie den selbst gehosteten Integrationslauf Zeitschlüssel erneut.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ByIntegrationRuntimeName (Standard)
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### ByResourceId
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String> [-WhatIf]
 [-Confirm]
```

### ByIntegrationRuntimeObject
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force]
 [-InputObject] <PSIntegrationRuntime> [-WhatIf] [-Confirm]
```

## Beschreibung
Das Cmdlet **New-AzureRmDataFactoryV2IntegrationRuntimeKey** regeneriert den Integrationslauf Zeitschlüssel mit dem Schlüsselnamen, der durch den Parameter "keyname" angegeben wird. Der vorherige Schlüssel ist ungültig.

## Beispiele

### Beispiel 1: Generieren eines neuen Schlüssels für eine Integrationslaufzeit
```
PS C:\> New-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

Das Cmdlet generiert den Schlüssel "authKey2" für die Integrationslaufzeit mit dem Namen "Test-SelfHost-IR" neu.

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

### -KeyName
Der Authentifizierungsschlüssel Name der selbst gehosteten Integrationslaufzeit.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AuthKey1, AuthKey2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Der Name der Integrationslaufzeit.

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

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

### Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys


## Notizen

## Verwandte Links
[Get-AzureRmDataFactoryV2IntegrationRuntimeKey]()
