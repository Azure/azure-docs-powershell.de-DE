---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/new-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
ms.openlocfilehash: 77bf93905b0cba4e8f8a23cb9f3cb8945fff74f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501310"
---
# New-AzureRmTag

## Synopsis
Erstellt eine vordefinierte Azure-Kategorie oder fügt Werte zu einem vorhandenen Tag hinzu.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureRmTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmTag** erstellt ein vordefiniertes Azure-Tag mit einem optionalen vordefinierten Wert.
Sie können es auch verwenden, um zusätzliche Werte zu vorhandenen vordefinierten Tags hinzuzufügen.
Wenn Sie ein vordefiniertes Tag erstellen möchten, geben Sie einen eindeutigen Tag-Namen ein.
Wenn Sie einen Wert zu einem vorhandenen vordefinierten Tag hinzufügen möchten, geben Sie den Namen des vorhandenen Tags und den neuen Wert an.

Dieses Cmdlet gibt ein Objekt zurück, das das neue oder geänderte Tag mit seinen Werten und der Anzahl der Ressourcen darstellt, auf die es angewendet wurde.

Das Azure-Tags-Modul, in dem **New-AzureRmTag** enthalten ist, kann Ihnen dabei helfen, vordefinierte Azure-Tags zu verwalten.
Bei einem Azure-Tag handelt es sich um ein Name-Wert-Paar, mit dem Sie Ihre Azure-Ressourcen und Ressourcengruppen kategorisieren können, beispielsweise nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu Ressourcen und Gruppen zu überwachen.

Sie können Tags in einem einzigen Schritt definieren und anwenden, doch mit vordefinierten Tags können Sie standardmäßige, konsistente, vorhersagbare Namen und Werte für die Tags in Ihrem Abonnement einrichten.
Wenn das Abonnement vordefinierte Tags enthält, können Sie nicht definierte Tags oder Werte auf eine Ressource oder eine Ressourcengruppe im Abonnement anwenden.

Wenn Sie eine vordefinierte Kategorie auf eine Ressource oder eine Ressourcengruppe anwenden möchten, verwenden Sie den *Tag* -Parameter des New-AzureRmTag-Cmdlets.
Verwenden Sie den *Tag* -Parameter des Get-AzureRMResourceGroup-Cmdlets, um nach Ressourcengruppen mit einem angegebenen Tag-Namen oder-Namen und-Wert zu suchen.

Jedes Tag hat einen Namen.
Die Werte sind optional.
Ein vordefiniertes Azure-Tag kann mehrere Werte aufweisen, doch wenn Sie das Tag auf eine Ressource oder eine Ressourcengruppe anwenden, wenden Sie den Tagnamen und nur einen seiner Werte an.
So können Sie beispielsweise eine vordefinierte Abteilungs Kategorie mit einem Wert für jede Abteilung erstellen, beispielsweise Finance, Personalwesen und IT.
Wenn Sie die Kategorie "Abteilung" auf eine Ressource anwenden, wenden Sie nur einen vordefinierten Wert wie "Finance" an.

## Beispiele

### Beispiel 1: Erstellen eines vordefinierten Tags
```
PS C:\>New-AzureRmTag -Name "FY2015"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====

        Finance     0
```

Dieser Befehl erstellt ein vordefiniertes Tag mit dem Namen FY2015.
Dieses Tag hat keine Werte.
Sie können eine Kategorie ohne Werte auf eine Ressource oder eine Ressourcengruppe anwenden oder mithilfe von **New-AzureRmTag** dem Tag Werte hinzufügen.
Sie können auch einen Wert angeben, wenn Sie die Kategorie auf die Ressourcen-oder Ressourcengruppe anwenden.

### Beispiel 2: Erstellen eines vordefinierten Tags mit einem Wert
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

Mit diesem Befehl wird eine vordefinierte Kategorie mit dem Namen "Department" mit dem Wert "Finance" erstellt.

### Beispiel 3: Hinzufügen eines Werts zu einem vordefinierten Tag
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 PS C:\>New-AzureRmTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

Mit diesen Befehlen wird ein vordefiniertes Tag mit dem Namen Department mit zwei Werten erstellt.
Wenn der Tag-Name vorhanden ist, fügt **New-AzureRmTag** den Wert dem vorhandenen Tag hinzu, anstatt eine neue zu erstellen.

### Beispiel 4: Verwenden eines vordefinierten Tags
```
PS C:\>New-AzureRmTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 PS C:\>Set-AzureRmResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
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
    CostCenter   0001 PS C:\>Get-AzureRmTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 PS C:\>Get-AzureRmResourceGroup -Tag @{Name="CostCenter"}
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

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen der Kategorie an.
Wenn Sie ein neues vordefiniertes Tag erstellen möchten, geben Sie einen eindeutigen Namen ein.

Wenn Sie einen Wert zu einer vorhandenen Kategorie hinzufügen möchten, geben Sie den Namen des vorhandenen Tags ein.
Wenn ein vorhandenes vordefiniertes Tag den angegebenen Namen aufweist, fügt **New-AzureRmTag** den angegebenen Wert, falls vorhanden, dem Tag mit diesem Namen hinzu, anstatt eine neue Kategorie zu erstellen.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Wert
Gibt einen Tag-Wert an.
Vordefinierte Tags können mehrere Werte haben, aber Sie können in jedem Befehl nur einen Wert eingeben.
Dieser Parameter ist optional, da Tags Namen ohne Werte enthalten können.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### Microsoft. Azure. Commands. Tags. Model. PSTag

## Notizen

## Verwandte Links

[Get-AzureRmTag](./Get-AzureRmTag.md)

[Remove-AzureRmTag](./Remove-AzureRmTag.md)


