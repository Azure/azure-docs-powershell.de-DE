---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: a1c9743d02f10102d9343709599dbed694d37a2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918264"
---
# Get-AzNotificationHubsNamespaceAuthorizationRule

## SYNOPSIS
Ruft Informationen zu den Autorisierungsregeln ab, die einem Benachrichtigungshubnamespace zugeordnet sind.

## SYNTAX

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Get-AzNotificationHubsNamespaceAuthorizationRule** gibt Informationen zu den Sas-Autorisierungsregeln (Shared Access Signature) zurück, die einem Benachrichtigungshubnamespace zugeordnet sind.
Sie können Informationen zu allen Regeln zurückgeben, die dem Namespace zugeordnet sind.
Alternativ können Sie durch Einbeziehung des *Parameters AuthorizationRule* Informationen für eine bestimmte Regel zurückgeben.
Autorisierungsregeln verwalten den Zugriff auf Namespaces.
Dies erfolgt durch die Erstellung von Links als URIs, die auf unterschiedlichen Berechtigungsstufen basieren.
Plattformebenen können eine der folgenden sein: 
- Anhören
- Senden
- Manage Clients werden basierend auf der entsprechenden Berechtigungsstufe an eine dieser URIs geleitet.
Beispielsweise wird ein Client mit der Berechtigung "Anhören" an den URI geleitet, um diese Berechtigung zu erhalten.
Dieses Cmdlet ruft nur die Autorisierungsregeln ab, die einem Namespace zugeordnet sind.
Um Informationen zum Namespace selbst zu erhalten, verwenden Sie Get-AzNotificationHubsNamespace.

## BEISPIELE

### Beispiel 1: Informationen zu allen Autorisierungsregeln, die Namespaces zugewiesen sind
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

Dieser Befehl ruft Informationen zu allen Autorisierungsregeln ab, die sowohl dem Namespace ContosoNamespace als auch der Ressourcengruppe ContosoNotificationsGroup zugewiesen sind.

### Beispiel 2: Informationen zu einer Autorisierungsregel erhalten
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

Dieser Befehl ruft Informationen zu einer einzelnen Namespaceautorisierungsregel namens ListenRule ab.
Sie müssen den Namespace und die Ressourcengruppe enthalten, wenn Sie Informationen zu einer bestimmten Autorisierungsregel erhalten.

## PARAMETER

### -AuthorizationRule
Gibt den Namen einer SAS-Authentifizierungsregel an.
Diese Regeln bestimmen den Typ des Zugriffs, den Benutzer auf den Namespace haben.

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
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden

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
Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von Benachrichtigungshubs.

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
Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die einfach die Bestandsverwaltung und die Azure-Verwaltung unterstützt.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes

## NOTIZEN

## VERWANDTE LINKS

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[New-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


