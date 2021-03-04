---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/disable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: e14f74af1c8e50ddc5bc3281fca71b1e2d740e3b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918016"
---
# Disable-AzTrafficManagerEndpoint

## SYNOPSIS
Deaktiviert einen Endpunkt in einem Traffic Manager-Profil.

## SYNTAX

### Felder
```
Disable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Objekt
```
Disable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Disable-AzTrafficManagerEndpoint** deaktiviert einen Endpunkt in einem Azure Traffic Manager-Profil.

Sie können den Pipelineoperator verwenden, um ein **TrafficManagerEndpoint-Objekt** an dieses Cmdlet zu übergeben, oder Sie können ein **TrafficManagerEndpoint-Objekt** mit dem *Parameter TrafficManagerEndpoint* übergeben.

Alternativ können Sie den Endpunktnamen und -typ mithilfe der Parameter *Name* und *Typ* zusammen mit den Parametern *ProfileName* und *ResourceGroupName* angeben.

## BEISPIELE

### Beispiel 1: Deaktivieren eines Endpunkts nach Name
```
PS C:\> Disable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

Mit diesem Befehl wird der externe Endpunkt contoso im Profil "ContosoProfile" in der Ressourcengruppe ResourceGroup11 deaktiviert.
Der Befehl fordert Sie zur Bestätigung auf.

### Beispiel 2: Deaktivieren eines Endpunkts mithilfe der Pipeline
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerEndpoint -Force
```

Dieser Befehl ruft den externen Endpunkt namens Contoso aus dem Profil "ContosoProfile" in ResourceGroup11 ab.
Der Befehl übergibt diesen Endpunkt dann mithilfe des Pipelineoperators an das **Cmdlet Disable-AzTrafficManagerEndpoint.**
Dieses Cmdlet deaktiviert diesen Endpunkt.
Der Befehl gibt den Parameter *"Erzwingen"* an.
Daher werden Sie nicht zur Bestätigung aufgefordert.

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

### -Erzwingen
Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen des Traffic Manager-Endpunkts an, den dieses Cmdlet deaktiviert.

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
Gibt den Namen eines Traffic Manager-Profils an, in dem dieses Cmdlet einen Endpunkt deaktiviert.
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
Dieses Cmdlet deaktiviert einen Traffic Manager-Endpunkt in der Gruppe, die von diesem Parameter angegeben wird.

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
Gibt den Traffic Manager-Endpunkt an, den dieses Cmdlet deaktiviert.
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
Gibt den Endpunkttyp an, den dieses Cmdlet dem Traffic Manager-Profil hinzufügt.
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

### -Bestätigen
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
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

[Enable-AzTrafficManagerEndpoint](./Enable-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerEndpoint](./Get-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[New-AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerEndpoint](./Remove-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


