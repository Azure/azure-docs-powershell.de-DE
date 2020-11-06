---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: 2530d4b0075856b6a172bdcf104474d320f657bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501454"
---
# New-AzureRmNotificationHubsNamespaceAuthorizationRules

## Synopsis
Erstellt eine Autorisierungsregel und weist diese Regel einem Benachrichtigungs-Hub-Namespace zu.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### InputFileParameterSet
```
New-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SASRuleParameterSet
```
New-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmNotificationHubsNamespaceAuthorizationRules** erstellt eine Autorisierungsregel für die Shared Access-Signatur (SAS) und weist Sie einem Notification Hub-Namespace zu.
Autorisierungsregeln verwalten Benutzerrechte für den Namespace und die benachrichtigungshubs, die in diesem Namespace enthalten sind.

Dieses Cmdlet bietet zwei Möglichkeiten, um eine neue Autorisierungsregel zu erstellen und Sie einem Namespace zuzuweisen.
Sie können eine Instanz des **SharedAccessAuthorizationRuleAttributes** -Objekts erstellen und dieses Objekt dann mit den Eigenschaftswerten konfigurieren, die die neue Regel besitzen soll.
Dies kann mit .NET Framework erfolgen.
Sie können diese Eigenschaftswerte dann mithilfe des *SASRule* -Parameters in Ihre neue Regel kopieren.

Sie können auch eine JSON-Datei (JavaScript Object Notation) erstellen, die die relevanten Konfigurationswerte enthält, und diese Werte dann mithilfe des *Input* File-Parameters anwenden.
Eine JSON-Datei ist eine Textdatei, die Syntax ähnlich der folgenden verwendet:

{  
    "Name": "ContosoAuthorizationRule";  
    "Primär Primär": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =";  
    "Rechte": \[  
        "Hören",  
        Senden  
    \]  
}

Bei Verwendung in Verbindung mit dem Cmdlet **New-AzureRmNotificationHubsNamespaceAuthorizationRules** erstellt das vorangehende JSON-Beispiel eine Autorisierungsregel mit dem Namen ContosoAuthorizationRule, die Benutzern das Abhören und Senden von Rechten an den Namespace ermöglicht.
Der für die Authentifizierung verwendete *Primär Primär* Code kann mithilfe des folgenden Windows PowerShell-Befehls nach dem Zufallsprinzip generiert werden:

\[Convert \] :: Base64-Wert ((1.. 32 |% { \[ Byte/] (Get-Random-mindestens 0-Maximum 255)))

## Beispiele

### Beispiel 1: Erstellen einer Autorisierungsregel und Zuweisen der Autorisierung zu einem Namespace
```
PS C:\>New-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

Dieser Befehl erstellt eine Autorisierungsregel und weist diese Regel dem Namespace ContosoNamespace zu.
Beim Erstellen dieser Regel müssen Sie den entsprechenden Namespace und die Ressourcengruppe angeben, der der Namespace zugewiesen ist.
Sie müssen jedoch keine Informationen über die Regel selbst angeben: Regel Informationen werden aus der Eingabedatei C:\Configuration\NamespaceAuthorizationRules.json übernommen.

## Parameter

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

### -Eingabefeld
Gibt den Pfad zu einer JSON-Datei an, die Konfigurationsinformationen für die neue Autorisierungsregel enthält.

```yaml
Type: String
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

Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.
Die neuen Regeln müssen einem vorhandenen Namespace zugewiesen werden.
Das Cmdlet **New-AzureRmNotificationHubsNamespaceAuthorizationRules** kann keinen neuen Namespace erstellen.

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
Gibt die Ressourcengruppe an, der der Namespace zugewiesen ist.

Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und Azure-Verwaltung unterstützt.

Sie müssen eine vorhandene Ressourcengruppe verwenden.
Dieses Cmdlet kann keine neue Ressourcengruppe erstellen.

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

### -SASRule
Gibt das **SharedAccessAuthorizationRuleAttributes** -Objekt an, das Konfigurationsinformationen für die neuen Regeln enthält.

```yaml
Type: SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes

## Notizen

## Verwandte Links

[Get-AzureRmNotificationHubAuthorizationRules](./Get-AzureRmNotificationHubAuthorizationRules.md)

[Remove-AzureRmNotificationHubAuthorizationRules](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[Satz-AzureRmNotificationHubAuthorizationRules](./Set-AzureRmNotificationHubAuthorizationRules.md)


