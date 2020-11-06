---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurermtrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: 3c77ca67999ffa9cecbe35de4d4533f5d163f17f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504234"
---
# Add-AzureRmTrafficManagerEndpointConfig

## Synopsis
Fügt einen Endpunkt zu einem lokalen Traffic Manager-Profilobjekt hinzu.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Add-AzureRmTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Add-AzureRmTrafficManagerEndpointConfig** wird ein Endpunkt zu einem lokalen Azure Traffic Manager-Profilobjekt hinzugefügt.
Sie können ein Profil mithilfe der Cmdlets New-AzureRmTrafficManagerProfile oder Get-AzureRmTrafficManagerProfile abrufen.

Dieses Cmdlet funktioniert für das lokale Profilobjekt.
Übernehmen Sie Ihre Änderungen mithilfe des Set-AzureRmTrafficManagerProfile-Cmdlets an das Profil für Traffic Manager.
Verwenden Sie das New-AzureRmTrafficManagerEndpoint-Cmdlet, um einen Endpunkt zu erstellen und die Änderung in einem einzelnen Vorgang zu übernehmen.

## Beispiele

### Beispiel 1: Hinzufügen eines Endpunkts zu einem Profil
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

Der erste Befehl ruft ein Azure Traffic Manager-Profil mit dem Cmdlet **Get-AzureRmTrafficManagerProfile** ab.
Der Befehl speichert das lokale Profil in der $TrafficManagerProfile Variablen.

Der zweite Befehl fügt dem in $TrafficManagerProfile gespeicherten Profil einen Endpunkt mit dem Namen "Contoso" hinzu.
Der Befehl enthält Konfigurationsdaten für den Endpunkt.
Mit diesem Befehl wird nur das lokale Objekt geändert.

Der endgültige Befehl aktualisiert das Traffic Manager-Profil in Azure so, dass es dem lokalen Wert in $TrafficManagerProfile entspricht.

## Parameter

### -CustomHeader
Liste der benutzerdefinierten Headername-und Wert-Paare für Prüf Punkt Anforderungen

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndpointLocation
Gibt die Position des Endpunkts an, der in der Performance Traffic-Routing-Methode verwendet werden soll.
Dieser Parameter ist nur für Endpunkte der ExternalEndpoints oder des NestedEndpoints-Typs anwendbar.
Sie müssen diesen Parameter angeben, wenn die Methode zur Datenverkehrs Weiterleitung verwendet wird.

Geben Sie den Namen eines Azure-Bereichs an.
Eine vollständige Liste der Azure-Bereiche finden Sie unter Azure-Bereiche https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Endpunktname
Gibt den Namen des vom Cmdlet hinzugefügten Traffic Manager-Endpunkts an.

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

### -EndpointStatus
Gibt den Status des Endpunkts an.
Gültige Werte sind: 

- Aktiviert 
- Deaktiviert 

Wenn der Status aktiviert ist, wird der Endpunkt nach Endpunkt Integrität untersucht und in die Datenverkehrs Routingmethode einbezogen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Geomapping
Die Liste der Regionen, die diesem Endpunkt zugeordnet sind, wenn die "geographische" Verkehrs Routingmethode verwendet wird. Eine [vollständige Liste der akzeptierten Werte](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions)finden Sie in der Dokumentation des Traffic-Managers.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinChildEndpoints
Die Mindestanzahl von Endpunkten, die im untergeordneten Profil verfügbar sein müssen, damit der geschachtelte Endpunkt im übergeordneten Profil als verfügbar betrachtet werden kann.
Gilt nur für den Endpunkt des Typs "NestedEndpoints".

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Priorität
Gibt die Priorität an, die der Datenverkehrs-Manager dem Endpunkt zuweist.
Dieser Parameter wird nur verwendet, wenn das Traffic Manager-Profil mit der für Priority-Datenverkehrs Routing-Methode konfiguriert ist.
Gültige Werte sind ganze Zahlen von 1 bis 1000.
Niedrigere Werte stellen eine höhere Priorität dar.

Wenn Sie eine Priorität angeben, müssen Sie Prioritäten für alle Endpunkte im Profil angeben, und keine zwei Endpunkte können denselben Prioritätswert aufweisen.
Wenn Sie keine Prioritäten angeben, weist der Datenverkehrs-Manager den Endpunkten Standard Prioritätswerte zu, beginnend mit einem (1), in der Reihenfolge, in der das Profil die Endpunkte aufführt.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetMapping
Die Liste der Adressbereiche oder Subnetze, die diesem Endpunkt zugeordnet sind, wenn Sie die ̃Subnetâ €™ Traffic-Routingmethode verwenden.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Target
Gibt den vollqualifizierten DNS-Namen des Endpunkts an.
Traffic Manager gibt diesen Wert in DNS-Antworten zurück, wenn der Datenverkehr an diesen Endpunkt weitergeleitet wird.
Geben Sie diesen Parameter nur für den ExternalEndpoints-Endpunkttyp an.
Geben Sie bei anderen Endpunkttypen stattdessen den *TargetResourceId* -Parameter an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetResourceId
Gibt die Ressourcen-ID des Ziels an.
Geben Sie diesen Parameter nur für die AzureEndpoints-und NestedEndpoints-Endpunkttypen an.
Geben Sie für den ExternalEndpoints-Endpunkttyp stattdessen den *target* -Parameter an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerProfile
Gibt ein lokales **TrafficManagerProfile** -Objekt an.
Dieses Cmdlet ändert dieses lokale Objekt.
Verwenden Sie das Get-AzureRmTrafficManagerProfile-Cmdlet, um ein **TrafficManagerProfile** -Objekt zu erhalten.

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

### -Typ
Gibt den Typ des Endpunkts an, der vom Cmdlet zum Azure Traffic Manager-Profil hinzugefügt wird.
Gültige Werte sind: 

- AzureEndpoints
- ExternalEndpoints
- NestedEndpoints

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Gewicht
Gibt die Gewichtung an, die der Datenverkehrs-Manager dem Endpunkt zuweist.
Gültige Werte sind ganze Zahlen von 1 bis 1000.
Der Standardwert ist eins (1).
Dieser Parameter wird nur verwendet, wenn das Traffic Manager-Profil mit der gewichteten Traffic-Routing-Methode konfiguriert ist.

```yaml
Type: System.Nullable`1[System.UInt32]
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

### Microsoft. Azure. Commands. Network. TrafficManagerProfile
Dieses Cmdlet akzeptiert ein **TrafficManagerProfile** -Objekt für dieses Cmdlet.

## Ausgaben

### Microsoft. Azure. Commands. Network. TrafficManagerProfile
Dieses Cmdlet gibt ein geändertes **TrafficManagerProfile** -Objekt zurück.

## Notizen

## Verwandte Links

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerProfile.md)

[Neu – AzureRmTrafficManagerEndpoint](./New-AzureRmTrafficManagerEndpoint.md)

[Remove-AzureRmTrafficManagerEndpointConfig](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[Satz-AzureRmTrafficManagerProfile](./Set-AzureRmTrafficManagerProfile.md)


