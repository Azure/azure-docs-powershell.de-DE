---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
ms.openlocfilehash: 368ae4ad814c9414ea211ea6e44c2d3fbda005f7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165939"
---
# <span data-ttu-id="3f6a3-101">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="3f6a3-101">Get-AzSupportTicket</span></span>

## <span data-ttu-id="3f6a3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3f6a3-102">SYNOPSIS</span></span>
<span data-ttu-id="3f6a3-103">Support-Tickets erhalten.</span><span class="sxs-lookup"><span data-stu-id="3f6a3-103">Get support tickets.</span></span>

## <span data-ttu-id="3f6a3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f6a3-104">SYNTAX</span></span>

### <span data-ttu-id="3f6a3-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3f6a3-105">ListParameterSet (Default)</span></span>
```
Get-AzSupportTicket [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="3f6a3-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f6a3-106">GetByNameParameterSet</span></span>
```
Get-AzSupportTicket -Name <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="3f6a3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3f6a3-107">DESCRIPTION</span></span>
<span data-ttu-id="3f6a3-108">Ruft die Liste der Support Tickets ab.</span><span class="sxs-lookup"><span data-stu-id="3f6a3-108">Gets the list of support tickets.</span></span> <span data-ttu-id="3f6a3-109">Sie ruft alle Support-Tickets ab, wenn Sie keine Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="3f6a3-109">It will retrieve all the support tickets if you do not specify any parameters.</span></span> <span data-ttu-id="3f6a3-110">Sie können die Support Tickets auch nach Status oder "CreatedDate" filtern, indem Sie den Parameter Filter verwenden.</span><span class="sxs-lookup"><span data-stu-id="3f6a3-110">You can also filter the support tickets by Status or CreatedDate using the Filter parameter.</span></span> <span data-ttu-id="3f6a3-111">Nachfolgend finden Sie einige Beispiele für Filterwerte, die Sie angeben können.</span><span class="sxs-lookup"><span data-stu-id="3f6a3-111">Here are some examples of filter values that you can specify.</span></span>

| <span data-ttu-id="3f6a3-112">Szenario</span><span class="sxs-lookup"><span data-stu-id="3f6a3-112">Scenario</span></span>                                                         | <span data-ttu-id="3f6a3-113">Filter</span><span class="sxs-lookup"><span data-stu-id="3f6a3-113">Filter</span></span>                                           |
|------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="3f6a3-114">Abrufen von Tickets im geöffneten Zustand</span><span class="sxs-lookup"><span data-stu-id="3f6a3-114">Get tickets that are in open state</span></span>                               | <span data-ttu-id="3f6a3-115">"Status-EQ" Öffnen "</span><span class="sxs-lookup"><span data-stu-id="3f6a3-115">"Status eq 'Open'"</span></span>                               |
| <span data-ttu-id="3f6a3-116">Abrufen von Tickets, die sich im Status "geschlossen" befinden</span><span class="sxs-lookup"><span data-stu-id="3f6a3-116">Get tickets that are in closed state</span></span>                             | <span data-ttu-id="3f6a3-117">"Status-EQ" geschlossen "</span><span class="sxs-lookup"><span data-stu-id="3f6a3-117">"Status eq 'Closed'"</span></span>                             |
| <span data-ttu-id="3f6a3-118">Abrufen von Tickets, die am oder nach dem 20. Dez. 2019 erstellt wurden</span><span class="sxs-lookup"><span data-stu-id="3f6a3-118">Get tickets that were created on or after 20th Dec, 2019</span></span>         | <span data-ttu-id="3f6a3-119">"" CreatedDate "ge 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="3f6a3-119">"CreatedDate ge 2019-12-20"</span></span>                      |
| <span data-ttu-id="3f6a3-120">Abrufen von Tickets, die nach dem 20. Dez. 2019 erstellt wurden</span><span class="sxs-lookup"><span data-stu-id="3f6a3-120">Get tickets that were created after 20th Dec, 2019</span></span>               | <span data-ttu-id="3f6a3-121">"" CreatedDate "gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="3f6a3-121">"CreatedDate gt 2019-12-20"</span></span>                      |
| <span data-ttu-id="3f6a3-122">Ruft Tickets ab dem 20. Dezember, 2019, die im geöffneten Zustand sind</span><span class="sxs-lookup"><span data-stu-id="3f6a3-122">Gets tickets created after 20th Dec, 2019 that are in open state</span></span> | <span data-ttu-id="3f6a3-123">"" CreatedDate "gt 2019-12-20 und Status EQ" Öffnen "</span><span class="sxs-lookup"><span data-stu-id="3f6a3-123">"CreatedDate gt 2019-12-20 and Status eq 'Open'"</span></span> |


<span data-ttu-id="3f6a3-124">Dieses Cmdlet unterstützt Paging über First-und Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="3f6a3-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="3f6a3-125">Sie können auch ein einzelnes Support Ticket abrufen, indem Sie den Ticket Namen angeben.</span><span class="sxs-lookup"><span data-stu-id="3f6a3-125">You can also retrieve a single support ticket by specifying the ticket name.</span></span> 

## <span data-ttu-id="3f6a3-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3f6a3-126">EXAMPLES</span></span>

