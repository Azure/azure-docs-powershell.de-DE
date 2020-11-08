---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: 058f4a61f1e7ff2fe7f416ea0e4ada098c9efe51
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003986"
---
# Get-AzTag

## Synopsis
Ruft vordefinierte Azure-Tags ab | Ruft den gesamten Satz von Tags für eine Ressource oder ein Abonnement ab.

## Syntax

### GetPredefinedTagParameterSet
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceIdParameterSet
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung

**GetPredefinedTagSet** : mit dem Cmdlet **Get-AzTag werden** in Ihrem Abonnement vordefinierte Azure-Tags abgerufen.
Dieses Cmdlet gibt grundlegende Informationen zu den Tags oder detaillierte Informationen zu Tags und deren Werten zurück.
Alle Ausgabeobjekte enthalten eine Count-Eigenschaft, die die Anzahl der Ressourcen und Ressourcengruppen darstellt, auf die die Kategorien und Werte angewendet wurden.
Das Azure-Tags-Modul, in dem **Get-AzTag** enthalten ist, kann Ihnen helfen, vordefinierte Azure-Tags zu verwalten.
Bei einem Azure-Tag handelt es sich um ein Name-Wert-Paar, mit dem Sie Ihre Azure-Ressourcen und Ressourcengruppen kategorisieren können, beispielsweise nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu Ressourcen und Gruppen zu überwachen.
Sie können Tags in einem einzigen Schritt definieren und anwenden, doch mit vordefinierten Tags können Sie standardmäßige, konsistente, vorhersagbare Namen und Werte für die Tags in Ihrem Abonnement einrichten.
Verwenden Sie das New-AzTag-Cmdlet, um eine vordefinierte Kategorie zu erstellen.
Wenn Sie eine vordefinierte Kategorie auf eine Ressourcengruppe anwenden möchten, verwenden Sie den *Tag* -Parameter des New-AzTag-Cmdlets.
Verwenden Sie den *Tag* -Parameter des Get-AzResourceGroup-Cmdlets, um Ressourcengruppen nach einem bestimmten Tag-Namen oder-Namen und-Wert zu durchsuchen.

**GetByResourceIdParameterSet** : das Cmdlet " **Get-AzTag** " mit einer Ressourcen **Quelle** Ruft den gesamten Satz von Tags für eine Ressource oder ein Abonnement ab.

## Beispiele

### Beispiel 1: Abrufen aller vordefinierten Tags
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

Dieser Befehl ruft alle vordefinierten Tags im Abonnement ab.
Die Count-Eigenschaft zeigt, wie oft das Tag auf Ressourcen und Ressourcengruppen im Abonnement angewendet wurde.

### Beispiel 2: Abrufen einer Kategorie nach Name
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

Dieser Befehl erhält detaillierte Informationen über das Department-Tag und seine Werte.
Die Count-Eigenschaft zeigt an, wie oft das Tag und jeder seiner Werte auf Ressourcen und Ressourcengruppen im Abonnement angewendet wurde.

### Beispiel 3: Abrufen von Werten aller Tags
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

Dieser Befehl verwendet den *detaillierten* Parameter, um detaillierte Informationen zu allen vordefinierten Tags im Abonnement abzurufen.
Die Verwendung des Parameters *detaillierte* entspricht der Verwendung des Parameters *Name* für jedes Tag.

### Beispiel 4: Abrufen der gesamten Gruppe von Transpondern in einem Abonnement

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

### Beispiel 5: Abrufen der gesamten Gruppe von Tags für eine Ressource

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

Mit diesem Befehl wird der gesamte Satz von Tags für die Ressource mit {Ressourcenkennung} abgerufen.

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

### -Detailliert
Gibt an, dass dieser Vorgang der Ausgabe Informationen zu Transponder Werten hinzufügt.

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
Der Name des vordefinierten Tags.
Standardmäßig ruft **Get-AzTag** grundlegende Informationen zu allen vordefinierten Tags im Abonnement ab.
Wenn Sie den Parameter *Name* angeben, hat der *Detail* Parameter keine Auswirkungen.

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

### -Resourcen-Nr
Der Ressourcenbezeichner für die markierte Entität. Eine Ressource, eine Ressourcengruppe oder ein Abonnement können markiert sein.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

### System. Management. Automation. Switchparameter

## Ausgaben

### Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag | Microsoft. Azure. Commands. Tags. Model. PSTagResource

## Notizen

## Verwandte Links

[Neu – AzTag](./New-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)

[Update-AzTag](./Update-AzTag.md)
