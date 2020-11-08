---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: B96A64DD-9005-4B04-A720-6FCF33797E8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1fa73aa4e38c8d222da6e73508e9a18a15c1e3f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006297"
---
# Remove-AzureTrafficManagerProfile

## Synopsis
Entfernt ein Traffic Manager-Profil.

## Syntax

```
Remove-AzureTrafficManagerProfile -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureTrafficManagerProfile** entfernt ein Microsoft Azure Traffic Manager-Profil aus dem aktuellen Abonnement.

## Beispiele

### Beispiel 1: Entfernen eines Traffic Manager-Profils
```
PS C:\>Remove-AzureTrafficManagerProfile -Name "MyProfile"
```

Mit diesem Befehl wird das Traffic Manager-Profil mit dem Namen myprofil entfernt.

### Beispiel 2: Entfernen eines Traffic Manager-Profils
```
PS C:\>Remove-AzureTrafficManagerProfile -Name "MyProfile" -Force -PassThru
```

Mit diesem Befehl wird das Traffic Manager-Profil mit dem Namen myprofil entfernt, ohne dass Sie zur Bestätigung aufgefordert werden, und die Ergebnisse werden zurückgegeben.

## Parameter

### -Force
Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.

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

### -Name
Gibt den Namen des zu löschenden Traffic Manager-Profils an.

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

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Neu – AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[Satz-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


