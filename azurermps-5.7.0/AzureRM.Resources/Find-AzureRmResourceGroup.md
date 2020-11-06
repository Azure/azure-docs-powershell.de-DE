---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: EFBBFB60-D972-47B8-997E-B737F0CA007E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/find-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
ms.openlocfilehash: 42e268a36cf6ea45d4a36ef1a7c3edd825c6e8ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498869"
---
# Find-AzureRmResourceGroup

## Synopsis
Sucht nach Ressourcengruppen.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Find-AzureRmResourceGroup [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Suchen-AzureRmResourceGroup** " sucht nach Ressourcengruppen, wobei die angegebenen Parameter verwendet werden.

## Beispiele

### Beispiel 1: Suchen nach allen Ressourcengruppen
```
PS C:\>Find-AzureRmResourceGroup
```

Dieser Befehl findet alle Ressourcengruppen.

### Beispiel 2: Suchen nach Ressourcengruppen nach Tag-Name
```
PS C:\>Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
```

Dieser Befehl findet alle Ressourcengruppen, die eine Kategorie mit dem Namen "Testtag" aufweisen.

### Beispiel 3: Suchen von Ressourcengruppen nach Tag-Name und-Wert
```
PS C:\>Find-AzureRmResourceGroup -Tag @{"testtag" = "testval" }
```

Dieser Befehl findet alle Ressourcengruppen mit dem Tag Testtag und dem Wert testVal.

## Parameter

### -ApiVersion
Gibt die Version der zu verwendenden Ressourcenanbieter-API an. Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -Pre
Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Gibt Tag-Informationen als Hashtabelle an, um die Ergebnisse zu filtern. Verwenden Sie die folgenden Formate:

@ {Tagname = $NULL} oder @ {Tagname = ' tagValue '}.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### System. Management. Automation. PSObject

## Notizen

## Verwandte Links
