---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/test-azurermrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
ms.openlocfilehash: adf7c4b7f8d80e16b49d9d55b742a55279232a07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498870"
---
# Test-AzureRmRelayName

## Synopsis
Überprüft die Verfügbarkeit des angegebenen Namespace namens.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Test-AzureRmRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Test-AzureRmRelayName** " Überprüfen der Verfügbarkeit des Namespace namens

## Beispiele

### Beispiel 1
```
PS C:\> Test-AzureRmRelayName -Namespace TestingtheAvailability
```

### Beispiel 2
```
PS C:\> Test-AzureRmRelayName -Namespace Testi
```

### Beispiel 3
```
PS C:\> Test-AzureRmRelayName -Namespace Test123
```

Gibt den Status der Verfügbarkeit des Namespacenamens zurück

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

### -Namespace
Name des Relay-Namespaces.

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

### [Microsoft. Azure. Commands. Relay. Models. CheckNameAvailabilityResultAttributes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]

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

