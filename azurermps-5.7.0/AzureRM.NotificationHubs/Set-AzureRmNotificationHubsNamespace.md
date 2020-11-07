---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: b1fe6ae9085dcfc1d74eaf86af831a1e984a9143
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665180"
---
# Set-AzureRmNotificationHubsNamespace

## Synopsis
Legt Eigenschaftswerte für einen Notification Hub-Namespace fest.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Set-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Set-AzureRmNotificationHubsNamespace** " legt die Eigenschaftswerte eines vorhandenen Benachrichtigungs-Hub-Namespace fest.

Namespaces sind logische Container, die Ihnen beim organisieren und Verwalten Ihrer benachrichtigungshubs helfen.
Sie müssen über mindestens einen Benachrichtigungs-Hub-Namespace verfügen.
Darüber hinaus müssen alle benachrichtigungshubs über einen zugewiesenen Namespace verfügen.

Dieses Cmdlet wird in erster Linie verwendet, um einen Namespace zu aktivieren und zu deaktivieren.
Wenn ein Namespace deaktiviert ist, können Benutzer keine Verbindung mit einem der benachrichtigungshubs im Namespace herstellen, und Administratoren können diese Hubs auch nicht verwenden, um Push-Benachrichtigungen zu senden.
Wenn Sie einen deaktivierten Namespace erneut aktivieren möchten, verwenden Sie dieses Cmdlet, um die **State** -Eigenschaft des Namespaces auf Active festzulegen.

Sie können dieses Cmdlet auch verwenden, um einen Namespace als kritisch zu kennzeichnen.
Dadurch wird verhindert, dass der Namespace gelöscht wird.
Um einen kritischen Namespace zu entfernen, müssen Sie zuerst das kritische Tag entfernen.

## Beispiele

### Beispiel 1: Deaktivieren eines Namespaces
```
PS C:\>Set-AzureRmNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

Mit diesem Befehl wird der Namespacenamens ContosoPartners deaktiviert, der sich im Rechenzentrum von West-US befindet und der ContosoNotificationsGroup-Ressourcengruppe zugewiesen ist.

### Beispiel 2: Aktivieren eines Namespaces
```
PS C:\>Set-AzureRmNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

Mit diesem Befehl wird der Namespacenamens ContosoPartners im West US-Rechenzentrum aktiviert und der ContosoNotificationsGroup-Ressourcengruppe zugewiesen.

## Parameter

### -Kritisch
Gibt an, ob es sich bei dem Namespace um einen kritischen Namespace handelt.
Kritische Namespaces können nicht gelöscht werden.
Um einen kritischen Namespace zu löschen, müssen Sie den Wert dieser Eigenschaft auf "false" festlegen, um den Namespace als nicht kritisch zu kennzeichnen.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Force
Keine Bestätigung anfordern.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Standort
Gibt den Anzeigenamen des Rechenzentrums an, das den Namespace hostet.
Sie können diesen Parameter zwar auf einen beliebigen gültigen Azure-Speicherort setzen, doch sollten Sie für optimale Leistung ein Rechenzentrum verwenden, das sich in der Nähe der meisten Benutzer befindet.

Führen Sie den folgenden Befehl aus, um eine aktuelle Liste der Azure-Speicherorte abzurufen:

`Get-AzureLocation | Select-Object DisplayName`

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Gibt den Namespace an, der vom Cmdlet geändert wird.

Namespaces bieten eine Möglichkeit zum Gruppieren und Kategorisieren von benachrichtigungshubs.

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

### -SkuTier
SKU-Ebene des Namespaces

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bundesland
Gibt den aktuellen Zustand des Namespaces an.
Die zulässigen Werte für diesen Parameter sind: aktiv und deaktiviert.

```yaml
Type: NamespaceState
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Gibt Namen-Wert-Paare an, die zum Kategorisieren und organisieren von Azure-Elementen verwendet werden können.
Tags funktionieren ähnlich wie Schlüsselwörter und funktionieren in einer Bereitstellung.
Wenn Sie beispielsweise nach allen Elementen mit der Tag-Abteilung suchen, gibt die Suche alle Azure-Elemente zurück, die diese Kategorie aufweisen, und zwar unabhängig von Elementen wie Elementtyp, Speicherort oder Ressourcengruppe.

Ein einzelnes Tag besteht aus zwei Teilen: dem *Namen* und (optional) dem *Wert*.
In Department: IT lautet der Tag-Name beispielsweise Department, und der Tag-Wert ist er.
Verwenden Sie zum Hinzufügen einer Kategorie die Hashtabellen Syntax ähnlich dieser, wodurch das Tag CalendarYear: 2016 erstellt wird:

-Tags @ {Name = "CalendarYear"; Value = "2016"}

Wenn Sie mehrere Tags im gleichen Befehl hinzufügen möchten, trennen Sie die einzelnen Tags durch Kommas:

-Tag @ {Name = "CalendarYear"; Value = "2016"}, @ {Name = "FiscalYear"; Wert = "2017"}

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### Microsoft. Azure. Commands. NotificationHubs. Models. NamespaceAttributes

## Notizen

## Verwandte Links

[Get-AzureRmNotificationHubsNamespace](./Get-AzureRmNotificationHubsNamespace.md)

[Neu – AzureRmNotificationHubsNamespace](./New-AzureRmNotificationHubsNamespace.md)

[Remove-AzureRmNotificationHubsNamespace](./Remove-AzureRmNotificationHubsNamespace.md)


