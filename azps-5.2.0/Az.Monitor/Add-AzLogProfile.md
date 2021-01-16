---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
ms.openlocfilehash: bc0f1a6aacc6188a982fe75fa021bdafdc4e02de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98289438"
---
# Add-AzLogProfile

## SYNOPSIS
Erstellt ein neues Aktivitätsprotokollprofil. Dieses Profil wird verwendet, um das Aktivitätsprotokoll entweder in einem Azure -Speicherkonto zu archivieren oder es in einen Azure-Ereignishub im selben Abonnement zu streamen. 

## SYNTAX

```
Add-AzLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Add-AzLogProfile"** erstellt ein Protokollprofil.
- **Speicherkonto** – Es wird nur das Standardspeicherkonto (Premiumspeicherkonto wird nicht unterstützt) unterstützt. Dies kann entweder vom Typ "ARM" oder "Klassisch" sein. Wenn es bei einem Speicherkonto protokolliert wird, werden die Kosten für das Speichern des Aktivitätsprotokolls zu normalen Standardspeicherraten abgerechnet. Pro Abonnement kann nur ein Protokollprofil erstellt werden, damit pro Abonnement nur ein Speicherkonto zum Exportieren des Aktivitätsprotokolls verwendet werden kann. 
- **Ereignishub** – Pro Abonnement kann nur ein Protokollprofil erstellt werden, damit pro Abonnement nur ein Ereignishub zum Exportieren des Aktivitätsprotokolls verwendet werden kann. Wenn das Aktivitätsprotokoll auf einen Ereignishub gestreamt wird, gelten die Standardpreise für den Ereignishub. Im Aktivitätsprotokoll können Ereignisse zu einer Region gehören oder "Global" sein. Global bedeutet im Wesentlichen, dass es sich bei diesen Ereignissen um regionagnostische Zeichen handelt und unabhängig von der Region sind, tatsächlich fallen die meisten Ereignisse in diese Kategorie. Wenn das Aktivitätsprotokollprofil über das Portal festgelegt wird, wird implizit "Global" zusammen mit allen anderen in der Benutzeroberfläche ausgewählten Regionen hinzufügt. Bei Verwendung des Cmdlets muss der Speicherort als "Global" explizit unabhängig von einer anderen Region erwähnt werden. 
**Hinweis:** Wenn **"Global" an** den Speicherorten nicht festgelegt wird, wird ein Großteil des Aktivitätsprotokolls nicht exportiert. Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung vom Benutzer anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.

## BEISPIELE

### Beispiel 1: Hinzufügen eines neuen Protokollprofils zum Exportieren des Aktivitätsprotokolls, das mit der Standortbedingung in ein Speicherkonto abgestimmt ist
```powershell
Add-AzLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

### Beispiel 2

Erstellt ein neues Aktivitätsprotokollprofil. (automatisch generiert)

```powershell <!-- Aladdin Generated Example --> 
Add-AzLogProfile -Location 'Global' -Name ExportLogProfile -RetentionInDays <Int32> -ServiceBusRuleId <String> -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## PARAMETERS

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
Gültige Werte: Führen Sie das Cmdlet "Unter" aus, um die neueste Liste der Speicherorte zu erhalten. Get-AzLocation | DisplayName auswählen

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
Gibt die Aufbewahrungsrichtlinie in Tagen an. Dies ist die Anzahl der Tage, die die Protokolle im angegebenen Speicherkonto beibehalten werden. Um die Daten für immer auf **0 zu speichern, legen Sie diese auf 0.** Wenn er nicht angegeben ist, wird standardmäßig **"0" verwendet.** Für die Datenaufbewahrung gelten normale Standardspeicher- oder Ereignishub-Abrechnungssätze.

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
Gibt die ID der Servicebusregel an.

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
Gibt die ID des Speicherkontos an. "ID" ist beispielsweise die vollqualifizierte Ressourcen-ID des Speicherkontos.  
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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## AUSGABEN

### Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzLogProfile](./Get-AzLogProfile.md)

[Remove-AzLogProfile](./Remove-AzLogProfile.md)


