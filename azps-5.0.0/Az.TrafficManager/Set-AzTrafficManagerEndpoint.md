---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 0000a7a1dba5f175d70fb93631176a49a9da2d13
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180142"
---
# Set-AzTrafficManagerEndpoint

## Synopsis
Aktualisiert einen Traffic Manager-Endpunkt.

## Syntax

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzTrafficManagerEndpoint** " aktualisiert einen Endpunkt in Azure Traffic Manager.
Dieses Cmdlet aktualisiert die Einstellungen von einem lokalen Endpunkt Objekt.
Sie können das Endpunkt Objekt entweder mithilfe des *TrafficManagerEndpoint* -Parameters oder mithilfe der Pipeline angeben.

Mithilfe des Get-AzTrafficManagerEndpoint-Cmdlets können Sie ein lokales Objekt abrufen, das einen Endpunkt darstellt.
Ändern Sie das Objekt lokal, und verwenden Sie dann die **Einstellung AzTrafficManagerEndpoint** , um die Änderungen zu übernehmen.

## Beispiele

### Beispiel 1: Aktualisieren eines Endpunkts
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

Der erste Befehl ruft einen Azure Traffic Manager-Endpunkt mit dem Cmdlet **Get-AzTrafficManagerEndpoint** ab.
Der Befehl speichert den Endpunkt lokal in der $TrafficManagerEndpoint-Variablen.

Der zweite Befehl ändert diesen Endpunkt lokal.
Mit diesem Befehl wird die Endpunkt Gewichtung auf 20 geändert.

Der dritte Befehl aktualisiert den Endpunkt im Traffic Manager so, dass er dem lokalen Wert in $TrafficManagerEndpoint entspricht.

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

### -TrafficManagerEndpoint
Gibt ein lokales **TrafficManagerEndpoint** -Objekt an.
Dieses Cmdlet aktualisiert den Datenverkehrs-Manager, um diesem lokalen Objekt zu entsprechen.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint

## Ausgaben

### Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint

## Notizen

## Verwandte Links
