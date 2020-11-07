---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
ms.openlocfilehash: 07a8747f94f9c1fb93bbff06ce855363088a67a0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846160"
---
# Get-AzSupportTicketCommunication

## Synopsis
Support-Ticket Kommunikation erhalten.

## Syntax

### GetByNameParameterSet (Standard)
```
Get-AzSupportTicketCommunication -SupportTicketName <String> [-Name <String>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

### GetByParentObjectParameterSet
```
Get-AzSupportTicketCommunication [-Name <String>] -SupportTicketObject <PSSupportTicket> [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## Beschreibung
Ruft die Kommunikation für ein Support Ticket ab. Sie ruft alle Kommunikationen für ein Ticket ab, wenn Sie keine weiteren Parameter angeben. Sie können die Kommunikation auch nach "CreatedDate" oder CommunicationType mithilfe des Filters-Parameters filtern. Nachfolgend finden Sie einige Beispiele für Filterwerte, die Sie angeben können.


| Szenario                                                        | Filter                                                     |
|-----------------------------------------------------------------|------------------------------------------------------------|
| Abrufen von webkommunikationen                                          | "CommunicationType EQ" Web ""                               |
| Telefonnachrichten erhalten                                        | "CommunicationType EQ" Telefon "                             |
| Abrufen von Mitteilungen, die am oder nach dem 20. Dezember 2019 erstellt wurden | "" CreatedDate "ge 2019-12-20"                                |
| Abrufen von Kommunikationen, die nach dem 20. Dezember 2019 erstellt wurden       | "" CreatedDate "gt 2019-12-20"                                |
| Ruft die Webkommunikation ab, die nach dem 20. Dezember 2019 erstellt wurde.            | "" CreatedDate "gt 2019-12-20 und CommunicationType EQ" Web " |


Dieses Cmdlet unterstützt Paging über First-und Skip-Parameter.

Sie können auch eine einzelne Support Ticket-Kommunikation abrufen, indem Sie den Kommunikations Namen angeben. 

## Beispiele

### Beispiel 1: Abrufen der gesamten Kommunikation für ein Support Ticket
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

### Beispiel 2: Abrufen einer einzelnen Kommunikation mit dem Namen eines Support Tickets
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Name "testmessage1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage1 user@contoso.com     test message   2/4/2020 9:38:14 PM
```

### Beispiel 3: Abrufen der ersten 2 Kommunikation für ein Support Ticket
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### Beispiel 4: Abrufen der nächsten 2 Kommunikation nach dem Überspringen der ersten 2 Kommunikation für ein Support Ticket
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Skip 2 -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage4 user@contoso.com     test message4  2/4/2020 9:38:14 PM
testmessage5 user@contoso.com     test message5  2/4/2020 9:36:36 PM
```

### Beispiel 5: Abrufen der gesamten Webkommunikation für ein Support Ticket
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web'"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### Beispiel 6: Abrufen der gesamten Kommunikation, die am oder nach dem 20. Dezember erstellt wurde, 2019 für ein Support Ticket
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### Beispiel 7: Abrufen aller webkommunikationen, die am oder nach dem 20. Dezember erstellt wurden, 2019 für ein Support Ticket
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web' and CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### Beispiel 8: Abrufen der gesamten Kommunikation für ein Support Ticket durch Piping Support Ticket-Objekt
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Get-AzSupportTicketCommunication

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
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
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Kommunikations Name.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SupportTicketName
Name des Support Tickets

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

### -SupportTicketObject
Support-Ticket-Objekt.

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### Microsoft. Azure. Commands. Support. Models. PSSupportTicket

## Ausgaben

### Microsoft. Azure. Commands. Support. Models. PSSupportTicketCommunication

## Notizen

## Verwandte Links
