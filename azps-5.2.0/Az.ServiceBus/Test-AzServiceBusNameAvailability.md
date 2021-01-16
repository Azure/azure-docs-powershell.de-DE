---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
ms.openlocfilehash: adaf7485b0af16821a1f4adec7919422bef07f90
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369031"
---
# <span data-ttu-id="b9047-101">Test-AzServiceBusNameAvailability</span><span class="sxs-lookup"><span data-stu-id="b9047-101">Test-AzServiceBusNameAvailability</span></span>

## <span data-ttu-id="b9047-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9047-102">SYNOPSIS</span></span>
<span data-ttu-id="b9047-103">Überprüft die Verfügbarkeit der angegebenen Warteschlange oder des angegebenen Themanamens.</span><span class="sxs-lookup"><span data-stu-id="b9047-103">Checks the Availability of the given Queue or Topic name</span></span>

## <span data-ttu-id="b9047-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9047-104">SYNTAX</span></span>

### <span data-ttu-id="b9047-105">QueueCheckNameAvailabilitySet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b9047-105">QueueCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Queue]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9047-106">TopicCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b9047-106">TopicCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Topic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9047-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b9047-107">DESCRIPTION</span></span>
<span data-ttu-id="b9047-108">Das **Cmdlet "Test-AzServiceBusNameAvailability"** überprüft die Verfügbarkeit des bereitgestellten Namens der Warteschlange oder des Themas</span><span class="sxs-lookup"><span data-stu-id="b9047-108">The **Test-AzServiceBusNameAvailability** Cmdlet Check Availability of the provided Name of Queue or Topic</span></span>

## <span data-ttu-id="b9047-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b9047-109">EXAMPLES</span></span>

### <span data-ttu-id="b9047-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b9047-110">Example 1</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameQueue -Queue
True
```

<span data-ttu-id="b9047-111">Gibt "True" zurück, wenn $nameQueue angegebenen Namen "Verfügbar" ist, oder "False" zurückgibt, wenn $nameQueue angegebener Name nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b9047-111">Returns True if the Provided $nameQueue name is Availabile or returns False if Provided $nameQueue name in not available</span></span>

### <span data-ttu-id="b9047-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b9047-112">Example 2</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameTopic -Topic
True
```

<span data-ttu-id="b9047-113">Gibt "True" zurück, wenn $nameTopic angegebenen Namen "Verfügbarkeit" ist, oder "False" zurück, wenn "Provided $nameTopic Name nicht verfügbar" ist.</span><span class="sxs-lookup"><span data-stu-id="b9047-113">Returns True if the Provided $nameTopic name is Availabile or returns False if Provided $nameTopic name in not available</span></span>

## <span data-ttu-id="b9047-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9047-114">PARAMETERS</span></span>

### <span data-ttu-id="b9047-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9047-115">-DefaultProfile</span></span>
<span data-ttu-id="b9047-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b9047-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9047-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b9047-117">-Name</span></span>
<span data-ttu-id="b9047-118">Warteschlangenname zum Überprüfen der Namensverfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="b9047-118">Queue Name to check the Name Availability</span></span>

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

### <span data-ttu-id="b9047-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b9047-119">-Namespace</span></span>
<span data-ttu-id="b9047-120">Namespacename des Servicebus</span><span class="sxs-lookup"><span data-stu-id="b9047-120">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="b9047-121">-Queue</span><span class="sxs-lookup"><span data-stu-id="b9047-121">-Queue</span></span>
<span data-ttu-id="b9047-122">So überprüfen Sie die Namensverfügbarkeit für den Warteschlangennamen</span><span class="sxs-lookup"><span data-stu-id="b9047-122">To Check Name Availability for Queue Name</span></span>

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

### <span data-ttu-id="b9047-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9047-123">-ResourceGroupName</span></span>
<span data-ttu-id="b9047-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="b9047-124">Resource Group Name</span></span>

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

### <span data-ttu-id="b9047-125">-Topic</span><span class="sxs-lookup"><span data-stu-id="b9047-125">-Topic</span></span>
<span data-ttu-id="b9047-126">So überprüfen Sie die Namensverfügbarkeit für den Themanamen</span><span class="sxs-lookup"><span data-stu-id="b9047-126">To Check Name Availability for Topic Name</span></span>

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

### <span data-ttu-id="b9047-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9047-127">CommonParameters</span></span>
<span data-ttu-id="b9047-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9047-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b9047-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9047-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9047-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b9047-130">INPUTS</span></span>

### <span data-ttu-id="b9047-131">System.String</span><span class="sxs-lookup"><span data-stu-id="b9047-131">System.String</span></span>

## <span data-ttu-id="b9047-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b9047-132">OUTPUTS</span></span>

### <span data-ttu-id="b9047-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b9047-133">System.Boolean</span></span>

## <span data-ttu-id="b9047-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b9047-134">NOTES</span></span>

## <span data-ttu-id="b9047-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b9047-135">RELATED LINKS</span></span>
