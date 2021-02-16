---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 0000a7a1dba5f175d70fb93631176a49a9da2d13
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149801"
---
# Set-AzTrafficManagerEndpoint

## SYNOPSIS
Aktualisiert einen Datenverkehrs-Manager-Endpunkt.

## SYNTAX

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Set-AzTrafficManagerEndpoint"** aktualisiert einen Endpunkt in Azure Traffic Manager.
Dieses Cmdlet aktualisiert die Einstellungen eines lokalen Endpunktobjekts.
Sie können das Endpunktobjekt entweder mithilfe des *Parameters "TrafficManagerEndpoint"* oder mithilfe der Pipeline angeben.

Sie können ein lokales Objekt, das einen Endpunkt darstellt, mithilfe des Get-AzTrafficManagerEndpoint abrufen.
Ändern Sie das Objekt lokal, und verwenden Sie **dann "Set-AzTrafficManagerEndpoint",** um Ihre Änderungen zu commiten.

## BEISPIELE

### Beispiel 1: Aktualisieren eines Endpunkts
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

Der erste Befehl ruft einen Azure Traffic -Manager-Endpunkt mithilfe des **Cmdlets "Get-AzTrafficManagerEndpoint"** ab.
Der Befehl speichert den Endpunkt lokal in der $TrafficManagerEndpoint Variable.

Der zweite Befehl ändert diesen Endpunkt lokal.
Mit diesem Befehl wird die Endpunktgewichtung in "20" geändert.

Mit dem dritten Befehl wird der Endpunkt im Verkehrs-Manager so aktualisiert, dass er dem lokalen Wert in der $TrafficManagerEndpoint.

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

### -TrafficManagerEndpoint
Gibt ein lokales **TrafficManagerEndpoint-Objekt** an.
Mit diesem Cmdlet wird der Datenverkehrs-Manager so aktualisiert, dass er diesem lokalen Objekt entsprechen kann.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## AUSGABEN

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
