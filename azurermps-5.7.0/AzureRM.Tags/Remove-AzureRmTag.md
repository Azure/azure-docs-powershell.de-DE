---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/remove-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
ms.openlocfilehash: f51411c4683a79283ad5e0a73554f6db3ce7e52e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662206"
---
# Remove-AzureRmTag

## Synopsis
Löscht vordefinierte Azure-Tags oder-Werte.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Remove-AzureRmTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureRmTag** löscht vordefinierte Azure-Tags und-Werte aus Ihrem Abonnement.
Verwenden Sie den *value* -Parameter, um bestimmte Werte aus einem vordefinierten Tag zu löschen.
Standardmäßig löscht **Remove-AzureRmTag** das angegebene Tag und alle seine Werte. Sie können eine Kategorie oder einen Wert, der aktuell auf eine Ressource oder eine Ressourcengruppe angewendet wird, nicht löschen.

Verwenden Sie vor der Verwendung von **Remove-AzureRmTag** den *Tag* -Parameter des Set-AzureRMResourceGroup-Cmdlets, um das Tag oder die Werte aus der Ressourcen-oder Ressourcengruppe zu löschen.

Das Azure-Tags-Modul, in dem **Remove-AzureRmTag** enthalten ist, kann Ihnen bei der Verwaltung Ihrer vordefinierten Azure-Tags helfen.
Bei einem Azure-Tag handelt es sich um ein Name-Wert-Paar, mit dem Sie Ihre Azure-Ressourcen und Ressourcengruppen kategorisieren können, beispielsweise nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu Ressourcen und Gruppen zu überwachen.

Sie können Tags in einem einzigen Schritt definieren und anwenden, doch mit vordefinierten Tags können Sie standardmäßige, konsistente, vorhersagbare Namen und Werte für die Tags in Ihrem Abonnement einrichten.
Wenn das Abonnement vordefinierte Tags enthält, können Sie nicht definierte Tags oder Werte auf eine Ressource oder eine Ressourcengruppe im Abonnement anwenden.

## Beispiele

### Beispiel 1: Löschen eines vordefinierten Tags
```
PS C:\>Remove-AzureRmTag -Name "Department"
```

Mit diesem Befehl wird das vordefinierte Tag "Department" und alle zugehörigen Ressourcen gelöscht.
Wenn das Tag auf Ressourcen oder Ressourcengruppen angewendet wurde, schlägt der Befehl fehl.

### Beispiel 2: Löschen eines Werts aus einem vordefinierten Tag
```
PS C:\>Remove-AzureRmTag -Name "Department" -Value "HumanResources" -PassThru
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
Gibt den Namen der zu löschenden Kategorie an.
Standardmäßig entfernt **Remove-AzureRmTag** das angegebene Tag und alle seine Werte.
Verwenden Sie den *Wert* -Parameter, um ausgewählte Werte zu löschen, aber die Kategorie nicht zu löschen.

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

### -PassThru
Gibt ein Objekt zurück, das das gelöschte Tag oder das resultierende Tag mit gelöschten Werten darstellt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Wert
Löscht die angegebenen Werte aus dem vordefinierten Tag, löscht das Tag aber nicht.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### None oder Microsoft. Azure. Commands. Tags. Model. PSTag

## Notizen

## Verwandte Links

[Get-AzureRmTag](./Get-AzureRmTag.md)

[Neu – AzureRmTag](./New-AzureRmTag.md)


