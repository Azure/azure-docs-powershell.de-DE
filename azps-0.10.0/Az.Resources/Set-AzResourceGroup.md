---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: d645f430c21a1e9675a0f356cffacbad6a7b5740
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843183"
---
# Set-AzResourceGroup

## Synopsis
Ändert eine Ressourcengruppe.

## Syntax

### SetByResourceGroupName (Standard)
```
Set-AzResourceGroup [-Name] <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceGroupId
```
Set-AzResourceGroup [-Tag] <Hashtable> [-Id] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzResourceGroup** " ändert die Eigenschaften einer Ressourcengruppe.
Mit diesem Cmdlet können Sie die auf eine Ressourcengruppe angewendeten Azure-Tags hinzufügen, ändern oder löschen.
Geben Sie den Parameter *Name* an, um die Ressourcengruppe zu identifizieren, und den *Tag* -Parameter, um die Kategorien zu ändern.
Sie können dieses Cmdlet nicht verwenden, um den Namen einer Ressourcengruppe zu ändern.

## Beispiele

### Beispiel 1: Anwenden einer Kategorie auf eine Ressourcengruppe
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

Mit diesem Befehl wird eine Abteilungs Kategorie mit einem Wert auf eine Ressourcengruppe angewendet, die über keine vorhandenen Kategorien verfügt.

### Beispiel 2: Hinzufügen von Kategorien zu einer Ressourcengruppe
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

In diesem Beispiel wird ein statustag mit dem Wert Approved und einem FY2016-Tag zu einer Ressourcengruppe hinzugefügt, die über vorhandene Tags verfügt. Da die von Ihnen angegebenen Tags die vorhandenen Tags ersetzen, müssen Sie die vorhandenen Tags in die neue Tag-Sammlung einbeziehen, oder Sie werden verloren gehen.
Der erste Befehl ruft die ContosoRG-Ressourcengruppe ab und verwendet die dot-Methode, um den Wert ihrer Tags-Eigenschaft abzurufen. Der Befehl speichert die Tags in der $Tags-Variablen.
Der zweite Befehl ruft die Tags in der $Tags Variablen ab.
Der dritte Befehl verwendet den + = Zuweisungsoperator, um dem Array von Tags in der $Tags Variablen die Tags "Status" und "FY2016" hinzuzufügen.
Der vierte Befehl verwendet den *Tag* -Parameter von "AzResourceGroup", um die Tags in der $Tags-Variablen auf die ContosoRG **-** Ressourcengruppe anzuwenden.
Der fünfte Befehl ruft alle auf die ContosoRG-Ressourcengruppe angewendeten Tags ab. Die Ausgabe zeigt, dass die Ressourcengruppe die Kategorie "Abteilung" und die beiden neuen Kategorien "Status" und "FY2015" enthält.

### Beispiel 3: Löschen aller Tags für eine Ressourcengruppe
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
```

Dieser Befehl gibt den *Tag* -Parameter mit einem leeren Hashtabellenwert an, um alle Tags aus der ContosoRG-Ressourcengruppe zu löschen.

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
Aliases: AzContext, AzureCredential

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
Position: 0
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
Position: 0
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
Schlüssel-Wert-Paare in Form einer Hashtabelle Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"} ein Tag ist ein Name-Wert-Paar, das Sie erstellen und auf Ressourcen und Ressourcengruppen anwenden können. Nachdem Sie Ressourcen und Gruppen Kategorien zugewiesen haben, können Sie den *Tag* -Parameter von Get-AzResource und Get-AzResourceGroup verwenden, um nach Ressourcen und Gruppen nach Tag-Name oder Name und Wert zu suchen. Sie können Kategorien verwenden, um Ihre Ressourcen zu kategorisieren, beispielsweise nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu den Ressourcen zu überwachen.
Wenn Sie ein Tag hinzufügen oder ändern möchten, müssen Sie die Sammlung von Tags für die Ressourcengruppe ersetzen. Wenn Sie eine Kategorie löschen möchten, geben Sie eine Hashtabelle mit allen Tags, die aktuell auf die Ressourcengruppe angewendet werden, in " **Get-AzResourceGroup** " ein, mit Ausnahme der Kategorie, die Sie löschen möchten. Wenn Sie alle Kategorien aus einer Ressourcengruppe löschen möchten, geben Sie eine leere Hashtabelle an: `@{}` .

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### Microsoft. Azure. Commands. resources. Models. PSResourceGroup

## Notizen

## Verwandte Links

[Get-AzResource](./Get-AzResource.md)

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[Neu – AzResourceGroup](./New-AzResourceGroup.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)
