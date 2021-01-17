---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 4795e89013acaadcc08477370441ff5acdded85a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382793"
---
# Remove-AzTrafficManagerEndpointConfig

## SYNOPSIS
Entfernt einen Endpunkt aus einem lokalen Traffic Manager-Profilobjekt.

## SYNTAX

```
Remove-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Remove-AzTrafficManagerEndpointConfig"** entfernt einen Endpunkt aus einem lokalen Azure Traffic Manager-Profilobjekt.
Sie können ein Profil mithilfe des cmdlets Get-AzTrafficManagerProfile erhalten.

Dieses Cmdlet wird für das lokale Profilobjekt verwendet.
Sie können Ihre Änderungen am Profil für Traffic Manager mithilfe des cmdlets Set-AzTrafficManagerProfile festlegen.
Verwenden Sie zum Entfernen eines Endpunkts und Zum Commit von Änderungen in einem einzigen Vorgang das Remove-AzTrafficManagerEndpoint Cmdlet.

## BEISPIELE

### Beispiel 1: Entfernen eines Endpunkts
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerEndpointConfig -EndpointName "contoso" -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

Der erste Befehl ruft ein Azure Traffic -Manager-Profil mithilfe des **Cmdlets "Get-AzTrafficManagerProfile"** ab.
Der Befehl speichert das lokale Profil in der $TrafficManagerProfile Variable.

Mit dem zweiten Befehl wird ein Azure-Endpunkt namens "contoso" aus dem Profil entfernt, das in $TrafficManagerProfile.
Mit diesem Befehl wird nur das lokale Objekt geändert.

Der letzte Befehl aktualisiert das Datenverkehrs-Manager-Profil mit dem Namen ContosoProfile so, dass es mit dem lokalen Wert in der $TrafficManagerProfile.

## PARAMETERS

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -EndpointName
Gibt den Namen des Verkehrs-Manager-Endpunkts an, den dieses Cmdlet entfernt.

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
Gibt ein lokales **"TrafficManagerProfile"-Objekt** an.
Dieses Cmdlet ändert dieses lokale Objekt.
Verwenden Sie zum **Abrufen eines TrafficManagerProfile-Objekts** das Get-AzTrafficManagerProfile Cmdlet.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile

## AUSGABEN

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Add-AzTrafficManagerEndpointConfig](./Add-AzTrafficManagerEndpointConfig.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerEndpoint](./Remove-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


