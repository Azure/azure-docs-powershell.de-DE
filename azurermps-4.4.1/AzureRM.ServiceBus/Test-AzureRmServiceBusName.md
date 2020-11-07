---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: 892177efebb3a62e40f79b80b1ac67c488e048d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664431"
---
# Test-AzureRmServiceBusName

## Synopsis
Überprüft die Verfügbarkeit des angegebenen Namespace namens.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Test-AzureRmServiceBusName [-Namespace] <String>
```

## Beschreibung
Das Cmdlet " **Test-AzureRmServiceBusName** " Überprüfen der Verfügbarkeit des Namespace namens

## Beispiele

### Beispiel 1
```
PS C:\> Test-AzureRmServiceBusName -Namespace TestingtheAvailability
```

### Beispiel 2
```
PS C:\> Test-AzureRmServiceBusName -Namespace Testi
```

### Beispiel 3
```
PS C:\> Test-AzureRmServiceBusName -Namespace Test123
```

Gibt den Status der Verfügbarkeit des Namespacenamens zurück

## Parameter

### -Namespace
Name des ServiceBus-Namespaces.

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
### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### -Namespace
 System. String

## Ausgaben

### [Microsoft. Azure. Commands. ServiceBus. Models. CheckNameAvailabilityResultAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]

### Beispiel 1
NameAvailable-Grund Nachricht
------------- ------ -------
         True   None

### Beispiel 2
NameAvailable-Grund Nachricht
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### Beispiel 3
NameAvailable-Grund Nachricht
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## Notizen

## Verwandte Links
