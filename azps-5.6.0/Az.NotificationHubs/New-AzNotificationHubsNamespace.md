---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
ms.openlocfilehash: 20a4da67030962a238838247a7dcf137208e56b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918243"
---
# New-AzNotificationHubsNamespace

## SYNOPSIS
Erstellt einen Benachrichtigungshubnamespace.

## SYNTAX

```
New-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet New-AzNotificationHubsNamespace** erstellt einen Benachrichtigungshubnamespace.
Namespaces sind logische Container, mit deren Hilfe Sie Ihre Benachrichtigungshubs organisieren und verwalten können.
Sie müssen über mindestens einen Benachrichtigungshubnamespace verfügen.
Ein einzelner Namespace kann mehrere Hubs haben.
Sie können über mehrere Namespaces verfügen, um Ihre Hubs zu organisieren oder bestimmten Personen die Berechtigung zum Verwalten einer ausgewählten Teilmenge Ihrer Hubs zu erteilen.
Um einen Namespace zu erstellen, stellen Sie sicher, dass Sie einen eindeutigen Namen für den Namespace angeben. geben Sie das Rechenzentrum an, in dem sich der Namespace befindet. und geben Sie die Ressourcengruppe an, der der Namespace zugewiesen wird.
Nachdem der Namespace erstellt wurde, können Sie das New-AzNotificationHubsNamespaceAuthorizationRules-Cmdlet verwenden, um diesem Namespace Autorisierungsregeln zuzuordnen.
Autorisierungsregeln werden verwendet, um Berechtigungen für den Namespace zu verwalten.

## BEISPIELE

### Beispiel 1: Erstellen eines Benachrichtigungshubs
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

Mit diesem Befehl wird ein Benachrichtigungshub namens ContosoPartners erstellt.
Der Namespace befindet sich im West US-Rechenzentrum und wird der Ressourcengruppe ContosoNotificationsGroup zugewiesen.

### Beispiel 2: Erstellen eines Benachrichtigungshubs mit Tags
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

Mit diesem Befehl wird ein Benachrichtigungshub namens ContosoPartners erstellt.
Der Namespace befindet sich im West US-Rechenzentrum und wird der Ressourcengruppe ContosoNotificationsGroup zugewiesen.
Darüber hinaus erstellt dieser Befehl ein -Tag mit dem Namen Audience und dem Wert PartnerOrganizations und wird dem -Namespace zugewiesen.
Dadurch wird sichergestellt, dass der Namespace immer angezeigt wird, wenn Sie nach Elementen filtern, für die das Audience-Tag auf PartnerOrganizations festgelegt ist.

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

### -Location
Gibt den Anzeigenamen des Rechenzentrums an, in dem der Namespace gehostet wird.
Obwohl Sie diesen Parameter auf einen beliebigen gültigen Speicherort festlegen können, sollten Sie für optimale Leistung ein Rechenzentrum verwenden, das sich in der Nähe der Meisten Ihrer Benutzer befindet.

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

### -ResourceGroup
Gibt die Ressourcengruppe an, der der Namespace zugewiesen wird.
Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die einfach die Bestandsverwaltung und -verwaltung unterstützt.

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
Sku-Ebene des Namespaces

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

### -Tag
Gibt Namen-Wert-Paare an, die zum Kategorisieren und Organisieren von Azure-Elementen verwendet werden können.
Tags funktionieren ähnlich wie Schlüsselwörter und funktionieren in einer Bereitstellung.
Wenn Sie beispielsweise mit dem Tag Department:IT nach allen Elementen suchen, gibt die Suche alle Azure-Elemente zurück, die über dieses Tag verfügen, unabhängig von Elementen wie Elementtyp, Speicherort oder Ressourcengruppe.
Ein einzelnes Tag besteht aus zwei Teilen: dem *Namen* und optional dem *Wert.*
In Department:IT ist der Tagname beispielsweise Abteilung, und der Tagwert ist IT.
Zum Hinzufügen eines Tags verwenden Sie die Syntax einer Hashtabelle ähnlich der folgenden, wodurch das Tag CalendarYear:2016 erstellt wird:

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

### System.Collections.Hashtable

## AUSGABEN

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes

## NOTIZEN

## VERWANDTE LINKS

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


