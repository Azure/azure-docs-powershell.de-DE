---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
ms.openlocfilehash: e0702c8893aad7f82de5de5681d8cc14da0b3681
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823875"
---
# Disable-AzTrafficManagerProfile

## Synopsis
Deaktiviert ein Traffic Manager-Profil.

## Syntax

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

## Beschreibung
Das Cmdlet **Disable-AzTrafficManagerProfile** deaktiviert ein Azure Traffic Manager-Profil.
Sie können das Profilobjekt mithilfe der Pipeline oder als Parameterwert angeben.
Alternativ können Sie das Profil mithilfe der Parameter *Name* und *ResourceGroupName* angeben.

## Beispiele

### Beispiel 1: Deaktivieren eines durch den Namen angegebenen Profils
```
PS C:\>Disable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

Dieser Befehl deaktiviert das Profil mit dem Namen ContosoProfile in ResourceGroup11.
Der Befehl fordert Sie zur Bestätigung auf.

### Beispiel 2: Deaktivieren eines Profils mithilfe der Pipeline
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerProfile -Force
```

Dieser Befehl ruft das Profil mit dem Namen ContosoProfile in ResourceGroup11 ab.
Der Befehl übergibt dann dieses Profil mithilfe des Pipelineoperators an das Cmdlet **Disable-AzTrafficManagerProfile** .
Dieses Cmdlet deaktiviert dieses Profil.
Der Befehl gibt den Parameter *Force* an.
Daher werden Sie nicht zur Bestätigung aufgefordert.

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

### -Force
Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.

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
Mit diesem Cmdlet wird ein Datenverkehrs-Manager-Profil in der Gruppe deaktiviert, die dieser Parameter angibt.

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
Gibt ein zu deaktivierenden **TrafficManagerProfile** -Objekt an.
Verwenden Sie das Get-AzTrafficManagerProfile-Cmdlet, um ein **TrafficManagerProfile** -Objekt zu erhalten.

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
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

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
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile

## Ausgaben

### System. Boolean

## Notizen

## Verwandte Links

[Enable-AzTrafficManagerProfile](./Enable-AzTrafficManagerProfile.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[Neu – AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerProfile](./Remove-AzTrafficManagerProfile.md)

[Satz-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


