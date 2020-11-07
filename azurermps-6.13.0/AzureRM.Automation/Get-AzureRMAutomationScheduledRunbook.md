---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EE854F8A-4B6B-4831-992A-6EC318BEE234
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: e2b458e7a1f739b7891768d197f1993da065d09f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663698"
---
# Get-AzureRmAutomationScheduledRunbook

## Synopsis
Ruft Automatisierungs runbooks und zugeordnete Zeitpläne ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Seitensaller (Standard)
```
Get-AzureRmAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByJobScheduleId
```
Get-AzureRmAutomationScheduledRunbook -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByRunbookName
```
Get-AzureRmAutomationScheduledRunbook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByRunbookNameAndScheduleName
```
Get-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByScheduleName
```
Get-AzureRmAutomationScheduledRunbook -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmAutomationScheduledRunbook** " Ruft einen oder mehrere Azure Automation-runbooks und zugeordnete Zeitpläne ab.
Standardmäßig ruft dieses Cmdlet alle geplanten runbooks ab.
Geben Sie den Namen eines runbooks oder einen Terminplan oder beides an, um bestimmte runbooks-Zeitpläne anzuzeigen.

## Beispiele

### Beispiel 1: Abrufen aller geplanten runbooks
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

Dieser Befehl ruft alle geplanten runbooks im Azure Automation-Konto mit dem Namen Contoso17 ab.

### Beispiel 2: Abrufen aller einem runbooks zugeordneten Zeitpläne
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbk01"
```

Dieser Befehl ruft alle geplanten runbooks für das runbooks-Runbk01 im Azure-Automatisierungs Konto mit dem Namen Contoso17 ab.

### Beispiel 3: Abrufen aller runbooks, die einem Terminplan zugeordnet sind
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ScheduleName "Schedule01"
```

Dieser Befehl ruft alle geplanten runbooks für den Terminplan-Schedule01 im Azure-Automatisierungs Konto mit dem Namen Contoso17 ab.

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

### -JobScheduleId
Gibt die ID eines geplanten Auftrags an, den dieses Cmdlet erhält.

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByJobScheduleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe für geplante runbooks an, die dieses Cmdlet erhält.

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
Gibt den Namen einer runbooks an, für die dieses Cmdlet geplante runbooks erhält.

```yaml
Type: System.String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScheduleName
Gibt den Namen eines Zeitplans an, für den dieses Cmdlet geplante runbooks erhält.

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
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

### System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

### System. String

## Ausgaben

### Microsoft. Azure. Commands. Automation. Model. JobSchedule

## Notizen

## Verwandte Links

[Registrieren-AzureRmAutomationScheduledRunbook](./Register-AzureRMAutomationScheduledRunbook.md)

[Registrierung aufheben-AzureRmAutomationScheduledRunbook](./Unregister-AzureRMAutomationScheduledRunbook.md)


