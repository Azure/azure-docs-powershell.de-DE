---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
ms.openlocfilehash: 741a888287ba7fcb4a9b54c1281a6a27be5fbb0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664236"
---
# <span data-ttu-id="4a91d-101">Get-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="4a91d-101">Get-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="4a91d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4a91d-102">SYNOPSIS</span></span>
<span data-ttu-id="4a91d-103">Ruft die freigegebenen Zugriffstasten ab, die zum Veröffentlichen von Ereignissen in einem Ereignis Raster Thema verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a91d-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a91d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a91d-104">SYNTAX</span></span>

### <span data-ttu-id="4a91d-105">TopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4a91d-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a91d-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a91d-106">TopicInputObjectParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a91d-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a91d-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a91d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4a91d-108">DESCRIPTION</span></span>
<span data-ttu-id="4a91d-109">Ruft die freigegebenen Zugriffstasten ab, die zum Veröffentlichen von Ereignissen in einem Ereignis Raster Thema verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a91d-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="4a91d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4a91d-110">EXAMPLES</span></span>

### <span data-ttu-id="4a91d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4a91d-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="4a91d-112">Ruft die freigegebenen Zugriffstasten des Ereignis Rasters Topic \` THEMA1 hat \` in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="4a91d-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="4a91d-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4a91d-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzureRmEventGridTopicKey
```

<span data-ttu-id="4a91d-114">Ruft die freigegebenen Zugriffstasten des Ereignis Rasters Topic \` THEMA1 hat \` in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="4a91d-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="4a91d-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a91d-115">PARAMETERS</span></span>

### <span data-ttu-id="4a91d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a91d-116">-DefaultProfile</span></span>
<span data-ttu-id="4a91d-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4a91d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a91d-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4a91d-118">-InputObject</span></span>
<span data-ttu-id="4a91d-119">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4a91d-119">EventGrid Topic object.</span></span>

```yaml
Type: PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a91d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4a91d-120">-Name</span></span>
<span data-ttu-id="4a91d-121">EventGrid-Themen Name</span><span class="sxs-lookup"><span data-stu-id="4a91d-121">EventGrid Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a91d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a91d-122">-ResourceGroupName</span></span>
<span data-ttu-id="4a91d-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4a91d-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a91d-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4a91d-124">-ResourceId</span></span>
<span data-ttu-id="4a91d-125">Ressourcenbezeichner, der das Thema des Ereignis Rasters darstellt.</span><span class="sxs-lookup"><span data-stu-id="4a91d-125">Resource Identifier representing the Event Grid Topic.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a91d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a91d-126">CommonParameters</span></span>
<span data-ttu-id="4a91d-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a91d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a91d-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a91d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a91d-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4a91d-129">INPUTS</span></span>

### <span data-ttu-id="4a91d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4a91d-130">System.String</span></span>

## <span data-ttu-id="4a91d-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4a91d-131">OUTPUTS</span></span>

### <span data-ttu-id="4a91d-132">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="4a91d-132">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="4a91d-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="4a91d-133">NOTES</span></span>

## <span data-ttu-id="4a91d-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4a91d-134">RELATED LINKS</span></span>

