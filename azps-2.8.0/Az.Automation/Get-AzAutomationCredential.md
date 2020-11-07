---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
ms.openlocfilehash: 3a13605618c5cda3c247cd6b0812732ce018bafe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658071"
---
# Get-AzAutomationCredential

## Synopsis
Ruft Automatisierungs Anmeldeinformationen ab.

## Syntax

### Seitensaller (Standard)
```
Get-AzAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzAutomationCredential** " ruft mindestens eine Azure-Automatisierungs Anmeldeinformationen ab.
Standardmäßig werden alle Anmeldeinformationen zurückgegeben.
Geben Sie den Namen der Anmeldeinformationen an, um bestimmte Anmeldeinformationen abzurufen.
Aus Sicherheitsgründen gibt dieses Cmdlet keine Kennwörter für Anmeldeinformationen zurück.

## Beispiele

### Beispiel 1: Abrufen aller Anmeldeinformationen
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

Dieser Befehl ruft Metadaten für alle Anmeldeinformationen im Automatisierungs Konto mit dem Namen Contoso17 ab.

### Beispiel 2: Abrufen von Anmeldeinformationen
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

Dieser Befehl ruft Metadaten für die Anmeldeinformationen mit dem Namen ContosoCredential im Automatisierungs Konto mit dem Namen Contoso17 ab.

## Parameter

### -AutomationAccountName
Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet Anmeldeinformationen abruft.

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
Gibt den Namen der abzurufenden Anmeldeinformationen an.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt die Ressourcengruppe an, für die dieses Cmdlet Anmeldeinformationen abruft.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. Automation. Model. CredentialInfo

## Notizen

## Verwandte Links

[Neu – AzAutomationCredential](./New-AzAutomationCredential.md)

[Remove-AzAutomationCredential](./Remove-AzAutomationCredential.md)

[Satz-AzAutomationCredential](./Set-AzAutomationCredential.md)


