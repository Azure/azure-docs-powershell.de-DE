---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 51A1B699-03F6-4BB9-9186-FDFFB094F16A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 72420272e04519fa888660f8ccb6d432ecb0ee5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006581"
---
# Enable-AzureTrafficManagerProfile

## Synopsis
Aktiviert ein Traffic Manager-Profil.

## Syntax

```
Enable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **enable-AzureTrafficManagerProfile** aktiviert ein Microsoft Azure Traffic Manager-Profil.
Geben Sie den *passthru* -Parameter an, um anzuzeigen, ob der Vorgang erfolgreich ausgeführt wurde.

## Beispiele

### Beispiel 1: Aktivieren eines Traffic Manager-Profils
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile"
```

Mit diesem Befehl wird das Traffic Manager-Profil mit dem Namen myprofil aktiviert.

### Beispiel 2: Aktivieren eines Traffic Manager-Profils und Anzeigen der Ergebnisse
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

Dieser Befehl aktiviert das Traffic Manager-Profil mit dem Namen myProfile und zeigt an, ob der Befehl erfolgreich war.

## Parameter

### -Name
Gibt den Namen des zu aktivierenden Traffic Manager-Profils an.

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

### -PassThru
Gibt $true zurück, wenn der Vorgang erfolgreich war; andernfalls $false.
Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest. Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

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

### System. Boolean
Dieses Cmdlet generiert $true oder $false.
Wenn der Vorgang erfolgreich ist und Sie den *passthru* -Parameter angeben, gibt dieses Cmdlet den Wert $true zurück.

## Notizen

## Verwandte Links

[Deaktivieren-AzureTrafficManagerProfile](./Disable-AzureTrafficManagerProfile.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Neu – AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[Remove-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)

[Satz-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


