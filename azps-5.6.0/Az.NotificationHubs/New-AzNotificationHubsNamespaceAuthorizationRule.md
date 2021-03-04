---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 49a856ef38d529c7d60b7c09b4d4a4fcdab5b59b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918240"
---
# New-AzNotificationHubsNamespaceAuthorizationRule

## SYNOPSIS
Erstellt eine Autorisierungsregel und weist diese Regel einem Benachrichtigungshubnamespace zu.

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
Das **Cmdlet New-AzNotificationHubsNamespaceAuthorizationRule** erstellt eine Sas-Autorisierungsregel (Shared Access Signature) und weist sie einem Benachrichtigungshub-Namespace zu.
Autorisierungsregeln verwalten Benutzerrechte für den Namespace und die Benachrichtigungshubs, die in diesem Namespace enthalten sind.
Dieses Cmdlet bietet zwei Möglichkeiten zum Erstellen einer neuen Autorisierungsregel und zum Zuweisen zu einem Namespace.
Sie können eine Instanz des **SharedAccessAuthorizationRuleAttributes-Objekts** erstellen und dieses Objekt dann mit den Eigenschaftswerten konfigurieren, die die neue Regel besitzen soll.
Dies kann mithilfe von .NET Framework.
Anschließend können Sie diese Eigenschaftswerte mithilfe des *SASRule-Parameters* in ihre neue Regel kopieren.
Alternativ können Sie eine JSON-Datei (JavaScript Object Notation) erstellen, die die relevanten Konfigurationswerte enthält, und diese Werte dann mithilfe des Parameters *InputFile* anwenden.
Eine #A0 ist eine Textdatei, die eine syntax ähnliche Syntax wie die folgende verwendet: {  
    "Name": "ContosoAuthorizationRule",  
    "PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",  
    "Rechte": \[  
        "Hören",  
        "Senden"  
    \]  
} Bei Verwendung in Verbindung mit **dem Cmdlet New-AzNotificationHubsNamespaceAuthorizationRule** wird im vorherigen JSON-Beispiel eine Autorisierungsregel mit dem Namen ContosoAuthorizationRule erstellt, die Benutzern Listen- und Sendeberechtigungen für den Namespace gewährt.
Der *für* die Authentifizierung verwendete Primärschlüssel kann mithilfe des folgenden Windows PowerShell-Befehls zufällig generiert werden: \[ Konvertieren \] ::ToBase64String(((1,32 |% { \[ Byte/](Get-Random -Minimum 0 -Maximum 255) }))

## BEISPIELE

### Beispiel 1: Erstellen einer Autorisierungsregel und Zuweisen zu einem Namespace
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

Dieser Befehl erstellt eine Autorisierungsregel und weist diese Regel dem Namespace ContosoNamespace zu.
Beim Erstellen dieser Regel müssen Sie den entsprechenden Namespace und die Ressourcengruppe angeben, der der Namespace zugewiesen ist.
Sie müssen jedoch keine Informationen zur Regel selbst angeben: Regelinformationen werden aus der Eingabedatei C:\Configuration\NamespaceAuthorizationRules.jsübernommen.

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

### -InputFile
Gibt den Pfad zu einer JSON-Datei an, der Konfigurationsinformationen für die neue Autorisierungsregel enthält.

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
Das **Cmdlet New-AzNotificationHubsNamespaceAuthorizationRule** kann keinen neuen Namespace erstellen.

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
Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die einfach die Bestandsverwaltung und die Azure-Verwaltung unterstützt.
Sie müssen eine vorhandene Ressourcengruppe verwenden.
Dieses Cmdlet kann keine neue Ressourcengruppe erstellen.

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

### -Bestätigen
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

### -WhatIf
Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes

## NOTIZEN

## VERWANDTE LINKS

[Get-AzNotificationHubAuthorizationRule](./Get-AzNotificationHubAuthorizationRule.md)

[Remove-AzNotificationHubAuthorizationRule](./Remove-AzNotificationHubAuthorizationRule.md)

[Set-AzNotificationHubAuthorizationRule](./Set-AzNotificationHubAuthorizationRule.md)


