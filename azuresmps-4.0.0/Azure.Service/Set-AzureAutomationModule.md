---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 9CED6E53-B65C-4D55-8AC7-9E8A8B143544
online version: ''
schema: 2.0.0
ms.openlocfilehash: da8f0e3bdc9e1cf573e9189e49feda85ee8c1b90
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006036"
---
# Set-AzureAutomationModule

## Synopsis

Aktualisiert ein Modul in der Automatisierung.

## Syntax

```
Set-AzureAutomationModule -Name <String> [-Tags <IDictionary>] [-ContentLinkUri <Uri>]
 [-ContentLinkVersion <String>] -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

Das Cmdlet " **Satz-AzureAutomationModule** " importiert eine neue Version eines Moduls oder ändert die Konfiguration des Moduls in Azure-Automatisierung.

## Beispiele

### Beispiel 1: Aktualisieren eines Moduls
```
PS C:\> Set-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri ".\ContosoModule.zip" -ContentLinkVersion "1.1"
```

Dieser Befehl importiert eine aktualisierte Version eines vorhandenen Moduls mit dem Namen ContosoModule in das Azure-Automatisierungs Konto mit dem Namen Contoso17.

## Parameter

### -AutomationAccountName
Gibt den Namen des Automatisierungs Kontos mit dem Modul an.

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

### -ContentLinkUri
Gibt den Pfad zur Moduldatei an.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ContentLinkVersion
Gibt die Version des Moduls an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen des Moduls an.

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

### -Tags
Gibt Tags für das Modul an.

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. Automation. Model. Module

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureAutomationModule](./Get-AzureAutomationModule.md)

[Neu – AzureAutomationModule](./New-AzureAutomationModule.md)

[Remove-AzureAutomationModule](./Remove-AzureAutomationModule.md)


