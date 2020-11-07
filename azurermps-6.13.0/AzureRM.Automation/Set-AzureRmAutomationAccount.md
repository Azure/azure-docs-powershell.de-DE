---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
ms.openlocfilehash: 7a0341221dee0f282508377d1233e30deae1fcee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662194"
---
# Set-AzureRmAutomationAccount

## Synopsis
Ändert ein Automatisierungs Konto.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Set-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>]
 [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureRmAutomationAccount** " ändert ein Azure-Automatisierungs Konto.
Weitere Informationen zu Automatisierungs Konten finden Sie unter New-AzureRmAutomationAccount-Cmdlet.

## Beispiele

### Beispiel 1: Einrichten der Tags für ein Automatisierungs Konto
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

Der erste Befehl weist der $Tags-Variablen zwei Schlüssel-Wert-Paare zu.
Der zweite Befehl legt Tags in $Tags für das Automatisierungs Konto mit dem Namen "AutomationAccount01" fest.

### Beispiel 2: Ändern des Plans für ein Automatisierungs Konto
```
PS C:\>Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

Dieser Befehl ändert den Plan in Basic für das Automatisierungs Konto mit dem Namen AutomationAccount01.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -Name
Gibt den Namen des Automatisierungs Kontos an, das von diesem Cmdlet geändert wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Plan
Gibt den Plan für das Automatisierungs Konto an.
Gültige Werte sind:
- Grundlegende
- Kostenlos

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe an, die das Automatisierungs Konto enthält, das von diesem Cmdlet geändert wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tags
Schlüssel-Wert-Paare in Form einer Hashtabelle Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

### System. Collections. IDictionary

## Ausgaben

### Microsoft. Azure. Commands. Automation. Model. AutomationAccount

## Notizen

## Verwandte Links

[Get-AzureRmAutomationAccount](./Get-AzureRmAutomationAccount.md)

[Neu – AzureRmAutomationAccount](./New-AzureRmAutomationAccount.md)

[Remove-AzureRmAutomationAccount](./Remove-AzureRmAutomationAccount.md)
