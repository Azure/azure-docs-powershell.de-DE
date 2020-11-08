---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 5d7ef8e2fd778b5bcaaea1413bddd85eceb0582c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009526"
---
# Enable-AzTrafficManagerEndpoint

## Synopsis
Aktiviert einen Endpunkt in einem Traffic Manager-Profil.

## Syntax

### Felder
```
Enable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Objekt
```
Enable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **enable-AzTrafficManagerEndpoint** aktiviert einen Endpunkt in einem Azure Traffic Manager-Profil.

Sie können den Pipelineoperator verwenden, um ein **TrafficManagerEndpoint** -Objekt an dieses Cmdlet zu übergeben, oder Sie können mithilfe des *TrafficManagerEndpoint* -Parameters ein **TrafficManagerEndpoint** -Objekt angeben.

Sie können auch den Endpunktnamen und-Typ angeben, indem Sie die Parameter *Name* und *Type* zusammen mit den Parametern *Profilname* und *ResourceGroupName* verwenden.

## Beispiele

### Beispiel 1: Aktivieren eines Endpunkts aus einem Profil
```
PS C:\>Enable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

Dieser Befehl aktiviert den externen Endpunkt mit dem Namen "Contoso" im Profil "ContosoProfile" in der Ressourcengruppe ResourceGroup11.

### Beispiel 2: Aktivieren eines Endpunkts mithilfe der Pipeline
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerEndpoint
```

Dieser Befehl ruft den externen Endpunkt mit dem Namen "Contoso" aus dem Profil "ContosoProfile" in ResourceGroup11 ab.
Der Befehl übergibt diesen Endpunkt dann mithilfe des Pipelineoperators an das Cmdlet **enable-AzTrafficManagerEndpoint** .
Dieses Cmdlet aktiviert diesen Endpunkt.

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
Gibt den Namen des Traffic Manager-Endpunkts an, den dieses Cmdlet aktiviert.

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
Gibt den Namen eines Traffic Manager-Profils an, in dem dieses Cmdlet einen Endpunkt aktiviert.
Verwenden Sie das Get-AzTrafficManagerProfile-Cmdlet, um ein Profil zu erhalten.

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
Dieses Cmdlet aktiviert einen Datenverkehrs-Manager-Endpunkt in der Gruppe, den dieser Parameter angibt.

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
Gibt den Endpunkt des Datenverkehrs-Managers an, den dieses Cmdlet aktiviert.
Verwenden Sie das Get-AzTrafficManagerEndpoint-Cmdlet, um ein **TrafficManagerEndpoint** -Objekt zu erhalten.

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
Gibt den Typ des Endpunkts an, den dieses Cmdlet im Traffic Manager-Profil deaktiviert.
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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint

## Ausgaben

### System. Boolean

## Notizen

## Verwandte Links

[Deaktivieren-AzTrafficManagerEndpoint](./Disable-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerEndpoint](./Get-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[Neu – AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[Neu – AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerEndpoint](./Remove-AzTrafficManagerEndpoint.md)

[Satz-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


