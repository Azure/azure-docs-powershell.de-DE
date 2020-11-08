---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
ms.openlocfilehash: 010698183dec206002c0966fb8f37d629d24794a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003189"
---
# New-AzAutoscaleNotification

## Synopsis
Erstellt eine AutoScale-e-Mail-Benachrichtigung.

## Syntax

```
New-AzAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzAutoscaleNotification** erstellt eine e-Mail-Benachrichtigung für die autoskala.

## Beispiele

### Beispiel 1: Erstellen einer AutoScale-e-Mail-Benachrichtigung
```
PS C:\>New-AzAutoscaleNotification -CustomEmail "pattif@contoso.com, davidchew@contoso.net"
```

Mit diesem Befehl wird eine Autosacale-e-Mail-Benachrichtigung für zwei angegebene Adressen erstellt.

### Beispiel 2: Erstellen einer AutoScale-e-Mail-Benachrichtigung für den Abonnement Administrator
```
PS C:\>New-AzAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

Mit diesem Befehl wird eine Autosacale-e-Mail-Benachrichtigung für den Abonnement Administrator erstellt.

## Parameter

### -CustomEmail
Gibt eine durch trennzeichengetrennte Liste von e-Mail-Adressen an.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
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

### -SendEmailToSubscriptionAdministrator
Gibt an, dass dieser Vorgang eine e-Mail-Benachrichtigung an den Abonnement Administrator sendet.

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

### -SendEmailToSubscriptionCoAdministrator
Gibt an, dass dieser Vorgang eine e-Mail-Benachrichtigung an die Co-Administratoren des Abonnements sendet.

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

### -Webhook
Gibt eine durch trennzeichengetrennte Liste der AutoScale-webhooks an.

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. Azure. Management. Monitor. Management. Models. WebhookNotification []

### System. String []

### System. Management. Automation. Switchparameter

## Ausgaben

### Microsoft. Azure. Management. Monitor. Management. Models. AutoscaleNotification

## Notizen

## Verwandte Links

[Neu – AzAutoscaleWebhook](./New-AzAutoscaleWebhook.md)


