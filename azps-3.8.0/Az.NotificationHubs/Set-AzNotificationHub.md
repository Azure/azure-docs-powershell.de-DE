---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
ms.openlocfilehash: 3dc4a81731f42ce6a27ae5d23fb7c81af76cf789
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94002974"
---
# Set-AzNotificationHub

## Synopsis
Legt Eigenschaftswerte für einen Benachrichtigungs-Hub fest.

## Syntax

### InputFileParameterSet
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NotificationHubParameterSet
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet " **festlegen-AzNotificationHub** " werden die Eigenschaftenwerte eines benachrichtigungshubs geändert.
Sie können einen Benachrichtigungs-Hub-Eigenschaftswert auf zwei Arten ändern.
Zum einen können Sie eine Instanz des **NotificationHubAttributes** -Objekts erstellen und dieses Objekt dann mit den Eigenschaftswerten konfigurieren, die der neue Hub besitzen soll.
Dies kann über das .NET Framework erfolgen.
Sie können diese Eigenschaftswerte dann mithilfe des *NotificationHubObj* -Parameters in ihren Hub kopieren.
Sie können auch eine JSON-Datei (JavaScript Object Notation) erstellen, die die relevanten Konfigurationswerte enthält, und diese Werte dann über den *Input* file-Parameter übernehmen.
Eine JSON-Datei ist eine Textdatei, die Syntax ähnlich der folgenden verwendet: {  
    "Name": "ContosoNotificationHub";  
    "Standort": "West US",  
} Bei Verwendung in Verbindung mit dem Cmdlet " **Set-AzNotificationHub** " legt das obige JSON-Beispiel den Positionswert eines benachrichtigungshubs mit dem Namen ContosoNotificationHub auf West US fest.

## Beispiele

### Beispiel 1: Ändern der Eigenschaftswerte für einen Benachrichtigungs-Hub
```
PS C:\>Set-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

Mit diesem Befehl werden die Eigenschaftenwerte für einen Benachrichtigungs-Hub geändert, der im ContosoNamespace-Namespace gefunden und der Ressourcengruppe ContosoNotificationsGroup zugewiesen wurde.
Die Eigenschaftenwerte sowie der Name des zu ändernden Hubs werden nicht im Befehl angegeben.
Stattdessen sind diese Informationen in der Eingabedatei C:\Configuration\Hubs.json enthalten.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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
Gibt den Pfad zu einer JSON-Datei an, die Konfigurationsinformationen für den Benachrichtigungs-Hub enthält.

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
Gibt den Namespace an, dem der Benachrichtigungs-Hub zugewiesen ist.
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

### -NotificationHubObj
Gibt das **NotificationHubAttributes** -Objekt an, das Konfigurationsinformationen für den Hub enthält, die von diesem Cmdlet geändert werden.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes
Parameter Sets: NotificationHubParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroup
Gibt die Ressourcengruppe an, der der Benachrichtigungs-Hub zugewiesen ist.
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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes

## Notizen

## Verwandte Links

[Get-AzNotificationHub](./Get-AzNotificationHub.md)

[Neu – AzNotificationHub](./New-AzNotificationHub.md)

[Remove-AzNotificationHub](./Remove-AzNotificationHub.md)


