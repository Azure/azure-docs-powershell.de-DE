---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/disable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
ms.openlocfilehash: 4d667b1435a7396082f0626d8f55882f7c37b8ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918019"
---
# Disable-AzTrafficManagerProfile

## SYNOPSIS
Deaktiviert ein Traffic Manager-Profil.

## SYNTAX

### Felder
```
Disable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objekt
```
Disable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Disable-AzTrafficManagerProfile** deaktiviert ein Azure Traffic Manager-Profil.
Sie können das Profilobjekt mithilfe der Pipeline oder als Parameterwert angeben.
Alternativ können Sie das Profil mithilfe der Parameter *Name* und *ResourceGroupName* angeben.

## BEISPIELE

### Beispiel 1: Deaktivieren eines profils, das nach Name angegeben ist
```
PS C:\>Disable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

Mit diesem Befehl wird das Profil contosoProfile in ResourceGroup11 deaktiviert.
Der Befehl fordert Sie zur Bestätigung auf.

### Beispiel 2: Deaktivieren eines Profils mithilfe der Pipeline
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerProfile -Force
```

Dieser Befehl ruft das Profil "ContosoProfile" in "ResourceGroup11" ab.
Der Befehl übergibt dieses Profil dann mithilfe des Pipelineoperators an das **Cmdlet Disable-AzTrafficManagerProfile.**
Dieses Cmdlet deaktiviert dieses Profil.
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
Gibt den Namen des Traffic Manager-Profils an, das von diesem Cmdlet deaktiviert wird.

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
Dieses Cmdlet deaktiviert ein Traffic Manager-Profil in der Gruppe, die von diesem Parameter angegeben wird.

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

### -TrafficManagerProfile
Gibt ein **TrafficManagerProfile-Objekt an,** das deaktiviert werden soll.
Zum Abrufen eines **TrafficManagerProfile-Objekts** verwenden Sie das Get-AzTrafficManagerProfile Cmdlet.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile

## AUSGABEN

### System.Boolean

## NOTIZEN

## VERWANDTE LINKS

[Enable-AzTrafficManagerProfile](./Enable-AzTrafficManagerProfile.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerProfile](./Remove-AzTrafficManagerProfile.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


