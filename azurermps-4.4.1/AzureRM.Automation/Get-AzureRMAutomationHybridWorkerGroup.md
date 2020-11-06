---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9B0BBBB4-A7A0-4243-9264-362A00F5B399
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationHybridWorkerGroup.md
ms.openlocfilehash: 1f2c82bc51cb5faba9f5b1dd0524e7aced2f0b84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500969"
---
# Get-AzureRMAutomationHybridWorkerGroup

## Synopsis
Ruft Hybrid-runbooks-Arbeitsgruppen ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Seitensaller (Standard)
```
Get-AzureRMAutomationHybridWorkerGroup [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzureRMAutomationHybridWorkerGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmAutomationHybridWorkerGroup** " ruft Azure Automation Hybrid runbooks Worker Groups ab.
Um eine bestimmte Gruppe zu erhalten, geben Sie den Namen an.

## Beispiele

### Beispiel 1: Abrufen aller Hybrid runbooks Worker-Gruppen
```
PS C:\>Get-AzureRMAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17"
```

Dieser Befehl ruft alle Hybriden runbooks-Arbeitsgruppen im Automatisierungs Konto mit dem Namen Contoso17 ab.

### Beispiel 2: Abrufen einer einzelnen Hybriden runbooks Worker-Gruppe
```
PS C:\>Get-AzureRMAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17" -Name "HybridRunbookWorkerGroup01"
```

Dieser Befehl ruft die Hybrid-runbooks-Arbeitsgruppe mit dem Namen HybridRunbookWorkerGroup01 im Automatisierungs Konto mit dem Namen Contoso17 ab.

### Beispiel 3: Abrufen der Arbeitskräfte in einer hybriden runbooks Worker-Gruppe
```
PS C:\>(Get-AzureRMAutomationHybridWorker -ResourceGroupName ResourceGroupName01 -AutomationAccountName Contoso17 -Name "HybridRunbookWorkerGroup01" ).RunbookWorker
```

Dieser Befehl ruft die Hybrid-runbooks-worker in der Hybrid-runbooks-Arbeitsgruppe mit dem Namen HybridRunbookWorkerGroup01 im Automatisierungs Konto mit dem Namen Contoso17 ab.

## Parameter

### -AutomationAccountName
Gibt den Namen eines Automatisierungs Kontos an.

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

### -Name
Gibt den Namen der Hybriden runbooks-Arbeitsgruppe an.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Group

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an.

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

### Zeichenfolge
Der Parameter "Name" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.

## Ausgaben

### Microsoft. Azure. Commands. Automation. Model. HybridRunbookWorker

## Notizen

## Verwandte Links

