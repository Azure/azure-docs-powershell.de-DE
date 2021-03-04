---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: b44c861e06c1043fd53e470cfba1e322ce1f1f48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939416"
---
# Get-AzTag

## SYNOPSIS
Ruft vordefinierte Azure-Tags | Ruft den gesamten Satz von Tags für eine Ressource oder ein Abonnement ab.

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

**GetPredefinedTagSet:** Das **Get-AzTag-Cmdlet** ruft vordefinierte #A0 in Ihrem Abonnement ab.
Dieses Cmdlet gibt grundlegende Informationen zu den Tags oder detaillierte Informationen zu Tags und deren Werten zurück.
Alle Ausgabeobjekte enthalten eine Count-Eigenschaft, die die Anzahl der Ressourcen und Ressourcengruppen darstellt, auf die die Tags und Werte angewendet wurden.
Das Azure-Tags-Modul, zu dem **Get-AzTag** gehört, kann Ihnen bei der Verwaltung vordefinierter #A0 helfen.
Ein Azure-Tag ist ein Namen-Wert-Paar, das Sie verwenden können, um Ihre Azure-Ressourcen und Ressourcengruppen zu kategorisieren, z. B. nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu den Ressourcen und Gruppen nachverfolgt zu werden.
Sie können Tags in einem einzigen Schritt definieren und anwenden, aber mit vordefinierten Tags können Sie standardmäßige, konsistente, vorhersagbare Namen und Werte für die Tags in Ihrem Abonnement festlegen.
Zum Erstellen eines vordefinierten Tags verwenden Sie das New-AzTag Cmdlet.
Verwenden Sie zum Anwenden eines vordefinierten Tags auf eine Ressourcengruppe den *Parameter Tag* des New-AzTag Cmdlets.
Wenn Sie Ressourcengruppen nach einem bestimmten Tagnamen oder -namen und -wert durchsuchen möchten, verwenden Sie den *Parameter Tag* des cmdlets Get-AzResourceGroup cmdlet.

**GetByResourceIdParameterSet**: Das **Get-AzTag-Cmdlet** mit **einer ResourceId** ruft den gesamten Satz von Tags für eine Ressource oder ein Abonnement ab.

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
Die Count-Eigenschaft zeigt an, wie oft das Tag auf Ressourcen und Ressourcengruppen im Abonnement angewendet wurde.

### Beispiel 2: Erhalten eines Tags nach Name
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

Dieser Befehl ruft detaillierte Informationen zum Tag "Department" und deren Werten ab.
Die Count-Eigenschaft zeigt an, wie oft das Tag und jeder seiner Werte auf Ressourcen und Ressourcengruppen im Abonnement angewendet wurde.

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

Dieser Befehl verwendet den *Parameter Detail,* um detaillierte Informationen zu allen vordefinierten Tags im Abonnement zu erhalten.
Die Verwendung *des Parameters* Detail entspricht der Verwendung des *Parameters Name* für jedes Tag.

### Beispiel 4: Erhalten der gesamten Gruppe von Tags für ein Abonnement

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

Mit diesem Befehl wird der gesamte Satz von Tags für das Abonnement mit {subId} abgerufen.

### Beispiel 5: Gesamte Gruppe von Tags für eine Ressource

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

Mit diesem Befehl wird der gesamte Satz von Tags für die Ressource mit {resourceId} abgerufen.

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

### -Detailliert
Gibt an, dass mit diesem Vorgang Informationen zu Tagwerten zur Ausgabe addiert werden.

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
Wenn Sie den *Parameter Name angeben,* hat der *Parameter Detail* keine Auswirkung.

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
Der Ressourcenbezeichner für die markierte Entität. Eine Ressource, eine Ressourcengruppe oder ein Abonnement kann markiert werden.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### System.String

### System.Management.Automation.SwitchParameter

## AUSGABEN

### Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource

## NOTIZEN

## VERWANDTE LINKS

[New-AzTag](./New-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

[Update-AzTag](./Update-AzTag.md)
