---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: b4603566b793cbded7e593c9e4a23c3788c140de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504314"
---
# Get-AzureRmNotificationHubsNamespace

## Synopsis
Ruft Informationen zu einem Notification Hub-Namespace ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
**Das Cmdlet "Get-AzureRmNotificationHubsNamespace"** Ruft Informationen zu Notification Hub-Namespaces ab.
Dieses Cmdlet bietet Ihnen die Möglichkeit, Informationen für alle Ihre Namespaces, Informationen zu den Namespaces, die einer bestimmten Ressourcengruppe zugeordnet sind, zu erhalten. oder um Informationen zu einem bestimmten Namespace zurückzugeben.
Namespaces sind logische Container, die Ihnen beim organisieren und Verwalten Ihrer benachrichtigungshubs helfen.
Sie müssen über mindestens einen Benachrichtigungs-Hub-Namespace verfügen: alle benachrichtigungshubs müssen einem Namespace zugewiesen werden.
Ein einzelner Namespace kann mehrere Hubs beherbergen, was bedeutet, dass Sie möglicherweise nur einen Namespace in Ihrer Organisation benötigen.
Sie können jedoch auch mehrere Namespaces haben, um Ihre Hubs besser zu organisieren oder bestimmten Personen die Berechtigung zum Verwalten einer ausgewählten Teilmenge von Hubs zu erteilen.
Das Cmdlet " **Get-AzureRmNotificationHubsNamespace** " gibt grundlegende Informationen zum Namespace selbst zurück.
Verwenden Sie Get-AzureRmNotificationHubsNamespaceAuthorizationRules, um Informationen zu den Autorisierungsregeln abzurufen, die einem Namespace zugeordnet sind.

## Beispiele

### Beispiel 1: Abrufen von Informationen für alle Notification Hub-Namespaces
```
PS C:\>Get-AzureRmNotificationHubsNamespace
```

Dieser Befehl gibt Informationen für alle Ihre Benachrichtigungs-Hub-Namespaces zurück.

### Beispiel 2: Abrufen von Informationen für einen einzelnen Notification Hub-Namespace
```
PS C:\>Get-AzureRmNotificationHubsNamespace -Namespace "ContosoNamespace"
```

Dieser Befehl ruft Informationen für einen einzelnen Benachrichtigungs-Hub-Namespace ab: ContosoNamespace.

### Beispiel 3: Abrufen von Informationen für alle benachrichtigungshubs, die einem bestimmten Namespace zugewiesen sind
```
PS C:\>Get-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

Dieser Befehl ruft Informationen für alle Notification Hub-Namespaces ab, die der Ressourcengruppe ContosoNotificationsGroup zugeordnet sind.

## Parameter

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

### -Namespace
Gibt einen eindeutigen Namen für den Namespace an.
Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
Gibt die Ressourcengruppe an, der der Namespace zugewiesen ist.
Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und Azure-Verwaltung unterstützt.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. NotificationHubs. Models. NamespaceAttributes

## Notizen

## Verwandte Links

[Get-AzureRmNotificationHubsNamespaceAuthorizationRules](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[Neu – AzureRmNotificationHubsNamespace](./New-AzureRmNotificationHubsNamespace.md)

[Remove-AzureRmNotificationHubsNamespace](./Remove-AzureRmNotificationHubsNamespace.md)

[Satz-AzureRmNotificationHubsNamespace](./Set-AzureRmNotificationHubsNamespace.md)


