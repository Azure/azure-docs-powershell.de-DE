---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHub.md
ms.openlocfilehash: af2cc43b5f70c8a892e8b8fad0177a804689f007
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498249"
---
# Get-AzureRmNotificationHub

## Synopsis
Ruft Informationen zu ihren benachrichtigungshubs ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmNotificationHub** " Ruft Informationen zu den benachrichtigungshubs in einem angegebenen Namespace ab, die einer angegebenen Ressourcengruppe zugewiesen sind.
So können Sie beispielsweise Informationen zu allen benachrichtigungshubs im Namespace ContosoNamespace abrufen und der ContosoNotificationsGroup-Ressourcengruppe zugewiesen werden.
Alternativ können Sie den *NotificationHub* -Parameter verwenden, um die zurückgegebenen Daten auf Informationen zu einem bestimmten Benachrichtigungs-Hub zu begrenzen.
Benachrichtigungshubs werden verwendet, um Push-Benachrichtigungen an mehrere Clients unabhängig von der Plattform zu senden, wie beispielsweise IOS, Android, Windows Phone 8 und Windows Store, die von diesen Clients verwendet werden.
Diese Hubs sind in etwa mit einzelnen apps vergleichbar, und jede Ihrer Apps verfügt in der Regel über einen eigenen Benachrichtigungs-Hub.
Dieses Cmdlet ruft nur Informationen über den Hub selbst ab.
Andere Cmdlets, wie "Get-AzureRmNotificationHubAuthorizationRules", "Get-AzureRmNotificationHubListKeys" und "Get-AzureRmNotificationHubPNSCredentials", sind erforderlich, um Informationen zu den Autorisierungsregeln eines Hubs, Verbindungszeichenfolgen und Anmeldeinformationen für den Platt Form Benachrichtigungsdienst abzurufen.

## Beispiele

### Beispiel 1: Abrufen von Informationen für alle benachrichtigungshubs in einem bestimmten Namespace
```
PS C:\>Get-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

Dieser Befehl ruft Informationen für alle benachrichtigungshubs im Namespace mit dem Namen ContosoNamespace ab, die der Ressourcengruppe ContosoNotificationsGroup zugewiesen wurden.

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
Gibt den Namespace an, dem der Benachrichtigungs-Hub zugewiesen ist.
Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.

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

### -NotificationHub
Gibt den Namen des benachrichtigungshubs an, den dieses Cmdlet erhält.
Benachrichtigungshubs werden verwendet, um Push-Benachrichtigungen an mehrere Clients zu senden, unabhängig von der Plattform, die von diesen Clients verwendet wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
Gibt die Ressourcengruppe an, der der Benachrichtigungs-Hub zugewiesen ist.
Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und Azure-Verwaltung unterstützt.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes

## Notizen

## Verwandte Links

[Get-AzureRmNotificationHubAuthorizationRules](./Get-AzureRmNotificationHubAuthorizationRules.md)

[Get-AzureRmNotificationHubListKeys](./Get-AzureRmNotificationHubListKeys.md)

[Get-AzureRmNotificationHubPNSCredentials](./Get-AzureRmNotificationHubPNSCredentials.md)

[Neu – AzureRmNotificationHub](./New-AzureRmNotificationHub.md)

[Remove-AzureRmNotificationHub](./Remove-AzureRmNotificationHub.md)

[Satz-AzureRmNotificationHub](./Set-AzureRmNotificationHub.md)


