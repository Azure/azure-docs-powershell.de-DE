---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
ms.openlocfilehash: 24a42fba23427f437cb064e1915c19e36e7a71bf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158745"
---
# New-AzNotificationHubsNamespace

## SYNOPSIS
Erstellt einen Benachrichtigungshub-Namespace.

## SYNTAX

```
New-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "New-AzNotificationHubsNamespace"** erstellt einen Benachrichtigungshub-Namespace.
Namespaces sind logische Container, mit deren Hilfe Sie Ihre Benachrichtigungshubs organisieren und verwalten können.
Sie müssen über mindestens einen Benachrichtigungshub-Namespace verfügen.
Ein einzelner Namespace kann mehrere Hubs haben.
Sie können über mehrere Namespaces verfügen, um Ihre Hubs zu organisieren oder bestimmten Personen die Berechtigung zum Verwalten einer ausgewählten Teilmenge Ihrer Hubs zu erteilen.
Um einen Namespace zu erstellen, stellen Sie sicher, dass Sie einen eindeutigen Namen für den Namespace angeben. geben Sie das Rechenzentrum an, in dem sich der Namespace befinden soll; und geben Sie die Ressourcengruppe an, der der Namespace zugewiesen werden soll.
Nachdem der Namespace erstellt wurde, können Sie das cmdlet New-AzNotificationHubsNamespaceAuthorizationRules verwenden, um diesem Namespace Autorisierungsregeln zuzuordnen.
Autorisierungsregeln werden verwendet, um Berechtigungen für den Namespace zu verwalten.

## BEISPIELE

### Beispiel 1: Erstellen eines Benachrichtigungshubs
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

Mit diesem Befehl wird ein Benachrichtigungshub namens "ContosoPartners" erstellt.
Der Namespace befindet sich im Rechenzentrum "USA, Westen" und wird der Ressourcengruppe "ContosoNotificationsGroup" zugewiesen.

### Beispiel 2: Erstellen eines Benachrichtigungshubs mit Tags
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

Mit diesem Befehl wird ein Benachrichtigungshub namens "ContosoPartners" erstellt.
Der Namespace befindet sich im Rechenzentrum "USA, Westen" und wird der Ressourcengruppe "ContosoNotificationsGroup" zugewiesen.
Darüber hinaus erstellt dieser Befehl ein Tag mit dem Namen "Audience" und dem Wert "PartnerOrganizations" und wird dem Namespace zugewiesen.
Dadurch wird sichergestellt, dass der Namespace immer angezeigt wird, wenn Sie nach Elementen filtern, für die das Tag "Audience" auf "PartnerOrganizations" festgelegt ist.

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

### -Location
Gibt den Anzeigenamen des Rechenzentrums an, das den Namespace hosten soll.
Obwohl Sie diesen Parameter auf einen beliebigen gültigen Speicherort festlegen können, können Sie zur optimalen Leistung ein Rechenzentrum verwenden, das sich in der Nähe der Mehrzahl der Benutzer befindet.

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
Gibt den Namen des neuen Namespace an.
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
Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln so, dass sie einfach zur Bestandsverwaltung und Verwaltung beitragen.

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

### -Tag
Gibt Name-Wert-Paare an, die zum Kategorisieren und Organisieren von Azure-Elementen verwendet werden können.
Tags funktionieren ähnlich wie Schlüsselwörter und funktionieren in einer gesamten Bereitstellung.
Wenn Sie z. B. nach allen Elementen mit dem Tag "Department:IT" suchen, gibt die Suche alle Azure-Elemente zurück, die dieses Tag enthalten, unabhängig von Elementtyp, Speicherort oder Ressourcengruppe.
Ein einzelnes Tag besteht aus zwei Teilen: dem *Namen* und optional dem *Wert.*
In "Department:IT" ist der Tagname beispielsweise "Department" (Abteilung) und der Tagwert "IT".
Verwenden Sie zum Hinzufügen eines Tags eine ähnliche Hashtabellensyntax wie die folgende, wodurch das Tag "CalendarYear:2016" erstellt wird:

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

### System.Collections.Hashtable

## AUSGABEN

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


