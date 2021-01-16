---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: 0523041357becb38475bb496c94ba1fd48c5acaf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305592"
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
Das **Cmdlet "Set-AzResourceGroup"** ändert die Eigenschaften einer Ressourcengruppe.
Sie können dieses Cmdlet verwenden, um die einer Ressourcengruppe zugeordneten Azure-Tags hinzuzufügen, zu ändern oder zu löschen.
Geben Sie den *Parameter "Name"* an, um die Ressourcengruppe zu identifizieren, und den *Parameter "Tag",* um die Tags zu ändern.
Sie können dieses Cmdlet nicht verwenden, um den Namen einer Ressourcengruppe zu ändern.

## BEISPIELE

### Beispiel 1: Anwenden einer Markierung auf eine Ressourcengruppe
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

Dieser Befehl wendet ein Tag "Department" mit dem Wert "IT" auf eine Ressourcengruppe an, die keine Tags enthält.

### Beispiel 2: Hinzufügen von Tags zu einer Ressourcengruppe
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

In diesem Beispiel wird einer Ressourcengruppe, die vorhandene Tags enthält, ein Statustag mit dem Wert "Genehmigt" und ein "FY2016"-Tag hinzufügt. Da die von Ihnen angegebenen Tags die vorhandenen Tags ersetzen, müssen Sie die vorhandenen Tags in die neue Tagsammlung hinzufügen, da sie verloren gehen.
Der erste Befehl ruft die Ressourcengruppe "ContosoRG" ab und ruft den Wert der Eigenschaft "Tags" mithilfe der dot-Methode ab. Der Befehl speichert die Tags in der $Tags Variable.
Der zweite Befehl ruft die Tags in der Variablen $Tags ab.
Der dritte Befehl verwendet den Zuordnungsoperator += zum Hinzufügen der Tags "Status" und "FY2016" zum Array der Tags in der $Tags Variable.
Der vierte Befehl verwendet den *Parameter "Tag"* von **"Set-AzResourceGroup",** um die Tags in der Variablen "$Tags" auf die Ressourcengruppe "ContosoRG" anzuwenden.
Der fünfte Befehl ruft alle Tags ab, die der Ressourcengruppe "ContosoRG" zugeordnet sind. Die Ausgabe zeigt, dass die Ressourcengruppe das Tag "Department" und die beiden neuen Tags "Status" und "FY2015" enthält.

### Beispiel 3: Löschen aller Tags für eine Ressourcengruppe
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
```

Dieser Befehl gibt den *Parameter "Tag"* mit einem leeren Hashtabellenwert an, um alle Tags aus der Ressourcengruppe "ContosoRG" zu löschen.

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
Schlüssel-Wert-Paare in Form einer Hashtabelle. Beispiel: @{key0="value0";key1=$null;key2="wert2"} Ein Tag ist ein Name-Wert-Paar, das Sie erstellen und auf Ressourcen- und Ressourcengruppen anwenden können. Nachdem Sie Ressourcen und Gruppen Tags zugewiesen haben, können Sie den *Parameter "Tag"* von Get-AzResource und Get-AzResourceGroup verwenden, um nach Ressourcen und Gruppen nach Tagname oder Name und Wert zu suchen. Sie können Kategorien verwenden, um Ihre Ressourcen zu kategorisieren, z. B. nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu den Ressourcen zu verfolgen.
Zum Hinzufügen oder Ändern eines Tags müssen Sie die Sammlung von Tags für die Ressourcengruppe ersetzen. Wenn Sie ein Tag löschen möchten, geben Sie in **"Get-AzResourceGroup"** eine Hashtabelle mit allen aktuell auf die Ressourcengruppe angewendeten Tags ein, mit Ausnahme des tags, das Sie löschen möchten. Um alle Tags aus einer Ressourcengruppe zu löschen, geben Sie eine leere Hashtabelle `@{}` an:

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

### System.Collections.Hashtable

## AUSGABEN

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzResource](./Get-AzResource.md)

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResourceGroup](./New-AzResourceGroup.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)
