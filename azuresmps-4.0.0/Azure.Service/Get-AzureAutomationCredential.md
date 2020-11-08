---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C69558DB-78C3-4162-99C3-1300C3FE5287
online version: ''
schema: 2.0.0
ms.openlocfilehash: aa73cf467ffc3675b17b6c59ef5bd07483803267
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005865"
---
# Get-AzureAutomationCredential

## Synopsis

Ruft eine Azure-Automatisierungs Anmeldeinformationen ab.

## Syntax

### Seitensaller (Standard)
```
Get-AzureAutomationCredential -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByName
```
Get-AzureAutomationCredential -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

Das Cmdlet " **Get-AzureAutomationCredential** " ruft mindestens eine Microsoft Azure-Automatisierungs Anmeldeinformationen ab.
Standardmäßig werden alle Anmeldeinformationen zurückgegeben.
Um eine bestimmte Anmeldeinformationen abzurufen, geben Sie den Namen an.

## Beispiele

### Beispiel 1: Abrufen aller Anmeldeinformationen
```
PS C:\> Get-AzureAutomationCredential -AutomationAccountName "Contoso17"
```

Dieser Befehl ruft alle Anmeldeinformationen im Automatisierungs Konto mit dem Namen Contoso17 ab.

### Beispiel 2: Abrufen von Anmeldeinformationen
```
PS C:\> Get-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential"
```

Dieser Befehl ruft die Anmeldeinformationen mit dem Namen myCredential ab.

## Parameter

### -AutomationAccountName
Gibt den Namen des Automatisierungs Kontos mit den Anmeldeinformationen an, die abgerufen werden sollen.

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
Gibt den Namen der abzurufenden Anmeldeinformationen an.

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

### Microsoft. Azure. Commands. Automation. Model. CredentialInfo

## Notizen

## Verwandte Links

[Neu – AzureAutomationCredential](./New-AzureAutomationCredential.md)

[Remove-AzureAutomationCredential](./Remove-AzureAutomationCredential.md)

[Satz-AzureAutomationCredential](./Set-AzureAutomationCredential.md)


