---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/get-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
ms.openlocfilehash: 106ee61629c1252300d63ca686848ba7cc926cea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933571"
---
# <span data-ttu-id="38dad-101">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="38dad-101">Get-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="38dad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38dad-102">SYNOPSIS</span></span>
<span data-ttu-id="38dad-103">Erhalten Sie Supportticketkommunikation.</span><span class="sxs-lookup"><span data-stu-id="38dad-103">Get support ticket communications.</span></span>

## <span data-ttu-id="38dad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38dad-104">SYNTAX</span></span>

### <span data-ttu-id="38dad-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="38dad-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSupportTicketCommunication -SupportTicketName <String> [-Name <String>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

### <span data-ttu-id="38dad-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="38dad-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSupportTicketCommunication [-Name <String>] -SupportTicketObject <PSSupportTicket> [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## <span data-ttu-id="38dad-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38dad-107">DESCRIPTION</span></span>
<span data-ttu-id="38dad-108">Ruft Kommunikationen für ein Supportticket ab.</span><span class="sxs-lookup"><span data-stu-id="38dad-108">Gets communications for a support ticket.</span></span> <span data-ttu-id="38dad-109">Sie ruft alle Kommunikationen für ein Ticket ab, wenn Sie keine anderen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="38dad-109">It will retrieve all the communications for a ticket if you do not specify any other parameters.</span></span> <span data-ttu-id="38dad-110">Sie können die Kommunikation auch mithilfe des Parameters Filter nach CreatedDate oder CommunicationType filtern.</span><span class="sxs-lookup"><span data-stu-id="38dad-110">You can also filter the communications by CreatedDate or CommunicationType using the Filter parameter.</span></span> <span data-ttu-id="38dad-111">Hier sind einige Beispiele für Filterwerte, die Sie angeben können.</span><span class="sxs-lookup"><span data-stu-id="38dad-111">Here are some examples of filter values that you can specify.</span></span>


| <span data-ttu-id="38dad-112">Szenario</span><span class="sxs-lookup"><span data-stu-id="38dad-112">Scenario</span></span>                                                        | <span data-ttu-id="38dad-113">Filtern</span><span class="sxs-lookup"><span data-stu-id="38dad-113">Filter</span></span>                                                     |
|-----------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="38dad-114">Webkommunikation erhalten</span><span class="sxs-lookup"><span data-stu-id="38dad-114">Get Web communications</span></span>                                          | <span data-ttu-id="38dad-115">"CommunicationType eq 'Web'"</span><span class="sxs-lookup"><span data-stu-id="38dad-115">"CommunicationType eq 'Web'"</span></span>                               |
| <span data-ttu-id="38dad-116">Telefonkommunikation erhalten</span><span class="sxs-lookup"><span data-stu-id="38dad-116">Get Phone communications</span></span>                                        | <span data-ttu-id="38dad-117">"CommunicationType eq 'Phone'"</span><span class="sxs-lookup"><span data-stu-id="38dad-117">"CommunicationType eq 'Phone'"</span></span>                             |
| <span data-ttu-id="38dad-118">Erhalten von Kommunikationen, die am oder nach dem 20. Dez. 2019 erstellt wurden</span><span class="sxs-lookup"><span data-stu-id="38dad-118">Get communications that were created on or after 20th Dec, 2019</span></span> | <span data-ttu-id="38dad-119">"CreatedDate ge 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="38dad-119">"CreatedDate ge 2019-12-20"</span></span>                                |
| <span data-ttu-id="38dad-120">Erhalten von Kommunikationen, die nach dem 20. Dez. 2019 erstellt wurden</span><span class="sxs-lookup"><span data-stu-id="38dad-120">Get communications that were created after 20th Dec, 2019</span></span>       | <span data-ttu-id="38dad-121">"CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="38dad-121">"CreatedDate gt 2019-12-20"</span></span>                                |
| <span data-ttu-id="38dad-122">Ruft web communications created after 20th Dec, 2019</span><span class="sxs-lookup"><span data-stu-id="38dad-122">Gets Web communications created after 20th Dec, 2019</span></span>            | <span data-ttu-id="38dad-123">"CreatedDate gt 2019-12-20 und CommunicationType eq 'Web'"</span><span class="sxs-lookup"><span data-stu-id="38dad-123">"CreatedDate gt 2019-12-20 and CommunicationType eq 'Web'"</span></span> |


<span data-ttu-id="38dad-124">Dieses Cmdlet unterstützt die Auslagerung über die Parameter "First" und "Skip".</span><span class="sxs-lookup"><span data-stu-id="38dad-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="38dad-125">Sie können auch eine einzelne Supportticketkommunikation abrufen, indem Sie den Kommunikationsnamen angeben.</span><span class="sxs-lookup"><span data-stu-id="38dad-125">You can also retrieve a single support ticket communication by specifying the communication name.</span></span> 

## <span data-ttu-id="38dad-126">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="38dad-126">EXAMPLES</span></span>

### <span data-ttu-id="38dad-127">Beispiel 1: Abrufen aller Kommunikationen für ein Supportticket</span><span class="sxs-lookup"><span data-stu-id="38dad-127">Example 1: Retrieve all communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

