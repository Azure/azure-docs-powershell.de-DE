---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/new-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
ms.openlocfilehash: 0c8595605f5dc84c28e4e00ee66e72cdfc79256c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929179"
---
# <span data-ttu-id="bae2b-101">New-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="bae2b-101">New-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="bae2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bae2b-102">SYNOPSIS</span></span>
<span data-ttu-id="bae2b-103">Erstellt eine neue Supportticketkommunikation.</span><span class="sxs-lookup"><span data-stu-id="bae2b-103">Creates a new support ticket communication.</span></span>

## <span data-ttu-id="bae2b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bae2b-104">SYNTAX</span></span>

### <span data-ttu-id="bae2b-105">CreateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bae2b-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSupportTicketCommunication -SupportTicketName <String> -Name <String> -Subject <String> -Body <String>
 [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bae2b-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bae2b-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSupportTicketCommunication -SupportTicketObject <PSSupportTicket> -Name <String> -Subject <String>
 -Body <String> [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bae2b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bae2b-107">DESCRIPTION</span></span>
<span data-ttu-id="bae2b-108">Fügt einem Azure-Supportticket eine neue Kundenkommunikation hinzu.</span><span class="sxs-lookup"><span data-stu-id="bae2b-108">Adds a new customer communication to an Azure support ticket.</span></span>

## <span data-ttu-id="bae2b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bae2b-109">EXAMPLES</span></span>

### <span data-ttu-id="bae2b-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bae2b-110">Example 1</span></span>
```powershell
PS C:\> New-AzSupportTicketCommunication -Name "testmessage" -SupportTicketName "testticket" -Subject "test subject" -Body "test body" -Sender "user@contoso.com"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage  user@contoso.com     test subject   2/4/2020 9:38:14 PM
```

## <span data-ttu-id="bae2b-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bae2b-111">PARAMETERS</span></span>

### <span data-ttu-id="bae2b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bae2b-112">-AsJob</span></span>
<span data-ttu-id="bae2b-113">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="bae2b-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="bae2b-114">-Body</span><span class="sxs-lookup"><span data-stu-id="bae2b-114">-Body</span></span>
<span data-ttu-id="bae2b-115">Textkörper der Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="bae2b-115">Body of the communication.</span></span>

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

### <span data-ttu-id="bae2b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bae2b-116">-DefaultProfile</span></span>
<span data-ttu-id="bae2b-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bae2b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bae2b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="bae2b-118">-Name</span></span>
<span data-ttu-id="bae2b-119">Name der Kommunikationsressource.</span><span class="sxs-lookup"><span data-stu-id="bae2b-119">Name of the communication resource.</span></span>

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

### <span data-ttu-id="bae2b-120">-Sender</span><span class="sxs-lookup"><span data-stu-id="bae2b-120">-Sender</span></span>
<span data-ttu-id="bae2b-121">E-Mail-Adresse des Absenders.</span><span class="sxs-lookup"><span data-stu-id="bae2b-121">Email address of the sender.</span></span>

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

### <span data-ttu-id="bae2b-122">-Subject</span><span class="sxs-lookup"><span data-stu-id="bae2b-122">-Subject</span></span>
<span data-ttu-id="bae2b-123">Betreff der Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="bae2b-123">Subject of the communication.</span></span>

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

### <span data-ttu-id="bae2b-124">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="bae2b-124">-SupportTicketName</span></span>
<span data-ttu-id="bae2b-125">Name des Supporttickets.</span><span class="sxs-lookup"><span data-stu-id="bae2b-125">Support ticket name.</span></span>

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

### <span data-ttu-id="bae2b-126">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="bae2b-126">-SupportTicketObject</span></span>
<span data-ttu-id="bae2b-127">Unterstützen Sie das Ticketobjekt.</span><span class="sxs-lookup"><span data-stu-id="bae2b-127">Support ticket object.</span></span>

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

### <span data-ttu-id="bae2b-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bae2b-128">-Confirm</span></span>
<span data-ttu-id="bae2b-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bae2b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bae2b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bae2b-130">-WhatIf</span></span>
<span data-ttu-id="bae2b-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bae2b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bae2b-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bae2b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bae2b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bae2b-133">CommonParameters</span></span>
<span data-ttu-id="bae2b-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bae2b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bae2b-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bae2b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bae2b-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bae2b-136">INPUTS</span></span>

### <span data-ttu-id="bae2b-137">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="bae2b-137">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="bae2b-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bae2b-138">OUTPUTS</span></span>

### <span data-ttu-id="bae2b-139">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="bae2b-139">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="bae2b-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bae2b-140">NOTES</span></span>

## <span data-ttu-id="bae2b-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bae2b-141">RELATED LINKS</span></span>
