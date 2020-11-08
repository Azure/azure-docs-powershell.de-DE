---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2F66B0F2-37F3-4046-9FB0-B8C4B90D84A3
online version: ''
schema: 2.0.0
ms.openlocfilehash: d03364038a7a0563e5a8ab2f2f88d36b24da0ebc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006563"
---
# Get-AzureAutomationScheduledRunbook

## Synopsis

Ruft Azure Automation runbooks und zugeordnete Zeitpläne ab.

## Syntax

### Seitensaller (Standard)
```
Get-AzureAutomationScheduledRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByJobScheduleId
```
Get-AzureAutomationScheduledRunbook -JobScheduleId <Guid> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByRunbookName
```
Get-AzureAutomationScheduledRunbook -RunbookName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByRunbookNameAndScheduleName
```
Get-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByScheduleName
```
Get-AzureAutomationScheduledRunbook -ScheduleName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

Der **Get-AzureAutomationScheduledRunbook** ruft mindestens ein Azure Automation-runbooks und zugeordnete Zeitpläne ab.
Standardmäßig werden alle geplanten runbooks zurückgegeben.

Um einen bestimmten geplanten runbooks abzurufen, geben Sie den runbooks-Namen und den Terminplan Namen an.
Um alle einem runbooks zugeordneten Zeitpläne abzurufen, geben Sie nur den runbooks-Namen ein.
Um alle runbooks zu erhalten, die einem Terminplan zugeordnet sind, geben Sie nur den Terminplan Namen an.

## Beispiele

### Beispiel 1: Abrufen aller geplanten runbooks
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17"
```

Dieser Befehl ruft alle geplanten runbooks im Automatisierungs Konto mit dem Namen Contoso17 ab.

### Beispiel 2: Abrufen aller einem runbooks zugeordneten Zeitpläne
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -RunbookName "Runbk01"
```

Dieser Befehl ruft alle geplanten runbooks für das runbooks-Runbk01 im Automatisierungs Konto mit dem Namen Contoso17 ab.

### Beispiel 3: Abrufen aller runbooks, die einem Terminplan zugeordnet sind
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ScheduleName "Schedule01"
```

Dieser Befehl ruft alle geplanten runbooks für den Terminplan Schedule01 im Automatisierungs Konto mit dem Namen Contoso17 ab.

## Parameter

### -AutomationAccountName
Gibt den Namen eines Azure Automation-Kontos an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -JobScheduleId
Gibt die ID eines geplanten Auftrags an.

```yaml
Type: Guid
Parameter Sets: ByJobScheduleId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest.
Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunbookName
Gibt den Namen einer runbooks an.

```yaml
Type: String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScheduleName
Gibt den Namen eines Zeitplans an.

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. Azure. Commands. Automation. Model. JobSchedule

## Notizen

## Verwandte Links

[Registrieren-AzureAutomationScheduledRunbook](./Register-AzureAutomationScheduledRunbook.md)

[Registrierung aufheben-AzureAutomationScheduledRunbook](./Unregister-AzureAutomationScheduledRunbook.md)


