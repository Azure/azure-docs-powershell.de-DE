---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/powershell/module/az.monitor/add-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
ms.openlocfilehash: a5d60cbda668e963793dbb350950ea0e85812892
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932776"
---
# Add-AzLogProfile

## SYNOPSIS
Erstellt ein neues Aktivitätsprotokollprofil. Dieses Profil wird verwendet, um das Aktivitätsprotokoll entweder in einem Azure-Speicherkonto zu archivieren oder es an einen Azure-Ereignishub im gleichen Abonnement zu streamen. 

## SYNTAX

```
Add-AzLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Add-AzLogProfile-Cmdlet** erstellt ein Protokollprofil.
- **Speicherkonto** : Es wird nur das Standardspeicherkonto (Premiumspeicherkonto wird nicht unterstützt) unterstützt. Sie kann entweder vom Typ ARM oder klassisch sein. Wenn es bei einem Speicherkonto protokolliert wird, werden die Kosten für das Speichern des Aktivitätsprotokolls zu normalen Standardspeicherraten abgerechnet. Es kann nur ein Protokollprofil pro Abonnement sein, damit nur ein Speicherkonto pro Abonnement zum Exportieren des Aktivitätsprotokolls verwendet werden kann. 
- **Ereignishub** : Es kann nur ein Protokollprofil pro Abonnement sein, damit nur ein Ereignishub pro Abonnement zum Exportieren des Aktivitätsprotokolls verwendet werden kann. Wenn das Aktivitätsprotokoll an einen Ereignishub gestreamt wird, gelten standardmäßige Preise für Event Hubs. Im Aktivitätsprotokoll können Ereignisse eine Region betreffen oder "Global" sein. Global bedeutet im Wesentlichen, dass diese Ereignisse regionagnostisch sind und unabhängig von der Region sind, tatsächlich fallen die meisten Ereignisse in diese Kategorie. Wenn das Aktivitätsprotokollprofil über das Portal festgelegt wurde, wird implizit "Global" zusammen mit allen anderen auf der Benutzeroberfläche ausgewählten Regionen addiert. Bei Verwendung des Cmdlets muss der Speicherort als "Global" explizit erwähnt werden, abgesehen von jeder anderen Region. 
**Hinweis:** Wenn **Sie "Global" nicht in** den Speicherorten festlegen, wird ein Großteil des Aktivitätsprotokolls nicht exportiert. Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h. es kann eine Bestätigung vom Benutzer anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.

## BEISPIELE

### Beispiel 1: Hinzufügen eines neuen Protokollprofils zum Exportieren des Aktivitätsprotokolls, das mit der Standortbedingung in ein Speicherkonto übereinstimmen soll
```powershell
Add-AzLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

### Beispiel 2

Erstellt ein neues Aktivitätsprotokollprofil. (automatisch generiert)

```powershell <!-- Aladdin Generated Example --> 
Add-AzLogProfile -Location 'Global' -Name ExportLogProfile -RetentionInDays <Int32> -ServiceBusRuleId <String> -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## PARAMETER

### -Category
Gibt die Liste der Kategorien an.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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

### -Location
Gibt den Speicherort des Protokollprofils an.
Gültige Werte: Führen Sie unter cmdlet aus, um die neueste Liste der Speicherorte zu erhalten. Get-AzLocation | Wählen Sie Anzeigename aus.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen des Profils an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionInDays
Gibt die Aufbewahrungsrichtlinie in Tagen an. Dies ist die Anzahl der Tage, in der die Protokolle im angegebenen Speicherkonto aufbewahrt werden. Um die Daten für immer zu behalten, legen Sie dies auf **0 festgelegt.** Wenn sie nicht angegeben ist, wird standardmäßig **0 festgelegt.** Normale Standardspeicher- oder Ereignishubabrechnungssätze gelten für die Datenaufbewahrung.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceBusRuleId
Gibt die ID der Dienstbusregel an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountId
Gibt die ID des Speicherkontos an. ID ist die vollqualifizierte Ressourcen-ID des Speicherkontos, z. B.  
/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### System.String

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## AUSGABEN

### Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile

## NOTIZEN

## VERWANDTE LINKS

[Get-AzLogProfile](./Get-AzLogProfile.md)

[Remove-AzLogProfile](./Remove-AzLogProfile.md)


