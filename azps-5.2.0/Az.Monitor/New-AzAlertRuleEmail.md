---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: 592329ff0793fc99f8e5b0e7031a2248342102f9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296831"
---
# New-AzAlertRuleEmail

## SYNOPSIS
Erstellt eine E-Mail-Aktion für eine Warnungsregel.

## SYNTAX

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "New-AzAlertRuleEmail"** erstellt eine E-Mail-Aktion für eine Warnungsregel.

## BEISPIELE

### Beispiel 1: Erstellen einer E-Mail-Aktion einer Warnungsregel für Dienstbesitzer
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

Mit diesem Befehl wird eine E-Mail-Aktion für eine Warnungsregel erstellt, die an die Dienstbesitzer gesendet wird, wenn eine Warnungsregel ausgelöst wird.

### Beispiel 2: Erstellen einer E-Mail-Aktion einer Warnungsregel für Nicht-Dienst-Besitzer
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.com,davidchew@contoso.net
```

Mit diesem Befehl wird eine E-Mail-Aktion der Warnungsregel für die angegebenen E-Mail-Adressen erstellt, jedoch nicht für die Dienstbesitzer.

### Beispiel 3: Erstellen einer E-Mail-Aktion mit einer Warnungsregel für Dienstbesitzer und Nicht-Dienst-Besitzer
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.net -SendToServiceOwners
```

Mit diesem Befehl wird eine E-Mail-Aktion für eine Warnungsregel für die angegebene Adresse und für die Dienstbesitzer erstellt.

## PARAMETERS

### -CustomEmail
Gibt eine Liste von durch Kommas getrennten E-Mail-Adressen an.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
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

### -SendToServiceOwner
Gibt an, dass durch diesen Vorgang eine E-Mail an die Dienstbesitzer gesendet wird, wenn die Regel ausgibt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String[]

### System.Management.Automation.SwitchParameter

## AUSGABEN

### Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Add-AzLogAlertRule](./Add-AzLogAlertRule.md)

[Add-AzMetricAlertRule](./Add-AzMetricAlertRule.md)

[Add-AzWebtestAlertRule](./Add-AzWebtestAlertRule.md)

[New-AzAlertRuleWebhook](./New-AzAlertRuleWebhook.md)


