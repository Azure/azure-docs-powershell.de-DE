---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermalertruleemail
schema: 2.0.0
ms.openlocfilehash: 20134cc0f2eef927361439fb431bc4ab9308a9a1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850827"
---
# New-AzureRmAlertRuleEmail

## Synopsis
Erstellt eine e-Mail-Aktion für eine Warnungsregel.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureRmAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmAlertRuleEmail** erstellt eine e-Mail-Aktion für eine Warnungsregel.

## Beispiele

### Beispiel 1: Erstellen einer Warnungsregel-e-Mail-Aktion für Dienstbesitzer
```
PS C:\>New-AzureRmAlertRuleEmail -SendToServiceOwners
```

Mit diesem Befehl wird eine e-Mail-Benachrichtigungsaktion erstellt, die den Dienstbesitzern beim Auslösen einer Warnungsregel gesendet werden soll.

### Beispiel 2: Erstellen einer Warnungsregel-e-Mail-Aktion für nicht-Dienstbesitzer
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails pattif@contoso.com,davidchew@contoso.net
```

Mit diesem Befehl wird eine e-Mail-Benachrichtigungsaktion für die angegebenen e-Mail-Adressen erstellt, nicht jedoch für die Dienstbesitzer.

### Beispiel 3: Erstellen einer e-Mail-Aktion für Warnungsregeln für Dienstbesitzer und nicht Dienstbesitzer
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails pattif@contoso.net -SendToServiceOwners
```

Mit diesem Befehl wird eine e-Mail-Benachrichtigungsaktion für die angegebene Adresse und ihre Dienstbesitzer erstellt.

## Parameter

### -CustomEmail
Gibt eine Liste mit durch Kommas getrennten e-Mail-Adressen an.

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

### -SendToServiceOwner
Gibt an, dass dieser Vorgang eine e-Mail-Nachricht an die Dienstbesitzer sendet, wenn die Regel ausgelöst wird.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String []

### System. Management. Automation. Switchparameter

## Ausgaben

### Microsoft. Azure. Management. Monitor. Management. Models. RuleEmailAction

## Notizen

## Verwandte Links



[Add-AzureRmMetricAlertRule](./Add-AzureRmMetricAlertRule.md)

[Add-AzureRmWebtestAlertRule](./Add-AzureRmWebtestAlertRule.md)

[Neu – AzureRmAlertRuleWebhook](./New-AzureRmAlertRuleWebhook.md)


