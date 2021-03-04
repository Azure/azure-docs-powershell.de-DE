---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/test-azservicebusnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
ms.openlocfilehash: b97acb269ee38dc937c5deffb0b3e054b0222c4d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923400"
---
# <span data-ttu-id="337be-101">Test-AzServiceBusNameAvailability</span><span class="sxs-lookup"><span data-stu-id="337be-101">Test-AzServiceBusNameAvailability</span></span>

## <span data-ttu-id="337be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="337be-102">SYNOPSIS</span></span>
<span data-ttu-id="337be-103">Überprüft die Verfügbarkeit des angegebenen Warteschlangen- oder Themennamens</span><span class="sxs-lookup"><span data-stu-id="337be-103">Checks the Availability of the given Queue or Topic name</span></span>

## <span data-ttu-id="337be-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="337be-104">SYNTAX</span></span>

### <span data-ttu-id="337be-105">QueueCheckNameAvailabilitySet (Standard)</span><span class="sxs-lookup"><span data-stu-id="337be-105">QueueCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Queue]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="337be-106">TopicCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="337be-106">TopicCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Topic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="337be-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="337be-107">DESCRIPTION</span></span>
<span data-ttu-id="337be-108">Das **Cmdlet Test-AzServiceBusNameAvailability** Überprüft die Verfügbarkeit des bereitgestellten Namens der Warteschlange oder des Themas</span><span class="sxs-lookup"><span data-stu-id="337be-108">The **Test-AzServiceBusNameAvailability** Cmdlet Check Availability of the provided Name of Queue or Topic</span></span>

## <span data-ttu-id="337be-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="337be-109">EXAMPLES</span></span>

### <span data-ttu-id="337be-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="337be-110">Example 1</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameQueue -Queue
True
```

<span data-ttu-id="337be-111">Gibt "True" zurück, wenn $nameQueue angegebener Name "Verfügbar" oder "False" zurückgibt, wenn $nameQueue Angegebener Name in nicht verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="337be-111">Returns True if the Provided $nameQueue name is Availabile or returns False if Provided $nameQueue name in not available</span></span>

### <span data-ttu-id="337be-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="337be-112">Example 2</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameTopic -Topic
True
```

<span data-ttu-id="337be-113">Gibt "True" zurück, wenn $nameTopic bereitgestellter Name "Verfügbar" oder "False" zurückgibt, wenn $nameTopic Angegebener Name in nicht verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="337be-113">Returns True if the Provided $nameTopic name is Availabile or returns False if Provided $nameTopic name in not available</span></span>

## <span data-ttu-id="337be-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="337be-114">PARAMETERS</span></span>

### <span data-ttu-id="337be-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="337be-115">-DefaultProfile</span></span>
<span data-ttu-id="337be-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="337be-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="337be-117">-Name</span><span class="sxs-lookup"><span data-stu-id="337be-117">-Name</span></span>
<span data-ttu-id="337be-118">Warteschlangenname, um die Verfügbarkeit des Namens zu überprüfen</span><span class="sxs-lookup"><span data-stu-id="337be-118">Queue Name to check the Name Availability</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="337be-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="337be-119">-Namespace</span></span>
<span data-ttu-id="337be-120">Namespacename von Servicebus</span><span class="sxs-lookup"><span data-stu-id="337be-120">Servicebus Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="337be-121">-Queue</span><span class="sxs-lookup"><span data-stu-id="337be-121">-Queue</span></span>
<span data-ttu-id="337be-122">So überprüfen Sie die Verfügbarkeit von Namen für den Warteschlangennamen</span><span class="sxs-lookup"><span data-stu-id="337be-122">To Check Name Availability for Queue Name</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: QueueCheckNameAvailabilitySet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="337be-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="337be-123">-ResourceGroupName</span></span>
<span data-ttu-id="337be-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="337be-124">Resource Group Name</span></span>

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

### <span data-ttu-id="337be-125">-Topic</span><span class="sxs-lookup"><span data-stu-id="337be-125">-Topic</span></span>
<span data-ttu-id="337be-126">So überprüfen Sie die Verfügbarkeit von Namen für Den Themanamen</span><span class="sxs-lookup"><span data-stu-id="337be-126">To Check Name Availability for Topic Name</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TopicCheckNameAvailabilitySet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="337be-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="337be-127">CommonParameters</span></span>
<span data-ttu-id="337be-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="337be-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="337be-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="337be-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="337be-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="337be-130">INPUTS</span></span>

### <span data-ttu-id="337be-131">System.String</span><span class="sxs-lookup"><span data-stu-id="337be-131">System.String</span></span>

## <span data-ttu-id="337be-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="337be-132">OUTPUTS</span></span>

### <span data-ttu-id="337be-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="337be-133">System.Boolean</span></span>

## <span data-ttu-id="337be-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="337be-134">NOTES</span></span>

## <span data-ttu-id="337be-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="337be-135">RELATED LINKS</span></span>
