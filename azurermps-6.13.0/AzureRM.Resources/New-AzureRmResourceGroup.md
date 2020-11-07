---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroup.md
ms.openlocfilehash: 7264733055322c3d5886ff57f50d22e23f932a7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662494"
---
# New-AzureRmResourceGroup

## Synopsis
Erstellt eine Azure-Ressourcengruppe.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureRmResourceGroup -Name <String> -Location <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmResourceGroup** erstellt eine Azure-Ressourcengruppe.
Sie können eine Ressourcengruppe erstellen, indem Sie nur einen Namen und einen Speicherort verwenden, und dann mithilfe des New-AzureRmResource-Cmdlets Ressourcen erstellen, die der Ressourcengruppe hinzugefügt werden sollen.
Wenn Sie eine Bereitstellung zu einer vorhandenen Ressourcengruppe hinzufügen möchten, verwenden Sie das New-AzureRmResourceGroupDeployment-Cmdlet. Wenn Sie einer vorhandenen Ressourcengruppe eine Ressource hinzufügen möchten, verwenden Sie das Cmdlet **New-AzureRmResource** . Eine Azure-Ressource ist eine vom Benutzer verwaltete Azure-Entität, beispielsweise ein Datenbankserver, eine Datenbank oder eine Website. Eine Azure-Ressourcengruppe ist eine Sammlung von Azure-Ressourcen, die als Einheit bereitgestellt werden.

## Beispiele

### Beispiel 1: Erstellen einer leeren Ressourcengruppe
```
PS> New-AzureRmResourceGroup -Name RG01 -Location "South Central US"
```

Mit diesem Befehl wird eine Ressourcengruppe erstellt, die keine Ressourcen aufweist. Sie können die Cmdlets **New-AzureRmResource** oder **New-AzureRmResourceGroupDeployment** verwenden, um dieser Ressourcengruppe Ressourcen und Bereitstellungen hinzuzufügen.

### Beispiel 2: Erstellen einer leeren Ressourcengruppe mithilfe von Positionsparametern
```
PS> New-AzureRmResourceGroup RG01 "South Central US"
```

Mit diesem Befehl wird eine Ressourcengruppe erstellt, die keine Ressourcen aufweist.

### Beispiel 3: Erstellen einer Ressourcengruppe mit Tags
```
PS> New-AzureRmResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

Mit diesem Befehl wird eine leere Ressourcengruppe erstellt. Dieser Befehl entspricht dem Befehl in Beispiel 1, mit der Ausnahme, dass er der Ressourcengruppe Tags zuweist. Mit dem ersten Tag mit dem Namen Empty können Ressourcengruppen identifiziert werden, die keine Ressourcen aufweisen. Das zweite Tag hat den Namen Department und hat einen Wert für Marketing. Sie können eine Kategorie wie diese verwenden, um Ressourcengruppen für die Verwaltung oder Budgetierung zu kategorisieren.

## Parameter

### -ApiVersion
Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.
Sie können eine andere Version als die Standard Version angeben.

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
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -Standort
Gibt den Speicherort der Ressourcengruppe an. Geben Sie einen Azure Data Center-Standort an, beispielsweise West-oder Südostasien. Sie können eine Ressourcengruppe an einem beliebigen Ort platzieren. Die Ressourcengruppe muss sich nicht am gleichen Speicherort wie das Azure-Abonnement oder am gleichen Speicherort wie die Ressourcen befinden.
Verwenden Sie das Get-AzureRmResourceProvider-Cmdlet mit dem *ProviderNamespace* -Parameter, um zu bestimmen, welcher Speicherort die einzelnen Ressourcentypen unterstützt.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt einen Namen für die Ressourcengruppe an. Der Ressourcenname muss im Abonnement eindeutig sein. Wenn bereits eine Ressourcengruppe mit diesem Namen vorhanden ist, werden Sie vom Befehl zur Bestätigung aufgefordert, bevor die vorhandene Ressourcengruppe ersetzt wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.

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
Schlüssel-Wert-Paare in Form einer Hashtabelle Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"} um eine Kategorie hinzuzufügen oder zu ändern, müssen Sie die Sammlung von Tags für die Ressourcengruppe ersetzen.
Nachdem Sie Ressourcen und Gruppen Kategorien zugewiesen haben, können Sie mit dem *Tag* -Parameter von Get-AzureRmResource und Get-AzureRmResourceGroup nach Ressourcen und Gruppen nach Tag-Name oder nach Name und Wert suchen. Sie können Kategorien verwenden, um Ihre Ressourcen zu kategorisieren, beispielsweise nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu den Ressourcen zu überwachen.
Verwenden Sie das Get-AzureRMTag-Cmdlet, um ihre vordefinierten Tags abzurufen.

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

### Keine

## Ausgaben

### Microsoft. Azure. Commands. ResourceManagement. Models. PSResourceGroup

## Notizen

## Verwandte Links

[Get-AzureRmResourceProvider](./Get-AzureRmResourceProvider.md)

[Get-AzureRmResourceGroup](./Get-AzureRmResourceGroup.md)

[Neu – AzureRmResource](./New-AzureRmResource.md)

[Neu – AzureRmResourceGroupDeployment](./New-AzureRmResourceGroupDeployment.md)

[Remove-AzureRmResourceGroup](./Remove-AzureRmResourceGroup.md)

[Satz-AzureRmResourceGroup](./Set-AzureRmResourceGroup.md)
