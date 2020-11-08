---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 6D15837A-22A9-4C5A-8064-C3605088EA71
online version: ''
schema: 2.0.0
ms.openlocfilehash: d31a2ef49674054ca6bb257df67d3439f5abe074
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006079"
---
# Register-AzureAutomationScheduledRunbook

## Synopsis

Ordnet einem runbooks einen Terminplan zu.

## Syntax

### ByRunbookName (Standard)
```
Register-AzureAutomationScheduledRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByRunbookNameAndScheduleName
```
Register-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-Parameters <IDictionary>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

Das Cmdlet " **Register-AzureAutomationScheduledRunbook** " ordnet einem runbooks einen Terminplan zu.
Der runbooks beginnt basierend auf dem von Ihnen angegebenen Zeitplan mithilfe des *ScheduleName* -Parameters.

## Beispiele

### Beispiel 1: Zuordnen eines runbooks zu einem Terminplan
```
PS C:\> Register-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01"
```

Dieser Befehl ordnet die runbooks mit dem Namen Runbk01 dem Zeitplan mit dem Namen "Sched01" im Azure Automation-Konto mit dem Namen "Contoso17" zu.

## Parameter

### -AutomationAccountName
Gibt den Namen eines Automatisierungs Kontos an.

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

### -Parameter
```yaml
Type: IDictionary
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: 

Required: False
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
Gibt den Namen des runbooks an.

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScheduleName
Gibt den Namen des Zeitplans an.

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
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

[Neu – AzureAutomationSchedule](./New-AzureAutomationSchedule.md)

[Registrierung aufheben-AzureAutomationScheduledRunbook](./Unregister-AzureAutomationScheduledRunbook.md)


