---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FAB5E55D-95FC-4545-8BA6-EEFCFDB04200
online version: ''
schema: 2.0.0
ms.openlocfilehash: c311653b92219eb3bee0e3b1f8c8fe5caaee9846
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005843"
---
# Get-AzureOSVersion

## Synopsis
Listet alle Azure Guest-Betriebssysteme auf.

## Syntax

```
Get-AzureOSVersion [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureOSVersion** " listet alle verfügbaren Azure Guest-Betriebssysteme auf.

## Beispiele

### Beispiel 1: Abrufen aller verfügbaren Betriebssysteme
```
PS C:\> Get-AzureOSVersion
```

Dieser Befehl ruft ein Objekt ab, das eine Liste aller Versionen von Gastbetriebssystemen enthält, die im aktuellen Abonnement zur Verfügung stehen.

### Beispiel 2: Anzeigen von Betriebssysteminformationen in einer Tabelle
```
PS C:\> Get-AzureOSVersion | Format-Table -AutoSize -Property "Family", "FamilyLabel", "Version"
```

Dieser Befehl ruft ein Objekt ab, das eine Liste aller Versionen von Gastbetriebssystemen enthält, die im aktuellen Abonnement zur Verfügung stehen.
Der Befehl übergibt Sie mithilfe des Pipelineoperators an das Cmdlet **Format-Table** .
Dieses Cmdlet formatiert sie als Tabelle, in der die Betriebssystemfamilie, das Betriebssystemfamilien Etikett und die Version angezeigt werden.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureOSDisk](./Get-AzureOSDisk.md)


