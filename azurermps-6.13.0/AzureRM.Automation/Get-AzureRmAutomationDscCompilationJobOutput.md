---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D40BA2E2-50DF-4D51-A4D2-2D02AECBF20F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdsccompilationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJobOutput.md
ms.openlocfilehash: a7ddc25fa7c6bc52acbe9369c569db060cf63a06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476306"
---
# Get-AzureRmAutomationDscCompilationJobOutput

## Synopsis
Ruft die Protokollierungsdaten Ströme eines Automatisierungs-DSC-Kompilierungs Auftrags ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmAutomationDscCompilationJobOutput [-Id] <Guid> [-Stream <CompilationJobStreamType>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmAutomationDscCompilationJobOutput** " Ruft die Datenstrom Einträge eines APS-Kompilierungs Auftrags (Desired State Configuration, DSC) in Azure Automation ab.

## Beispiele

### Beispiel 1: Abrufen der Protokolle für einen DSC-Kompilierungs Auftrag
```
PS C:\>$Jobs = Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
PS C:\> $Jobs[0] | Get-AzureRmAutomationDscCompilationJobOutput -Stream "Any"
```

Der erste Befehl ruft die Kompilierungsaufträge im Automatisierungs Konto mit dem Namen Contoso17 mithilfe des Get-AzureRmAutomationDscCompilationJob-Cmdlets ab.
Der Befehl speichert diese Objekte in der $Jobs-Variablen.
Der zweite Befehl ruft die Ausgabe des Kompilierungs Auftrags für einen beliebigen Datenstrom für das erste Element des $Jobs-Arrays ab.

## Parameter

### -AutomationAccountName
Gibt den Namen des Automatisierungs Kontos an, das den DSC-Kompilierungs Auftrag enthält.

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

### -ID
Gibt die eindeutige ID des DSC-Kompilierungs Auftrags an, für den dieses Cmdlet Ausgabe erhält.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, die den DSC-Kompilierungs Auftrag enthält, für den dieses Cmdlet Datenstrom Einträge erhält.

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

### -Startzeit
Gibt eine Startzeit an.
Dieses Cmdlet ruft Datenstrom Einträge ab, die der DSC-Kompilierungs Auftrag nach dieser Zeit ausgibt.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Stream
Gibt den Typ des Datenstroms für die Ausgabe an, die dieses Cmdlet erhält.
Gültige Werte sind: 
- Alle 
- Warnung 
- Fehler 
- Ausführliche

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.CompilationJobStreamType
Parameter Sets: (All)
Aliases:
Accepted values: Warning, Error, Verbose, Any

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. GUID

### Microsoft. Azure. Commands. Automation. Common. CompilationJobStreamType

### System. Nullable ' 1 [[System. DateTimeOffset, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

### System. String

## Ausgaben

### Microsoft. Azure. Commands. Automation. Model. JobStream

## Notizen

## Verwandte Links

[Get-AzureRmAutomationDscCompilationJob](./Get-AzureRmAutomationDscCompilationJob.md)

[Anfang-AzureRmAutomationDscCompilationJob](./Start-AzureRmAutomationDscCompilationJob.md)


