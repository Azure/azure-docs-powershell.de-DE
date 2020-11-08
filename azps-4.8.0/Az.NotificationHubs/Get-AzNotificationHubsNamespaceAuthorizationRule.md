---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: f3ba8428a6f6a9e618872e1292234751979b3c4b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174963"
---
# Get-AzNotificationHubsNamespaceAuthorizationRule

## Synopsis
Ruft Informationen zu den Autorisierungsregeln ab, die einem Notification Hub-Namespace zugeordnet sind.

## Syntax

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzNotificationHubsNamespaceAuthorizationRule** " gibt Informationen zu den SAS-Autorisierungsregeln (Shared Access Signature) zurück, die einem Notification Hub-Namespace zugeordnet sind.
Sie können Informationen zu allen Regeln zurückgeben, die dem Namespace zugeordnet sind.
Alternativ können Sie auch durch Einschließen des *AuthorizationRule* -Parameters Informationen für eine bestimmte Regel zurückgeben.
Autorisierungsregeln verwalten den Zugriff auf Namespaces.
Dies erfolgt durch die Erstellung von Links als URIs basierend auf unterschiedlichen Berechtigungsstufen.
Plattformebenen können eine der folgenden sein: 
- Hören
- Senden
- Clients verwalten werden basierend auf der entsprechenden Berechtigungsstufe an einen dieser URIs weitergeleitet.
Beispielsweise wird ein Client, der die Berechtigung "anhören" erhält, an den URI für diese Berechtigung weitergeleitet.
Dieses Cmdlet ruft nur die Autorisierungsregeln ab, die einem Namespace zugeordnet sind.
Wenn Sie Informationen zum Namespace selbst abrufen möchten, verwenden Sie Get-AzNotificationHubsNamespace.

## Beispiele

### Beispiel 1: Abrufen von Informationen zu allen den Namespaces zugewiesenen Autorisierungsregeln
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

Dieser Befehl ruft Informationen zu allen Autorisierungsregeln ab, die sowohl dem Namespace-ContosoNamespace als auch der ContosoNotificationsGroup-Ressourcengruppe zugewiesen sind.

### Beispiel 2: Abrufen von Informationen zu einer Autorisierungsregel
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

Dieser Befehl ruft Informationen zu einer einzelnen Namespace Autorisierungsregel mit dem Namen ListenRule ab.
Sie müssen den Namespace und die Ressourcengruppe einbeziehen, wenn Sie Informationen zu einer bestimmten Autorisierungsregel erhalten.

## Parameter

### -AuthorizationRule
Gibt den Namen einer SAS-Authentifizierungsregel an.
Diese Regeln bestimmen die Art des Zugriffs, den Benutzer für den Namespace haben.

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
Gibt den Namespace an, dem die Autorisierungsregeln zugewiesen sind.
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

### -ResourceGroup
Gibt die Ressourcengruppe an, der die Autorisierungsregeln zugewiesen sind.
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

### Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes

## Notizen

## Verwandte Links

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[Neu – AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Satz-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


