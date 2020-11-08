---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9AC28E79-0E3F-4AED-8BFE-8D1C4DCB7715
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd7ece4f8f414df7be6e2d38920f516119f4b82a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006732"
---
# Get-AzureVMPuppetExtension

## Synopsis
Ruft die auf einem virtuellen Computer angewendete Marionetten Erweiterung ab.

## Syntax

```
Get-AzureVMPuppetExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureVMPuppetExtension** " Ruft die auf einem virtuellen Computer angewendete Marionetten Erweiterung ab.

## Beispiele

### Beispiel 1: Abrufen der auf einem virtuellen Computer angewendeten Marionetten Erweiterung
```
PS C:\> Get-AzureVMPuppetExtension -VM $VM
```

Mit diesem Befehl wird die auf einem virtuellen Computer angewendete Marionetten Erweiterung abgerufen.

## Parameter

### -Information
Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.

Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Weiterhin
- Ignorieren
- Erkundigen
- SilentlyContinue
- Beenden
- Anhalten

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Gibt eine Informations Variable an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -VM
Gibt das Objekt des beständigen virtuellen Computers an.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Remove-AzureVMPuppetExtension](./Remove-AzureVMPuppetExtension.md)

[Satz-AzureVMPuppetExtension](./Set-AzureVMPuppetExtension.md)


