---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceGroup.md
ms.openlocfilehash: a6fa8a27bacf5504564703d8669616f748aa95d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664439"
---
# Set-AzureRmResourceGroup

## Synopsis
Ändert eine Ressourcengruppe.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Listet die Ressourcengruppe auf, die auf dem Namen basiert. Standard
```
Set-AzureRmResourceGroup [-Name] <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Listet die Ressourcengruppe auf, die in der ID basiert.
```
Set-AzureRmResourceGroup [-Tag] <Hashtable> [-Id] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureRmResourceGroup** " ändert die Eigenschaften einer Ressourcengruppe.
Mit diesem Cmdlet können Sie die auf eine Ressourcengruppe angewendeten Azure-Tags hinzufügen, ändern oder löschen.
Geben Sie den Parameter *Name* an, um die Ressourcengruppe zu identifizieren, und den *Tag* -Parameter, um die Kategorien zu ändern.

Sie können dieses Cmdlet nicht verwenden, um den Namen einer Ressourcengruppe zu ändern.

## Beispiele

### Beispiel 1: Anwenden einer Kategorie auf eine Ressourcengruppe
```
PS C:\>Set-AzureRmResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

Mit diesem Befehl wird eine Abteilungs Kategorie mit einem Wert auf eine Ressourcengruppe angewendet, die über keine vorhandenen Kategorien verfügt.

### Beispiel 2: Hinzufügen von Kategorien zu einer Ressourcengruppe
```
PS C:\>$Tags = (Get-AzureRmResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzureRmResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

In diesem Beispiel wird ein statustag mit dem Wert Approved und einem FY2016-Tag zu einer Ressourcengruppe hinzugefügt, die über vorhandene Tags verfügt. Da die von Ihnen angegebenen Tags die vorhandenen Tags ersetzen, müssen Sie die vorhandenen Tags in die neue Tag-Sammlung einbeziehen, oder Sie werden verloren gehen.

Der erste Befehl ruft die ContosoRG-Ressourcengruppe ab und verwendet die dot-Methode, um den Wert ihrer Tags-Eigenschaft abzurufen. Der Befehl speichert die Tags in der $Tags-Variablen.

Der zweite Befehl ruft die Tags in der $Tags Variablen ab.

Der dritte Befehl verwendet den + = Zuweisungsoperator, um dem Array von Tags in der $Tags Variablen die Tags "Status" und "FY2016" hinzuzufügen.

Der vierte Befehl verwendet den *Tag* -Parameter von "AzureRmResourceGroup", um die Tags in der $Tags-Variablen auf die ContosoRG **-** Ressourcengruppe anzuwenden.

Der fünfte Befehl ruft alle auf die ContosoRG-Ressourcengruppe angewendeten Tags ab. Die Ausgabe zeigt, dass die Ressourcengruppe die Kategorie "Abteilung" und die beiden neuen Kategorien "Status" und "FY2015" enthält.

### Beispiel 3: Löschen aller Tags für eine Ressourcengruppe
```
PS C:\>Set-AzureRmResourceGroup -Name "ContosoRG" -Tag @{}
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

### -ID
Gibt die ID der zu ändernden Ressourcengruppe an.

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the Id.
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
Parameter Sets: Lists the resource group based in the name.
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
Schlüssel-Wert-Paare in Form einer Hashtabelle Zum Beispiel:

@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}

Bei einem Tag handelt es sich um ein Name-Wert-Paar, das Sie erstellen und auf Ressourcen und Ressourcengruppen anwenden können. Nachdem Sie Ressourcen und Gruppen Kategorien zugewiesen haben, können Sie den *Tag* -Parameter von Get-AzureRmResource und Get-AzureRmResourceGroup verwenden, um nach Ressourcen und Gruppen nach Tag-Name oder Name und Wert zu suchen. Sie können Kategorien verwenden, um Ihre Ressourcen zu kategorisieren, beispielsweise nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu den Ressourcen zu überwachen.

Wenn Sie ein Tag hinzufügen oder ändern möchten, müssen Sie die Sammlung von Tags für die Ressourcengruppe ersetzen. Wenn Sie eine Kategorie löschen möchten, geben Sie eine Hashtabelle mit allen Tags, die aktuell auf die Ressourcengruppe angewendet werden, in " **Get-AzureRmResourceGroup** " ein, mit Ausnahme der Kategorie, die Sie löschen möchten. Wenn Sie alle Kategorien aus einer Ressourcengruppe löschen möchten, geben Sie eine leere Hashtabelle an: `@{}` .

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### Microsoft. Azure. Commands. resources. Models. PSResourceGroup

## Notizen

## Verwandte Links

[Get-AzureRmResource](./Get-AzureRmResource.md)

[Get-AzureRmResourceGroup](./Get-AzureRmResourceGroup.md)

[Neu – AzureRmResourceGroup](./New-AzureRmResourceGroup.md)

[Remove-AzureRmResourceGroup](./Remove-AzureRmResourceGroup.md)
