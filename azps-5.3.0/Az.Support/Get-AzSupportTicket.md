---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
ms.openlocfilehash: 368ae4ad814c9414ea211ea6e44c2d3fbda005f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460064"
---
# Get-AzSupportTicket

## SYNOPSIS
Supporttickets erhalten.

## SYNTAX

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

## BESCHREIBUNG
Ruft die Liste der Supporttickets ab. Sie ruft alle Supporttickets ab, wenn Sie keine Parameter angeben. Sie können die Supporttickets auch mithilfe des Parameters "Filter" nach "Status" oder "CreatedDate" filtern. Im Folgenden finden Sie einige Beispiele für Filterwerte, die Sie angeben können.

| Szenario                                                         | Filter                                           |
|------------------------------------------------------------------|--------------------------------------------------|
| Tickets erhalten, die sich im geöffneten Zustand befinden                               | "Status eq 'Open'"                               |
| Tickets erhalten, die sich im geschlossenen Zustand befinden                             | "Status eq 'Closed'"                             |
| Tickets erhalten, die am oder nach dem 20. Dez. 2019 erstellt wurden         | "CreatedDate ge 2019-12-20"                      |
| Tickets erhalten, die nach dem 20. Dez. 2019 erstellt wurden               | "CreatedDate gt 2019-12-20"                      |
| Ruft Nach dem 20. Dezember 2019 erstellte Tickets ab, die sich im geöffneten Zustand befinden | "CreatedDate gt 2019-12-20 and Status eq 'Open'" |


Dieses Cmdlet unterstützt die Auslagerung über die Parameter "First" und "Skip".

Sie können auch ein einzelnes Supportticket abrufen, indem Sie den Ticketnamen angeben. 

## BEISPIELE

### Beispiel 1: Erhalten der ersten 2 Tickets
```powershell
PS C:\> Get-AzSupportTicket -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### Beispiel 2: Erhalten der ersten 2 Tickets nach dem Überspringen der ersten 2
```powershell
PS C:\> Get-AzSupportTicket -Skip 2 -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test3 test title3                  150010521000314 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test4 test title4                  150010521000315 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### Beispiel 3: Erhalten eines Supporttickets nach Name
```powershell
PS C:\> Get-AzSupportTicket -Name "test1"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
```

### Beispiel 4: Erhalten der ersten 2 nach Status gefilterten Supporttickets
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Closed'" -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### Beispiel 5: Alle Supporttickets erhalten, die sich im Status "Open" befinden und nach dem 20. Dezember 2019 erstellt wurden
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Open' and CreatedDate gt 2019-12-20"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test6 test title6                  150010521000311 Minimal  Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
test7 test title7                  150010521000312 Minimal  Billing                       Open   2/5/2020 1:33:53 AM
```

## PARAMETERS

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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
Name des Supporttickets, das dieses Cmdlet erhält.

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
Gibt die Gesamtzahl der Objekte im Datenset (eine ganze Zahl) gefolgt von den ausgewählten Objekten an.
Wenn das Cmdlet die Gesamtzahl nicht ermitteln kann, wird "Unbekannte Gesamtzahl" angezeigt. Die ganze Zahl weist eine Genauigkeitseigenschaft auf, die die Zuverlässigkeit des Gesamtanzahlswerts angibt.
Der Wert der Genauigkeit liegt zwischen 0,0 und 1,0, wobei 0,0 bedeutet, dass das Cmdlet die Objekte nicht zählen konnte, 1,0 bedeutet, dass die Anzahl exakt ist, und ein Wert zwischen 0,0 und 1,0 gibt eine immer zuverlässigere Schätzung an.

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
Ignoriert die angegebene Anzahl von Objekten und ruft dann die verbleibenden Objekte ab.
Geben Sie die Anzahl der zu überspringende Objekte ein.

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
Geben Sie die Anzahl der zu erhaltende Objekte ein.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Support.Models.PSSupportTicket

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
