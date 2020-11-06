---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: b6ece0370642d5ef0b913c96d3b817834b204e52
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504506"
---
# Get-AzureRmNotificationHubAuthorizationRules

## Synopsis
Ruft Informationen zu den Autorisierungsregeln ab, die einem Benachrichtigungs-Hub zugeordnet sind.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmNotificationHubAuthorizationRules** " Ruft Informationen zu den SAS-Autorisierungsregeln (Shared Access Signature) ab, die einem Benachrichtigungs-Hub zugeordnet sind.
Das Cmdlet gibt Informationen zu allen Regeln zurück, die einem Hub zugeordnet sind, oder ruft durch Einschließen des *AuthorizationRule* -Parameters Informationen zu einer bestimmten Regel ab.

Autorisierungsregeln verwalten den Zugriff auf Ihre benachrichtigungshubs.
Eine Autorisierungsregel erstellt Links als URI, die auf unterschiedlichen Berechtigungsstufen basieren.
Clients werden basierend auf der entsprechenden Berechtigungsstufe an einen dieser URIs weitergeleitet.
Beispielsweise wird ein Client mit der Berechtigung "anhören" an den URI für diese Berechtigung weitergeleitet.

Das Cmdlet " **Get-AzureRmNotificationHubAuthorizationRules** " ruft nur Informationen zu den Autorisierungsregeln ab, die einem Benachrichtigungs-Hub zugeordnet sind.
Wenn Sie Informationen zum Hub selbst abrufen möchten, verwenden Sie Get-AzureRmNotificationHub.

## Beispiele

### Beispiel 1: Abrufen von Informationen zu allen Autorisierungsregeln, die einem Benachrichtigungs-Hub zugewiesen sind
```
PS C:\>Get-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

Dieser Befehl ruft Informationen für alle Autorisierungsregeln ab, die dem Benachrichtigungs-Hub mit dem Namen ContosoInternalHub im Namespace ContosoNamespace zugewiesen wurden.
Sie müssen den Namespace angeben, in dem sich der Hub befindet, sowie die Ressourcengruppe, der der Hub zugewiesen wurde.

### Beispiel 2: Abrufen von Informationen zu Autorisierungsregeln, die einem Benachrichtigungs-Hub zugewiesen sind
```
PS C:\>Get-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

Dieser Befehl ruft Informationen für alle Autorisierungsregeln ab, die dem Benachrichtigungs-Hub mit dem Namen ContosoInternalHub im Namespace ContosoNamespace zugewiesen wurden.
Der Befehl verwendet den *AuthorizationRule* -Parameter, um die zurückgegebenen Daten auf eine einzelne Autorisierungsregel mit dem Namen ListenRule zu begrenzen.

## Parameter

### -AuthorizationRule
Gibt den Namen einer SAS-Authentifizierungsregel an.
Diese Regeln bestimmen die Art des Zugriffs, den Benutzer für den Benachrichtigungs-Hub haben.

```yaml
Type: String
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
Gibt den Namespace an, dem der Benachrichtigungs-Hub zugewiesen ist.
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

### -NotificationHub
Gibt den Benachrichtigungs-Hub an, dem dieses Cmdlet Autorisierungsregeln zuweist.
Benachrichtigungshubs werden verwendet, um Push-Benachrichtigungen an mehrere Clients zu senden, unabhängig von der Plattform, die von diesen Clients verwendet wird.

```yaml
Type: String
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

[Get-AzureRmNotificationHubsNamespaceAuthorizationRules](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[Neu – AzureRmNotificationHubAuthorizationRules](./New-AzureRmNotificationHubAuthorizationRules.md)

[Remove-AzureRmNotificationHubAuthorizationRules](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[Satz-AzureRmNotificationHubAuthorizationRules](./Set-AzureRmNotificationHubAuthorizationRules.md)


