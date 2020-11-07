---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/set-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 99f621824d10b574c7f64fb7653bc4154ba6766e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662712"
---
# Set-AzureRmTrafficManagerEndpoint

## Synopsis
Aktualisiert einen Traffic Manager-Endpunkt.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureRmTrafficManagerEndpoint** " aktualisiert einen Endpunkt in Azure Traffic Manager.
Dieses Cmdlet aktualisiert die Einstellungen von einem lokalen Endpunkt Objekt.
Sie können das Endpunkt Objekt entweder mithilfe des *TrafficManagerEndpoint* -Parameters oder mithilfe der Pipeline angeben.

Mithilfe des Get-AzureRmTrafficManagerEndpoint-Cmdlets können Sie ein lokales Objekt abrufen, das einen Endpunkt darstellt.
Ändern Sie das Objekt lokal, und verwenden Sie dann die **Einstellung AzureRmTrafficManagerEndpoint** , um die Änderungen zu übernehmen.

## Beispiele

### Beispiel 1: Aktualisieren eines Endpunkts
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

Der erste Befehl ruft einen Azure Traffic Manager-Endpunkt mit dem Cmdlet **Get-AzureRmTrafficManagerEndpoint** ab.
Der Befehl speichert den Endpunkt lokal in der $TrafficManagerEndpoint-Variablen.

Der zweite Befehl ändert diesen Endpunkt lokal.
Mit diesem Befehl wird die Endpunkt Gewichtung auf 20 geändert.

Der dritte Befehl aktualisiert den Endpunkt im Traffic Manager so, dass er dem lokalen Wert in $TrafficManagerEndpoint entspricht.

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

### -TrafficManagerEndpoint
Gibt ein lokales **TrafficManagerEndpoint** -Objekt an.
Dieses Cmdlet aktualisiert den Datenverkehrs-Manager, um diesem lokalen Objekt zu entsprechen.

```yaml
Type: TrafficManagerEndpoint
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

### Microsoft. Azure. Commands. Network. TrafficManagerEndpoint
Dieses Cmdlet akzeptiert ein **TrafficManagerEndpoint** -Objekt.

## Ausgaben

### Microsoft. Azure. Commands. Network. TrafficManagerEndpoint
Dieses Cmdlet gibt ein **TrafficManagerEndpoint** -Objekt zurück.

## Notizen

## Verwandte Links

