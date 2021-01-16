---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
ms.openlocfilehash: 9c4bdfe189c16f3e2f6f90d3197149bdc57c78c8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357957"
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
Das **Cmdlet "New-AzResourceGroup"** erstellt eine Azure-Ressourcengruppe.
Sie können eine Ressourcengruppe erstellen, indem Sie nur einen Namen und einen Ort verwenden und dann das Cmdlet New-AzResource verwenden, um Ressourcen zu erstellen, die der Ressourcengruppe hinzugefügt werden.
Wenn Sie einer vorhandenen Ressourcengruppe eine Bereitstellung hinzufügen möchten, verwenden Sie das New-AzResourceGroupDeployment-Cmdlet. Wenn Sie einer vorhandenen Ressourcengruppe eine Ressource hinzufügen möchten, verwenden Sie das **Cmdlet "New-AzResource".** Eine Azure-Ressource ist eine vom Benutzer verwaltete Azure-Entität, z. B. ein Datenbankserver, eine Datenbank oder eine Website. Eine Azure-Ressourcengruppe ist eine Sammlung von Azure-Ressourcen, die als Einheit bereitgestellt werden.

## BEISPIELE

### Beispiel 1: Erstellen einer leeren Ressourcengruppe
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US"
```

Mit diesem Befehl wird eine Ressourcengruppe erstellt, die keine Ressourcen hat. Sie können die **Cmdlets "New-AzResource"** oder **"New-AzResourceGroupDeployment"** verwenden, um dieser Ressourcengruppe Ressourcen und Bereitstellungen hinzuzufügen.

### Beispiel 2: Erstellen einer leeren Ressourcengruppe mithilfe von Positionsparametern
```
PS> New-AzResourceGroup RG01 "South Central US"
```

Mit diesem Befehl wird eine Ressourcengruppe erstellt, die keine Ressourcen hat.

### Beispiel 3: Erstellen einer Ressourcengruppe mit Tags
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

Mit diesem Befehl wird eine leere Ressourcengruppe erstellt. Dieser Befehl ist derselbe wie der Befehl in Beispiel 1, mit dem Ausnahme, dass er der Ressourcengruppe Tags zu weist. Das erste Tag namens "Leer" kann verwendet werden, um Ressourcengruppen zu identifizieren, die keine Ressourcen haben. Das zweite Tag hat den Namen "Department" und hat den Wert "Marketing". Sie können ein solches Tag verwenden, um Ressourcengruppen für Die Verwaltung oder Budgetierung zu kategorisieren.

## PARAMETERS

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

### -Force
Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.

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
Gibt den Speicherort der Ressourcengruppe an. Geben Sie einen Standort im Azure-Rechenzentrum an, z. B. "Usa, Westen" oder "Südostasien". Sie können eine Ressourcengruppe an einem beliebigen Ort platzieren. Die Ressourcengruppe muss sich nicht am selben Speicherort wie Ihr Abonnement oder an demselben Speicherort wie die Ressourcen befinden.
Um festzustellen, welcher Speicherort die einzelnen Ressourcentypen unterstützt, verwenden Sie das Get-AzResourceProvider cmdlet mit dem *Parameter "ProviderNamespace".*

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
Gibt einen Namen für die Ressourcengruppe an. Der Ressourcenname muss im Abonnement eindeutig sein. Wenn bereits eine Ressourcengruppe mit diesem Namen vorhanden ist, werden Sie vom Befehl zur Bestätigung aufgefordert, bevor Sie die vorhandene Ressourcengruppe ersetzen.

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
Nachdem Sie Ressourcen und Gruppen Tags zugewiesen haben, können Sie den Parameter *"Tag"* von Get-AzResource und Get-AzResourceGroup verwenden, um nach Ressourcen und Gruppen nach Tagname oder nach Name und Wert zu suchen. Sie können Kategorien verwenden, um Ihre Ressourcen zu kategorisieren, z. B. nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu den Ressourcen zu verfolgen.
Um die vordefinierten Tags zu erhalten, verwenden Sie das Get-AzTag Cmdlet.

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

### -Confirm
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

### -Waswenn
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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

### System.Collections.Hashtable

## AUSGABEN

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzResourceProvider](./Get-AzResourceProvider.md)

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResource](./New-AzResource.md)

[New-AzResourceGroupDeployment](./New-AzResourceGroupDeployment.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)

[Set-AzResourceGroup](./Set-AzResourceGroup.md)
