---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
ms.openlocfilehash: 368ae4ad814c9414ea211ea6e44c2d3fbda005f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302878"
---
# Get-AzSupportTicket

## Synopsis
Support-Tickets erhalten.

## Syntax

### ListParameterSet (Standard)
```
Get-AzSupportTicket [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### GetByNameParameterSet
```
Get-AzSupportTicket -Name <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## Beschreibung
Ruft die Liste der Support Tickets ab. Sie ruft alle Support-Tickets ab, wenn Sie keine Parameter angeben. Sie können die Support Tickets auch nach Status oder "CreatedDate" filtern, indem Sie den Parameter Filter verwenden. Nachfolgend finden Sie einige Beispiele für Filterwerte, die Sie angeben können.

| Szenario                                                         | Filter                                           |
|------------------------------------------------------------------|--------------------------------------------------|
| Abrufen von Tickets im geöffneten Zustand                               | "Status-EQ" Öffnen "                               |
| Abrufen von Tickets, die sich im Status "geschlossen" befinden                             | "Status-EQ" geschlossen "                             |
| Abrufen von Tickets, die am oder nach dem 20. Dez. 2019 erstellt wurden         | "" CreatedDate "ge 2019-12-20"                      |
| Abrufen von Tickets, die nach dem 20. Dez. 2019 erstellt wurden               | "" CreatedDate "gt 2019-12-20"                      |
| Ruft Tickets ab dem 20. Dezember, 2019, die im geöffneten Zustand sind | "" CreatedDate "gt 2019-12-20 und Status EQ" Öffnen " |


Dieses Cmdlet unterstützt Paging über First-und Skip-Parameter.

Sie können auch ein einzelnes Support Ticket abrufen, indem Sie den Ticket Namen angeben. 

## Beispiele

### Beispiel 1: erste 2 Tickets erhalten
```powershell
PS C:\> Get-AzSupportTicket -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### Beispiel 2: Abrufen der ersten 2 Tickets nach dem Überspringen der ersten 2
```powershell
PS C:\> Get-AzSupportTicket -Skip 2 -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test3 test title3                  150010521000314 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test4 test title4                  150010521000315 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### Beispiel 3: Abrufen eines Support Tickets nach Name
```powershell
PS C:\> Get-AzSupportTicket -Name "test1"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
```

### Beispiel 4: Abrufen der ersten 2 Support Tickets nach Status gefiltert
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Closed'" -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### Beispiel 5: Abrufen aller Support Tickets, die sich im geöffneten Zustand befinden und nach dem 20. Dezember 2019 erstellt wurden
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Open' and CreatedDate gt 2019-12-20"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test6 test title6                  150010521000311 Minimal  Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
test7 test title7                  150010521000312 Minimal  Billing                       Open   2/5/2020 1:33:53 AM
```

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### -Filter
Filter, der auf die Ergebnisse dieses Cmdlets angewendet werden soll.

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Name des Support Tickets, das dieses Cmdlet erhält.

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeTotalCount
Gibt die Gesamtzahl der Objekte in der Datengruppe (einer ganzen Zahl) an, gefolgt von den ausgewählten Objekten.
Wenn das Cmdlet die Gesamtanzahl nicht ermitteln kann, wird "unbekannte Gesamtanzahl" angezeigt. Die ganze Zahl verfügt über eine Genauigkeits Eigenschaft, die die Zuverlässigkeit des Gesamtanzahl Werts angibt.
Der Wert der Genauigkeit reicht von 0,0 bis 1,0, wobei 0,0 bedeutet, dass das Cmdlet die Objekte nicht zählen konnte, 1,0 bedeutet, dass die Anzahl exakt ist, und ein Wert zwischen 0,0 und 1,0 eine zunehmend zuverlässige Schätzung angibt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Skip
Ignoriert die angegebene Anzahl von Objekten und ruft dann die restlichen Objekte ab.
Geben Sie die Anzahl der zu überspringenden Objekte ein.

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -First
Ruft nur die angegebene Anzahl von Objekten ab.
Geben Sie die Anzahl der abzurufenden Objekte ein.

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Keine

## Ausgaben

### Microsoft. Azure. Commands. Support. Models. PSSupportTicket

## Notizen

## Verwandte Links
