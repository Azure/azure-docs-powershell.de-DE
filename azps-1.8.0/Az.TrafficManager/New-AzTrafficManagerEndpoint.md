---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 007fb7a309b9dd305f58d2f947d3d2dfc55078e6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658608"
---
# New-AzTrafficManagerEndpoint

## Synopsis
Erstellt einen Endpunkt in einem Traffic Manager-Profil.

## Syntax

```
New-AzTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String> -Type <String>
 [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzTrafficManagerEndpoint** erstellt einen Endpunkt in einem Azure Traffic Manager-Profil.

Dieses Cmdlet übergibt jeden neuen Endpunkt an den Traffic Manager-Dienst.
Verwenden Sie das Add-AzTrafficManagerEndpointConfig-Cmdlet, um mehrere Endpunkte zu einem lokalen Traffic Manager-Profilobjekt hinzuzufügen und Änderungen in einem einzelnen Vorgang zu übernehmen.

## Beispiele

### Beispiel 1: Erstellen eines externen Endpunkts für ein Profil
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

Dieser Befehl erstellt einen externen Endpunkt mit dem Namen "Contoso" im Profil "ContosoProfile" in der Ressourcengruppe mit dem Namen ResourceGroup11.

### Beispiel 2: Erstellen eines Azure-Endpunkts für ein Profil
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

Dieser Befehl erstellt einen Azure-Endpunkt mit dem Namen "Contoso" im Profil "ContosoProfile" in der Ressourcengruppen-ResouceGroup11.
Der Azure-Endpunkt verweist auf die Azure Web App, deren Azure Resource Manager-ID durch den URI-Pfad in *TargetResourceId* angegeben wird.
Der Befehl gibt keinen *EndpointLocation* -Parameter an, weil die Web App-Ressource den Speicherort bereitstellt.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndpointLocation
Gibt die Position des Endpunkts an, der in der Performance Traffic-Routing-Methode verwendet werden soll.
Dieser Parameter ist nur auf Endpunkte des ExternalEndpoints-oder NestedEndpoints-Typs anwendbar.
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
Die Liste der Regionen, die diesem Endpunkt zugeordnet sind, wenn die "geographische" Verkehrs Routingmethode verwendet wird. Eine vollständige Liste der akzeptierten Werte finden Sie in der Dokumentation des Traffic-Managers.

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
Geben Sie den Namen eines Azure-Bereichs an.
Eine vollständige Liste der Azure-Bereiche finden Sie unter Azure-Bereiche https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .

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

### -Name
Gibt den Namen des vom Cmdlet erstellten Traffic Manager-Endpunkts an.

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

### -Profilname
Gibt den Namen eines Traffic Manager-Profils an, dem dieses Cmdlet einen Endpunkt hinzufügt.
Verwenden Sie zum Abrufen eines Profils die New-AzTrafficManagerProfile-oder Get-AzTrafficManagerProfile-Cmdlets.

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

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe an.
Dieses Cmdlet erstellt einen Datenverkehrs-Manager-Endpunkt in der Gruppe, die dieser Parameter angibt.

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

### -Typ
Gibt den Typ des Endpunkts an, der vom Cmdlet zum Traffic Manager-Profil hinzugefügt wird.
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

### Keine

## Ausgaben

### Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint

## Notizen

## Verwandte Links

[Deaktivieren-AzTrafficManagerEndpoint](./Disable-AzTrafficManagerEndpoint.md)

[Enable-AzTrafficManagerEndpoint](./Enable-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerEndpoint](./Get-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[Neu – AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerEndpoint](./Remove-AzTrafficManagerEndpoint.md)

[Satz-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


