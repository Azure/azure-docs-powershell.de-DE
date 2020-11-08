---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: D88C6B17-5D0E-4E23-9C5C-DB38DED9061C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1518c351a67c84e6dacafd1fa8a394051f3bfeac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006137"
---
# New-AzureAutomationVariable

## Synopsis

Erstellt eine Automatisierungs Variable.

## Syntax

```
New-AzureAutomationVariable -Name <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

Das Cmdlet **New-AzureAutomationVariable** erstellt eine Variable in der Microsoft Azure-Automatisierung.

## Beispiele

### Beispiel 1: Erstellen einer neuen Variablen mit einem einfachen Wert
```
PS C:\> New-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyStringVariable" -Encrypted $False -Value "My String"
```

Dieser Befehl erstellt eine neue Variable mit dem Namen MyStringVariable mit einem Zeichenfolgenwert im Azure-Automatisierungs Konto mit dem Namen Contoso17.

### Beispiel 2: Erstellen einer neuen Variablen mit einem komplexen Wert
```
PS C:\> $vm = Get-AzureVM -ServiceName "MyVM" -Name "MyVM"
PS C:\> New-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyComplexVariable" -Encrypted $False -Value $vm
```

Diese Befehle erstellen eine neue Variable namens MyComplexVariable im Automatisierungs Konto mit dem Namen Contoso17.
Ein komplexes Objekt wird für seinen Wert verwendet, in diesem Fall für ein Objekt eines virtuellen Computers.

## Parameter

### -AutomationAccountName
Gibt den Namen des Automatisierungs Kontos an, in dem die Variable gespeichert werden soll.

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

### -Beschreibung
Gibt eine Beschreibung für die Variable an.

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

### -Verschlüsselt
Gibt an, ob der Wert der Variablen verschlüsselt gespeichert werden soll.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt einen Namen für die Variable an.

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

### -Wert
Gibt einen Wert an, der in der Variablen gespeichert werden soll.

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. Azure. Commands. Automation. Model. Variable

## Notizen

## Verwandte Links

[Get-AzureAutomationVariable](./Get-AzureAutomationVariable.md)

[Remove-AzureAutomationVariable](./Remove-AzureAutomationVariable.md)

[Satz-AzureAutomationVariable](./Set-AzureAutomationVariable.md)


