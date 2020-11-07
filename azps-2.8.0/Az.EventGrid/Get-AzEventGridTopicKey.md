---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
ms.openlocfilehash: b39f9c3c3c1d72624c612d2743b32d306eefa131
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651233"
---
# <span data-ttu-id="10389-101">Get-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="10389-101">Get-AzEventGridTopicKey</span></span>

## <span data-ttu-id="10389-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="10389-102">SYNOPSIS</span></span>
<span data-ttu-id="10389-103">Ruft die freigegebenen Zugriffstasten ab, die zum Veröffentlichen von Ereignissen in einem Ereignis Raster Thema verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="10389-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="10389-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="10389-104">SYNTAX</span></span>

### <span data-ttu-id="10389-105">TopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="10389-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10389-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="10389-106">TopicInputObjectParameterSet</span></span>
```
Get-AzEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="10389-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="10389-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10389-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10389-108">DESCRIPTION</span></span>
<span data-ttu-id="10389-109">Ruft die freigegebenen Zugriffstasten ab, die zum Veröffentlichen von Ereignissen in einem Ereignis Raster Thema verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="10389-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="10389-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="10389-110">EXAMPLES</span></span>

### <span data-ttu-id="10389-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="10389-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="10389-112">Ruft die freigegebenen Zugriffstasten des Ereignis Rasters Topic \` THEMA1 hat \` in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="10389-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="10389-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="10389-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzEventGridTopicKey
```

<span data-ttu-id="10389-114">Ruft die freigegebenen Zugriffstasten des Ereignis Rasters Topic \` THEMA1 hat \` in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="10389-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="10389-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="10389-115">PARAMETERS</span></span>

### <span data-ttu-id="10389-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10389-116">-DefaultProfile</span></span>
<span data-ttu-id="10389-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="10389-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10389-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="10389-118">-InputObject</span></span>
<span data-ttu-id="10389-119">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="10389-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="10389-120">-Name</span><span class="sxs-lookup"><span data-stu-id="10389-120">-Name</span></span>
<span data-ttu-id="10389-121">EventGrid-Themen Name</span><span class="sxs-lookup"><span data-stu-id="10389-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="10389-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10389-122">-ResourceGroupName</span></span>
<span data-ttu-id="10389-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="10389-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="10389-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="10389-124">-ResourceId</span></span>
<span data-ttu-id="10389-125">Ressourcenbezeichner, der das Thema des Ereignis Rasters darstellt.</span><span class="sxs-lookup"><span data-stu-id="10389-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="10389-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10389-126">CommonParameters</span></span>
<span data-ttu-id="10389-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10389-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10389-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10389-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10389-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="10389-129">INPUTS</span></span>

### <span data-ttu-id="10389-130">System. String</span><span class="sxs-lookup"><span data-stu-id="10389-130">System.String</span></span>

### <span data-ttu-id="10389-131">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="10389-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="10389-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="10389-132">OUTPUTS</span></span>

### <span data-ttu-id="10389-133">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="10389-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="10389-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="10389-134">NOTES</span></span>

## <span data-ttu-id="10389-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="10389-135">RELATED LINKS</span></span>
