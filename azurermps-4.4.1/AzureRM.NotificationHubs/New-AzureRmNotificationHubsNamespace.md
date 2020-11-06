---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: 501182c9307319dd84c61a14c2243d49cdb00541
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497013"
---
# New-AzureRmNotificationHubsNamespace

## Synopsis
Erstellt einen Benachrichtigungs-Hub-Namespace.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tags] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmNotificationHubsNamespace** erstellt einen Benachrichtigungs-Hub-Namespace.

Namespaces sind logische Container, die Ihnen beim organisieren und Verwalten Ihrer benachrichtigungshubs helfen.
Sie müssen über mindestens einen Benachrichtigungs-Hub-Namespace verfügen.
Ein einzelner Namespace kann mehrere Hubs beherbergen.
Sie können mehrere Namespaces haben, um Ihre Hubs zu organisieren oder bestimmten Personen die Berechtigung zum Verwalten einer ausgewählten Teilmenge ihrer Hubs zu erteilen.

Wenn Sie einen Namespace erstellen möchten, stellen Sie sicher, dass Sie einen eindeutigen Namen für den Namespace angeben. Geben Sie das Rechenzentrum an, in dem sich der Namespace befinden soll. und geben Sie die Ressourcengruppe an, der der Namespace zugewiesen werden soll.
Nachdem der Namespace erstellt wurde, können Sie das New-AzureRmNotificationHubsNamespaceAuthorizationRules-Cmdlet verwenden, um diesem Namespace Autorisierungsregeln zuzuweisen.
Autorisierungsregeln werden verwendet, um Berechtigungen für den Namespace zu verwalten.

## Beispiele

### Beispiel 1: Erstellen eines benachrichtigungshubs
```
PS C:\>New-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

Dieser Befehl erstellt einen Benachrichtigungs-Hub mit dem Namen ContosoPartners.
Der Namespace befindet sich im West-US-Rechenzentrum und wird der ContosoNotificationsGroup-Ressourcengruppe zugeordnet.

### Beispiel 2: Erstellen eines benachrichtigungshubs mit Tags
```
PS C:\>New-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

Dieser Befehl erstellt einen Benachrichtigungs-Hub mit dem Namen ContosoPartners.
Der Namespace befindet sich im West-US-Rechenzentrum und wird der ContosoNotificationsGroup-Ressourcengruppe zugeordnet.
Darüber hinaus erstellt dieser Befehl ein Tag mit dem Namen Audience und dem Wert PartnerOrganizations und wird dem Namespace zugewiesen.
Dadurch wird sichergestellt, dass der Namespace jedes Mal angezeigt wird, wenn Sie nach Elementen filtern, deren Audience-Tag auf PartnerOrganizations festgesetzt ist.

## Parameter

### -Standort
Gibt den Anzeigenamen des Rechenzentrums an, das den Namespace hosten soll.
Obwohl Sie diesen Parameter an einen beliebigen gültigen Speicherort setzen können, empfiehlt es sich, für optimale Leistung ein Rechenzentrum in der Nähe der meisten Benutzer zu verwenden.

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

### -Namespace
Gibt den Namen des neuen Namespaces an.
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
Gibt die Ressourcengruppe an, der der Namespace zugewiesen wird.
Ressourcengruppen organisieren Elemente wie Namespaces, benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die eine einfache Bestandsverwaltung und-Verwaltung unterstützt.

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

### -SkuTier
SKU-Ebene des Namespaces

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tags
Gibt Namen-Wert-Paare an, die zum Kategorisieren und organisieren von Azure-Elementen verwendet werden können.
Tags funktionieren ähnlich wie Schlüsselwörter und funktionieren in einer Bereitstellung.
Wenn Sie beispielsweise nach allen Elementen mit der Tag-Abteilung suchen, gibt die Suche alle Azure-Elemente zurück, die diese Kategorie aufweisen, und zwar unabhängig von Elementen wie Elementtyp, Speicherort oder Ressourcengruppe.

Ein einzelnes Tag besteht aus zwei Teilen: dem *Namen* und optional dem *Wert*.
Beispielsweise ist in Department: IT der Tag-Name Department, und der Tag-Wert ist dieser.
Verwenden Sie zum Hinzufügen einer Kategorie die Hashtabellen Syntax ähnlich dieser, wodurch das Tag CalendarYear: 2016 erstellt wird:

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
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

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. Azure. Commands. NotificationHubs. Models. NamespaceAttributes

## Notizen

## Verwandte Links

[Get-AzureRmNotificationHubsNamespace](./Get-AzureRmNotificationHubsNamespace.md)

[Remove-AzureRmNotificationHubsNamespace](./Remove-AzureRmNotificationHubsNamespace.md)

[Satz-AzureRmNotificationHubsNamespace](./Set-AzureRmNotificationHubsNamespace.md)


