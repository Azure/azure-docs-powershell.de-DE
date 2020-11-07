---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
ms.openlocfilehash: 396a328de8c075b49ae4dda181158c33518eaa8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823207"
---
# <span data-ttu-id="ed902-101">Test-AzServiceBusNameAvailability</span><span class="sxs-lookup"><span data-stu-id="ed902-101">Test-AzServiceBusNameAvailability</span></span>

## <span data-ttu-id="ed902-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ed902-102">SYNOPSIS</span></span>
<span data-ttu-id="ed902-103">Überprüft die Verfügbarkeit des angegebenen Warteschlangen-oder Themennamens.</span><span class="sxs-lookup"><span data-stu-id="ed902-103">Checks the Availability of the given Queue or Topic name</span></span>

## <span data-ttu-id="ed902-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed902-104">SYNTAX</span></span>

### <span data-ttu-id="ed902-105">QueueCheckNameAvailabilitySet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ed902-105">QueueCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Queue]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed902-106">TopicCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ed902-106">TopicCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Topic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed902-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed902-107">DESCRIPTION</span></span>
<span data-ttu-id="ed902-108">Das Cmdlet " **Test-AzServiceBusNameAvailability** " überprüft die Verfügbarkeit des bereitgestellten Namens der Warteschlange oder des Themas.</span><span class="sxs-lookup"><span data-stu-id="ed902-108">The **Test-AzServiceBusNameAvailability** Cmdlet Check Availability of the provided Name of Queue or Topic</span></span>

## <span data-ttu-id="ed902-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed902-109">EXAMPLES</span></span>

### <span data-ttu-id="ed902-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ed902-110">Example 1</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameQueue -Queue
True
```

<span data-ttu-id="ed902-111">Gibt "true" zurück, wenn der angegebene $nameQueue Name verfügbare ist, oder gibt "false" zurück, wenn $nameQueue Name in nicht verfügbar angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ed902-111">Returns True if the Provided $nameQueue name is Availabile or returns False if Provided $nameQueue name in not available</span></span>

### <span data-ttu-id="ed902-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ed902-112">Example 2</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameTopic -Topic
True
```

<span data-ttu-id="ed902-113">Gibt "true" zurück, wenn der angegebene $nameTopic Name verfügbare ist, oder gibt "false" zurück, wenn $nameTopic Name in nicht verfügbar angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ed902-113">Returns True if the Provided $nameTopic name is Availabile or returns False if Provided $nameTopic name in not available</span></span>

## <span data-ttu-id="ed902-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed902-114">PARAMETERS</span></span>

### <span data-ttu-id="ed902-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed902-115">-DefaultProfile</span></span>
<span data-ttu-id="ed902-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ed902-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed902-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ed902-117">-Name</span></span>
<span data-ttu-id="ed902-118">Warteschlangenname zum Überprüfen der Verfügbarkeit von Namen</span><span class="sxs-lookup"><span data-stu-id="ed902-118">Queue Name to check the Name Availability</span></span>

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

### <span data-ttu-id="ed902-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ed902-119">-Namespace</span></span>
<span data-ttu-id="ed902-120">ServiceBus-Namespace Name</span><span class="sxs-lookup"><span data-stu-id="ed902-120">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="ed902-121">-Queue</span><span class="sxs-lookup"><span data-stu-id="ed902-121">-Queue</span></span>
<span data-ttu-id="ed902-122">So überprüfen Sie die Verfügbarkeit von Namen für Warteschlangennamen</span><span class="sxs-lookup"><span data-stu-id="ed902-122">To Check Name Availability for Queue Name</span></span>

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

### <span data-ttu-id="ed902-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed902-123">-ResourceGroupName</span></span>
<span data-ttu-id="ed902-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="ed902-124">Resource Group Name</span></span>

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

### <span data-ttu-id="ed902-125">-Topic</span><span class="sxs-lookup"><span data-stu-id="ed902-125">-Topic</span></span>
<span data-ttu-id="ed902-126">So überprüfen Sie die Verfügbarkeit von Namen für den Themen Namen</span><span class="sxs-lookup"><span data-stu-id="ed902-126">To Check Name Availability for Topic Name</span></span>

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

### <span data-ttu-id="ed902-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed902-127">CommonParameters</span></span>
<span data-ttu-id="ed902-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed902-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ed902-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed902-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed902-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ed902-130">INPUTS</span></span>

### <span data-ttu-id="ed902-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ed902-131">System.String</span></span>

## <span data-ttu-id="ed902-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ed902-132">OUTPUTS</span></span>

### <span data-ttu-id="ed902-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ed902-133">System.Boolean</span></span>

## <span data-ttu-id="ed902-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="ed902-134">NOTES</span></span>

## <span data-ttu-id="ed902-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ed902-135">RELATED LINKS</span></span>
