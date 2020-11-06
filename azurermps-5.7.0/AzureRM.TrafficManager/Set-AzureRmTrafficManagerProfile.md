---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/set-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 58811a34a2f3d2b4684813c42723a5cab354a13f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501306"
---
# Set-AzureRmTrafficManagerProfile

## Synopsis
Aktualisiert ein Traffic Manager-Profil.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Set-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureRmTrafficManagerProfile** " aktualisiert ein Azure Traffic Manager-Profil.
Dieses Cmdlet aktualisiert die Einstellungen des Profils von einem lokalen Profilobjekt.
Sie können das Profilobjekt entweder mithilfe des *TrafficManagerProfile* -Parameters oder mithilfe der Pipeline angeben.

Sie können ein lokales Objekt, das ein Profil darstellt, mithilfe des Get-AzureRmTrafficManagerProfile-Cmdlets abrufen.
Ändern Sie das Objekt lokal, und verwenden Sie dann die **Einstellung AzureRmTrafficManagerProfile** , um die Änderungen zu übernehmen.

## Beispiele

### Beispiel 1: Aktualisieren eines Profils
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

Der erste Befehl ruft ein Azure Traffic Manager-Profil mithilfe des Get-AzureRmTrafficManagerProfile-Cmdlets ab.
Der Befehl speichert das Profil lokal in der $TrafficManagerProfile-Variablen.

Der zweite Befehl ändert das Profil lokal.
Mit diesem Befehl wird das Profil deaktiviert.

Der dritte Befehl aktualisiert das Traffic Manager-Profil mit dem Namen ContosoProfile so, dass es dem lokalen Wert in $TrafficManagerProfile entspricht.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerProfile
Gibt ein lokales **TrafficManagerProfile** -Objekt an.
Dieses Cmdlet aktualisiert den Datenverkehrs-Manager, um diesem lokalen Objekt zu entsprechen.

```yaml
Type: TrafficManagerProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. Network. TrafficManagerProfile
Dieses Cmdlet akzeptiert ein **TrafficManagerProfile** -Objekt.

## Ausgaben

### Microsoft. Azure. Commands. Network. TrafficManagerProfile
Dieses Cmdlet gibt ein **TrafficManagerProfile** -Objekt zurück.

## Notizen

## Verwandte Links

[Add-AzureRmTrafficManagerEndpointConfig](./Add-AzureRmTrafficManagerEndpointConfig.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerProfile.md)

[Neu – AzureRmTrafficManagerProfile](./New-AzureRmTrafficManagerProfile.md)

[Remove-AzureRmTrafficManagerEndpointConfig](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[Remove-AzureRmTrafficManagerProfile](./Remove-AzureRmTrafficManagerProfile.md)


