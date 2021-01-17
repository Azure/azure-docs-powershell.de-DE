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
# <span data-ttu-id="e3a34-101">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="e3a34-101">Get-AzSupportTicket</span></span>

## <span data-ttu-id="e3a34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3a34-102">SYNOPSIS</span></span>
<span data-ttu-id="e3a34-103">Supporttickets erhalten.</span><span class="sxs-lookup"><span data-stu-id="e3a34-103">Get support tickets.</span></span>

## <span data-ttu-id="e3a34-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e3a34-104">SYNTAX</span></span>

### <span data-ttu-id="e3a34-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e3a34-105">ListParameterSet (Default)</span></span>
```
Get-AzSupportTicket [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e3a34-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3a34-106">GetByNameParameterSet</span></span>
```
Get-AzSupportTicket -Name <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="e3a34-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e3a34-107">DESCRIPTION</span></span>
<span data-ttu-id="e3a34-108">Ruft die Liste der Supporttickets ab.</span><span class="sxs-lookup"><span data-stu-id="e3a34-108">Gets the list of support tickets.</span></span> <span data-ttu-id="e3a34-109">Sie ruft alle Supporttickets ab, wenn Sie keine Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="e3a34-109">It will retrieve all the support tickets if you do not specify any parameters.</span></span> <span data-ttu-id="e3a34-110">Sie können die Supporttickets auch mithilfe des Parameters "Filter" nach "Status" oder "CreatedDate" filtern.</span><span class="sxs-lookup"><span data-stu-id="e3a34-110">You can also filter the support tickets by Status or CreatedDate using the Filter parameter.</span></span> <span data-ttu-id="e3a34-111">Im Folgenden finden Sie einige Beispiele für Filterwerte, die Sie angeben können.</span><span class="sxs-lookup"><span data-stu-id="e3a34-111">Here are some examples of filter values that you can specify.</span></span>

| <span data-ttu-id="e3a34-112">Szenario</span><span class="sxs-lookup"><span data-stu-id="e3a34-112">Scenario</span></span>                                                         | <span data-ttu-id="e3a34-113">Filter</span><span class="sxs-lookup"><span data-stu-id="e3a34-113">Filter</span></span>                                           |
|------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="e3a34-114">Tickets erhalten, die sich im geöffneten Zustand befinden</span><span class="sxs-lookup"><span data-stu-id="e3a34-114">Get tickets that are in open state</span></span>                               | <span data-ttu-id="e3a34-115">"Status eq 'Open'"</span><span class="sxs-lookup"><span data-stu-id="e3a34-115">"Status eq 'Open'"</span></span>                               |
| <span data-ttu-id="e3a34-116">Tickets erhalten, die sich im geschlossenen Zustand befinden</span><span class="sxs-lookup"><span data-stu-id="e3a34-116">Get tickets that are in closed state</span></span>                             | <span data-ttu-id="e3a34-117">"Status eq 'Closed'"</span><span class="sxs-lookup"><span data-stu-id="e3a34-117">"Status eq 'Closed'"</span></span>                             |
| <span data-ttu-id="e3a34-118">Tickets erhalten, die am oder nach dem 20. Dez. 2019 erstellt wurden</span><span class="sxs-lookup"><span data-stu-id="e3a34-118">Get tickets that were created on or after 20th Dec, 2019</span></span>         | <span data-ttu-id="e3a34-119">"CreatedDate ge 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="e3a34-119">"CreatedDate ge 2019-12-20"</span></span>                      |
| <span data-ttu-id="e3a34-120">Tickets erhalten, die nach dem 20. Dez. 2019 erstellt wurden</span><span class="sxs-lookup"><span data-stu-id="e3a34-120">Get tickets that were created after 20th Dec, 2019</span></span>               | <span data-ttu-id="e3a34-121">"CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="e3a34-121">"CreatedDate gt 2019-12-20"</span></span>                      |
| <span data-ttu-id="e3a34-122">Ruft Nach dem 20. Dezember 2019 erstellte Tickets ab, die sich im geöffneten Zustand befinden</span><span class="sxs-lookup"><span data-stu-id="e3a34-122">Gets tickets created after 20th Dec, 2019 that are in open state</span></span> | <span data-ttu-id="e3a34-123">"CreatedDate gt 2019-12-20 and Status eq 'Open'"</span><span class="sxs-lookup"><span data-stu-id="e3a34-123">"CreatedDate gt 2019-12-20 and Status eq 'Open'"</span></span> |


<span data-ttu-id="e3a34-124">Dieses Cmdlet unterstützt die Auslagerung über die Parameter "First" und "Skip".</span><span class="sxs-lookup"><span data-stu-id="e3a34-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="e3a34-125">Sie können auch ein einzelnes Supportticket abrufen, indem Sie den Ticketnamen angeben.</span><span class="sxs-lookup"><span data-stu-id="e3a34-125">You can also retrieve a single support ticket by specifying the ticket name.</span></span> 

## <span data-ttu-id="e3a34-126">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e3a34-126">EXAMPLES</span></span>

