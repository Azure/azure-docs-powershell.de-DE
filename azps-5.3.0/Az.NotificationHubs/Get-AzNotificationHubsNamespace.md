---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
ms.openlocfilehash: 3d0e604d3984a40acde02fb1f977e2922ae2d1d7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472098"
---
# Get-AzNotificationHubsNamespace

## SYNOPSIS
Ruft Informationen zu einem Benachrichtigungshub-Namespace ab.

## SYNTAX

```
Get-AzNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
**Das Get-AzNotificationHubsNamespace-Cmdlet** ruft Informationen zu Benachrichtigungshub-Namespaces ab.
Dieses Cmdlet bietet Ihnen die Möglichkeit, Informationen zu allen Ihren Namespaces, Informationen zu den Namespaces, die einer bestimmten Ressourcengruppe zugewiesen sind, abrufen zu können. oder zum Zurückgeben von Informationen zu einem bestimmten Namespace.
Namespaces sind logische Container, mit deren Hilfe Sie Ihre Benachrichtigungshubs organisieren und verwalten können.
Sie müssen über mindestens einen Benachrichtigungshub-Namespace verfügen: Alle Benachrichtigungshubs müssen einem Namespace zugewiesen sein.
Ein einzelner Namespace kann mehrere Hubs haben, was bedeutet, dass Sie möglicherweise nur einen Namespace in Ihrer Organisation benötigen.
Sie können jedoch auch über mehrere Namespaces verfügen, um Ihre Hubs besser zu organisieren oder bestimmten Personen die Berechtigung zum Verwalten einer ausgewählten Teilmenge von Hubs zu erteilen.
Das **Cmdlet "Get-AzNotificationHubsNamespace"** gibt grundlegende Informationen über den Namespace selbst zurück.
Verwenden Sie Get-AzNotificationHubsNamespaceAuthorizationRules, um Informationen zu den einem Namespace zugeordneten Autorisierungsregeln zu erhalten.

## BEISPIELE

### Beispiel 1: Informationen für alle Namespaces des Benachrichtigungshubs
```
PS C:\>Get-AzNotificationHubsNamespace
```

Dieser Befehl gibt Informationen für alle Namespaces des Benachrichtigungshubs zurück.

### Beispiel 2: Informationen für einen einzelnen Benachrichtigungshub-Namespace
```
PS C:\>Get-AzNotificationHubsNamespace -Namespace "ContosoNamespace"
```

Dieser Befehl ruft Informationen für einen einzelnen Benachrichtigungshub-Namespace ab: ContosoNamespace.

### Beispiel 3: Informationen für alle Benachrichtigungshubs, die einem bestimmten Namespace zugewiesen sind
```
PS C:\>Get-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

Dieser Befehl ruft Informationen für alle Benachrichtigungshub-Namespaces ab, die der Ressourcengruppe "ContosoNotificationsGroup" zugewiesen sind.

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
Gibt einen eindeutigen Namen für den Namespace an.
Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von Benachrichtigungshubs.

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
Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln so, dass sie einfach die Bestandsverwaltung und die Verwaltung von Azure unterstützen.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzNotificationHubsNamespaceAuthorizationRule](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[New-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


