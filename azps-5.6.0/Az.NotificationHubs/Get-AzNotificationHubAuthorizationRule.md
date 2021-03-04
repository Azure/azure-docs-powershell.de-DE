---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/get-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 260cf95d04d6a923acbdeaa91a412aa0046d9ea0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918320"
---
# Get-AzNotificationHubAuthorizationRule

## SYNOPSIS
Ruft Informationen zu den Autorisierungsregeln ab, die einem Benachrichtigungshub zugeordnet sind.

## SYNTAX

```
Get-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Get-AzNotificationHubAuthorizationRule** ruft Informationen zu den Sas-Autorisierungsregeln (Shared Access Signature) ab, die einem Benachrichtigungshub zugeordnet sind.
Das Cmdlet gibt Informationen zu allen Regeln zurück, die einem Hub zugeordnet sind, oder ruft durch Einbeziehung des *Parameters AuthorizationRule* Informationen zu einer bestimmten Regel ab.
Autorisierungsregeln verwalten den Zugriff auf Ihre Benachrichtigungshubs.
Eine Autorisierungsregel erstellt Links als URI, basierend auf unterschiedlichen Berechtigungsstufen.
Clients werden basierend auf der entsprechenden Berechtigungsstufe an eine dieser URIs geleitet.
Beispielsweise wird ein Client mit der Berechtigung "Anhören" für diese Berechtigung an den URI geleitet.
Das **Cmdlet Get-AzNotificationHubAuthorizationRule** ruft nur Informationen zu den Autorisierungsregeln ab, die einem Benachrichtigungshub zugeordnet sind.
Um Informationen zum Hub selbst zu erhalten, verwenden Sie Get-AzNotificationHub.

## BEISPIELE

### Beispiel 1: Informationen zu allen Autorisierungsregeln, die einem Benachrichtigungshub zugewiesen sind
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

Dieser Befehl ruft Informationen zu allen Autorisierungsregeln ab, die dem Benachrichtigungshub "ContosoInternalHub" im Namespace ContosoNamespace zugewiesen sind.
Sie müssen den Namespace angeben, in dem sich der Hub befindet, sowie die Ressourcengruppe, der der Hub zugewiesen wurde.

### Beispiel 2: Erhalten von Informationen für eine Autorisierungsregeln, die einem Benachrichtigungshub zugewiesen sind
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

Dieser Befehl ruft Informationen zu allen Autorisierungsregeln ab, die dem Benachrichtigungshub "ContosoInternalHub" im Namespace ContosoNamespace zugewiesen sind.
Der Befehl verwendet den *Parameter AuthorizationRule,* um die zurückgegebenen Daten auf eine einzelne Autorisierungsregel namens ListenRule zu beschränken.

## PARAMETER

### -AuthorizationRule
Gibt den Namen einer SAS-Authentifizierungsregel an.
Diese Regeln bestimmen den Typ des Zugriffs, den Benutzer auf den Benachrichtigungshub haben.

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
Gibt den Namespace an, dem der Benachrichtigungshub zugewiesen ist.
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

### -NotificationHub
Gibt den Benachrichtigungshub an, dem dieses Cmdlet Autorisierungsregeln zugibt.
Benachrichtigungshubs werden verwendet, um Pushbenachrichtigungen an mehrere Clients zu senden, unabhängig von der Plattform, die von diesen Clients verwendet wird.

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
Gibt die Ressourcengruppe an, der der Benachrichtigungshub zugewiesen ist.
Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die die Bestandsverwaltung und Azure-Verwaltung vereinfacht.

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

[Get-AzNotificationHubsNamespaceAuthorizationRule](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[New-AzNotificationHubAuthorizationRule](./New-AzNotificationHubAuthorizationRule.md)

[Remove-AzNotificationHubAuthorizationRule](./Remove-AzNotificationHubAuthorizationRule.md)

[Set-AzNotificationHubAuthorizationRule](./Set-AzNotificationHubAuthorizationRule.md)


