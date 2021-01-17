---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: eaf34373cb17fea94c498e16f623cef4bf65e937
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460987"
---
# New-AzNotificationHubsNamespaceAuthorizationRule

## SYNOPSIS
Erstellt eine Autorisierungsregel und weist diese Regel einem Benachrichtigungshub-Namespace zu.

## SYNTAX

### InputFileParameterSet
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SASRuleParameterSet
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "New-AzNotificationHubsNamespaceAuthorizationRule"** erstellt eine SAS (Shared Access Signature)-Autorisierungsregel und weist sie einem Benachrichtigungshub-Namespace zu.
Autorisierungsregeln verwalten Benutzerrechte für den Namespace und die in diesem Namespace enthaltenen Benachrichtigungshubs.
Dieses Cmdlet bietet zwei Möglichkeiten zum Erstellen einer neuen Autorisierungsregel und zum Zuweisen dieser Regel zu einem Namespace.
Sie können eine Instanz des **SharedAccessAuthorizationRuleAttributes-Objekts** erstellen und dieses Objekt dann mit den Eigenschaftswerten konfigurieren, die die neue Regel besitzen soll.
Dies kann mit .NET Framework geschehen.
Anschließend können Sie diese Eigenschaftswerte mithilfe des Parameters *SASRule* in die neue Regel kopieren.
Alternativ können Sie eine JSON(JavaScript Object Notation)-Datei erstellen, die die relevanten Konfigurationswerte enthält, und diese Werte dann mithilfe des *Parameters InputFile* anwenden.
Eine #A0 ist eine Textdatei, in der die folgende Syntax verwendet wird: {  
    "Name": "ContosoAuthorizationRule",  
    "PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",  
    "Rechte": \[  
        "Zuhören",  
        "Senden"  
    \]  
} Bei Verwendung in Verbindung mit dem **Cmdlet "New-AzNotificationHubsNamespaceAuthorizationRule"** wird im vorangehenden Beispiel eine Autorisierungsregel namens "ContosoAuthorizationRule" erstellt, die Benutzern Listen- und Sendeberechtigungen für den Namespace gewährt.
Der für die Authentifizierung verwendete *Primärschlüssel* kann mithilfe des folgenden Windows PowerShell-Befehls zufällig generiert werden: \[ Convert \] ::ToBase64String((1..32 |% { \[ byte/](Get-Random -Minimum 0 -Maximum 255) }))

## BEISPIELE

### Beispiel 1: Erstellen einer Autorisierungsregel und Zuweisen zu einem Namespace
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

Mit diesem Befehl wird eine Autorisierungsregel erstellt und dem Namespace "ContosoNamespace" zugewiesen.
Beim Erstellen dieser Regel müssen Sie den entsprechenden Namespace und die Ressourcengruppe angeben, der der Namespace zugewiesen ist.
Sie müssen jedoch keine Informationen zu der Regel selbst angeben: Regelinformationen werden aus der Eingabedatei C:\Configuration\NamespaceAuthorizationRules.jsverwendet.

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

### -InputFile
Gibt den Pfad zu einer JSON-Datei an, die Konfigurationsinformationen für die neue Autorisierungsregel enthält.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namespace
Gibt den Namespace an, dem die Autorisierungsregeln zugewiesen werden.
Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von Benachrichtigungshubs.
Die neuen Regeln müssen einem vorhandenen Namespace zugewiesen werden.
Das **Cmdlet "New-AzNotificationHubsNamespaceAuthorizationRule"** kann keinen neuen Namespace erstellen.

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
Gibt die Ressourcengruppe an, der der Namespace zugewiesen ist.
Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln so, dass sie einfach die Bestandsverwaltung und die Verwaltung von Azure unterstützen.
Sie müssen eine vorhandene Ressourcengruppe verwenden.
Mit diesem Cmdlet kann keine neue Ressourcengruppe erstellt werden.

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

### -SASRule
Gibt das **SharedAccessAuthorizationRuleAttributes-Objekt** an, das Konfigurationsinformationen für die neuen Regeln enthält.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Waswenn
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzNotificationHubAuthorizationRule](./Get-AzNotificationHubAuthorizationRule.md)

[Remove-AzNotificationHubAuthorizationRule](./Remove-AzNotificationHubAuthorizationRule.md)

[Set-AzNotificationHubAuthorizationRule](./Set-AzNotificationHubAuthorizationRule.md)