### <span data-ttu-id="e3a34-127">Beispiel 1: Erhalten der ersten 2 Tickets</span><span class="sxs-lookup"><span data-stu-id="e3a34-127">Example 1: Get first 2 tickets</span></span>
```powershell
PS C:\> Get-AzSupportTicket -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="e3a34-128">Beispiel 2: Erhalten der ersten 2 Tickets nach dem Überspringen der ersten 2</span><span class="sxs-lookup"><span data-stu-id="e3a34-128">Example 2: Get first 2 tickets after skipping the first 2</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Skip 2 -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test3 test title3                  150010521000314 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test4 test title4                  150010521000315 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="e3a34-129">Beispiel 3: Erhalten eines Supporttickets nach Name</span><span class="sxs-lookup"><span data-stu-id="e3a34-129">Example 3: Get a support ticket by name</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="e3a34-130">Beispiel 4: Erhalten der ersten 2 nach Status gefilterten Supporttickets</span><span class="sxs-lookup"><span data-stu-id="e3a34-130">Example 4: Get first 2 support tickets filtered by status</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Closed'" -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="e3a34-131">Beispiel 5: Alle Supporttickets erhalten, die sich im Status "Open" befinden und nach dem 20. Dezember 2019 erstellt wurden</span><span class="sxs-lookup"><span data-stu-id="e3a34-131">Example 5: Get all support tickets that are in Open state and created after Dec 20th, 2019</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Open' and CreatedDate gt 2019-12-20"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test6 test title6                  150010521000311 Minimal  Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
test7 test title7                  150010521000312 Minimal  Billing                       Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="e3a34-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3a34-132">PARAMETERS</span></span>

### <span data-ttu-id="e3a34-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3a34-133">-DefaultProfile</span></span>
<span data-ttu-id="e3a34-134">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e3a34-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3a34-135">-Filter</span><span class="sxs-lookup"><span data-stu-id="e3a34-135">-Filter</span></span>
<span data-ttu-id="e3a34-136">Filter, der auf die Ergebnisse dieses Cmdlets angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e3a34-136">Filter to be applied to the results of this cmdlet.</span></span>

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

### <span data-ttu-id="e3a34-137">-Name</span><span class="sxs-lookup"><span data-stu-id="e3a34-137">-Name</span></span>
<span data-ttu-id="e3a34-138">Name des Supporttickets, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="e3a34-138">Name of support ticket that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e3a34-139">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="e3a34-139">-IncludeTotalCount</span></span>
<span data-ttu-id="e3a34-140">Gibt die Gesamtzahl der Objekte im Datenset (eine ganze Zahl) gefolgt von den ausgewählten Objekten an.</span><span class="sxs-lookup"><span data-stu-id="e3a34-140">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="e3a34-141">Wenn das Cmdlet die Gesamtzahl nicht ermitteln kann, wird "Unbekannte Gesamtzahl" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e3a34-141">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="e3a34-142">Die ganze Zahl weist eine Genauigkeitseigenschaft auf, die die Zuverlässigkeit des Gesamtanzahlswerts angibt.</span><span class="sxs-lookup"><span data-stu-id="e3a34-142">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="e3a34-143">Der Wert der Genauigkeit liegt zwischen 0,0 und 1,0, wobei 0,0 bedeutet, dass das Cmdlet die Objekte nicht zählen konnte, 1,0 bedeutet, dass die Anzahl exakt ist, und ein Wert zwischen 0,0 und 1,0 gibt eine immer zuverlässigere Schätzung an.</span><span class="sxs-lookup"><span data-stu-id="e3a34-143">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="e3a34-144">-Skip</span><span class="sxs-lookup"><span data-stu-id="e3a34-144">-Skip</span></span>
<span data-ttu-id="e3a34-145">Ignoriert die angegebene Anzahl von Objekten und ruft dann die verbleibenden Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="e3a34-145">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="e3a34-146">Geben Sie die Anzahl der zu überspringende Objekte ein.</span><span class="sxs-lookup"><span data-stu-id="e3a34-146">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="e3a34-147">-First</span><span class="sxs-lookup"><span data-stu-id="e3a34-147">-First</span></span>
<span data-ttu-id="e3a34-148">Ruft nur die angegebene Anzahl von Objekten ab.</span><span class="sxs-lookup"><span data-stu-id="e3a34-148">Gets only the specified number of objects.</span></span>
<span data-ttu-id="e3a34-149">Geben Sie die Anzahl der zu erhaltende Objekte ein.</span><span class="sxs-lookup"><span data-stu-id="e3a34-149">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="e3a34-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3a34-150">CommonParameters</span></span>
<span data-ttu-id="e3a34-151">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3a34-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3a34-152">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3a34-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3a34-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e3a34-153">INPUTS</span></span>

### <span data-ttu-id="e3a34-154">Keine</span><span class="sxs-lookup"><span data-stu-id="e3a34-154">None</span></span>

## <span data-ttu-id="e3a34-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e3a34-155">OUTPUTS</span></span>

### <span data-ttu-id="e3a34-156">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="e3a34-156">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="e3a34-157">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e3a34-157">NOTES</span></span>

## <span data-ttu-id="e3a34-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e3a34-158">RELATED LINKS</span></span>
