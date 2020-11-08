---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
ms.openlocfilehash: 07a8747f94f9c1fb93bbff06ce855363088a67a0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175372"
---
# <span data-ttu-id="528dd-101">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="528dd-101">Get-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="528dd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="528dd-102">SYNOPSIS</span></span>
<span data-ttu-id="528dd-103">Support-Ticket Kommunikation erhalten.</span><span class="sxs-lookup"><span data-stu-id="528dd-103">Get support ticket communications.</span></span>

## <span data-ttu-id="528dd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="528dd-104">SYNTAX</span></span>

### <span data-ttu-id="528dd-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="528dd-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSupportTicketCommunication -SupportTicketName <String> [-Name <String>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

### <span data-ttu-id="528dd-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="528dd-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSupportTicketCommunication [-Name <String>] -SupportTicketObject <PSSupportTicket> [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## <span data-ttu-id="528dd-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="528dd-107">DESCRIPTION</span></span>
<span data-ttu-id="528dd-108">Ruft die Kommunikation für ein Support Ticket ab.</span><span class="sxs-lookup"><span data-stu-id="528dd-108">Gets communications for a support ticket.</span></span> <span data-ttu-id="528dd-109">Sie ruft alle Kommunikationen für ein Ticket ab, wenn Sie keine weiteren Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="528dd-109">It will retrieve all the communications for a ticket if you do not specify any other parameters.</span></span> <span data-ttu-id="528dd-110">Sie können die Kommunikation auch nach "CreatedDate" oder CommunicationType mithilfe des Filters-Parameters filtern.</span><span class="sxs-lookup"><span data-stu-id="528dd-110">You can also filter the communications by CreatedDate or CommunicationType using the Filter parameter.</span></span> <span data-ttu-id="528dd-111">Nachfolgend finden Sie einige Beispiele für Filterwerte, die Sie angeben können.</span><span class="sxs-lookup"><span data-stu-id="528dd-111">Here are some examples of filter values that you can specify.</span></span>


| <span data-ttu-id="528dd-112">Szenario</span><span class="sxs-lookup"><span data-stu-id="528dd-112">Scenario</span></span>                                                        | <span data-ttu-id="528dd-113">Filter</span><span class="sxs-lookup"><span data-stu-id="528dd-113">Filter</span></span>                                                     |
|-----------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="528dd-114">Abrufen von webkommunikationen</span><span class="sxs-lookup"><span data-stu-id="528dd-114">Get Web communications</span></span>                                          | <span data-ttu-id="528dd-115">"CommunicationType EQ" Web ""</span><span class="sxs-lookup"><span data-stu-id="528dd-115">"CommunicationType eq 'Web'"</span></span>                               |
| <span data-ttu-id="528dd-116">Telefonnachrichten erhalten</span><span class="sxs-lookup"><span data-stu-id="528dd-116">Get Phone communications</span></span>                                        | <span data-ttu-id="528dd-117">"CommunicationType EQ" Telefon "</span><span class="sxs-lookup"><span data-stu-id="528dd-117">"CommunicationType eq 'Phone'"</span></span>                             |
| <span data-ttu-id="528dd-118">Abrufen von Mitteilungen, die am oder nach dem 20. Dezember 2019 erstellt wurden</span><span class="sxs-lookup"><span data-stu-id="528dd-118">Get communications that were created on or after 20th Dec, 2019</span></span> | <span data-ttu-id="528dd-119">"" CreatedDate "ge 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="528dd-119">"CreatedDate ge 2019-12-20"</span></span>                                |
| <span data-ttu-id="528dd-120">Abrufen von Kommunikationen, die nach dem 20. Dezember 2019 erstellt wurden</span><span class="sxs-lookup"><span data-stu-id="528dd-120">Get communications that were created after 20th Dec, 2019</span></span>       | <span data-ttu-id="528dd-121">"" CreatedDate "gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="528dd-121">"CreatedDate gt 2019-12-20"</span></span>                                |
| <span data-ttu-id="528dd-122">Ruft die Webkommunikation ab, die nach dem 20. Dezember 2019 erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="528dd-122">Gets Web communications created after 20th Dec, 2019</span></span>            | <span data-ttu-id="528dd-123">"" CreatedDate "gt 2019-12-20 und CommunicationType EQ" Web "</span><span class="sxs-lookup"><span data-stu-id="528dd-123">"CreatedDate gt 2019-12-20 and CommunicationType eq 'Web'"</span></span> |


