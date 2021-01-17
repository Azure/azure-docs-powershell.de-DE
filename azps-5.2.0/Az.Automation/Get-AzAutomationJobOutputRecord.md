---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: 7bece0fd2a9de822a5fa2a513fc06d4d20d96e4c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373833"
---
# Get-AzAutomationJobOutputRecord

## SYNOPSIS
Ruft die vollständige Ausgabe eines Ausgabedatensatzs für einen Automatisierungsauftrag ab.

## SYNTAX

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzAutomationJobOutputRecord"** ruft die vollständige Ausgabe eines Ausgabedatensatz für einen Automatisierungsauftrag ab.
Obwohl das **Cmdlet "Get-AzAutomationJobOutput"** einen oder mehrere Auftragsausgabedatensätze auflistet, gibt es nur eine Zusammenfassung als Zeichenfolge des Werts eines ausgabedatensatz zurück.
Es gibt nicht den vollständigen Wert des ausgegebenen Werts eines Ausgabedatensatzs im ursprünglichen Typ zurück.
Darüber hinaus hat die Zusammenfassung eine maximale Länge, die der vollständige Wert, den dieses Cmdlet ausausgabet, möglicherweise überschreitet.

## BEISPIELE

### Beispiel 1: Vollständige Ausgabe eines Automatisierungsauftrags
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

Dieser Befehl ruft die vollständige Ausgabe des Auftrags ab, der die angegebene Auftrags-ID hat.

## PARAMETERS

### -AutomationAccountName
Gibt den Namen eines Automatisierungskontos an, für das dieses Cmdlet einen Auftragsausgabedatensatz erhält.

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
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Gibt die ID eines Auftragsausgabedatenblatts an, das von diesem Cmdlet abgerufen werden soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StreamRecordId

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -JobId
Gibt die ID eines Auftrags an, für den dieses Cmdlet einen Ausgabedatensatz erhält.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet einen Auftragsausgabedatensatz erhält.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.Guid

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Automation.Model.JobStreamRecord

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzAutomationJobOutput](./Get-AzAutomationJobOutput.md)


