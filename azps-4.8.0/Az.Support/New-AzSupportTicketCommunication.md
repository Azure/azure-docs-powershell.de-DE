---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
ms.openlocfilehash: 3a0191e1df223427ec7d60dfd92f7607e2c171b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166737"
---
# <span data-ttu-id="4662f-101">New-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="4662f-101">New-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="4662f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4662f-102">SYNOPSIS</span></span>
<span data-ttu-id="4662f-103">Erstellt eine neue Support Ticket-Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="4662f-103">Creates a new support ticket communication.</span></span>

## <span data-ttu-id="4662f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4662f-104">SYNTAX</span></span>

### <span data-ttu-id="4662f-105">CreateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4662f-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSupportTicketCommunication -SupportTicketName <String> -Name <String> -Subject <String> -Body <String>
 [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4662f-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4662f-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSupportTicketCommunication -SupportTicketObject <PSSupportTicket> -Name <String> -Subject <String>
 -Body <String> [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4662f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4662f-107">DESCRIPTION</span></span>
<span data-ttu-id="4662f-108">Fügt eine neue Kundenkommunikation zu einem Azure Support-Ticket hinzu.</span><span class="sxs-lookup"><span data-stu-id="4662f-108">Adds a new customer communication to an Azure support ticket.</span></span>

## <span data-ttu-id="4662f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4662f-109">EXAMPLES</span></span>

### <span data-ttu-id="4662f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4662f-110">Example 1</span></span>
```powershell
PS C:\> New-AzSupportTicketCommunication -Name "testmessage" -SupportTicketName "testticket" -Subject "test subject" -Body "test body" -Sender "user@contoso.com"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage  user@contoso.com     test subject   2/4/2020 9:38:14 PM
```

## <span data-ttu-id="4662f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="4662f-111">PARAMETERS</span></span>

### <span data-ttu-id="4662f-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4662f-112">-AsJob</span></span>
<span data-ttu-id="4662f-113">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="4662f-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="4662f-114">-Body</span><span class="sxs-lookup"><span data-stu-id="4662f-114">-Body</span></span>
<span data-ttu-id="4662f-115">Der Text der Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="4662f-115">Body of the communication.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4662f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4662f-116">-DefaultProfile</span></span>
<span data-ttu-id="4662f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4662f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4662f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4662f-118">-Name</span></span>
<span data-ttu-id="4662f-119">Der Name der Kommunikationsressource.</span><span class="sxs-lookup"><span data-stu-id="4662f-119">Name of the communication resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4662f-120">– Absender</span><span class="sxs-lookup"><span data-stu-id="4662f-120">-Sender</span></span>
<span data-ttu-id="4662f-121">E-Mail-Adresse des Absenders.</span><span class="sxs-lookup"><span data-stu-id="4662f-121">Email address of the sender.</span></span>

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

### <span data-ttu-id="4662f-122">-Betreff</span><span class="sxs-lookup"><span data-stu-id="4662f-122">-Subject</span></span>
<span data-ttu-id="4662f-123">Betreff der Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="4662f-123">Subject of the communication.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4662f-124">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="4662f-124">-SupportTicketName</span></span>
<span data-ttu-id="4662f-125">Name des Support Tickets</span><span class="sxs-lookup"><span data-stu-id="4662f-125">Support ticket name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4662f-126">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="4662f-126">-SupportTicketObject</span></span>
<span data-ttu-id="4662f-127">Support-Ticket-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4662f-127">Support ticket object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4662f-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4662f-128">-Confirm</span></span>
<span data-ttu-id="4662f-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4662f-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4662f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4662f-130">-WhatIf</span></span>
<span data-ttu-id="4662f-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4662f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4662f-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4662f-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4662f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4662f-133">CommonParameters</span></span>
<span data-ttu-id="4662f-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4662f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4662f-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4662f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4662f-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4662f-136">INPUTS</span></span>

### <span data-ttu-id="4662f-137">Microsoft. Azure. Commands. Support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="4662f-137">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="4662f-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4662f-138">OUTPUTS</span></span>

### <span data-ttu-id="4662f-139">Microsoft. Azure. Commands. Support. Models. PSSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="4662f-139">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="4662f-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="4662f-140">NOTES</span></span>

## <span data-ttu-id="4662f-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4662f-141">RELATED LINKS</span></span>
