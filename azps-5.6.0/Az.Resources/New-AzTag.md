---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: b5f80abac4c114ab60dcb130f229265c4aafd78f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928507"
---
# New-AzTag

## SYNOPSIS
Erstellt ein vordefiniertes Azure-Tag oder fügt werte zu einem vorhandenen Tag | Erstellt oder aktualisiert den gesamten Satz von Tags für eine Ressource oder ein Abonnement.

## SYNTAX

### CreatePredefinedTagParameterSet

```powershell
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### CreateByResourceIdParameterSet

```powershell
New-AzTag
   -ResourceId <String>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## BESCHREIBUNG

**CreatePredefinedTagSet**: Das **Cmdlet New-AzTag** erstellt ein vordefiniertes #A0 mit einem optionalen vordefinierten Wert.
Sie können sie auch verwenden, um vorhandenen vordefinierten Tags zusätzliche Werte hinzuzufügen.
Wenn Sie ein vordefiniertes Tag erstellen möchten, geben Sie einen eindeutigen Tagnamen ein.
Wenn Sie einem vorhandenen vordefinierten Tag einen Wert hinzufügen möchten, geben Sie den Namen des vorhandenen Tags und den neuen Wert an.
Dieses Cmdlet gibt ein -Objekt zurück, das das neue oder geänderte Tag mit seinen Werten und der Anzahl der Ressourcen darstellt, auf die es angewendet wurde.
Das Azure-Tags-Modul, zu dem **New-AzTag** gehört, kann Ihnen beim Verwalten vordefinierter #A0 helfen.
Ein Azure-Tag ist ein Namen-Wert-Paar, das Sie verwenden können, um Ihre Azure-Ressourcen und Ressourcengruppen zu kategorisieren, z. B. nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu den Ressourcen und Gruppen nachverfolgt zu werden.
Sie können Tags in einem einzigen Schritt definieren und anwenden, aber mit vordefinierten Tags können Sie standardmäßige, konsistente, vorhersagbare Namen und Werte für die Tags in Ihrem Abonnement festlegen.
Verwenden Sie zum Anwenden eines vordefinierten Tags auf eine Ressource oder Ressourcengruppe den *Parameter Tag* des New-AzTag Cmdlets.
Um nach Ressourcengruppen mit einem angegebenen Tagnamen oder Namen und Wert zu suchen, verwenden Sie den *Parameter Tag* des cmdlets Get-AzResourceGroup Cmdlet.
Jedes Tag hat einen Namen.
Die Werte sind optional.
Ein vordefiniertes Azure-Tag kann mehrere Werte enthalten, aber wenn Sie das Tag auf eine Ressource oder Ressourcengruppe anwenden, wenden Sie den Tagnamen und nur einen seiner Werte an.
Sie können z. B. ein vordefiniertes Department-Tag mit einem Wert für jede Abteilung erstellen, z. B. Finanzen, Personalwesen und IT.
Wenn Sie das Department-Tag auf eine Ressource anwenden, wenden Sie nur einen vordefinierten Wert an, z. B. Finanzen.

**CreateByResourceIdParameterSet**: Das **New-AzTag-Cmdlet** mit **einer ResourceId** erstellt oder aktualisiert den gesamten Satz von Tags für eine Ressource oder ein Abonnement.
Dieser Vorgang ermöglicht das Hinzufügen oder Ersetzen der gesamten Gruppe von Tags für die angegebene Ressource oder das angegebene Abonnement. Die angegebene Entität kann maximal 50 Tags enthalten.

## BEISPIELE

### Beispiel 1: Erstellen eines vordefinierten Tags
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

Mit diesem Befehl wird ein vordefiniertes Tag mit dem Namen "FY2015" erstellt.
Dieses Tag enthält keine Werte.
Sie können ein Tag ohne Werte auf eine Ressource oder Ressourcengruppe anwenden oder **New-AzTag** verwenden, um dem Tag Werte hinzuzufügen.
Sie können auch einen Wert angeben, wenn Sie das Tag auf die Ressource oder Ressourcengruppe anwenden.

### Beispiel 2: Erstellen eines vordefinierten Tags mit einem Wert
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

Mit diesem Befehl wird ein vordefiniertes Tag mit dem Namen "Abteilung" mit dem Wert "Finanzen" erstellt.

### Beispiel 3: Hinzufügen eines Werts zu einem vordefinierten Tag
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 
PS C:\>New-AzTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

Mit diesen Befehlen wird ein vordefiniertes Tag mit dem Namen "Abteilung" mit zwei Werten erstellt.
Wenn der Tagname vorhanden ist, addiert **New-AzTag** den Wert zum vorhandenen Tag, anstatt ein neues Tag zu erstellen.

### Beispiel 4: Verwenden eines vordefinierten Tags
```powershell
PS C:\>New-AzTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 
PS C:\>Set-AzResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
Name:      EngineerBlog
Location:  East US
Resources: 
            
  Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US
    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001 
PS C:\>Get-AzTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 
PS C:\>Get-AzResourceGroup -Tag @{Name="CostCenter"}
Name:      EngineerBlog
Location:  East US
Resources: 
     Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US

    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001
```

Die Befehle in diesem Beispiel erstellen und verwenden ein vordefiniertes Tag.

### Beispiel 5: Erstellt oder aktualisiert den gesamten Satz von Tags in einem Abonnement

```powershell
PS C:\>$Tags = @{"tagKey1"="tagValue1"; "tagKey2"="tagValue2"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId} -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

Mit diesem Befehl wird der gesamte Satz von Tags im Abonnement mit {subId} erstellt oder aktualisiert.

### Beispiel 6: Erstellt oder aktualisiert den gesamten Satz von Tags für eine Ressource

```powershell
PS C:\>$Tags = @{"Dept"="Finance"; "Status"="Normal"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

Mit diesem Befehl wird der gesamte Satz von Tags für die Ressource mit {resourceId} erstellt oder aktualisiert.

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
Gibt den vordefinierten Tagnamen an.
Wenn Sie ein neues vordefiniertes Tag erstellen möchten, geben Sie einen eindeutigen Namen ein.
Wenn Sie einem vorhandenen Tag einen Wert hinzufügen möchten, geben Sie den Namen des vorhandenen Tags ein.
Wenn ein vorhandenes vordefiniertes Tag den angegebenen Namen enthält, fügt **New-AzTag** dem Tag den angegebenen Wert (falls vorhanden) mit diesem Namen hinzu, anstatt ein neues Tag zu erstellen.

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Wert
Gibt einen vordefinierten Tagwert an.
Vordefinierte Tags können mehrere Werte enthalten, sie können aber nur einen Wert in jeden Befehl eingeben.
Dieser Parameter ist optional, da Tags Namen ohne Werte enthalten können.

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Der Ressourcenbezeichner für die Entität, die markiert wird. Eine Ressource, eine Ressourcengruppe oder ein Abonnement kann markiert werden.

```yaml
Type: System.String
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Die Tags, die für die Ressource verwendet werden müssen.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 1
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

### Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource

## NOTIZEN

## VERWANDTE LINKS

[Get-AzTag](./Get-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

[Update-AzTag](./Update-AzTag.md)