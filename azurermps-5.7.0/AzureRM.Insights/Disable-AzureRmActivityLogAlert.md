---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/disable-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Disable-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Disable-AzureRmActivityLogAlert.md
ms.openlocfilehash: 3a78dd91879082c39ae8d7d737484d532ff63f7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500601"
---
# Disable-AzureRmActivityLogAlert

## Synopsis
Deaktiviert eine Aktivitätsprotokoll Benachrichtigung und legt ihre Tags fest.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### DisableByNameAndResourceGroup
```
Disable-AzureRmActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisableByInputObject
```
Disable-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DisableByResourceId
```
Disable-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Disable-AzureRmActivityLogAlert deaktiviert** und Aktivitätsprotokoll Warnung und ermöglicht das Festlegen von Tags.
Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich gepatcht wird.

## Beispiele

### Beispiel 1: Deaktivieren einer Aktivitätsprotokoll Benachrichtigung
```
PS C:\>Disable-AzureRmActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

Mit diesem Befehl wird die Aktivitätsprotokoll Benachrichtigung namens alert1 in der Ressourcengruppe default-ActivityLogsAlerts deaktiviert.

Mit diesem Befehl wird die Tags-Eigenschaft der Aktivitätsprotokoll Benachrichtigung namens alert1 geändert und deaktiviert.

### Beispiel 2: Deaktivieren einer Aktivitätsprotokoll Benachrichtigung mit einem PSActivityLogAlertResource-Objekt als Eingabe
```
PS C:\>$obj = Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzureRmActivityLogAlert -InputObject $obj
```

Mit diesem Befehl wird eine Aktivitätsprotokoll Benachrichtigung mit dem Namen alert1 deaktiviert. Dafür wird ein PSActivityLogAlertResource-Objekt als Eingabeargument verwendet.

### Beispiel 3: Deaktivieren der ActivityLogAlert mit dem resourcecode-Parameter
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Disable-AzureRmActivityLogAlert
```

Mit diesem Befehl wird der ActivityLogAlert mit dem resourcecode-Parameter aus der Pipe deaktiviert.

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

### -Inputobject
Legt die Inputobject-Tags-Eigenschaft des Aufrufs fest, um den erforderlichen Namen, den Ressourcengruppennamen und die optionalen Tag-Eigenschaften zu extrahieren.

```yaml
Type: PSActivityLogAlertResource
Parameter Sets: DisableByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Der Name der Aktivitätsprotokoll Benachrichtigung.

```yaml
Type: String
Parameter Sets: DisableByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe, in der die Benachrichtigungs Ressource vorhanden sein wird.

```yaml
Type: String
Parameter Sets: DisableByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Resourcen-Nr
Legt die Eigenschaft "resourcetag-Tags" des Aufrufs fest, um den erforderlichen Namen, Eigenschaften von Ressourcengruppenname zu extrahieren.

```yaml
Type: String
Parameter Sets: DisableByResourceId
Aliases: 

Required: True
Position: Named
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

### Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource

## Notizen

## Verwandte Links

[Satz-AzureRmActivityLogAlert](./Set-AzureRmActivityLogAlert.md)

[Get-AzureRmActivityLogAlert](./Get-AzureRmActivityLogAlert.md)

[Remove-AzureRmActivityLogAlert](./Remove-AzureRmActivityLogAlert.md)

[Neu – AzureRmActionGroup](./New-AzureRmActionGroup.md)

[Neu – AzureRmActivityLogAlertCondition](./Get-AzureRmActivityLogAlertCondition.md)

[Enable-AzureRmActivityLogAlert](./Enable-AzureRmActivityLogAlert.md)
