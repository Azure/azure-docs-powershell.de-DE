---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/get-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
ms.openlocfilehash: 5a8d38adf8016d8f0a71877aa1717df9f3389c93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918267"
---
# Get-AzNotificationHubsNamespace

## SYNOPSIS
Ruft Informationen zu einem Benachrichtigungshubnamespace ab.

## SYNTAX

```
Get-AzNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
**Das Get-AzNotificationHubsNamespace-Cmdlet** ruft Informationen zu Benachrichtigungshub-Namespaces ab.
Dieses Cmdlet bietet Ihnen die Möglichkeit, Informationen für alle Ihre Namespaces, Informationen zu den Namespaces, die einer bestimmten Ressourcengruppe zugewiesen sind, zu erhalten. oder für die Rückgabe von Informationen zu einem bestimmten Namespace.
Namespaces sind logische Container, mit deren Hilfe Sie Ihre Benachrichtigungshubs organisieren und verwalten können.
Sie müssen über mindestens einen Benachrichtigungshubnamespace verfügen: Alle Benachrichtigungshubs müssen einem Namespace zugewiesen sein.
Ein einzelner Namespace kann mehrere Hubs haben, was bedeutet, dass Sie möglicherweise nur einen Namespace in Ihrer Organisation benötigen.
Sie können jedoch auch über mehrere Namespaces verfügen, um Ihre Hubs besser zu organisieren oder bestimmten Personen die Berechtigung zum Verwalten einer ausgewählten Teilmenge von Hubs zu erteilen.
Das **Get-AzNotificationHubsNamespace-Cmdlet** gibt grundlegende Informationen zum Namespace selbst zurück.
Verwenden Sie Get-AzNotificationHubsNamespaceAuthorizationRules, um Informationen zu den Autorisierungsregeln zu erhalten, die einem Namespace zugeordnet sind.

## BEISPIELE

### Beispiel 1: Informationen für alle Benachrichtigungshubnamespaces
```
PS C:\>Get-AzNotificationHubsNamespace
```

Dieser Befehl gibt Informationen für alle Ihre Benachrichtigungshub-Namespaces zurück.

### Beispiel 2: Informationen für einen einzelnen Benachrichtigungshubnamespace
```
PS C:\>Get-AzNotificationHubsNamespace -Namespace "ContosoNamespace"
```

Dieser Befehl ruft Informationen für einen einzelnen Benachrichtigungshubnamespace ab: ContosoNamespace.

### Beispiel 3: Informationen für alle Benachrichtigungshubs, die einem bestimmten Namespace zugewiesen sind
```
PS C:\>Get-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

Dieser Befehl ruft Informationen für alle Benachrichtigungshubnamespaces ab, die der Ressourcengruppe ContosoNotificationsGroup zugewiesen sind.

## PARAMETER

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
Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die einfach die Bestandsverwaltung und die Azure-Verwaltung unterstützt.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes

## NOTIZEN

## VERWANDTE LINKS

[Get-AzNotificationHubsNamespaceAuthorizationRule](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[New-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


