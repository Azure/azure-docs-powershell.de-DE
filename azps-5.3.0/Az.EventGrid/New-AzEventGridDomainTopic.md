---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
ms.openlocfilehash: 2923f05bc954c0570c49886c3a036ef78848a1e7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458724"
---
# <span data-ttu-id="8df7c-101">New-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="8df7c-101">New-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="8df7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8df7c-102">SYNOPSIS</span></span>
<span data-ttu-id="8df7c-103">Erstellt ein neues Azure Event Grid Domain Topic.</span><span class="sxs-lookup"><span data-stu-id="8df7c-103">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="8df7c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8df7c-104">SYNTAX</span></span>

```
New-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8df7c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8df7c-105">DESCRIPTION</span></span>
<span data-ttu-id="8df7c-106">Erstellt ein neues Azure Event Grid Domain Topic.</span><span class="sxs-lookup"><span data-stu-id="8df7c-106">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="8df7c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8df7c-107">EXAMPLES</span></span>

### <span data-ttu-id="8df7c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8df7c-108">Example 1</span></span>

<span data-ttu-id="8df7c-109">Erstellt ein "Event Grid Domain \` \` Topic1" in \` "Domäne1" \` unter der Ressourcengruppe \` "MyResourceGroupName". \`</span><span class="sxs-lookup"><span data-stu-id="8df7c-109">Creates an Event Grid Domain Topic \`Topic1\` in Domain \`Domain1\` under resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : topic1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/topic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

## <span data-ttu-id="8df7c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8df7c-110">PARAMETERS</span></span>

### <span data-ttu-id="8df7c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8df7c-111">-DefaultProfile</span></span>
<span data-ttu-id="8df7c-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8df7c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8df7c-113">-DomainName</span><span class="sxs-lookup"><span data-stu-id="8df7c-113">-DomainName</span></span>
<span data-ttu-id="8df7c-114">Name der EventGrid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="8df7c-114">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Domain

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8df7c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8df7c-115">-Name</span></span>
<span data-ttu-id="8df7c-116">Name des Themas "EventGrid".</span><span class="sxs-lookup"><span data-stu-id="8df7c-116">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainTopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8df7c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8df7c-117">-ResourceGroupName</span></span>
<span data-ttu-id="8df7c-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8df7c-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8df7c-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8df7c-119">-Confirm</span></span>
<span data-ttu-id="8df7c-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8df7c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8df7c-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8df7c-121">-WhatIf</span></span>
<span data-ttu-id="8df7c-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8df7c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8df7c-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8df7c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8df7c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8df7c-124">CommonParameters</span></span>
<span data-ttu-id="8df7c-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8df7c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8df7c-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8df7c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8df7c-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8df7c-127">INPUTS</span></span>

### <span data-ttu-id="8df7c-128">System.String</span><span class="sxs-lookup"><span data-stu-id="8df7c-128">System.String</span></span>

## <span data-ttu-id="8df7c-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8df7c-129">OUTPUTS</span></span>

### <span data-ttu-id="8df7c-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="8df7c-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="8df7c-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8df7c-131">NOTES</span></span>

## <span data-ttu-id="8df7c-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8df7c-132">RELATED LINKS</span></span>
