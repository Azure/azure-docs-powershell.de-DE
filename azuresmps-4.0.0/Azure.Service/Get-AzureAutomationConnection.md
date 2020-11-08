---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: DD881317-7366-4B55-B1CC-6AF0286F1C5D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 69ef6fc78280180a3722492e5a4b53a52c7bde2a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006576"
---
# Get-AzureAutomationConnection

## Synopsis

Ruft eine Azure-Automatisierungs Verbindung ab.

## Syntax

### Seitensaller (Standard)
```
Get-AzureAutomationConnection -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByConnectionName
```
Get-AzureAutomationConnection -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByConnectionTypeName
```
Get-AzureAutomationConnection -ConnectionTypeName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

Das Cmdlet " **Get-AzureAutomationConnection** " ruft mindestens eine Microsoft Azure-Automatisierungs Verbindung ab.
Standardmäßig werden alle Verbindungen zurückgegeben.
Um eine bestimmte Verbindung zu erhalten, geben Sie den Namen an.
Um alle Verbindungen eines bestimmten Typs abzurufen, geben Sie den Namen des Verbindungstyps an.

## Beispiele

### Beispiel 1: Abrufen aller Verbindungen
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17"
```

Dieser Befehl ruft alle Verbindungen im Automatisierungs Konto mit dem Namen Contoso17 ab.

### Beispiel 2: Abrufen aller Verbindungen eines Typs
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17" -ConnectionTypeName "Azure"
```

Dieser Befehl ruft alle Azure-Verbindungen im Automatisierungs Konto mit dem Namen Contoso17 ab.

### Beispiel 3: Abrufen einer Verbindung
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17" -Name "Azure"
```

Dieser Befehl ruft die Verbindung mit dem Namen myConnection ab.

## Parameter

### -AutomationAccountName
Gibt den Namen des Automatisierungs Kontos an, mit dem die Verbindung abgerufen werden soll.

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

### -ConnectionTypeName
Gibt den Namen eines Verbindungstyps für die Verbindungen an, die abgerufen werden sollen.

```yaml
Type: String
Parameter Sets: ByConnectionTypeName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen einer Verbindung an, die abgerufen werden soll.

```yaml
Type: String
Parameter Sets: ByConnectionName
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

### Microsoft. Azure. Commands. Automation. Model. Connection

## Notizen

## Verwandte Links

[Neu – AzureAutomationConnection](./New-AzureAutomationConnection.md)

[Remove-AzureAutomationConnection](./Remove-AzureAutomationConnection.md)

[Satz-AzureAutomationConnectionFieldValue](./Set-AzureAutomationConnectionFieldValue.md)


