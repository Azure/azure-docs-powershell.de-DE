---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: d270e3020e03a02461d9c54e19458af10401ee79
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176266"
---
# Get-AzNotificationHub

## Synopsis
Ruft Informationen zu ihren benachrichtigungshubs ab.

## Syntax

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzNotificationHub** " Ruft Informationen zu den benachrichtigungshubs in einem angegebenen Namespace ab, die einer angegebenen Ressourcengruppe zugewiesen sind.
So können Sie beispielsweise Informationen zu allen benachrichtigungshubs im Namespace ContosoNamespace abrufen und der ContosoNotificationsGroup-Ressourcengruppe zugewiesen werden.
Alternativ können Sie den *NotificationHub* -Parameter verwenden, um die zurückgegebenen Daten auf Informationen zu einem bestimmten Benachrichtigungs-Hub zu begrenzen.
Benachrichtigungshubs werden verwendet, um Push-Benachrichtigungen an mehrere Clients unabhängig von der Plattform zu senden, wie beispielsweise IOS, Android, Windows Phone 8 und Windows Store, die von diesen Clients verwendet werden.
Diese Hubs sind in etwa mit einzelnen apps vergleichbar, und jede Ihrer Apps verfügt in der Regel über einen eigenen Benachrichtigungs-Hub.
Dieses Cmdlet ruft nur Informationen über den Hub selbst ab.
Andere Cmdlets, wie "Get-AzNotificationHubAuthorizationRules", "Get-AzNotificationHubListKeys" und "Get-AzNotificationHubPNSCredentials", sind erforderlich, um Informationen zu den Autorisierungsregeln eines Hubs, Verbindungszeichenfolgen und Anmeldeinformationen für den Platt Form Benachrichtigungsdienst abzurufen.

## Beispiele

### Beispiel 1: Abrufen von Informationen für alle benachrichtigungshubs in einem bestimmten Namespace
```
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

Dieser Befehl ruft Informationen für alle benachrichtigungshubs im Namespace mit dem Namen ContosoNamespace ab, die der Ressourcengruppe ContosoNotificationsGroup zugewiesen wurden.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes

## Notizen

## Verwandte Links

[Get-AzNotificationHubAuthorizationRule](./Get-AzNotificationHubAuthorizationRule.md)

[Get-AzNotificationHubListKey](./Get-AzNotificationHubListKey.md)

[Get-AzNotificationHubPNSCredential](./Get-AzNotificationHubPNSCredential.md)

[Neu – AzNotificationHub](./New-AzNotificationHub.md)

[Remove-AzNotificationHub](./Remove-AzNotificationHub.md)

[Satz-AzNotificationHub](./Set-AzNotificationHub.md)


