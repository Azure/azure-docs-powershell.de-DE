---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: f40587460cf5e4a1d7f06bfb88229f6e4e3f7975
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93827068"
---
# Remove-AzTrafficManagerEndpointConfig

## Synopsis
Entfernt einen Endpunkt aus einem lokalen Traffic Manager-Profilobjekt.

## Syntax

```
Remove-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzTrafficManagerEndpointConfig** entfernt einen Endpunkt aus einem lokalen Azure Traffic Manager-Profilobjekt.
Sie können ein Profil mithilfe des Get-AzTrafficManagerProfile-Cmdlets abrufen.

Dieses Cmdlet funktioniert für das lokale Profilobjekt.
Übernehmen Sie Ihre Änderungen mithilfe des Set-AzTrafficManagerProfile-Cmdlets an das Profil für Traffic Manager.
Verwenden Sie das Remove-AzTrafficManagerEndpoint-Cmdlet, um einen Endpunkt zu entfernen und Änderungen in einem einzelnen Vorgang zu übernehmen.

## Beispiele

### Beispiel 1: Entfernen eines Endpunkts
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerEndpointConfig -EndpointName "contoso" -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

Der erste Befehl ruft ein Azure Traffic Manager-Profil mit dem Cmdlet **Get-AzTrafficManagerProfile** ab.
Der Befehl speichert das lokale Profil in der $TrafficManagerProfile Variablen.

Der zweite Befehl entfernt einen Azure-Endpunkt namens Contoso aus dem Profil, das in $TrafficManagerProfile gespeichert ist.
Mit diesem Befehl wird nur das lokale Objekt geändert.

Der endgültige Befehl aktualisiert das Traffic Manager-Profil mit dem Namen ContosoProfile so, dass es dem lokalen Wert in $TrafficManagerProfile entspricht.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Endpunktname
Gibt den Namen des Traffic Manager-Endpunkts an, den dieses Cmdlet entfernt.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerProfile
Gibt ein lokales **TrafficManagerProfile** -Objekt an.
Dieses Cmdlet ändert dieses lokale Objekt.
Verwenden Sie das Get-AzTrafficManagerProfile-Cmdlet, um ein **TrafficManagerProfile** -Objekt zu erhalten.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
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

### Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile

## Ausgaben

### Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile

## Notizen

## Verwandte Links

[Add-AzTrafficManagerEndpointConfig](./Add-AzTrafficManagerEndpointConfig.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerEndpoint](./Remove-AzTrafficManagerEndpoint.md)

[Satz-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


