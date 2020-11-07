---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationWebhook.md
ms.openlocfilehash: 97b9c37613563f269ba035062ba557de810e9ec3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662196"
---
# New-AzureRmAutomationWebhook

## Synopsis
Erstellt einen webhook für ein Automatisierungs-runbooks.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureRmAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmAutomationWebhook** erstellt einen webhook für ein Azure Automation-runbooks.
Achten Sie darauf, die webhook-URL zu speichern, die dieses Cmdlet zurückgibt, da Sie nicht erneut abgerufen werden kann.

## Beispiele

### Beispiel 1: Erstellen eines webhooks
```
PS C:\>$Webhook = New-AzureRmAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

Mit diesem Befehl wird ein webhook mit dem Namen Webhook06 für den runbooks namens ContosoRunbook im Automatisierungs Konto mit dem Namen AutomationAccount01 erstellt.
Der Befehl speichert den webhook in der $Webhook-Variablen.
Der webhook ist aktiviert.
Der webhook läuft zum angegebenen Zeitpunkt ab.
Dieser Befehl bietet keine Werte für webhook-Parameter.
Mit diesem Befehl wird der *Force* -Parameter angegeben.
Daher werden Sie nicht zur Bestätigung aufgefordert.

### Beispiel 2: Erstellen eines webhooks mit Parametern
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzureRmAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

Der erste Befehl erstellt ein Wörterbuch mit Parametern und speichert Sie in der $params-Variablen.
Der zweite Befehl erstellt einen webhook mit dem Namen "Webhook11" für den runbooks namens ContosoRunbook im Automatisierungs Konto mit dem Namen AutomationAccount01.
Der Befehl weist dem webhook die Parameter in $params zu.

## Parameter

### -AutomationAccountName
Gibt den Namen eines Automatisierungs Kontos an, in dem mit diesem Cmdlet ein webhook erstellt wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -ExpiryTime
Gibt die Ablaufzeit für den webhook als **DateTimeOffset** -Objekt an.
Sie können eine Zeichenfolge oder eine **DateTime** angeben, die in einen gültigen **DateTimeOffset** -Datentyp konvertiert werden kann.

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
ps_force

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsEnabled
Gibt an, ob der webhook aktiviert ist.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt einen Namen für den webhook an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Parameter
Gibt ein Wörterbuch mit Schlüssel-Wert-Paaren an.
Die Schlüssel sind die runbooks-Parameternamen.
Die Werte sind die runbooks-Parameterwerte.
Wenn der runbooks als Antwort auf einen webhook gestartet wird, werden diese Parameter an den runbooks übergeben.

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, für die mit diesem Cmdlet ein webhook erstellt wird.

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

### -RunbookName
Gibt den Namen der runbooks an, die dem webhook zugeordnet werden soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RunOn
Optionaler Name der Hybrid Arbeitskraft Gruppe, die die runbooks ausführen soll

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

### System. Boolean

### System. DateTimeOffset

## Ausgaben

### Microsoft. Azure. Commands. Automation. Model. webhook

## Notizen

## Verwandte Links

[Get-AzureRmAutomationWebhook](./Get-AzureRMAutomationWebhook.md)

[Remove-AzureRmAutomationWebhook](./Remove-AzureRMAutomationWebhook.md)

[Satz-AzureRmAutomationWebhook](./Set-AzureRMAutomationWebhook.md)


