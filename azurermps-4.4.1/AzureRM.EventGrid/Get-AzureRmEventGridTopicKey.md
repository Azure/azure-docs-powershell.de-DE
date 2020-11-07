---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
ms.openlocfilehash: 91e3acd227acd8a83dcd5ccb0beb2ed12d1cca99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665068"
---
# <span data-ttu-id="4cca3-101">Get-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="4cca3-101">Get-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="4cca3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4cca3-102">SYNOPSIS</span></span>
<span data-ttu-id="4cca3-103">Ruft die freigegebenen Zugriffstasten ab, die zum Veröffentlichen von Ereignissen in einem Ereignis Raster Thema verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4cca3-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cca3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4cca3-104">SYNTAX</span></span>

### <span data-ttu-id="4cca3-105">TopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4cca3-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cca3-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cca3-106">TopicInputObjectParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4cca3-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cca3-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4cca3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4cca3-108">DESCRIPTION</span></span>
<span data-ttu-id="4cca3-109">Ruft die freigegebenen Zugriffstasten ab, die zum Veröffentlichen von Ereignissen in einem Ereignis Raster Thema verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4cca3-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="4cca3-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4cca3-110">EXAMPLES</span></span>

### <span data-ttu-id="4cca3-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4cca3-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="4cca3-112">Ruft die freigegebenen Zugriffstasten des Ereignis Rasters Topic \` THEMA1 hat \` in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="4cca3-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="4cca3-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4cca3-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzureRmEventGridTopicKey
```

<span data-ttu-id="4cca3-114">Ruft die freigegebenen Zugriffstasten des Ereignis Rasters Topic \` THEMA1 hat \` in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="4cca3-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="4cca3-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cca3-115">PARAMETERS</span></span>

### <span data-ttu-id="4cca3-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4cca3-116">-InputObject</span></span>
<span data-ttu-id="4cca3-117">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4cca3-117">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="4cca3-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4cca3-118">-Name</span></span>
<span data-ttu-id="4cca3-119">EventGrid-Themen Name</span><span class="sxs-lookup"><span data-stu-id="4cca3-119">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="4cca3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cca3-120">-ResourceGroupName</span></span>
<span data-ttu-id="4cca3-121">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4cca3-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="4cca3-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4cca3-122">-ResourceId</span></span>
<span data-ttu-id="4cca3-123">Ressourcenbezeichner, der das Thema des Ereignis Rasters darstellt.</span><span class="sxs-lookup"><span data-stu-id="4cca3-123">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="4cca3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cca3-124">-DefaultProfile</span></span>
<span data-ttu-id="4cca3-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4cca3-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cca3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cca3-126">CommonParameters</span></span>
<span data-ttu-id="4cca3-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cca3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cca3-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cca3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cca3-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4cca3-129">INPUTS</span></span>

### <span data-ttu-id="4cca3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4cca3-130">System.String</span></span>

## <span data-ttu-id="4cca3-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4cca3-131">OUTPUTS</span></span>

### <span data-ttu-id="4cca3-132">Microsoft. Azure. Management. EventGrid. Models. TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="4cca3-132">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="4cca3-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="4cca3-133">NOTES</span></span>

## <span data-ttu-id="4cca3-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4cca3-134">RELATED LINKS</span></span>

