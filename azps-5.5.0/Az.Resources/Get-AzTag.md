---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: 058f4a61f1e7ff2fe7f416ea0e4ada098c9efe51
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172068"
---
# Get-AzTag

## SYNOPSIS
Ruft vordefinierte Azure-Tags-| Ruft die gesamte Gruppe von Tags für eine Ressource oder ein Abonnement ab.

## SYNTAX

### GetPredefinedTagParameterSet
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceIdParameterSet
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG

**GetPredefinedTagSet**: Das **Cmdlet "Get-AzTag"** ruft vordefinierte #A0 in Ihrem Abonnement ab.
Dieses Cmdlet gibt grundlegende Informationen zu den Kategorien oder detaillierte Informationen zu Tags und deren Werten zurück.
Alle Ausgabeobjekte enthalten eine Count-Eigenschaft, die die Anzahl der Ressourcen und Ressourcengruppen darstellt, auf die die Tags und Werte angewendet wurden.
Das Azure-Tags-Modul, **zu dem "Get-AzTag"** gehört, kann Sie bei der Verwaltung vordefinierter #A0 unterstützen.
Ein Azure-Tag ist ein Name-Wert-Paar, mit dem Sie Ihre Azure-Ressourcen und -Ressourcengruppen kategorisieren können, z. B. nach Abteilung oder Kostencenter, oder um Notizen oder Kommentare zu den Ressourcen und Gruppen nachverfolgt werden.
Sie können Tags in einem einzigen Schritt definieren und anwenden, aber mit vordefinierten Tags können Sie standardübliche, konsistente, vorhersehbare Namen und Werte für die Tags in Ihrem Abonnement festlegen.
Verwenden Sie zum Erstellen eines vordefinierten Tags das cmdlet New-AzTag-Cmdlet.
Wenn Sie eine vordefinierte Markierung auf eine Ressourcengruppe anwenden möchten, verwenden Sie den *Parameter "Tag"* des New-AzTag Cmdlets.
Um Ressourcengruppen nach einem bestimmten Tagnamen oder -namen und Wert zu durchsuchen, verwenden Sie den *Parameter "Tag"* des Get-AzResourceGroup Cmdlets.

**GetByResourceIdParameterSet**: Das **Cmdlet "Get-AzTag"** mit einer **ResourceId** ruft den gesamten Satz von Tags für eine Ressource oder ein Abonnement ab.

## BEISPIELE

### Beispiel 1: Alle vordefinierten Tags erhalten
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

Dieser Befehl ruft alle vordefinierten Tags im Abonnement ab.
Die Eigenschaft "Anzahl" zeigt an, wie oft das Tag auf Ressourcen und Ressourcengruppen im Abonnement angewendet wurde.

### Beispiel 2: Tag nach Name erhalten
```powershell
PS C:\>Get-AzTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

Dieser Befehl ruft detaillierte Informationen über das Tag "Department" und dessen Werte ab.
Die Eigenschaft "Anzahl" zeigt an, wie oft das Tag und die einzelnen Werte auf Ressourcen und Ressourcengruppen im Abonnement angewendet wurden.

### Beispiel 3: Erhalten von Werten aller Tags
```powershell
PS C:\>Get-AzTag -Detailed

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3


Name:   FY2015
Count:  2


Name:   CostCenter
Count:  20
Values: 

        Name        Count
        ==========  =====

        0001          5
        0002         10
        0003          5
```

Dieser Befehl verwendet den *Parameter "Detailed",* um detaillierte Informationen zu allen vordefinierten Tags im Abonnement zu erhalten.
Die Verwendung *des Parameters "Detailed"* entspricht der Verwendung des *Namensparameters* für jedes Tag.

### Beispiel 4: Den gesamten Satz markierungen für ein Abonnement erhalten

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

Dieser Befehl ruft die gesamte Gruppe von Tags für das Abonnement mit {subId} ab.

### Beispiel 5: Den gesamten Satz von Tags für eine Ressource erhalten

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

Dieser Befehl ruft die gesamte Gruppe von Tags für die Ressource mit {resourceId} ab.

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

### -Detailliert
Gibt an, dass dieser Vorgang der Ausgabe Informationen zu Tagwerten hinzufügt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Name des vordefinierten Tags.
Standardmäßig ruft **Get-AzTag** grundlegende Informationen zu allen vordefinierten Tags im Abonnement ab.
Wenn Sie den Parameter *"Name"* angeben, hat der *Parameter "Detailed"* keine Auswirkung.

```yaml
Type: System.String
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Der Ressourcenbezeichner für die markierte Entität. Möglicherweise ist eine Ressource, eine Ressourcengruppe oder ein Abonnement markiert.

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

### System.Management.Automation.SwitchParameter

## AUSGABEN

### Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[New-AzTag](./New-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

[Update-AzTag](./Update-AzTag.md)
