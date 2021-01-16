---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
ms.openlocfilehash: 07a8747f94f9c1fb93bbff06ce855363088a67a0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362114"
---
# Get-AzSupportTicketCommunication

## SYNOPSIS
Erhalten Sie Supportticketkommunikation.

## SYNTAX

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

## BESCHREIBUNG
Ruft Kommunikationen für ein Supportticket ab. Sie ruft die gesamte Kommunikation für ein Ticket ab, wenn Sie keine anderen Parameter angeben. Sie können die Kommunikation auch mithilfe des Parameters "Filter" nach CreatedDate oder CommunicationType filtern. Im Folgenden finden Sie einige Beispiele für Filterwerte, die Sie angeben können.


| Szenario                                                        | Filter                                                     |
|-----------------------------------------------------------------|------------------------------------------------------------|
| Webkommunikation erhalten                                          | "CommunicationType eq 'Web'"                               |
| Telefonkommunikation erhalten                                        | "CommunicationType eq 'Phone'"                             |
| Erhalten von Kommunikationen, die am oder nach dem 20. Dez. 2019 erstellt wurden | "CreatedDate ge 2019-12-20"                                |
| Erhalten von Kommunikationen, die nach dem 20. Dez. 2019 erstellt wurden       | "CreatedDate gt 2019-12-20"                                |
| Ruft web communications created after 20th Dec, 2019            | "CreatedDate gt 2019-12-20 and CommunicationType eq 'Web'" |


Dieses Cmdlet unterstützt die Auslagerung über die Parameter "First" und "Skip".

Sie können auch die Kommunikation eines einzelnen Supporttickets abrufen, indem Sie den Kommunikationsnamen angeben. 

## BEISPIELE

### Beispiel 1: Abrufen aller Kommunikationen für ein Supportticket
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

### Beispiel 2: Abrufen einer einzelnen Kommunikation nach dem Namen für ein Supportticket
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Name "testmessage1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage1 user@contoso.com     test message   2/4/2020 9:38:14 PM
```

### Beispiel 3: Abrufen der ersten 2 Kommunikation für ein Supportticket
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### Beispiel 4: Abrufen der nächsten 2 Kommunikation nach dem Überspringen der ersten 2 Kommunikation für ein Supportticket
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Skip 2 -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage4 user@contoso.com     test message4  2/4/2020 9:38:14 PM
testmessage5 user@contoso.com     test message5  2/4/2020 9:36:36 PM
```

### Beispiel 5: Abrufen aller Webkommunikationen für ein Supportticket
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web'"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### Beispiel 6: Abrufen aller Am oder nach dem 20. Dezember 2019 erstellten Kommunikationen für ein Supportticket
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### Beispiel 7: Abrufen aller Webkommunikationen, die am oder nach dem 20. Dezember 2019 erstellt wurden, für ein Supportticket
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web' and CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### Beispiel 8: Abrufen aller Kommunikationen für ein Supportticket durch Piping des Supportticketobjekts
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Get-AzSupportTicketCommunication

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
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
Filter, der auf die Ergebnisse dieses Cmdlets angewendet wird.

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
Kommunikationsname.

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
Name des Supporttickets.

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
Supportticketobjekt.

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
Meldet die Gesamtzahl der Objekte im Datenset (eine ganze Zahl) gefolgt von den ausgewählten Objekten.
Wenn das Cmdlet die Gesamtzahl nicht ermitteln kann, wird "Unbekannte Gesamtzahl" angezeigt. Die ganze Zahl hat eine Genauigkeitseigenschaft, die die Zuverlässigkeit des Gesamtanzahlswerts angibt.
Der Genauigkeitswert reicht von 0,0 bis 1,0, wobei 0,0 bedeutet, dass das Cmdlet die Objekte nicht zählen konnte, 1,0 bedeutet, dass die Anzahl exakt ist, und ein Wert zwischen 0,0 und 1,0 kennzeichnet eine immer zuverlässigere Schätzung.

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

### Microsoft.Azure.Commands.Support.Models.PSSupportTicket

## AUSGABEN

### Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
