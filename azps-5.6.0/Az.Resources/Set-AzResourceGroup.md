---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: f344c3cd08fb717d1229fb0abb4386c8a2d39d5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941440"
---
# Set-AzResourceGroup

## SYNOPSIS
Ändert eine Ressourcengruppe.

## SYNTAX

### SetByResourceGroupName (Standard)
```
Set-AzResourceGroup -Name <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceGroupId
```
Set-AzResourceGroup [-Tag] <Hashtable> -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Set-AzResourceGroup** ändert die Eigenschaften einer Ressourcengruppe.
Sie können dieses Cmdlet verwenden, um die auf eine Ressourcengruppe angewendeten Azure-Tags hinzuzufügen, zu ändern oder zu löschen.
Geben Sie den *Parameter Name* an, um die Ressourcengruppe und den Parameter Tag *zu identifizieren,* um die Tags zu ändern.
Sie können dieses Cmdlet nicht verwenden, um den Namen einer Ressourcengruppe zu ändern.

## BEISPIELE

### Beispiel 1: Anwenden eines Tags auf eine Ressourcengruppe
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

Mit diesem Befehl wird ein Department-Tag mit dem Wert IT auf eine Ressourcengruppe angewendet, die keine Tags enthält.

### Beispiel 2: Hinzufügen von Tags zu einer Ressourcengruppe
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

In diesem Beispiel wird einer Ressourcengruppe mit vorhandenen Tags ein Statustag mit dem Wert Genehmigt und ein FY2016-Tag hinzufügt. Da die von Ihnen angegebenen Tags die vorhandenen Tags ersetzen, müssen Sie die vorhandenen Tags in die neue Tag-Sammlung hinzufügen, oder Sie verlieren sie.
Der erste Befehl ruft die ContosoRG-Ressourcengruppe ab und verwendet die dot-Methode, um den Wert der Eigenschaft Tags zu erhalten. Der Befehl speichert die Tags in der $Tags Variablen.
Der zweite Befehl ruft die Tags in der Variablen $Tags ab.
Der dritte Befehl verwendet den +=-Zuordnungsoperator, um dem Array der Tags in der Variablen $Tags hinzuzufügen.
Der vierte Befehl verwendet den *Parameter Tag* von **Set-AzResourceGroup,** um die Tags in der $Tags auf die ContosoRG-Ressourcengruppe anzuwenden.
Der fünfte Befehl ruft alle Tags ab, die auf die ContosoRG-Ressourcengruppe angewendet wurden. Die Ausgabe zeigt, dass die Ressourcengruppe über das Department-Tag und die beiden neuen Tags Status und FY2015 verfügt.

### Beispiel 3: Löschen aller Tags für eine Ressourcengruppe
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
```

Dieser Befehl gibt den *Parameter Tag* mit einem leeren Hashtabellenwert an, um alle Tags aus der Ressourcengruppe ContosoRG zu löschen.

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

### -ID
Gibt die ID der zu ändernden Ressourcengruppe an.

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen der zu ändernden Ressourcengruppe an.

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: Named
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
Schlüssel-Wert-Paare in Form einer Hashtabelle. Beispiel: @{key0="value0";key1=$null;key2="value2"} Ein Tag ist ein Name-Wert-Paar, das Sie erstellen und auf Ressourcengruppen anwenden können. Nachdem Sie Ressourcen und Gruppen Tags zugewiesen haben, können Sie den Parameter *Tag* von Get-AzResource und Get-AzResourceGroup verwenden, um nach Ressourcen und Gruppen nach Tagname oder Namen und Wert zu suchen. Sie können Kategorien verwenden, um Ihre Ressourcen zu kategorisieren, z. B. nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu den Ressourcen nachverfolgt zu werden.
Zum Hinzufügen oder Ändern eines Tags müssen Sie die Sammlung von Tags für die Ressourcengruppe ersetzen. Wenn Sie ein Tag löschen möchten, geben Sie in **Get-AzResourceGroup** eine Hashtabelle mit allen Tags ein, die derzeit auf die Ressourcengruppe angewendet werden, mit Ausnahme des Tags, das Sie löschen möchten. Wenn Sie alle Tags aus einer Ressourcengruppe löschen möchten, geben Sie eine leere Hashtabelle an: `@{}` .

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

[Get-AzResource](./Get-AzResource.md)

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResourceGroup](./New-AzResourceGroup.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)
