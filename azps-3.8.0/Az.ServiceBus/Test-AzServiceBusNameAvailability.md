---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
ms.openlocfilehash: adaf7485b0af16821a1f4adec7919422bef07f90
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995584"
---
# <span data-ttu-id="aeaa9-101">Test-AzServiceBusNameAvailability</span><span class="sxs-lookup"><span data-stu-id="aeaa9-101">Test-AzServiceBusNameAvailability</span></span>

## <span data-ttu-id="aeaa9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aeaa9-102">SYNOPSIS</span></span>
<span data-ttu-id="aeaa9-103">Überprüft die Verfügbarkeit des angegebenen Warteschlangen-oder Themennamens.</span><span class="sxs-lookup"><span data-stu-id="aeaa9-103">Checks the Availability of the given Queue or Topic name</span></span>

## <span data-ttu-id="aeaa9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aeaa9-104">SYNTAX</span></span>

### <span data-ttu-id="aeaa9-105">QueueCheckNameAvailabilitySet (Standard)</span><span class="sxs-lookup"><span data-stu-id="aeaa9-105">QueueCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Queue]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aeaa9-106">TopicCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="aeaa9-106">TopicCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Topic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aeaa9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aeaa9-107">DESCRIPTION</span></span>
<span data-ttu-id="aeaa9-108">Das Cmdlet " **Test-AzServiceBusNameAvailability** " überprüft die Verfügbarkeit des bereitgestellten Namens der Warteschlange oder des Themas.</span><span class="sxs-lookup"><span data-stu-id="aeaa9-108">The **Test-AzServiceBusNameAvailability** Cmdlet Check Availability of the provided Name of Queue or Topic</span></span>

## <span data-ttu-id="aeaa9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aeaa9-109">EXAMPLES</span></span>

### <span data-ttu-id="aeaa9-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="aeaa9-110">Example 1</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameQueue -Queue
True
```

<span data-ttu-id="aeaa9-111">Gibt "true" zurück, wenn der angegebene $nameQueue Name verfügbare ist, oder gibt "false" zurück, wenn $nameQueue Name in nicht verfügbar angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="aeaa9-111">Returns True if the Provided $nameQueue name is Availabile or returns False if Provided $nameQueue name in not available</span></span>

### <span data-ttu-id="aeaa9-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="aeaa9-112">Example 2</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameTopic -Topic
True
```

<span data-ttu-id="aeaa9-113">Gibt "true" zurück, wenn der angegebene $nameTopic Name verfügbare ist, oder gibt "false" zurück, wenn $nameTopic Name in nicht verfügbar angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="aeaa9-113">Returns True if the Provided $nameTopic name is Availabile or returns False if Provided $nameTopic name in not available</span></span>

## <span data-ttu-id="aeaa9-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="aeaa9-114">PARAMETERS</span></span>

### <span data-ttu-id="aeaa9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeaa9-115">-DefaultProfile</span></span>
<span data-ttu-id="aeaa9-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aeaa9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aeaa9-117">-Name</span><span class="sxs-lookup"><span data-stu-id="aeaa9-117">-Name</span></span>
<span data-ttu-id="aeaa9-118">Warteschlangenname zum Überprüfen der Verfügbarkeit von Namen</span><span class="sxs-lookup"><span data-stu-id="aeaa9-118">Queue Name to check the Name Availability</span></span>

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

### <span data-ttu-id="aeaa9-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="aeaa9-119">-Namespace</span></span>
<span data-ttu-id="aeaa9-120">ServiceBus-Namespace Name</span><span class="sxs-lookup"><span data-stu-id="aeaa9-120">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="aeaa9-121">-Queue</span><span class="sxs-lookup"><span data-stu-id="aeaa9-121">-Queue</span></span>
<span data-ttu-id="aeaa9-122">So überprüfen Sie die Verfügbarkeit von Namen für Warteschlangennamen</span><span class="sxs-lookup"><span data-stu-id="aeaa9-122">To Check Name Availability for Queue Name</span></span>

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

### <span data-ttu-id="aeaa9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aeaa9-123">-ResourceGroupName</span></span>
<span data-ttu-id="aeaa9-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="aeaa9-124">Resource Group Name</span></span>

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

### <span data-ttu-id="aeaa9-125">-Topic</span><span class="sxs-lookup"><span data-stu-id="aeaa9-125">-Topic</span></span>
<span data-ttu-id="aeaa9-126">So überprüfen Sie die Verfügbarkeit von Namen für den Themen Namen</span><span class="sxs-lookup"><span data-stu-id="aeaa9-126">To Check Name Availability for Topic Name</span></span>

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

### <span data-ttu-id="aeaa9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeaa9-127">CommonParameters</span></span>
<span data-ttu-id="aeaa9-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aeaa9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="aeaa9-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aeaa9-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeaa9-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aeaa9-130">INPUTS</span></span>

### <span data-ttu-id="aeaa9-131">System. String</span><span class="sxs-lookup"><span data-stu-id="aeaa9-131">System.String</span></span>

## <span data-ttu-id="aeaa9-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aeaa9-132">OUTPUTS</span></span>

### <span data-ttu-id="aeaa9-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aeaa9-133">System.Boolean</span></span>

## <span data-ttu-id="aeaa9-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="aeaa9-134">NOTES</span></span>

## <span data-ttu-id="aeaa9-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aeaa9-135">RELATED LINKS</span></span>
