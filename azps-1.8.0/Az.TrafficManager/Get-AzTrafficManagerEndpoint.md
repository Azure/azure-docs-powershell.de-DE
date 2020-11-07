---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 4556C345-55D0-431C-B980-219D5ED14E5F
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/get-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 9ac1bb863053fc322265613a24d90b700d1846cc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658610"
---
# Get-AzTrafficManagerEndpoint

## Synopsis
Ruft einen Endpunkt für ein Traffic Manager-Profil ab.

## Syntax

### Felder
```
Get-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Objekt
```
Get-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzTrafficManagerEndpoint** " Ruft einen Endpunkt für ein Azure Traffic Manager-Profil ab.

Sie können dieses Objekt lokal ändern und dann Änderungen am Profil mithilfe des Set-AzTrafficManagerEndpoint-Cmdlets vornehmen.
Geben Sie den Endpunkt mithilfe der Parameter *Name* und *Type* an.
Sie können das Traffic Manager-Profil entweder mit dem Parameter ProfileName und *ResourceGroupName* oder durch Angeben eines **TrafficManagerProfile** *-Objekts* angeben.
Sie können diesen Wert auch über die Pipeline übergeben.

## Beispiele

### Beispiel 1: Abrufen eines Endpunkts
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

Dieser Befehl ruft den Azure-Endpunkt mit dem Namen "Contoso" aus dem Profil "ContosoProfile" in der Ressourcengruppe "ResourceGroup11" ab und speichert dieses Objekt dann in der $TrafficManagerEndpoint-Variablen.

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

### -Name
Gibt den Namen des Traffic Manager-Endpunkts an, den dieses Cmdlet erhält.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profilname
Gibt den Namen des Traffic Manager-Endpunkts an, den dieses Cmdlet erhält.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe an.
Dieses Cmdlet ruft einen Datenverkehrs-Manager-Endpunkt in der Gruppe ab, die dieser Parameter angibt.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerEndpoint
Gibt den Endpunkt des Datenverkehrs-Managers an, den dieses Cmdlet erhält.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
Parameter Sets: Fields
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint

## Ausgaben

### Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint

## Notizen

## Verwandte Links

[Deaktivieren-AzTrafficManagerEndpoint](./Disable-AzTrafficManagerEndpoint.md)

[Enable-AzTrafficManagerEndpoint](./Enable-AzTrafficManagerEndpoint.md)

[Neu – AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[Remove-AzTrafficManagerEndpoint](./Remove-AzTrafficManagerEndpoint.md)

[Satz-AzTrafficManagerEndpoint](./Set-AzTrafficManagerEndpoint.md)


