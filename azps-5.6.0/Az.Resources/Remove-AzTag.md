---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 201e341ce05b22597f05601d7d269d2eb27c2358
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932328"
---
# Remove-AzTag

## SYNOPSIS
Löscht vordefinierte Azure-Tags oder -Werte | Löscht den gesamten Satz von Tags für eine Ressource oder ein Abonnement.

## SYNTAX

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

## BESCHREIBUNG

**RemovePredefinedTagSet**: Das **Cmdlet Remove-AzTag** löscht vordefinierte #A0 und -Werte aus Ihrem Abonnement.
Wenn Sie bestimmte Werte aus einem vordefinierten Tag löschen möchten, verwenden Sie den *Parameter Wert.*
Standardmäßig löscht **Remove-AzTag** das angegebene Tag und alle seine Werte. Sie können ein Tag oder einen Wert, der derzeit auf eine Ressource oder Ressourcengruppe angewendet wird, nicht löschen.
Verwenden Sie vor der Verwendung von **Remove-AzTag** den Parameter *Tag* des cmdlets Set-AzResourceGroup, um das Tag oder die Werte aus der Ressource oder Ressourcengruppe zu löschen.
Das Azure-Tags-Modul, zu dem **Remove-AzTag** gehört, kann Ihnen bei der Verwaltung Ihrer vordefinierten #A0 helfen.
Ein Azure-Tag ist ein Namen-Wert-Paar, das Sie verwenden können, um Ihre Azure-Ressourcen und Ressourcengruppen zu kategorisieren, z. B. nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu den Ressourcen und Gruppen nachverfolgt zu werden.
Sie können Tags in einem einzigen Schritt definieren und anwenden, aber mit vordefinierten Tags können Sie standardmäßige, konsistente, vorhersagbare Namen und Werte für die Tags in Ihrem Abonnement festlegen.

**RemoveByResourceIdParameterSet**: Das **Cmdlet Remove-AzTag** mit **einer ResourceId** löscht den gesamten Satz von Tags für eine Ressource oder ein Abonnement.

## BEISPIELE

### Beispiel 1: Löschen eines vordefinierten Tags
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

Mit diesem Befehl werden das vordefinierte Tag "Abteilung" und alle werte gelöscht.
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

Mit diesem Befehl wird der Wert "HumanResources" aus dem vordefinierten Department-Tag gelöscht.
Das -Tag wird nicht gelöscht.
Wenn der Wert auf Ressourcen oder Ressourcengruppen angewendet wurde, schlägt der Befehl fehl.

### Beispiel 3: Löscht den gesamten Satz von Tags in einem Abonnement

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

Mit diesem Befehl wird der gesamte Satz von Tags im Abonnement mit {subId} gelöscht. Es gibt das gelöschte Objekt nicht zurück, wenn "-PassThru" nicht übergeben wird.

### Beispiel 4: Löscht den gesamten Satz von Tags für eine Ressource.

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

Mit diesem Befehl wird der gesamte Satz von Tags für die Ressource mit {resourceId} gelöscht. Es gibt das gelöschte Auswerfen zurück, wenn "-PassThru" übergeben wird.

## PARAMETER

### -DefaultProfile
Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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
Gibt den Namen des vordefinierten Tags an, das entfernt werden soll.
Standardmäßig entfernt **Remove-AzTag** das angegebene Tag und alle seine Werte.
Um ausgewählte Werte zu löschen, aber nicht das -Tag zu löschen, verwenden Sie den *Parameter Wert.*

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
Löscht die angegebenen Werte aus dem vordefinierten Tag, löscht aber nicht das -Tag.

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

### -ResourceId
Der Ressourcenbezeichner für die markierte Entität. Eine Ressource, eine Ressourcengruppe oder ein Abonnement kann markiert werden.

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
Gibt ein -Objekt zurück, das das gelöschte Tag oder das resultierende Tag mit gelöschten Wert darstellt.

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

### System.String[]

### System.Management.Automation.SwitchParameter

## AUSGABEN

### Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource

## NOTIZEN

## VERWANDTE LINKS

[Get-AzTag](./Get-AzTag.md)

[New-AzTag](./New-AzTag.md)

[Update-AzTag](./Update-AzTag.md)