<span data-ttu-id="528dd-124">Dieses Cmdlet unterstützt Paging über First-und Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="528dd-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="528dd-125">Sie können auch eine einzelne Support Ticket-Kommunikation abrufen, indem Sie den Kommunikations Namen angeben.</span><span class="sxs-lookup"><span data-stu-id="528dd-125">You can also retrieve a single support ticket communication by specifying the communication name.</span></span> 

## <span data-ttu-id="528dd-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="528dd-126">EXAMPLES</span></span>

### <span data-ttu-id="528dd-127">Beispiel 1: Abrufen der gesamten Kommunikation für ein Support Ticket</span><span class="sxs-lookup"><span data-stu-id="528dd-127">Example 1: Retrieve all communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

### <span data-ttu-id="528dd-128">Beispiel 2: Abrufen einer einzelnen Kommunikation mit dem Namen eines Support Tickets</span><span class="sxs-lookup"><span data-stu-id="528dd-128">Example 2: Retrieve a single communication by it's name for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Name "testmessage1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage1 user@contoso.com     test message   2/4/2020 9:38:14 PM
```

### <span data-ttu-id="528dd-129">Beispiel 3: Abrufen der ersten 2 Kommunikation für ein Support Ticket</span><span class="sxs-lookup"><span data-stu-id="528dd-129">Example 3: Retrieve first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="528dd-130">Beispiel 4: Abrufen der nächsten 2 Kommunikation nach dem Überspringen der ersten 2 Kommunikation für ein Support Ticket</span><span class="sxs-lookup"><span data-stu-id="528dd-130">Example 4: Retrieve next 2 communications after skipping first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Skip 2 -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage4 user@contoso.com     test message4  2/4/2020 9:38:14 PM
testmessage5 user@contoso.com     test message5  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="528dd-131">Beispiel 5: Abrufen der gesamten Webkommunikation für ein Support Ticket</span><span class="sxs-lookup"><span data-stu-id="528dd-131">Example 5: Retrieve all Web communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web'"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="528dd-132">Beispiel 6: Abrufen der gesamten Kommunikation, die am oder nach dem 20. Dezember erstellt wurde, 2019 für ein Support Ticket</span><span class="sxs-lookup"><span data-stu-id="528dd-132">Example 6: Retrieve all communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="528dd-133">Beispiel 7: Abrufen aller webkommunikationen, die am oder nach dem 20. Dezember erstellt wurden, 2019 für ein Support Ticket</span><span class="sxs-lookup"><span data-stu-id="528dd-133">Example 7: Retrieve all Web communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web' and CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="528dd-134">Beispiel 8: Abrufen der gesamten Kommunikation für ein Support Ticket durch Piping Support Ticket-Objekt</span><span class="sxs-lookup"><span data-stu-id="528dd-134">Example 8: Retrieve all communications for a support ticket by piping support ticket object</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Get-AzSupportTicketCommunication

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

## <span data-ttu-id="528dd-135">Parameter</span><span class="sxs-lookup"><span data-stu-id="528dd-135">PARAMETERS</span></span>

### <span data-ttu-id="528dd-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="528dd-136">-DefaultProfile</span></span>
<span data-ttu-id="528dd-137">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="528dd-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="528dd-138">-Filter</span><span class="sxs-lookup"><span data-stu-id="528dd-138">-Filter</span></span>
<span data-ttu-id="528dd-139">Filter, der auf die Ergebnisse dieses Cmdlets angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="528dd-139">Filter to be applied to the results of this cmdlet.</span></span>

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

### <span data-ttu-id="528dd-140">-Name</span><span class="sxs-lookup"><span data-stu-id="528dd-140">-Name</span></span>
<span data-ttu-id="528dd-141">Kommunikations Name.</span><span class="sxs-lookup"><span data-stu-id="528dd-141">Communication name.</span></span>

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

### <span data-ttu-id="528dd-142">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="528dd-142">-SupportTicketName</span></span>
<span data-ttu-id="528dd-143">Name des Support Tickets</span><span class="sxs-lookup"><span data-stu-id="528dd-143">Support ticket name.</span></span>

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

### <span data-ttu-id="528dd-144">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="528dd-144">-SupportTicketObject</span></span>
<span data-ttu-id="528dd-145">Support-Ticket-Objekt.</span><span class="sxs-lookup"><span data-stu-id="528dd-145">Support ticket object.</span></span>

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

### <span data-ttu-id="528dd-146">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="528dd-146">-IncludeTotalCount</span></span>
<span data-ttu-id="528dd-147">Gibt die Gesamtzahl der Objekte in der Datengruppe (einer ganzen Zahl) an, gefolgt von den ausgewählten Objekten.</span><span class="sxs-lookup"><span data-stu-id="528dd-147">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="528dd-148">Wenn das Cmdlet die Gesamtanzahl nicht ermitteln kann, wird "unbekannte Gesamtanzahl" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="528dd-148">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="528dd-149">Die ganze Zahl verfügt über eine Genauigkeits Eigenschaft, die die Zuverlässigkeit des Gesamtanzahl Werts angibt.</span><span class="sxs-lookup"><span data-stu-id="528dd-149">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="528dd-150">Der Wert der Genauigkeit reicht von 0,0 bis 1,0, wobei 0,0 bedeutet, dass das Cmdlet die Objekte nicht zählen konnte, 1,0 bedeutet, dass die Anzahl exakt ist, und ein Wert zwischen 0,0 und 1,0 eine zunehmend zuverlässige Schätzung angibt.</span><span class="sxs-lookup"><span data-stu-id="528dd-150">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="528dd-151">-Skip</span><span class="sxs-lookup"><span data-stu-id="528dd-151">-Skip</span></span>
<span data-ttu-id="528dd-152">Ignoriert die angegebene Anzahl von Objekten und ruft dann die restlichen Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="528dd-152">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="528dd-153">Geben Sie die Anzahl der zu überspringenden Objekte ein.</span><span class="sxs-lookup"><span data-stu-id="528dd-153">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="528dd-154">-First</span><span class="sxs-lookup"><span data-stu-id="528dd-154">-First</span></span>
<span data-ttu-id="528dd-155">Ruft nur die angegebene Anzahl von Objekten ab.</span><span class="sxs-lookup"><span data-stu-id="528dd-155">Gets only the specified number of objects.</span></span>
<span data-ttu-id="528dd-156">Geben Sie die Anzahl der abzurufenden Objekte ein.</span><span class="sxs-lookup"><span data-stu-id="528dd-156">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="528dd-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="528dd-157">CommonParameters</span></span>
<span data-ttu-id="528dd-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="528dd-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="528dd-159">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="528dd-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="528dd-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="528dd-160">INPUTS</span></span>

### <span data-ttu-id="528dd-161">Microsoft. Azure. Commands. Support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="528dd-161">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="528dd-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="528dd-162">OUTPUTS</span></span>

### <span data-ttu-id="528dd-163">Microsoft. Azure. Commands. Support. Models. PSSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="528dd-163">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="528dd-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="528dd-164">NOTES</span></span>

## <span data-ttu-id="528dd-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="528dd-165">RELATED LINKS</span></span>
