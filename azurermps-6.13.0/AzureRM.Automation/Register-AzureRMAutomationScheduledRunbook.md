---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F79AFF9A-CEDA-4E57-B5DB-9D0A7CDA6D27
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/register-azurermautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: deb6611fedbb1f88b9668b4750e096056ea8b1b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663013"
---
# Register-AzureRmAutomationScheduledRunbook

## Synopsis
Ordnet eine runbooks einem Terminplan zu.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ByRunbookName (Standard)
```
Register-AzureRmAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByRunbookNameAndScheduleName
```
Register-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-Parameters <IDictionary>] [-RunOn <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Register-AzureRmAutomationScheduledRunbook** " ordnet eine Azure Automation-runbooks einem Terminplan zu.
Der runbooks beginnt basierend auf dem von Ihnen angegebenen Zeitplan mithilfe des *ScheduleName* -Parameters.

## Beispiele

### Beispiel 1: Zuordnen eines runbooks zu einem Terminplan
```
PS C:\>Register-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01" -ResourceGroupName "ResourceGroup01"
```

Dieser Befehl ordnet die runbooks mit dem Namen Runbk01 dem Zeitplan mit dem Namen "Sched01" im Azure Automation-Konto mit dem Namen "Contoso17" zu.

## Parameter

### -AutomationAccountName
Gibt ein Automatisierungs Konto für das runbooks an, auf dem dieses Cmdlet ausgeführt wird.

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

### -Parameter
Gibt eine Hashtabelle mit Schlüssel-Wert-Paaren an.
Die Schlüssel sind runbooks-Parameternamen.
Die Werte sind runbooks-Parameterwerte.
Wenn der runbooks als Antwort auf den zugeordneten Zeitplan gestartet wird, werden diese Parameter an den runbooks übergeben.

```yaml
Type: System.Collections.IDictionary
Parameter Sets: ByRunbookNameAndScheduleName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe für den geplanten runbooks an.

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
Gibt den Namen der runbooks an, die dieses Cmdlet einem Terminplan zuordnet.

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RunOn
Der Name der Hybriden runbooks-Arbeitsgruppe.

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScheduleName
Gibt den Namen des Zeitplans an, dem dieses Cmdlet eine runbooks zugeordnet hat.

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. Automation. Model. JobSchedule

## Notizen

## Verwandte Links

[Get-AzureRmAutomationScheduledRunbook](./Get-AzureRMAutomationScheduledRunbook.md)

[Registrierung aufheben-AzureRmAutomationScheduledRunbook](./Unregister-AzureRMAutomationScheduledRunbook.md)


