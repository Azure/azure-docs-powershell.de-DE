---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
ms.openlocfilehash: 46d6ba805b6995c0d984149d699ce0679f682407
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009428"
---
# Get-AzAutomationAccount

## Synopsis
Ruft Automatisierungs Konten in einer Ressourcengruppe ab.

## Syntax

### Seitensaller (Standard)
```
Get-AzAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByAutomationAccountName
```
Get-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzAutomationAccount** " ruft Azure Automation-Konten in einer Ressourcengruppe ab.
Weitere Informationen zu Automatisierungs Konten finden Sie unter New-AzAutomationAccount-Cmdlet.

## Beispiele

### Beispiel 1: Abrufen aller Konten
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03"
```

Dieser Befehl ruft alle Automatisierungs Konten in der Ressourcengruppe mit dem Namen ResourceGroup03 ab.

### Beispiel 2: Abrufen eines Kontos
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

Dieser Befehl ruft das Automatisierungs Konto mit dem Namen ContosoAutomationAccount in der Ressourcengruppe mit dem Namen ContosoResourceGroup ab.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -Name
Gibt den Namen des Automatisierungs Kontos an, das dieses Cmdlet erhält.

```yaml
Type: System.String
Parameter Sets: ByAutomationAccountName
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet Automatisierungs Konten erhält.

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByAutomationAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. Automation. Model. AutomationAccount

## Notizen

## Verwandte Links

[Neu – AzAutomationAccount](./New-AzAutomationAccount.md)

[Remove-AzAutomationAccount](./Remove-AzAutomationAccount.md)

[Satz-AzAutomationAccount](./Set-AzAutomationAccount.md)


