---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 73F90276-FABD-414A-B29D-83F371C1ED21
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0544b4d5fafcb388b65271e736f43a15f02980c5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006574"
---
# Get-AzureAutomationModule

## Synopsis

Rufen Sie ein Azure-Automatisierungs Modul ab.

## Syntax

### Seitensaller (Standard)
```
Get-AzureAutomationModule -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByName
```
Get-AzureAutomationModule -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

Das Cmdlet " **Get-AzureAutomationModule** " ruft mindestens ein Microsoft Azure-Automatisierungs Modul ab.
Standardmäßig werden alle Module zurückgegeben.
Um ein bestimmtes Modul abzurufen, geben Sie dessen Namen ein.

## Beispiele

### Beispiel 1: Abrufen aller Module
```
PS C:\> Get-AzureAutomationModule -AutomationAccountName "Contoso17"
```

Dieser Befehl ruft alle Module im Azure Automation-Konto mit dem Namen Contoso17 ab.

### Beispiel 2: Abrufen eines Moduls
```
PS C:\> Get-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule"
```

Dieser Befehl ruft ein Modul mit dem Namen ContosoModule im Azure Automation-Konto mit dem Namen Contoso17.

## Parameter

### -AutomationAccountName
Gibt den Namen des Automatisierungs Kontos mit dem abzurufenden runbooks an.

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

### -Name
Gibt den Namen des abzurufenden Moduls an.

```yaml
Type: String
Parameter Sets: ByName
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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. Azure. Commands. Automation. Model. Module

## Notizen

## Verwandte Links

[Neu – AzureAutomationModule](./New-AzureAutomationModule.md)

[Remove-AzureAutomationModule](./Remove-AzureAutomationModule.md)

[Satz-AzureAutomationModule](./Set-AzureAutomationModule.md)


