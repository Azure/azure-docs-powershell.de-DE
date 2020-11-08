---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: ECE9C2A6-7DA2-4477-B877-9970FBE26D7C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8f378cbf8926a650699ec50a2a0a42873dcb7528
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005899"
---
# Disable-AzureTrafficManagerProfile

## Synopsis
Deaktiviert ein Traffic Manager-Profil.

## Syntax

```
Disable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Disable-AzureTrafficManagerProfile** deaktiviert ein Microsoft Azure Traffic Manager-Profil.
Sie können den *passthru* -Parameter verwenden, um anzuzeigen, ob der Vorgang erfolgreich ausgeführt wurde.

## Beispiele

### Beispiel 1: Deaktivieren eines Traffic Manager-Profils und Anzeigen der Ergebnisse
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

Mit diesem Befehl wird das Traffic Manager-Profil mit dem Namen myprofil deaktiviert.
Der Befehl gibt den *passthru* -Parameter an, um anzuzeigen, ob der Befehl erfolgreich war.

### Beispiel 2: Deaktivieren eines Traffic Manager-Profils und Anzeigen von Ergebnissen
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile"
```

Dieser Befehl deaktiviert das Traffic Manager-Profil mit dem Namen "Mein Profil", zeigt aber nicht an, ob der Befehl erfolgreich war.

## Parameter

### -Name
Gibt den Namen des zu deaktivierenden Traffic Manager-Profils an.

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

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Neu – AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[Remove-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)

[Satz-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


