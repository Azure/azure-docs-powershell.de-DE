---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
ms.openlocfilehash: b0690882cc230a92fd6e81e38832f2fc352e131c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292546"
---
# <span data-ttu-id="e9f85-101">Get-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="e9f85-101">Get-AzEventGridTopicKey</span></span>

## <span data-ttu-id="e9f85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9f85-102">SYNOPSIS</span></span>
<span data-ttu-id="e9f85-103">Ruft die freigegebenen Zugriffstasten ab, die zum Veröffentlichen von Ereignissen in einem Ereignisrasterthema verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e9f85-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="e9f85-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e9f85-104">SYNTAX</span></span>

### <span data-ttu-id="e9f85-105">TopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e9f85-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9f85-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9f85-106">TopicInputObjectParameterSet</span></span>
```
Get-AzEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e9f85-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9f85-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9f85-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e9f85-108">DESCRIPTION</span></span>
<span data-ttu-id="e9f85-109">Ruft die freigegebenen Zugriffstasten ab, die zum Veröffentlichen von Ereignissen in einem Ereignisrasterthema verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e9f85-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="e9f85-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e9f85-110">EXAMPLES</span></span>

### <span data-ttu-id="e9f85-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e9f85-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="e9f85-112">Ruft die freigegebenen Zugriffstasten des Themas "Veranstaltungsraster", \` \` Thema1, in der Ressourcengruppe \` "MyResourceGroupName" \` ab.</span><span class="sxs-lookup"><span data-stu-id="e9f85-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="e9f85-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e9f85-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzEventGridTopicKey
```

<span data-ttu-id="e9f85-114">Ruft die freigegebenen Zugriffstasten des Themas "Veranstaltungsraster", \` \` Thema1, in der Ressourcengruppe \` "MyResourceGroupName" \` ab.</span><span class="sxs-lookup"><span data-stu-id="e9f85-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="e9f85-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9f85-115">PARAMETERS</span></span>

### <span data-ttu-id="e9f85-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9f85-116">-DefaultProfile</span></span>
<span data-ttu-id="e9f85-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e9f85-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9f85-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9f85-118">-InputObject</span></span>
<span data-ttu-id="e9f85-119">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e9f85-119">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9f85-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e9f85-120">-Name</span></span>
<span data-ttu-id="e9f85-121">Name des EventGrid-Themas.</span><span class="sxs-lookup"><span data-stu-id="e9f85-121">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9f85-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9f85-122">-ResourceGroupName</span></span>
<span data-ttu-id="e9f85-123">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="e9f85-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9f85-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9f85-124">-ResourceId</span></span>
<span data-ttu-id="e9f85-125">Ressourcenbezeichner, der das Thema "Veranstaltungsraster" darstellt.</span><span class="sxs-lookup"><span data-stu-id="e9f85-125">Resource Identifier representing the Event Grid Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9f85-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9f85-126">CommonParameters</span></span>
<span data-ttu-id="e9f85-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9f85-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9f85-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9f85-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9f85-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e9f85-129">INPUTS</span></span>

### <span data-ttu-id="e9f85-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e9f85-130">System.String</span></span>

### <span data-ttu-id="e9f85-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="e9f85-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="e9f85-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e9f85-132">OUTPUTS</span></span>

### <span data-ttu-id="e9f85-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="e9f85-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="e9f85-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e9f85-134">NOTES</span></span>

## <span data-ttu-id="e9f85-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e9f85-135">RELATED LINKS</span></span>
