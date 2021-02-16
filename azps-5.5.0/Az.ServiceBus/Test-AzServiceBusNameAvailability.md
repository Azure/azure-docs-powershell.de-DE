---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
ms.openlocfilehash: adaf7485b0af16821a1f4adec7919422bef07f90
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165900"
---
# <span data-ttu-id="4b8a0-101">Test-AzServiceBusNameAvailability</span><span class="sxs-lookup"><span data-stu-id="4b8a0-101">Test-AzServiceBusNameAvailability</span></span>

## <span data-ttu-id="4b8a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b8a0-102">SYNOPSIS</span></span>
<span data-ttu-id="4b8a0-103">Überprüft die Verfügbarkeit der angegebenen Warteschlange oder des angegebenen Themanamens.</span><span class="sxs-lookup"><span data-stu-id="4b8a0-103">Checks the Availability of the given Queue or Topic name</span></span>

## <span data-ttu-id="4b8a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b8a0-104">SYNTAX</span></span>

### <span data-ttu-id="4b8a0-105">QueueCheckNameAvailabilitySet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4b8a0-105">QueueCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Queue]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b8a0-106">TopicCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4b8a0-106">TopicCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Topic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b8a0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b8a0-107">DESCRIPTION</span></span>
<span data-ttu-id="4b8a0-108">Das **Cmdlet "Test-AzServiceBusNameAvailability"** überprüft die Verfügbarkeit des bereitgestellten Namens der Warteschlange oder des Themas</span><span class="sxs-lookup"><span data-stu-id="4b8a0-108">The **Test-AzServiceBusNameAvailability** Cmdlet Check Availability of the provided Name of Queue or Topic</span></span>

## <span data-ttu-id="4b8a0-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4b8a0-109">EXAMPLES</span></span>

### <span data-ttu-id="4b8a0-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4b8a0-110">Example 1</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameQueue -Queue
True
```

<span data-ttu-id="4b8a0-111">Gibt "True" zurück, wenn $nameQueue angegebenen Namen "Verfügbar" ist, oder "False" zurückgibt, wenn $nameQueue angegebener Name nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="4b8a0-111">Returns True if the Provided $nameQueue name is Availabile or returns False if Provided $nameQueue name in not available</span></span>

### <span data-ttu-id="4b8a0-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4b8a0-112">Example 2</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameTopic -Topic
True
```

<span data-ttu-id="4b8a0-113">Gibt "True" zurück, wenn $nameTopic angegebenen Namen "Verfügbarkeit" ist, oder "False" zurückgibt, wenn $nameTopic angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="4b8a0-113">Returns True if the Provided $nameTopic name is Availabile or returns False if Provided $nameTopic name in not available</span></span>

## <span data-ttu-id="4b8a0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b8a0-114">PARAMETERS</span></span>

### <span data-ttu-id="4b8a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b8a0-115">-DefaultProfile</span></span>
<span data-ttu-id="4b8a0-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4b8a0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b8a0-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4b8a0-117">-Name</span></span>
<span data-ttu-id="4b8a0-118">Warteschlangenname zum Überprüfen der Namensverfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="4b8a0-118">Queue Name to check the Name Availability</span></span>

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

### <span data-ttu-id="4b8a0-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4b8a0-119">-Namespace</span></span>
<span data-ttu-id="4b8a0-120">Namespacename des Servicebus</span><span class="sxs-lookup"><span data-stu-id="4b8a0-120">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="4b8a0-121">-Queue</span><span class="sxs-lookup"><span data-stu-id="4b8a0-121">-Queue</span></span>
<span data-ttu-id="4b8a0-122">So überprüfen Sie die Namensverfügbarkeit für den Warteschlangennamen</span><span class="sxs-lookup"><span data-stu-id="4b8a0-122">To Check Name Availability for Queue Name</span></span>

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

### <span data-ttu-id="4b8a0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b8a0-123">-ResourceGroupName</span></span>
<span data-ttu-id="4b8a0-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="4b8a0-124">Resource Group Name</span></span>

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

### <span data-ttu-id="4b8a0-125">-Topic</span><span class="sxs-lookup"><span data-stu-id="4b8a0-125">-Topic</span></span>
<span data-ttu-id="4b8a0-126">So überprüfen Sie die Namensverfügbarkeit für den Themanamen</span><span class="sxs-lookup"><span data-stu-id="4b8a0-126">To Check Name Availability for Topic Name</span></span>

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

### <span data-ttu-id="4b8a0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b8a0-127">CommonParameters</span></span>
<span data-ttu-id="4b8a0-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b8a0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4b8a0-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b8a0-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b8a0-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4b8a0-130">INPUTS</span></span>

### <span data-ttu-id="4b8a0-131">System.String</span><span class="sxs-lookup"><span data-stu-id="4b8a0-131">System.String</span></span>

## <span data-ttu-id="4b8a0-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4b8a0-132">OUTPUTS</span></span>

### <span data-ttu-id="4b8a0-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4b8a0-133">System.Boolean</span></span>

## <span data-ttu-id="4b8a0-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4b8a0-134">NOTES</span></span>

## <span data-ttu-id="4b8a0-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4b8a0-135">RELATED LINKS</span></span>