### <span data-ttu-id="3f6a3-127">Beispiel 1: erste 2 Tickets erhalten</span><span class="sxs-lookup"><span data-stu-id="3f6a3-127">Example 1: Get first 2 tickets</span></span>
```powershell
PS C:\> Get-AzSupportTicket -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="3f6a3-128">Beispiel 2: Abrufen der ersten 2 Tickets nach dem Überspringen der ersten 2</span><span class="sxs-lookup"><span data-stu-id="3f6a3-128">Example 2: Get first 2 tickets after skipping the first 2</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Skip 2 -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test3 test title3                  150010521000314 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test4 test title4                  150010521000315 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="3f6a3-129">Beispiel 3: Abrufen eines Support Tickets nach Name</span><span class="sxs-lookup"><span data-stu-id="3f6a3-129">Example 3: Get a support ticket by name</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="3f6a3-130">Beispiel 4: Abrufen der ersten 2 Support Tickets nach Status gefiltert</span><span class="sxs-lookup"><span data-stu-id="3f6a3-130">Example 4: Get first 2 support tickets filtered by status</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Closed'" -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="3f6a3-131">Beispiel 5: Abrufen aller Support Tickets, die sich im geöffneten Zustand befinden und nach dem 20. Dezember 2019 erstellt wurden</span><span class="sxs-lookup"><span data-stu-id="3f6a3-131">Example 5: Get all support tickets that are in Open state and created after Dec 20th, 2019</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Open' and CreatedDate gt 2019-12-20"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test6 test title6                  150010521000311 Minimal  Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
test7 test title7                  150010521000312 Minimal  Billing                       Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="3f6a3-132">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f6a3-132">PARAMETERS</span></span>

### <span data-ttu-id="3f6a3-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f6a3-133">-DefaultProfile</span></span>
<span data-ttu-id="3f6a3-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3f6a3-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f6a3-135">-Filter</span><span class="sxs-lookup"><span data-stu-id="3f6a3-135">-Filter</span></span>
<span data-ttu-id="3f6a3-136">Filter, der auf die Ergebnisse dieses Cmdlets angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f6a3-136">Filter to be applied to the results of this cmdlet.</span></span>

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

### <span data-ttu-id="3f6a3-137">-Name</span><span class="sxs-lookup"><span data-stu-id="3f6a3-137">-Name</span></span>
<span data-ttu-id="3f6a3-138">Name des Support Tickets, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="3f6a3-138">Name of support ticket that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3f6a3-139">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="3f6a3-139">-IncludeTotalCount</span></span>
<span data-ttu-id="3f6a3-140">Gibt die Gesamtzahl der Objekte in der Datengruppe (einer ganzen Zahl) an, gefolgt von den ausgewählten Objekten.</span><span class="sxs-lookup"><span data-stu-id="3f6a3-140">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="3f6a3-141">Wenn das Cmdlet die Gesamtanzahl nicht ermitteln kann, wird "unbekannte Gesamtanzahl" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3f6a3-141">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="3f6a3-142">Die ganze Zahl verfügt über eine Genauigkeits Eigenschaft, die die Zuverlässigkeit des Gesamtanzahl Werts angibt.</span><span class="sxs-lookup"><span data-stu-id="3f6a3-142">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="3f6a3-143">Der Wert der Genauigkeit reicht von 0,0 bis 1,0, wobei 0,0 bedeutet, dass das Cmdlet die Objekte nicht zählen konnte, 1,0 bedeutet, dass die Anzahl exakt ist, und ein Wert zwischen 0,0 und 1,0 eine zunehmend zuverlässige Schätzung angibt.</span><span class="sxs-lookup"><span data-stu-id="3f6a3-143">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="3f6a3-144">-Skip</span><span class="sxs-lookup"><span data-stu-id="3f6a3-144">-Skip</span></span>
<span data-ttu-id="3f6a3-145">Ignoriert die angegebene Anzahl von Objekten und ruft dann die restlichen Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="3f6a3-145">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="3f6a3-146">Geben Sie die Anzahl der zu überspringenden Objekte ein.</span><span class="sxs-lookup"><span data-stu-id="3f6a3-146">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="3f6a3-147">-First</span><span class="sxs-lookup"><span data-stu-id="3f6a3-147">-First</span></span>
<span data-ttu-id="3f6a3-148">Ruft nur die angegebene Anzahl von Objekten ab.</span><span class="sxs-lookup"><span data-stu-id="3f6a3-148">Gets only the specified number of objects.</span></span>
<span data-ttu-id="3f6a3-149">Geben Sie die Anzahl der abzurufenden Objekte ein.</span><span class="sxs-lookup"><span data-stu-id="3f6a3-149">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="3f6a3-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f6a3-150">CommonParameters</span></span>
<span data-ttu-id="3f6a3-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f6a3-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f6a3-152">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f6a3-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f6a3-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3f6a3-153">INPUTS</span></span>

### <span data-ttu-id="3f6a3-154">Keine</span><span class="sxs-lookup"><span data-stu-id="3f6a3-154">None</span></span>

## <span data-ttu-id="3f6a3-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3f6a3-155">OUTPUTS</span></span>

### <span data-ttu-id="3f6a3-156">Microsoft. Azure. Commands. Support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="3f6a3-156">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="3f6a3-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="3f6a3-157">NOTES</span></span>

## <span data-ttu-id="3f6a3-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3f6a3-158">RELATED LINKS</span></span>
