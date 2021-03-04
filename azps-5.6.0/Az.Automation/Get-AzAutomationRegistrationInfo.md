---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
ms.openlocfilehash: aaa4a87f14572650fb0c1f969c11f0a3ed9cf0e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949763"
---
# Get-AzAutomationRegistrationInfo

## SYNOPSIS
Ruft Registrierungsinformationen zum Onboarding eines DSC-Knotens oder Hybridarbeiters in die Automatisierung ab.

## SYNTAX

```
Get-AzAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzAutomationRegistrationInfo-Cmdlet** ruft den Endpunkt und die Schlüssel ab, die zum Onboardn eines Dsc-Knotens (Desired State Configuration) oder hybriden Workers in ein Azure Automation-Konto erforderlich sind.

## BEISPIELE

### Beispiel 1: Informationen zur Registrierung erhalten
```
PS C:\>Get-AzAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

Dieser Befehl ruft die Registrierungsinformationen für das Automatisierungskonto namens AutomationAccount01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab.

## PARAMETER

### -AutomationAccountName
Gibt den Namen des Automatisierungskontos an, für das dieses Cmdlet Registrierungsinformationen erhält.

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

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe an.
Dieses Cmdlet ruft Registrierungsinformationen für die Ressourcengruppe ab, die dieser Parameter angibt.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Automation.Model.AgentRegistration

## NOTIZEN

## VERWANDTE LINKS

[Get-AzAutomationAccount](./Get-AzAutomationAccount.md)

[Get-AzAutomationDscNode](./Get-AzAutomationDscNode.md)

[New-AzAutomationKey](./New-AzAutomationKey.md)


