---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 22a43739ec63f8287ce51c4c4f4a125b4e5b1c65
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180028"
---
# Remove-AzTag

## Synopsis
Löscht vordefinierte Azure-Tags oder-Werte | Löscht den gesamten Satz von Tags für eine Ressource oder ein Abonnement.

## Syntax

### RemovePredefinedTagParameterSet

```powershell
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveByResourceIdParameterSet

```powershell
Remove-AzTag
   -ResourceId <String>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## Beschreibung

**RemovePredefinedTagSet** : das Cmdlet **Remove-AzTag** löscht vordefinierte Azure-Tags und-Werte aus Ihrem Abonnement.
Verwenden Sie den *value* -Parameter, um bestimmte Werte aus einem vordefinierten Tag zu löschen.
Standardmäßig löscht **Remove-AzTag** das angegebene Tag und alle seine Werte. Sie können eine Kategorie oder einen Wert, der aktuell auf eine Ressource oder eine Ressourcengruppe angewendet wird, nicht löschen.
Verwenden Sie vor der Verwendung von **Remove-AzTag** den *Tag* -Parameter des Set-AzResourceGroup-Cmdlets, um das Tag oder die Werte aus der Ressourcen-oder Ressourcengruppe zu löschen.
Das Azure-Tags-Modul, in dem **Remove-AzTag** enthalten ist, kann Ihnen bei der Verwaltung Ihrer vordefinierten Azure-Tags helfen.
Bei einem Azure-Tag handelt es sich um ein Name-Wert-Paar, mit dem Sie Ihre Azure-Ressourcen und Ressourcengruppen kategorisieren können, beispielsweise nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu Ressourcen und Gruppen zu überwachen.
Sie können Tags in einem einzigen Schritt definieren und anwenden, doch mit vordefinierten Tags können Sie standardmäßige, konsistente, vorhersagbare Namen und Werte für die Tags in Ihrem Abonnement einrichten.

**RemoveByResourceIdParameterSet** : das Cmdlet " **Remove-AzTag** " mit einer **Resourcen** -Kennung löscht den gesamten Satz von Tags für eine Ressource oder ein Abonnement.

## Beispiele

### Beispiel 1: Löschen eines vordefinierten Tags
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

Mit diesem Befehl wird das vordefinierte Tag namens Department und alle zugehörigen Werte gelöscht.
Wenn das Tag auf Ressourcen oder Ressourcengruppen angewendet wurde, schlägt der Befehl fehl.

### Beispiel 2: Löschen eines Werts aus einem vordefinierten Tag
```powershell
PS C:\>Remove-AzTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

Dieser Befehl löscht den HumanResources-Wert aus dem vordefinierten Department-Tag.
Die Kategorie wird nicht gelöscht.
Wenn der Wert auf Ressourcen oder Ressourcengruppen angewendet wurde, schlägt der Befehl fehl.

### Beispiel 3: Löschen der gesamten Gruppe von Tags in einem Abonnement

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

Mit diesem Befehl wird der gesamte Satz von Tags im Abonnement mit {subId} gelöscht. Sie gibt das gelöschte Objekt nicht zurück, wenn es nicht "-passthru" übergibt.

### Beispiel 4: Löschen der gesamten Gruppe von Tags für eine Ressource

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -PassThru

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

Mit diesem Befehl wird der gesamte Satz von Tags für die Ressource mit {Ressourcen-Nr} gelöscht. Bei der Übergabe von "-passthru" wird der gelöschte Oject-Wert zurückgegeben.

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

### -Name
Gibt den Namen des zu entfernenden vordefinierten Tags an.
Standardmäßig entfernt **Remove-AzTag** das angegebene Tag und alle seine Werte.
Verwenden Sie den *Wert* -Parameter, um ausgewählte Werte zu löschen, aber die Kategorie nicht zu löschen.

```yaml
Type: System.String
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Wert
Löscht die angegebenen Werte aus dem vordefinierten Tag, löscht das Tag aber nicht.

```yaml
Type: System.String[]
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Resourcen-Nr
Der Ressourcenbezeichner für die markierte Entität. Eine Ressource, eine Ressourcengruppe oder ein Abonnement können markiert sein.

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Gibt ein Objekt zurück, das das gelöschte Tag oder das resultierende Tag mit gelöschten Werten darstellt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

### System. String []

### System. Management. Automation. Switchparameter

## Ausgaben

### Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag | Microsoft. Azure. Commands. Tags. Model. PSTagResource

## Notizen

## Verwandte Links

[Get-AzTag](./Get-AzTag.md)

[Neu – AzTag](./New-AzTag.md)

[Update-AzTag](./Update-AzTag.md)