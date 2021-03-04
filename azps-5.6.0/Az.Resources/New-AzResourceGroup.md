---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
ms.openlocfilehash: e32d5f53b13b26a93f23e4e557c6bad20911a776
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946920"
---
# New-AzResourceGroup

## SYNOPSIS
Erstellt eine Azure-Ressourcengruppe.

## SYNTAX

```
New-AzResourceGroup [-Name] <String> [-Location] <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet New-AzResourceGroup** erstellt eine Azure-Ressourcengruppe.
Sie können eine Ressourcengruppe erstellen, indem Sie nur einen Namen und einen Speicherort verwenden und dann das cmdlet New-AzResource verwenden, um Ressourcen zu erstellen, die der Ressourcengruppe hinzugefügt werden.
Zum Hinzufügen einer Bereitstellung zu einer vorhandenen Ressourcengruppe verwenden Sie das New-AzResourceGroupDeployment Cmdlet. Wenn Sie einer vorhandenen Ressourcengruppe eine Ressource hinzufügen möchten, verwenden Sie das **Cmdlet New-AzResource.** Eine Azure-Ressource ist eine vom Benutzer verwaltete Azure-Entität, z. B. ein Datenbankserver, eine Datenbank oder eine Website. Eine Azure-Ressourcengruppe ist eine Sammlung von Azure-Ressourcen, die als Einheit bereitgestellt werden.

## BEISPIELE

### Beispiel 1: Erstellen einer leeren Ressourcengruppe
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US"
```

Mit diesem Befehl wird eine Ressourcengruppe ohne Ressourcen erstellt. Sie können die **Cmdlets New-AzResource** oder **New-AzResourceGroupDeployment** verwenden, um dieser Ressourcengruppe Ressourcen und Bereitstellungen hinzuzufügen.

### Beispiel 2: Erstellen einer leeren Ressourcengruppe mit Positionsparametern
```
PS> New-AzResourceGroup RG01 "South Central US"
```

Mit diesem Befehl wird eine Ressourcengruppe ohne Ressourcen erstellt.

### Beispiel 3: Erstellen einer Ressourcengruppe mit Tags
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

Mit diesem Befehl wird eine leere Ressourcengruppe erstellt. Dieser Befehl ist mit dem Befehl in Beispiel 1 identisch, mit der Ausnahme, dass er der Ressourcengruppe Tags zu weist. Das erste Tag mit dem Namen Leer kann verwendet werden, um Ressourcengruppen zu identifizieren, die keine Ressourcen haben. Das zweite Tag trägt den Namen "Abteilung" und hat den Wert "Marketing". Sie können ein Tag wie dieses verwenden, um Ressourcengruppen für die Verwaltung oder Budgetierung zu kategorisieren.

## PARAMETER

### -ApiVersion
Gibt die vom Ressourcenanbieter unterstützte API-Version an.
Sie können eine andere Version als die Standardversion angeben.

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

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden

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

### -Location
Gibt den Speicherort der Ressourcengruppe an. Geben Sie einen Azure-Rechenzentrumsspeicherort an, z. B. West-USA oder Südostasien. Sie können eine Ressourcengruppe an einem beliebigen Speicherort platzieren. Die Ressourcengruppe muss sich nicht an demselben Speicherort wie Ihr Azure-Abonnement oder an demselben Speicherort wie die Ressourcen befinden.
Um zu ermitteln, welcher Speicherort die einzelnen Ressourcentypen unterstützt, verwenden Get-AzResourceProvider cmdlet mit dem *Parameter ProviderNamespace.*

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt einen Namen für die Ressourcengruppe an. Der Ressourcenname muss im Abonnement eindeutig sein. Wenn eine Ressourcengruppe mit diesem Namen bereits vorhanden ist, werden Sie mit dem Befehl zur Bestätigung aufgefordert, bevor Sie die vorhandene Ressourcengruppe ersetzen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.

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

### -Tag
Schlüssel-Wert-Paare in Form einer Hashtabelle. Beispiel: @{key0="value0";key1=$null;key2="value2"} Zum Hinzufügen oder Ändern eines Tags müssen Sie die Sammlung von Tags für die Ressourcengruppe ersetzen.
Nachdem Sie Ressourcen und Gruppen Tags zugewiesen  haben, können Sie den Parameter Tag von Get-AzResource und Get-AzResourceGroup verwenden, um nach Ressourcen und Gruppen nach Dem Tagnamen oder nach Name und Wert zu suchen. Sie können Kategorien verwenden, um Ihre Ressourcen zu kategorisieren, z. B. nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu den Ressourcen nachverfolgt zu werden.
Verwenden Sie das cmdlet Get-AzTag, um ihre vordefinierten Tags zu erhalten.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### System.String

### System.Collections.Hashtable

## AUSGABEN

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup

## NOTIZEN

## VERWANDTE LINKS

[Get-AzResourceProvider](./Get-AzResourceProvider.md)

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResource](./New-AzResource.md)

[New-AzResourceGroupDeployment](./New-AzResourceGroupDeployment.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)

[Set-AzResourceGroup](./Set-AzResourceGroup.md)
