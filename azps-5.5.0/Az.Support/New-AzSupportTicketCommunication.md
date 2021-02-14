---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
ms.openlocfilehash: 3a0191e1df223427ec7d60dfd92f7607e2c171b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150049"
---
# <span data-ttu-id="2d3b0-101">New-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="2d3b0-101">New-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="2d3b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d3b0-102">SYNOPSIS</span></span>
<span data-ttu-id="2d3b0-103">Erstellt eine neue Kommunikation für Supporttickets.</span><span class="sxs-lookup"><span data-stu-id="2d3b0-103">Creates a new support ticket communication.</span></span>

## <span data-ttu-id="2d3b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d3b0-104">SYNTAX</span></span>

### <span data-ttu-id="2d3b0-105">CreateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2d3b0-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSupportTicketCommunication -SupportTicketName <String> -Name <String> -Subject <String> -Body <String>
 [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d3b0-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d3b0-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSupportTicketCommunication -SupportTicketObject <PSSupportTicket> -Name <String> -Subject <String>
 -Body <String> [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2d3b0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d3b0-107">DESCRIPTION</span></span>
<span data-ttu-id="2d3b0-108">Fügt einem Supportticket für Azure eine neue Kundenkommunikation hinzu.</span><span class="sxs-lookup"><span data-stu-id="2d3b0-108">Adds a new customer communication to an Azure support ticket.</span></span>

## <span data-ttu-id="2d3b0-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2d3b0-109">EXAMPLES</span></span>

### <span data-ttu-id="2d3b0-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2d3b0-110">Example 1</span></span>
```powershell
PS C:\> New-AzSupportTicketCommunication -Name "testmessage" -SupportTicketName "testticket" -Subject "test subject" -Body "test body" -Sender "user@contoso.com"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage  user@contoso.com     test subject   2/4/2020 9:38:14 PM
```

## <span data-ttu-id="2d3b0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d3b0-111">PARAMETERS</span></span>

### <span data-ttu-id="2d3b0-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d3b0-112">-AsJob</span></span>
<span data-ttu-id="2d3b0-113">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="2d3b0-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="2d3b0-114">-Body</span><span class="sxs-lookup"><span data-stu-id="2d3b0-114">-Body</span></span>
<span data-ttu-id="2d3b0-115">Textkörper der Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="2d3b0-115">Body of the communication.</span></span>

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

### <span data-ttu-id="2d3b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d3b0-116">-DefaultProfile</span></span>
<span data-ttu-id="2d3b0-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2d3b0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d3b0-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2d3b0-118">-Name</span></span>
<span data-ttu-id="2d3b0-119">Name der Kommunikationsressource.</span><span class="sxs-lookup"><span data-stu-id="2d3b0-119">Name of the communication resource.</span></span>

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

### <span data-ttu-id="2d3b0-120">-Sender</span><span class="sxs-lookup"><span data-stu-id="2d3b0-120">-Sender</span></span>
<span data-ttu-id="2d3b0-121">E-Mail-Adresse des Absenders.</span><span class="sxs-lookup"><span data-stu-id="2d3b0-121">Email address of the sender.</span></span>

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

### <span data-ttu-id="2d3b0-122">-Subject</span><span class="sxs-lookup"><span data-stu-id="2d3b0-122">-Subject</span></span>
<span data-ttu-id="2d3b0-123">Thema der Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="2d3b0-123">Subject of the communication.</span></span>

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

### <span data-ttu-id="2d3b0-124">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="2d3b0-124">-SupportTicketName</span></span>
<span data-ttu-id="2d3b0-125">Name des Supporttickets.</span><span class="sxs-lookup"><span data-stu-id="2d3b0-125">Support ticket name.</span></span>

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

### <span data-ttu-id="2d3b0-126">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="2d3b0-126">-SupportTicketObject</span></span>
<span data-ttu-id="2d3b0-127">Supportticketobjekt.</span><span class="sxs-lookup"><span data-stu-id="2d3b0-127">Support ticket object.</span></span>

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

### <span data-ttu-id="2d3b0-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d3b0-128">-Confirm</span></span>
<span data-ttu-id="2d3b0-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2d3b0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d3b0-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2d3b0-130">-WhatIf</span></span>
<span data-ttu-id="2d3b0-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d3b0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d3b0-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d3b0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d3b0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d3b0-133">CommonParameters</span></span>
<span data-ttu-id="2d3b0-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d3b0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d3b0-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d3b0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d3b0-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2d3b0-136">INPUTS</span></span>

### <span data-ttu-id="2d3b0-137">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="2d3b0-137">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="2d3b0-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2d3b0-138">OUTPUTS</span></span>

### <span data-ttu-id="2d3b0-139">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="2d3b0-139">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="2d3b0-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2d3b0-140">NOTES</span></span>

## <span data-ttu-id="2d3b0-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2d3b0-141">RELATED LINKS</span></span>
