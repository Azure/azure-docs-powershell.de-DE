---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 28136DC3-520B-4134-8736-93D86EEABAE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf9fd7b67b63ce2bddb762c7006722b6035ffe87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005742"
---
# Get-AzureTrafficManagerProfile

## Synopsis
Ruft die Details eines Traffic Manager-Profils ab.

## Syntax

```
Get-AzureTrafficManagerProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureTrafficManagerProfile** " Ruft die Details eines Microsoft Azure Traffic Manager-Profils ab.
Wenn Sie den Parameter *Name* nicht angeben, listet das Cmdlet die Datenverkehrs-Manager-Profile im aktuellen Abonnement auf.

## Beispiele

### Beispiel 1: Abrufen der Liste der Datenverkehrs-Manager-Profile in einem Abonnement
```
PS C:\>Get-AzureTrafficManagerProfile
```

Dieser Befehl ruft die Liste der Datenverkehrs-Manager-Profile in Ihrem Abonnement ab.

### Beispiel 2: Abrufen eines Traffic Manager-Profils
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile"
```

Dieser Befehl ruft das Traffic Manager-Profil mit dem Namen "myProfile" ab.

### Beispiel 3: Hinzufügen eines Endpunkts zu einem Traffic Manager-Profil
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Add-AzureTrafficManagerEndpoint -DomainName "Myapp2.cloudapp.net" -TrafficManagerProfile $MyTrafficManagerProfile -Type "CloudService" -Status "Enabled" | Set-AzureTrafficManagerProfile
```

Mit diesem Befehl wird ein Endpunkt zu einem Traffic Manager-Profil hinzugefügt und dann das Profil gespeichert.

## Parameter

### -Name
Gibt den Namen des abzurufenden Traffic Manager-Profils an.

```yaml
Type: String
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

### Microsoft. WindowsAzure. Commands. Utilities. Trafficmanager. Models. IProfileWithDefinition
Dieses Cmdlet generiert ein Profilobjekt oder Objekte des Datenverkehrs-Managers.

## Notizen

## Verwandte Links

[Add-AzureTrafficManagerEndpoint](./Add-AzureTrafficManagerEndpoint.md)

[Deaktivieren-AzureTrafficManagerProfile](./Disable-AzureTrafficManagerProfile.md)

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[Neu – AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[Remove-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)

[Satz-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


