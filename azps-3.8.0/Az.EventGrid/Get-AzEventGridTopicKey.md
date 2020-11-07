---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
ms.openlocfilehash: a956e0e99db44e5f92b4d9ec772158b262434c05
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846083"
---
# <span data-ttu-id="79082-101">Get-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="79082-101">Get-AzEventGridTopicKey</span></span>

## <span data-ttu-id="79082-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="79082-102">SYNOPSIS</span></span>
<span data-ttu-id="79082-103">Ruft die freigegebenen Zugriffstasten ab, die zum Veröffentlichen von Ereignissen in einem Ereignis Raster Thema verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="79082-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="79082-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="79082-104">SYNTAX</span></span>

### <span data-ttu-id="79082-105">TopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="79082-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79082-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79082-106">TopicInputObjectParameterSet</span></span>
```
Get-AzEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="79082-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="79082-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79082-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="79082-108">DESCRIPTION</span></span>
<span data-ttu-id="79082-109">Ruft die freigegebenen Zugriffstasten ab, die zum Veröffentlichen von Ereignissen in einem Ereignis Raster Thema verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="79082-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="79082-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="79082-110">EXAMPLES</span></span>

### <span data-ttu-id="79082-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="79082-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="79082-112">Ruft die freigegebenen Zugriffstasten des Ereignis Rasters Topic \` THEMA1 hat \` in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="79082-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="79082-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="79082-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzEventGridTopicKey
```

<span data-ttu-id="79082-114">Ruft die freigegebenen Zugriffstasten des Ereignis Rasters Topic \` THEMA1 hat \` in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="79082-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="79082-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="79082-115">PARAMETERS</span></span>

### <span data-ttu-id="79082-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79082-116">-DefaultProfile</span></span>
<span data-ttu-id="79082-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="79082-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79082-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="79082-118">-InputObject</span></span>
<span data-ttu-id="79082-119">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="79082-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="79082-120">-Name</span><span class="sxs-lookup"><span data-stu-id="79082-120">-Name</span></span>
<span data-ttu-id="79082-121">EventGrid-Themen Name</span><span class="sxs-lookup"><span data-stu-id="79082-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="79082-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79082-122">-ResourceGroupName</span></span>
<span data-ttu-id="79082-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="79082-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="79082-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="79082-124">-ResourceId</span></span>
<span data-ttu-id="79082-125">Ressourcenbezeichner, der das Thema des Ereignis Rasters darstellt.</span><span class="sxs-lookup"><span data-stu-id="79082-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="79082-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79082-126">CommonParameters</span></span>
<span data-ttu-id="79082-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79082-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79082-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79082-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79082-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="79082-129">INPUTS</span></span>

### <span data-ttu-id="79082-130">System. String</span><span class="sxs-lookup"><span data-stu-id="79082-130">System.String</span></span>

### <span data-ttu-id="79082-131">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="79082-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="79082-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="79082-132">OUTPUTS</span></span>

### <span data-ttu-id="79082-133">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="79082-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="79082-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="79082-134">NOTES</span></span>

## <span data-ttu-id="79082-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="79082-135">RELATED LINKS</span></span>
