---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 22a43739ec63f8287ce51c4c4f4a125b4e5b1c65
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156452"
---
# Remove-AzTag

## SYNOPSIS
Löscht vordefinierte Azure-Tags oder -| Löscht den gesamten Satz von Tags für eine Ressource oder ein Abonnement.

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

**RemovePredefinedTagSet:** Das **Cmdlet "Remove-AzTag"** löscht vordefinierte #A0 und -Werte aus Ihrem Abonnement.
Verwenden Sie den Parameter *"Value",* um bestimmte Werte aus einem vordefinierten Tag zu löschen.
Standardmäßig löscht **"Remove-AzTag"** das angegebene Tag und alle werte. Sie können ein Tag oder einen Wert, der derzeit auf eine Ressource oder Ressourcengruppe angewendet wird, nicht löschen.
Bevor Sie **"Remove-AzTag"** verwenden, verwenden Sie den Parameter *"Tag"* des cmdlets Set-AzResourceGroup, um das Tag oder die Werte aus der Ressourcengruppe zu löschen.
Das Azure-Tags-Modul, zu dem **"Remove-AzTag"** gehört, kann Ihnen dabei helfen, Ihre vordefinierten #A0 zu verwalten.
Ein Azure-Tag ist ein Name-Wert-Paar, mit dem Sie Ihre Azure-Ressourcen und -Ressourcengruppen kategorisieren können, z. B. nach Abteilung oder Kostencenter, oder um Notizen oder Kommentare zu den Ressourcen und Gruppen nachverfolgt werden.
Sie können Tags in einem einzigen Schritt definieren und anwenden, aber mit vordefinierten Tags können Sie standardübliche, konsistente, vorhersehbare Namen und Werte für die Tags in Ihrem Abonnement festlegen.

**RemoveByResourceIdParameterSet:** Das **Cmdlet "Remove-AzTag"** mit einer **ResourceId** löscht den gesamten Satz von Tags für eine Ressource oder ein Abonnement.

## BEISPIELE

### Beispiel 1: Löschen eines vordefinierten Tags
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

Mit diesem Befehl werden das vordefinierte Tag "Abteilung" und alle Werte gelöscht.
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

Mit diesem Befehl wird der Wert "HumanResources" aus dem vordefinierten Tag "Department" gelöscht.
Das Tag wird nicht gelöscht.
Wenn der Wert auf Ressourcen oder Ressourcengruppen angewendet wurde, schlägt der Befehl fehl.

### Beispiel 3: Löscht die gesamte Gruppe von Kategorien in einem Abonnement.

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

Mit diesem Befehl wird der gesamte Satz von Tags im Abonnement mit {subId} gelöscht. Wenn "-PassThru" nicht übergeben wird, wird das gelöschte Objekt nicht zurückgeben.

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

Mit diesem Befehl wird der gesamte Satz von Markierungen für die Ressource mit {resourceId} gelöscht. Beim Übergeben von "-PassThru" wird das gelöschte Auswerfen zurückgegeben.

## PARAMETERS

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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
Standardmäßig entfernt **"Remove-AzTag"** das angegebene Tag und alle werte.
Verwenden Sie den Parameter *"Value",* um ausgewählte Werte zu löschen, das Tag aber nicht zu löschen.

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

### -Value
Löscht die angegebenen Werte aus dem vordefinierten Tag, aber nicht das Tag.

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
Der Ressourcenbezeichner für die markierte Entität. Möglicherweise ist eine Ressource, eine Ressourcengruppe oder ein Abonnement markiert.

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
Gibt ein Objekt zurück, das das gelöschte Tag oder das resultierende Tag mit einem gelöschten Wert darstellt.

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

### System.String[]

### System.Management.Automation.SwitchParameter

## AUSGABEN

### Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzTag](./Get-AzTag.md)

[New-AzTag](./New-AzTag.md)

[Update-AzTag](./Update-AzTag.md)