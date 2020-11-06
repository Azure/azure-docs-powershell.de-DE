---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: ade411d6d8ca19a5c17afd87388f9f7ab90d64d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505437"
---
# Get-AzureRmNotificationHubsNamespaceAuthorizationRules

## Synopsis
Ruft Informationen zu den Autorisierungsregeln ab, die einem Notification Hub-Namespace zugeordnet sind.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmNotificationHubsNamespaceAuthorizationRules** " gibt Informationen zu den SAS-Autorisierungsregeln (Shared Access Signature) zurück, die einem Notification Hub-Namespace zugeordnet sind.
Sie können Informationen zu allen Regeln zurückgeben, die dem Namespace zugeordnet sind.
Alternativ können Sie auch durch Einschließen des *AuthorizationRule* -Parameters Informationen für eine bestimmte Regel zurückgeben.

Autorisierungsregeln verwalten den Zugriff auf Namespaces.
Dies erfolgt durch die Erstellung von Links als URIs basierend auf unterschiedlichen Berechtigungsstufen.
Plattformebenen können eine der folgenden sein: 

- Hören
- Senden
- Verwalten

Clients werden basierend auf der entsprechenden Berechtigungsstufe an einen dieser URIs weitergeleitet.
Beispielsweise wird ein Client, der die Berechtigung "anhören" erhält, an den URI für diese Berechtigung weitergeleitet.

Dieses Cmdlet ruft nur die Autorisierungsregeln ab, die einem Namespace zugeordnet sind.
Wenn Sie Informationen zum Namespace selbst abrufen möchten, verwenden Sie Get-AzureRmNotificationHubsNamespace.

## Beispiele

### Beispiel 1: Abrufen von Informationen zu allen den Namespaces zugewiesenen Autorisierungsregeln
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

Dieser Befehl ruft Informationen zu allen Autorisierungsregeln ab, die sowohl dem Namespace-ContosoNamespace als auch der ContosoNotificationsGroup-Ressourcengruppe zugewiesen sind.

### Beispiel 2: Abrufen von Informationen zu einer Autorisierungsregel
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

Dieser Befehl ruft Informationen zu einer einzelnen Namespace Autorisierungsregel mit dem Namen ListenRule ab.
Sie müssen den Namespace und die Ressourcengruppe einbeziehen, wenn Sie Informationen zu einer bestimmten Autorisierungsregel erhalten.

## Parameter

### -AuthorizationRule
Gibt den Namen einer SAS-Authentifizierungsregel an.
Diese Regeln bestimmen die Art des Zugriffs, den Benutzer für den Namespace haben.

```yaml
Type: String
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
Gibt den Namespace an, dem die Autorisierungsregeln zugewiesen sind.
Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.

```yaml
Type: String
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

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes]

## Notizen

## Verwandte Links

[Get-AzureRmNotificationHubsNamespace](./Get-AzureRmNotificationHubsNamespace.md)

[Neu – AzureRmNotificationHubsNamespace](./New-AzureRmNotificationHubsNamespace.md)

[Remove-AzureRmNotificationHubsNamespace](./Remove-AzureRmNotificationHubsNamespace.md)

[Satz-AzureRmNotificationHubsNamespace](./Set-AzureRmNotificationHubsNamespace.md)


