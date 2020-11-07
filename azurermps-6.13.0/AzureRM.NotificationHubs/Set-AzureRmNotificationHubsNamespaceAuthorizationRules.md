---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: F0981A7A-1B17-4141-A267-927E5B78BE5F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: f86eff8bae46e2a9f626566ccfdcc6e3d23a6e82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662797"
---
# Set-AzureRmNotificationHubsNamespaceAuthorizationRules

## Synopsis
Legt Autorisierungsregeln für einen Benachrichtigungs-Hub-Namespace fest.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### InputFileParameterSet
```
Set-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SASRuleParameterSet
```
Set-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureRmNotificationHubsNamespaceAuthorizationRules** " ändert eine Berechtigungsregel für eine freigegebene zugriffssignatur (SAS), die einem Benachrichtigungs-Hub-Namespace zugewiesen ist.
Autorisierungsregeln verwalten Benutzerrechte für den Namespace und die benachrichtigungshubs, die in diesem Namespace enthalten sind.
Dieses Cmdlet bietet zwei Möglichkeiten zum Ändern einer Autorisierungsregel, die einem Namespace zugewiesen ist.
Zum einen können Sie eine Instanz des **SharedAccessAuthorizationRuleAttributes** -Objekts erstellen und dieses Objekt dann mit den Eigenschaftswerten konfigurieren, die die Regel besitzen soll.
Sie können das .NET Framework verwenden, um dies zu erreichen.
Sie können diese Eigenschaftswerte dann über den *SASRule* -Parameter in die Regel kopieren.
Sie können auch eine JSON-Datei (JavaScript Object Notation) erstellen, die die relevanten Konfigurationswerte enthält, und diese Werte dann über den *Input* file-Parameter übernehmen.
Eine JSON-Datei ist eine Textdatei, die ähnlich wie diese Syntax verwendet wird: {  
    "Name": "ContosoAuthorizationRule";  
    "Primär Primär": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =";  
    "Rechte": \[  
        "Hören",  
        Senden  
    \]  
} Bei Verwendung in Verbindung mit dem Cmdlet " **setAzureRmNotificationHubsNamespaceAuthorizationRules** " ändert das vorangehende JSON-Beispiel eine Autorisierungsregel namens ContosoAuthorizationRule, um Benutzern das Abhören und Senden von Rechten an den Namespace zu ermöglichen.

## Beispiele

### Beispiel 1: Ändern einer Autorisierungsregel, die einem Namespace zugewiesen ist
```
PS C:\>Set-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -InputFile "C:\Configuration\AuthorizationRules.json"
```

Mit diesem Befehl wird eine Autorisierungsregel geändert, die dem Namespace mit dem Namen ContosoNamespace zugewiesen ist.
Sie müssen die Ressourcengruppe angeben, der der Namespace zugewiesen ist.
Informationen zur Autorisierungsregel sind nicht im Befehl selbst enthalten.
Stattdessen werden die Informationen aus der Eingabedatei C:\Configuration\AuthorizationRules.jsauf abgerufen.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Keine Bestätigung anfordern.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Eingabefeld
Gibt den Pfad zu einer JSON-Datei an, die Konfigurationsinformationen für die neue Regel enthält.

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
Gibt den Namespace an, der die Autorisierungsregeln enthält, die von diesem Cmdlet geändert werden.
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

### -ResourceGroup
Gibt die Ressourcengruppe an, der der Namespace zugewiesen ist.
Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und Azure-Verwaltung unterstützt.

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
Gibt das **SharedAccessAuthorizationRuleAttributes** -Objekt an, das Konfigurationsinformationen für die Autorisierungsregeln enthält, die von diesem Cmdlet geändert werden.

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
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes

## Notizen

## Verwandte Links

[Get-AzureRmNotificationHubsNamespaceAuthorizationRules](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[Neu – AzureRmNotificationHubsNamespaceAuthorizationRules](./New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[Remove-AzureRmNotificationHubsNamespaceAuthorizationRules](./Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md)


