---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/set-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
ms.openlocfilehash: 7535ff45b8350cb107b7593dc78ab0709d747f8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918171"
---
# Set-AzNotificationHubsNamespace

## SYNOPSIS
Legt Eigenschaftswerte für einen Benachrichtigungshubnamespace fest.

## SYNTAX

```
Set-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Set-AzNotificationHubsNamespace** legt die Eigenschaftswerte eines vorhandenen Benachrichtigungshub-Namespaces fest.
Namespaces sind logische Container, mit deren Hilfe Sie Ihre Benachrichtigungshubs organisieren und verwalten können.
Sie müssen über mindestens einen Benachrichtigungshubnamespace verfügen.
Darüber hinaus müssen alle Benachrichtigungshubs über einen zugewiesenen Namespace verfügen.
Dieses Cmdlet wird in erster Linie zum Aktivieren und Deaktivieren eines Namespaces verwendet.
Wenn ein Namespace deaktiviert ist, können Benutzer keine Verbindung mit einem der Benachrichtigungshubs im Namespace herstellen, und Administratoren können diese Hubs auch nicht zum Senden von Pushbenachrichtigungen verwenden.
Wenn Sie einen deaktivierten Namespace erneut aktivieren möchten, verwenden Sie dieses Cmdlet, um die **State-Eigenschaft** des Namespaces auf Aktiv zu setzen.
Sie können dieses Cmdlet auch verwenden, um einen Namespace als kritisch zu kennzeichnen.
Dadurch wird verhindert, dass der Namespace gelöscht wird.
Zum Entfernen eines kritischen Namespaces müssen Sie zuerst das Critical-Tag entfernen.

## BEISPIELE

### Beispiel 1: Deaktivieren eines Namespaces
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

Mit diesem Befehl wird der Namespace contosoPartners deaktiviert, der sich im West US-Rechenzentrum befindet und der Ressourcengruppe ContosoNotificationsGroup zugewiesen ist.

### Beispiel 2: Aktivieren eines Namespaces
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

Mit diesem Befehl wird der Namespace "ContosoPartners" aktiviert, der sich im West US-Rechenzentrum befindet und der Ressourcengruppe ContosoNotificationsGroup zugewiesen ist.

## PARAMETER

### -Kritisch
Gibt an, ob der Namespace ein kritischer Namespace ist.
Kritische Namespaces können nicht gelöscht werden.
Zum Löschen eines kritischen Namespaces müssen Sie den Wert dieser Eigenschaft auf False festlegen, um den Namespace als nicht kritisch zu kennzeichnen.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Erzwingen
Bitten Sie nicht um Bestätigung.

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

### -Location
Gibt den Anzeigenamen des Rechenzentrums an, das den -Namespace hostet.
Obwohl Sie diesen Parameter auf einen beliebigen gültigen Azure-Speicherort festlegen können, sollten Sie für optimale Leistung ein Rechenzentrum verwenden, das sich in der Nähe der Meisten Ihrer Benutzer befindet.
Führen Sie den folgenden Befehl aus, um eine aktuelle Liste der Azure-Speicherorte zu erhalten: `Get-AzLocation | Select-Object DisplayName`

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
Gibt den Namespace an, den dieses Cmdlet ändert.
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
Gibt die Ressourcengruppe an, der der Namespace zugewiesen ist.
Ressourcengruppen organisieren Elemente wie Namespaces, Benachrichtigungshubs und Autorisierungsregeln auf eine Weise, die einfach die Bestandsverwaltung und die Azure-Verwaltung unterstützt.

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

### -State
Gibt den aktuellen Zustand des Namespaces an.
Die zulässigen Werte für diesen Parameter sind: Aktiv und Deaktiviert.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState
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
Gibt Namen-Wert-Paare an, die zum Kategorisieren und Organisieren von Azure-Elementen verwendet werden können.
Tags funktionieren ähnlich wie Schlüsselwörter und funktionieren in einer Bereitstellung.
Wenn Sie beispielsweise mit dem Tag Department:IT nach allen Elementen suchen, gibt die Suche alle Azure-Elemente zurück, die über dieses Tag verfügen, unabhängig von Elementen wie Elementtyp, Speicherort oder Ressourcengruppe.
Ein einzelnes Tag besteht aus zwei Teilen: dem *Namen* und (optional) dem *Wert.*
In Department:IT ist der Tagname beispielsweise Abteilung, und der Tagwert ist IT.
Zum Hinzufügen eines Tags verwenden Sie eine ähnliche Syntax für Hashtabellen, wodurch das Tag CalendarYear:2016 erstellt wird: -Tags @{Name="CalendarYear"; Value="2016"} Wenn Sie mehrere Tags in demselben Befehl hinzufügen möchten, trennen Sie die einzelnen Tags durch Kommas: -Tag @{Name="CalendarYear"; Value="2016"}, @{Name="FiscalYear"; Value="2017"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
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

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState

### System.Boolean

### System.Collections.Hashtable

## AUSGABEN

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes

## NOTIZEN

## VERWANDTE LINKS

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[New-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)


