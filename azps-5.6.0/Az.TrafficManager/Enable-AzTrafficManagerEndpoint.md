---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/enable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 5ab6ba03b9803cc8726eff458776f8ee40d48793
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918011"
---
# Enable-AzTrafficManagerEndpoint

## SYNOPSIS
Aktiviert einen Endpunkt in einem Traffic Manager-Profil.

## SYNTAX

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

## BESCHREIBUNG
Das **Cmdlet Enable-AzTrafficManagerEndpoint** ermöglicht einen Endpunkt in einem Azure Traffic Manager-Profil.

Sie können den Pipelineoperator verwenden, um ein **TrafficManagerEndpoint-Objekt** an dieses Cmdlet zu übergeben, oder Sie können ein **TrafficManagerEndpoint-Objekt** mithilfe des *TrafficManagerEndpoint-Parameters* angeben.

Alternativ können Sie den Endpunktnamen und -typ mithilfe der Parameter *Name* und *Typ* zusammen mit den Parametern *ProfileName* und *ResourceGroupName* angeben.

## BEISPIELE

### Beispiel 1: Aktivieren eines Endpunkts aus einem Profil
```
PS C:\>Enable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

Dieser Befehl aktiviert den externen Endpunkt "contoso" im Profil "ContosoProfile" in der Ressourcengruppe ResourceGroup11.

### Beispiel 2: Aktivieren eines Endpunkts mithilfe der Pipeline
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerEndpoint
```

Dieser Befehl ruft den externen Endpunkt namens Contoso aus dem Profil "ContosoProfile" in ResourceGroup11 ab.
Der Befehl übergibt diesen Endpunkt dann mithilfe des Pipelineoperators an das **Enable-AzTrafficManagerEndpoint-Cmdlet.**
Dieses Cmdlet ermöglicht diesen Endpunkt.

## PARAMETER

### -DefaultProfile
Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -ProfileName
Gibt den Namen eines Traffic Manager-Profils an, in dem dieses Cmdlet einen Endpunkt aktiviert.
Verwenden Sie das cmdlet Get-AzTrafficManagerProfile, um ein Profil zu erhalten.

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
Dieses Cmdlet aktiviert einen Traffic Manager-Endpunkt in der Gruppe, die von diesem Parameter angegeben wird.

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
Gibt den Traffic Manager-Endpunkt an, den dieses Cmdlet aktiviert.
Zum Abrufen eines **TrafficManagerEndpoint-Objekts** verwenden Sie das Get-AzTrafficManagerEndpoint Cmdlet.

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

### -Type
Gibt den Endpunkttyp an, den dieses Cmdlet im Traffic Manager-Profil deaktiviert.
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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## AUSGABEN

### System.Boolean

## NOTIZEN

## VERWANDTE LINKS

[Disable-AzTrafficManagerEndpoint](./Disable-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerEndpoint](./Get-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[New-AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerEndpoint](./Remove-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


