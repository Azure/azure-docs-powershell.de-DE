---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJob.md
ms.openlocfilehash: 4509190a8417379c9d5bc9eae9d6d12609def4aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505682"
---
# Get-AzureRmAutomationJob

## Synopsis
Ruft Automatisierungs runbooks Aufträge ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Seitensaller (Standard)
```
Get-AzureRmAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByJobId
```
Get-AzureRmAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByRunbookName
```
Get-AzureRmAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmAutomationJob** " ruft runbooks-Aufträge in Azure-Automatisierung ab.

## Beispiele

### Beispiel 1: Abrufen eines bestimmten runbooks-Auftrags
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

Dieser Befehl ruft den Auftrag ab, der die angegebene GUID aufweist.

### Beispiel 2: Abrufen aller Aufträge für eine runbooks
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

Dieser Befehl ruft alle Aufträge ab, die einem runbooks mit dem Namen Runbook02 zugeordnet sind.

### Beispiel 3: Abrufen aller ausgeführten Aufträge
```
PS C:\>Get-AzureRmAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

Dieser Befehl ruft alle ausgeführten Aufträge im Automatisierungs Konto mit dem Namen Contoso17 ab.

## Parameter

### -AutomationAccountName
Gibt den Namen eines Automatisierungs Kontos an, für das dieses Cmdlet Aufträge erhält.

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

### -EndTime
Gibt die Endzeit für einen Auftrag als **DateTimeOffset** -Objekt an.
Sie können eine Zeichenfolge angeben, die in einen gültigen **DateTimeOffset** konvertiert werden kann.
Dieses Cmdlet ruft Aufträge ab, die eine Endzeit am oder vor dem Wert aufweisen, den dieser Parameter angibt.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Gibt die ID eines Auftrags an, den dieses Cmdlet erhält.

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet Aufträge erhält.

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
Gibt den Namen einer runbooks an, für die dieses Cmdlet Aufträge erhält.

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Startzeit
Gibt die Startzeit eines Auftrags als **DateTimeOffset** -Objekt an.
Dieses Cmdlet ruft Aufträge ab, die eine Startzeit am oder hinter dem Wert haben, den dieser Parameter angibt.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status
Gibt den Status eines Auftrags an.
Dieses Cmdlet ruft Aufträge ab, deren Status diesem Parameter entspricht.
Gültige Werte sind: 

- Aktivieren
- Abgeschlossen
- Fehlgeschlagen
- Queued
- Wieder
- Ausgeführt
- Ausgangs
- Funktioniert nicht mehr
- Beenden
- Ausgesetzt
- Suspending

```yaml
Type: System.String
Parameter Sets: ByAll, ByRunbookName
Aliases: 
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

## Ausgaben

### Microsoft. Azure. Commands. Automation. Model. Job

## Notizen

## Verwandte Links

[Get-AzureRmAutomationJobOutput](./Get-AzureRMAutomationJobOutput.md)

[Lebenslauf-AzureRmAutomationJob](./Resume-AzureRMAutomationJob.md)

[Stopp-AzureRmAutomationJob](./Stop-AzureRMAutomationJob.md)

[Suspend-AzureRmAutomationJob](./Suspend-AzureRMAutomationJob.md)


