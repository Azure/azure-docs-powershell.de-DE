---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
ms.openlocfilehash: 5e0766039a9becb65aaec13d08e46f751893b8dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499921"
---
# Get-AzureRmTag

## Synopsis
Ruft vordefinierte Azure-Tags ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmTag** " ruft vordefinierte Azure-Tags in Ihrem Abonnement ab.
Dieses Cmdlet gibt grundlegende Informationen zu den Tags oder detaillierte Informationen zu Tags und deren Werten zurück.
Alle Ausgabeobjekte enthalten eine Count-Eigenschaft, die die Anzahl der Ressourcen und Ressourcengruppen darstellt, auf die die Kategorien und Werte angewendet wurden.

Das Azure-Tags-Modul, in dem **Get-AzureRMTag** enthalten ist, kann Ihnen helfen, vordefinierte Azure-Tags zu verwalten.
Bei einem Azure-Tag handelt es sich um ein Name-Wert-Paar, mit dem Sie Ihre Azure-Ressourcen und Ressourcengruppen kategorisieren können, beispielsweise nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu Ressourcen und Gruppen zu überwachen.

Sie können Tags in einem einzigen Schritt definieren und anwenden, doch mit vordefinierten Tags können Sie standardmäßige, konsistente, vorhersagbare Namen und Werte für die Tags in Ihrem Abonnement einrichten.
Wenn das Abonnement vordefinierte Tags enthält, können Sie nicht definierte Tags oder Werte auf eine Ressource oder eine Ressourcengruppe im Abonnement anwenden.

Verwenden Sie das New-AzureRmTag-Cmdlet, um eine vordefinierte Kategorie zu erstellen.
Wenn Sie eine vordefinierte Kategorie auf eine Ressourcengruppe anwenden möchten, verwenden Sie den *Tag* -Parameter des New-AzureRmTag-Cmdlets.
Verwenden Sie den *Tag* -Parameter des Get-AzureRMResourceGroup-Cmdlets, um Ressourcengruppen nach einem bestimmten Tag-Namen oder-Namen und-Wert zu durchsuchen.

## Beispiele

### Beispiel 1: Abrufen aller vordefinierten Tags
```
PS C:\>Get-AzureRmTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

Dieser Befehl ruft alle vordefinierten Tags im Abonnement ab.
Die Count-Eigenschaft zeigt, wie oft das Tag auf Ressourcen und Ressourcengruppen im Abonnement angewendet wurde.

### Beispiel 2: Abrufen einer Kategorie nach Name
```
PS C:\>Get-AzureRmTag -Name "Department"

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
```
PS C:\>Get-AzureRmTag -Detailed

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

## Parameter

### -Detailliert
Gibt an, dass dieser Vorgang der Ausgabe Informationen zu Transponder Werten hinzufügt.

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

### -Name
Gibt den Namen des abzurufenden Transponders an.
Standardmäßig ruft **Get-AzureRmTag** grundlegende Informationen zu allen vordefinierten Tags im Abonnement ab.
Wenn Sie den Parameter *Name* angeben, hat der *Detail* Parameter keine Auswirkungen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
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

### Microsoft. Azure. Commands. Tags. Model. PSTag, Microsoft. Azure. Commands. Tags

## Notizen

## Verwandte Links

[Neu – AzureRmTag](./New-AzureRmTag.md)

[Remove-AzureRmTag](./Remove-AzureRmTag.md)


