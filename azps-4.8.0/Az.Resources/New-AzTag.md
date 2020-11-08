---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: 176328452c123c3d3cada88940efcdadf88943e0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165666"
---
# New-AzTag

## Synopsis
Erstellt eine vordefinierte Azure-Kategorie oder addiert Werte zu einem vorhandenen Tag | Erstellt oder aktualisiert den gesamten Satz von Tags für eine Ressource oder ein Abonnement.

## Syntax

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

## Beschreibung

**CreatePredefinedTagSet** : das Cmdlet **New-AzTag** erstellt ein vordefiniertes Azure-Tag mit einem optionalen vordefinierten Wert.
Sie können es auch verwenden, um zusätzliche Werte zu vorhandenen vordefinierten Tags hinzuzufügen.
Wenn Sie ein vordefiniertes Tag erstellen möchten, geben Sie einen eindeutigen Tag-Namen ein.
Wenn Sie einen Wert zu einem vorhandenen vordefinierten Tag hinzufügen möchten, geben Sie den Namen des vorhandenen Tags und den neuen Wert an.
Dieses Cmdlet gibt ein Objekt zurück, das das neue oder geänderte Tag mit seinen Werten und der Anzahl der Ressourcen darstellt, auf die es angewendet wurde.
Das Azure-Tags-Modul, in dem **New-AzTag** enthalten ist, kann Ihnen dabei helfen, vordefinierte Azure-Tags zu verwalten.
Bei einem Azure-Tag handelt es sich um ein Name-Wert-Paar, mit dem Sie Ihre Azure-Ressourcen und Ressourcengruppen kategorisieren können, beispielsweise nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu Ressourcen und Gruppen zu überwachen.
Sie können Tags in einem einzigen Schritt definieren und anwenden, doch mit vordefinierten Tags können Sie standardmäßige, konsistente, vorhersagbare Namen und Werte für die Tags in Ihrem Abonnement einrichten.
Wenn Sie eine vordefinierte Kategorie auf eine Ressource oder eine Ressourcengruppe anwenden möchten, verwenden Sie den *Tag* -Parameter des New-AzTag-Cmdlets.
Verwenden Sie den *Tag* -Parameter des Get-AzResourceGroup-Cmdlets, um nach Ressourcengruppen mit einem angegebenen Tag-Namen oder-Namen und-Wert zu suchen.
Jedes Tag hat einen Namen.
Die Werte sind optional.
Ein vordefiniertes Azure-Tag kann mehrere Werte aufweisen, doch wenn Sie das Tag auf eine Ressource oder eine Ressourcengruppe anwenden, wenden Sie den Tagnamen und nur einen seiner Werte an.
So können Sie beispielsweise eine vordefinierte Abteilungs Kategorie mit einem Wert für jede Abteilung erstellen, beispielsweise Finance, Personalwesen und IT.
Wenn Sie die Kategorie "Abteilung" auf eine Ressource anwenden, wenden Sie nur einen vordefinierten Wert wie "Finance" an.

**CreateByResourceIdParameterSet** : das Cmdlet **New-AzTag** mit einer **Resourcen** -Kennung erstellt oder aktualisiert den gesamten Satz von Tags für eine Ressource oder ein Abonnement.
Dieser Vorgang ermöglicht das Hinzufügen oder Ersetzen der gesamten Gruppe von Tags für die angegebene Ressource oder das angegebene Abonnement. Die angegebene Entität kann maximal 50-Tags enthalten.

## Beispiele

### Beispiel 1: Erstellen eines vordefinierten Tags
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

Dieser Befehl erstellt ein vordefiniertes Tag mit dem Namen FY2015.
Dieses Tag hat keine Werte.
Sie können eine Kategorie ohne Werte auf eine Ressource oder eine Ressourcengruppe anwenden oder mithilfe von **New-AzTag** dem Tag Werte hinzufügen.
Sie können auch einen Wert angeben, wenn Sie die Kategorie auf die Ressourcen-oder Ressourcengruppe anwenden.

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

Mit diesem Befehl wird eine vordefinierte Kategorie mit dem Namen "Department" mit dem Wert "Finance" erstellt.

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

Mit diesen Befehlen wird ein vordefiniertes Tag mit dem Namen Department mit zwei Werten erstellt.
Wenn der Tag-Name vorhanden ist, fügt **New-AzTag** den Wert dem vorhandenen Tag hinzu, anstatt eine neue zu erstellen.

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

Mit den Befehlen in diesem Beispiel wird ein vordefiniertes Tag erstellt und verwendet.

### Beispiel 5: Erstellen oder Aktualisieren der gesamten Gruppe von Tags in einem Abonnement

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

### Beispiel 6: Erstellen oder Aktualisieren der gesamten Gruppe von Tags für eine Ressource

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

Mit diesem Befehl wird der gesamte Satz von Tags für die Ressource mit {Ressourcenkennung} erstellt oder aktualisiert.

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
Gibt den vordefinierten Tagnamen an.
Wenn Sie ein neues vordefiniertes Tag erstellen möchten, geben Sie einen eindeutigen Namen ein.
Wenn Sie einen Wert zu einer vorhandenen Kategorie hinzufügen möchten, geben Sie den Namen des vorhandenen Tags ein.
Wenn ein vorhandenes vordefiniertes Tag den angegebenen Namen aufweist, fügt **New-AzTag** den angegebenen Wert, falls vorhanden, dem Tag mit diesem Namen hinzu, anstatt eine neue Kategorie zu erstellen.

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
Gibt einen vordefinierten Tag-Wert an.
Vordefinierte Tags können mehrere Werte haben, aber Sie können in jedem Befehl nur einen Wert eingeben.
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

### -Resourcen-Nr
Der Ressourcenbezeichner für die Entität, die markiert wird. Eine Ressource, eine Ressourcengruppe oder ein Abonnement können markiert sein.

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
Die Tags, die auf die Ressource gesetzt werden sollen.

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

### System. Collections. Hashtable

## Ausgaben

### Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag | Microsoft. Azure. Commands. Tags. Model. PSTagResource

## Notizen

## Verwandte Links

[Get-AzTag](./Get-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

[Update-AzTag](./Update-AzTag.md)
