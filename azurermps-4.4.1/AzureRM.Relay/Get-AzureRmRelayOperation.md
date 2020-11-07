---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayOperation.md
ms.openlocfilehash: 8cd5e0a74f26f4744e2c086b4d689a8d06ebf5b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662620"
---
# Get-AzureRmRelayOperation

## Synopsis
Liste unterstützter Relay-Vorgänge

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmRelayOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmRelayOperation** " listet die unterstützten Relay-Vorgänge auf.

## Beispiele

### Beispiel 1
```
PS C:\> Get-AzureRmRelayOperation
```

Listet Relay-unterstützte Vorgänge auf

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Relay. Models. OperationAttributes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]
Namensanzeige
----                                                                            -------
Microsoft.Relay/checkNamespaceAvailability/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/register/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/write Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/read Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/Delete Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/authorizationRules/write Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/authorizationRules/delete Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/authorizationRules/listkeys/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/write Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/read Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/Delete Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/authorizationRules/write Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/authorizationRules/delete Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/authorizationRules/listkeys/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/write Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/read Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/Delete Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/authorizationRules/write Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/authorizationRules/delete Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/authorizationRules/listkeys/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes

## Notizen

## Verwandte Links

