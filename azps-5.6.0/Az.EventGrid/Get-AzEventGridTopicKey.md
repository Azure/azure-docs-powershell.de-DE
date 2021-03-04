---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
ms.openlocfilehash: 92a70d16f8cd1db2c37c1247c994a3c406df5a54
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938768"
---
# <span data-ttu-id="c5f02-101">Get-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="c5f02-101">Get-AzEventGridTopicKey</span></span>

## <span data-ttu-id="c5f02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5f02-102">SYNOPSIS</span></span>
<span data-ttu-id="c5f02-103">Ruft die freigegebenen Zugriffstasten ab, die zum Veröffentlichen von Ereignissen in einem Thema "Ereignisraster" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c5f02-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="c5f02-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c5f02-104">SYNTAX</span></span>

### <span data-ttu-id="c5f02-105">TopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c5f02-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5f02-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5f02-106">TopicInputObjectParameterSet</span></span>
```
Get-AzEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c5f02-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5f02-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5f02-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c5f02-108">DESCRIPTION</span></span>
<span data-ttu-id="c5f02-109">Ruft die freigegebenen Zugriffstasten ab, die zum Veröffentlichen von Ereignissen in einem Thema "Ereignisraster" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c5f02-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="c5f02-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c5f02-110">EXAMPLES</span></span>

### <span data-ttu-id="c5f02-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c5f02-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="c5f02-112">Ruft die freigegebenen Zugriffstasten des Themas "Ereignisraster" \` Topic1 \` in der Ressourcengruppe \` MyResourceGroupName \` ab.</span><span class="sxs-lookup"><span data-stu-id="c5f02-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c5f02-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c5f02-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzEventGridTopicKey
```

<span data-ttu-id="c5f02-114">Ruft die freigegebenen Zugriffstasten des Themas "Ereignisraster" \` Topic1 \` in der Ressourcengruppe \` MyResourceGroupName \` ab.</span><span class="sxs-lookup"><span data-stu-id="c5f02-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="c5f02-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c5f02-115">PARAMETERS</span></span>

### <span data-ttu-id="c5f02-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5f02-116">-DefaultProfile</span></span>
<span data-ttu-id="c5f02-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c5f02-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5f02-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5f02-118">-InputObject</span></span>
<span data-ttu-id="c5f02-119">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c5f02-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="c5f02-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c5f02-120">-Name</span></span>
<span data-ttu-id="c5f02-121">Name des EventGrid-Themas.</span><span class="sxs-lookup"><span data-stu-id="c5f02-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="c5f02-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5f02-122">-ResourceGroupName</span></span>
<span data-ttu-id="c5f02-123">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="c5f02-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="c5f02-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5f02-124">-ResourceId</span></span>
<span data-ttu-id="c5f02-125">Ressourcenbezeichner, der das Thema "Ereignisraster" darstellt.</span><span class="sxs-lookup"><span data-stu-id="c5f02-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="c5f02-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5f02-126">CommonParameters</span></span>
<span data-ttu-id="c5f02-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5f02-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5f02-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5f02-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5f02-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c5f02-129">INPUTS</span></span>

### <span data-ttu-id="c5f02-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c5f02-130">System.String</span></span>

### <span data-ttu-id="c5f02-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="c5f02-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="c5f02-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c5f02-132">OUTPUTS</span></span>

### <span data-ttu-id="c5f02-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="c5f02-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="c5f02-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c5f02-134">NOTES</span></span>

## <span data-ttu-id="c5f02-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c5f02-135">RELATED LINKS</span></span>
