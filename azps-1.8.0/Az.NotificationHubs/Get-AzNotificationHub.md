---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: ea16c01e5c528742702dd08f1f2bd4c14e0cebcd
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399939"
---
# Get-AzNotificationHub

## SYNOPSIS
Ruft Informationen zu Ihren Benachrichtigungshubs ab.

## SYNTAX

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzNotificationHub-Cmdlet** ruft Informationen zu den Benachrichtigungshubs in einem angegebenen Namespace ab und wird einer bestimmten Ressourcengruppe zugewiesen.
Sie können z. B. Informationen zu allen Benachrichtigungshubs im Namespace "ContosoNamespace" erhalten und der Ressourcengruppe "ContosoNotificationsGroup" zugewiesen sein.
Alternativ können Sie den Parameter *NotificationHub* verwenden, um die zurückgegebenen Daten auf Informationen zu einem bestimmten Benachrichtigungshub zu beschränken.
Benachrichtigungshubs werden verwendet, um Pushbenachrichtigungen an mehrere Clients zu senden, unabhängig von der von diesen Clients verwendeten Plattform, z. B. iOS, Android, Windows Phone 8 und Windows Store.
Diese Hubs entsprechen in etwa einzelnen Apps, und jede Ihrer Apps hat in der Regel einen eigenen Benachrichtigungshub.
Dieses Cmdlet ruft nur Informationen über den Hub selbst ab.
Andere Cmdlets wie "Get-AzNotificationHubAuthorizationRules", "Get-AzNotificationHubListKeys" und "Get-AzNotificationHubPNSCredentials" sind erforderlich, um Informationen zu den Autorisierungsregeln, Verbindungszeichenfolgen und Anmeldeinformationen des Plattformbenachrichtigungsdiensts zu erhalten.

## BEISPIELE

### Beispiel 1: Informationen für alle Benachrichtigungshubs in einem bestimmten Namespace
```
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

Dieser Befehl ruft Informationen für alle Benachrichtigungshubs im Namespace "ContosoNamespace" ab, die der Ressourcengruppe "ContosoNotificationsGroup" zugewiesen wurden.

## PARAMETERS

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
Gibt den Namen des Benachrichtigungshubs an, den dieses Cmdlet erhält.
Benachrichtigungshubs werden verwendet, um Pushbenachrichtigungen unabhängig von der von diesen Clients verwendeten Plattform an mehrere Clients zu senden.

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
Gibt die Ressourcengruppe an, der der Benachrichtigungshub zugewiesen ist.
Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln so, dass sie einfach die Bestandsverwaltung und die Verwaltung von Azure unterstützen.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN




[New-AzNotificationHub](./New-AzNotificationHub.md)

[Remove-AzNotificationHub](./Remove-AzNotificationHub.md)

[Set-AzNotificationHub](./Set-AzNotificationHub.md)


