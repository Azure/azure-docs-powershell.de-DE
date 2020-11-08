---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 7c85bafabede1c905efaf000721e5f8d6bee1572
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004710"
---
# Get-AzNotificationHubAuthorizationRule

## Synopsis
Ruft Informationen zu den Autorisierungsregeln ab, die einem Benachrichtigungs-Hub zugeordnet sind.

## Syntax

```
Get-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzNotificationHubAuthorizationRule** " Ruft Informationen zu den SAS-Autorisierungsregeln (Shared Access Signature) ab, die einem Benachrichtigungs-Hub zugeordnet sind.
Das Cmdlet gibt Informationen zu allen Regeln zurück, die einem Hub zugeordnet sind, oder ruft durch Einschließen des *AuthorizationRule* -Parameters Informationen zu einer bestimmten Regel ab.
Autorisierungsregeln verwalten den Zugriff auf Ihre benachrichtigungshubs.
Eine Autorisierungsregel erstellt Links als URI, die auf unterschiedlichen Berechtigungsstufen basieren.
Clients werden basierend auf der entsprechenden Berechtigungsstufe an einen dieser URIs weitergeleitet.
Beispielsweise wird ein Client mit der Berechtigung "anhören" an den URI für diese Berechtigung weitergeleitet.
Das Cmdlet " **Get-AzNotificationHubAuthorizationRule** " ruft nur Informationen zu den Autorisierungsregeln ab, die einem Benachrichtigungs-Hub zugeordnet sind.
Wenn Sie Informationen zum Hub selbst abrufen möchten, verwenden Sie Get-AzNotificationHub.

## Beispiele

### Beispiel 1: Abrufen von Informationen zu allen Autorisierungsregeln, die einem Benachrichtigungs-Hub zugewiesen sind
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

Dieser Befehl ruft Informationen für alle Autorisierungsregeln ab, die dem Benachrichtigungs-Hub mit dem Namen ContosoInternalHub im Namespace ContosoNamespace zugewiesen wurden.
Sie müssen den Namespace angeben, in dem sich der Hub befindet, sowie die Ressourcengruppe, der der Hub zugewiesen wurde.

### Beispiel 2: Abrufen von Informationen zu Autorisierungsregeln, die einem Benachrichtigungs-Hub zugewiesen sind
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

Dieser Befehl ruft Informationen für alle Autorisierungsregeln ab, die dem Benachrichtigungs-Hub mit dem Namen ContosoInternalHub im Namespace ContosoNamespace zugewiesen wurden.
Der Befehl verwendet den *AuthorizationRule* -Parameter, um die zurückgegebenen Daten auf eine einzelne Autorisierungsregel mit dem Namen ListenRule zu begrenzen.

## Parameter

### -AuthorizationRule
Gibt den Namen einer SAS-Authentifizierungsregel an.
Diese Regeln bestimmen die Art des Zugriffs, den Benutzer für den Benachrichtigungs-Hub haben.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
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
Gibt den Benachrichtigungs-Hub an, dem dieses Cmdlet Autorisierungsregeln zuweist.
Benachrichtigungshubs werden verwendet, um Push-Benachrichtigungen an mehrere Clients zu senden, unabhängig von der Plattform, die von diesen Clients verwendet wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
Gibt die Ressourcengruppe an, der der Benachrichtigungs-Hub zugewiesen ist.
Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die zur Vereinfachung der Bestandsverwaltung und der Azure-Verwaltung beizutragen.

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

[Get-AzNotificationHubsNamespaceAuthorizationRule](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[Neu – AzNotificationHubAuthorizationRule](./New-AzNotificationHubAuthorizationRule.md)

[Remove-AzNotificationHubAuthorizationRule](./Remove-AzNotificationHubAuthorizationRule.md)

[Satz-AzNotificationHubAuthorizationRule](./Set-AzNotificationHubAuthorizationRule.md)