### <span data-ttu-id="38dad-128">Beispiel 2: Abrufen einer einzelnen Kommunikation nach dem Namen eines Supporttickets</span><span class="sxs-lookup"><span data-stu-id="38dad-128">Example 2: Retrieve a single communication by it's name for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Name "testmessage1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage1 user@contoso.com     test message   2/4/2020 9:38:14 PM
```

### <span data-ttu-id="38dad-129">Beispiel 3: Abrufen der ersten 2-Kommunikation für ein Supportticket</span><span class="sxs-lookup"><span data-stu-id="38dad-129">Example 3: Retrieve first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="38dad-130">Beispiel 4: Abrufen der nächsten 2-Kommunikation nach dem Überspringen der ersten 2-Kommunikation für ein Supportticket</span><span class="sxs-lookup"><span data-stu-id="38dad-130">Example 4: Retrieve next 2 communications after skipping first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Skip 2 -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage4 user@contoso.com     test message4  2/4/2020 9:38:14 PM
testmessage5 user@contoso.com     test message5  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="38dad-131">Beispiel 5: Abrufen aller Webkommunikationen für ein Supportticket</span><span class="sxs-lookup"><span data-stu-id="38dad-131">Example 5: Retrieve all Web communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web'"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="38dad-132">Beispiel 6: Abrufen aller kommunikationen, die am oder nach dem 20. Dezember 2019 für ein Supportticket erstellt wurden</span><span class="sxs-lookup"><span data-stu-id="38dad-132">Example 6: Retrieve all communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="38dad-133">Beispiel 7: Abrufen aller Webkommunikationen, die am oder nach dem 20. Dezember 2019 für ein Supportticket erstellt wurden</span><span class="sxs-lookup"><span data-stu-id="38dad-133">Example 7: Retrieve all Web communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web' and CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="38dad-134">Beispiel 8: Abrufen aller Kommunikationen für ein Supportticket durch Piping-Supportticketobjekt</span><span class="sxs-lookup"><span data-stu-id="38dad-134">Example 8: Retrieve all communications for a support ticket by piping support ticket object</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Get-AzSupportTicketCommunication

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

## <span data-ttu-id="38dad-135">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="38dad-135">PARAMETERS</span></span>

### <span data-ttu-id="38dad-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38dad-136">-DefaultProfile</span></span>
<span data-ttu-id="38dad-137">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="38dad-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38dad-138">-Filter</span><span class="sxs-lookup"><span data-stu-id="38dad-138">-Filter</span></span>
<span data-ttu-id="38dad-139">Filtern, um auf die Ergebnisse dieses Cmdlets angewendet zu werden.</span><span class="sxs-lookup"><span data-stu-id="38dad-139">Filter to be applied to the results of this cmdlet.</span></span>

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

### <span data-ttu-id="38dad-140">-Name</span><span class="sxs-lookup"><span data-stu-id="38dad-140">-Name</span></span>
<span data-ttu-id="38dad-141">Kommunikationsname.</span><span class="sxs-lookup"><span data-stu-id="38dad-141">Communication name.</span></span>

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

### <span data-ttu-id="38dad-142">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="38dad-142">-SupportTicketName</span></span>
<span data-ttu-id="38dad-143">Name des Supporttickets.</span><span class="sxs-lookup"><span data-stu-id="38dad-143">Support ticket name.</span></span>

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

### <span data-ttu-id="38dad-144">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="38dad-144">-SupportTicketObject</span></span>
<span data-ttu-id="38dad-145">Unterstützen Sie das Ticketobjekt.</span><span class="sxs-lookup"><span data-stu-id="38dad-145">Support ticket object.</span></span>

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

### <span data-ttu-id="38dad-146">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="38dad-146">-IncludeTotalCount</span></span>
<span data-ttu-id="38dad-147">Gibt die Gesamtanzahl der Objekte im Datenset (eine ganze Zahl) gefolgt von den ausgewählten Objekten an.</span><span class="sxs-lookup"><span data-stu-id="38dad-147">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="38dad-148">Wenn das Cmdlet die Gesamtanzahl nicht ermitteln kann, wird "Unbekannte Gesamtanzahl" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="38dad-148">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="38dad-149">Die ganze Zahl weist eine Genauigkeitseigenschaft auf, die die Zuverlässigkeit des Gesamtwertswerts angibt.</span><span class="sxs-lookup"><span data-stu-id="38dad-149">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="38dad-150">Der Wert der Genauigkeit reicht von 0,0 bis 1,0, wobei 0,0 bedeutet, dass das Cmdlet die Objekte nicht zählen konnte, 1,0 bedeutet, dass die Anzahl exakt ist, und ein Wert zwischen 0,0 und 1,0 gibt eine immer zuverlässigere Schätzung an.</span><span class="sxs-lookup"><span data-stu-id="38dad-150">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="38dad-151">-Skip</span><span class="sxs-lookup"><span data-stu-id="38dad-151">-Skip</span></span>
<span data-ttu-id="38dad-152">Ignoriert die angegebene Anzahl von Objekten und ruft dann die verbleibenden Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="38dad-152">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="38dad-153">Geben Sie die Anzahl der zu überspringende Objekte ein.</span><span class="sxs-lookup"><span data-stu-id="38dad-153">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="38dad-154">-First</span><span class="sxs-lookup"><span data-stu-id="38dad-154">-First</span></span>
<span data-ttu-id="38dad-155">Ruft nur die angegebene Anzahl von Objekten ab.</span><span class="sxs-lookup"><span data-stu-id="38dad-155">Gets only the specified number of objects.</span></span>
<span data-ttu-id="38dad-156">Geben Sie die Anzahl der zu erhaltende Objekte ein.</span><span class="sxs-lookup"><span data-stu-id="38dad-156">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="38dad-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38dad-157">CommonParameters</span></span>
<span data-ttu-id="38dad-158">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38dad-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38dad-159">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38dad-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38dad-160">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="38dad-160">INPUTS</span></span>

### <span data-ttu-id="38dad-161">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="38dad-161">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="38dad-162">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="38dad-162">OUTPUTS</span></span>

### <span data-ttu-id="38dad-163">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="38dad-163">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="38dad-164">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="38dad-164">NOTES</span></span>

## <span data-ttu-id="38dad-165">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="38dad-165">RELATED LINKS</span></span>
