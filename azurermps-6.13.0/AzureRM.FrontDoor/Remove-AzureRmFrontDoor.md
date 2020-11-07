---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/remove-azurermfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoor.md
ms.openlocfilehash: 8eae5034080bd1035cfe7e8331ca015820688e63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662175"
---
# Remove-AzureRmFrontDoor

## Synopsis
Entfernen des Front-Load-Balancer

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ByFieldsParameterSet (Standard)
```
Remove-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObjectParameterSet
```
Remove-AzureRmFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdParameterSet
```
Remove-AzureRmFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Remove-AzureRmFrontDoor** wird ein Front-Door Load Balancer unter dem aktuellen Abonnement entfernt

## Beispiele

### Beispiel 1: Entfernen Sie "frontdoor1" in der Ressourcengruppe "RG1" unter dem aktuellen Abonnement.
```powershell
PS C:\> Remove-AzureRmFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

Entfernen Sie "frontdoor1" in der Ressourcengruppe "RG1" unter dem aktuellen Abonnement.

### Beispiel 2: Entfernen Sie alle FrontDoors in der Ressourcengruppe "RG1" unter dem aktuellen Abonnement.
```powershell
PS C:\> Get-AzureRmFrontDoor -ResourceGroupName "rg1" | Remove-AzureRmFrontDoor
```

Entfernen Sie alle FrontDoors in der Ressourcengruppe "RG1" unter dem aktuellen Abonnement.

### Beispiel 3: Entfernen aller FrontDoors unter dem aktuellen Abonnement.
```powershell
PS C:\> Get-AzureRmFrontDoor | Remove-AzureRmFrontDoor
```

Entfernen Sie alle FrontDoors unter dem aktuellen Abonnement.

### Beispiel 4: Entfernen Sie alle FrontDoors mit dem Namen "frontdoor1" unter dem aktuellen Abonnement.
```powershell
PS C:\> Remove-AzureRmFrontDoor -Name "frontdoor1" | Remove-AzureRmFrontDoor
```

Entfernen Sie alle FrontDoors mit dem Namen "frontdoor1" unter dem aktuellen Abonnement.

## Parameter

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

### -Inputobject
Das zu löschende Haustür Objekt.

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Der Name der zu löschenden Haustür.

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Objekt zurückgeben (sofern angegeben).

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

### -ResourceGroupName
Die Ressourcengruppe, zu der die Haustür gehört.

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Resourcen-Nr
Ressourcen-ID der zu löschenden Haustür

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. Haustür. Models. PSFrontDoor

### System. String

### System. Management. Automation. Switchparameter

## Ausgaben

### System. Boolean

## Notizen

## Verwandte Links

[Neu – AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)
