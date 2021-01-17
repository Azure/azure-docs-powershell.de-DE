---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
ms.openlocfilehash: fc108c633b70cc1eed32bcc0574ad25109a065fc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469883"
---
# <span data-ttu-id="2c0cf-101">Get-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="2c0cf-101">Get-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="2c0cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c0cf-102">SYNOPSIS</span></span>
<span data-ttu-id="2c0cf-103">Ruft die Details einer bestimmten Consumergruppe für Ereignishubs ab, oder ruft eine Liste von Consumergruppen in einem Ereignishub ab.</span><span class="sxs-lookup"><span data-stu-id="2c0cf-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

## <span data-ttu-id="2c0cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c0cf-104">SYNTAX</span></span>

```
Get-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c0cf-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2c0cf-105">DESCRIPTION</span></span>
<span data-ttu-id="2c0cf-106">Das Get-AzEventHubConsumerGroup-Cmdlet ruft entweder die Details einer bestimmten Consumergruppe für Ereignishubs oder eine Liste von Consumergruppen in einem bestimmten Ereignishub ab.</span><span class="sxs-lookup"><span data-stu-id="2c0cf-106">The Get-AzEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="2c0cf-107">Wenn der Name einer Verbrauchergruppe angegeben wird, werden die Details einer einzelnen Verbrauchergruppe zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2c0cf-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="2c0cf-108">Wenn der Name einer Consumergruppe nicht angegeben wird, wird eine Liste der Consumergruppen im angegebenen Ereignishub zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2c0cf-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="2c0cf-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2c0cf-109">EXAMPLES</span></span>

### <span data-ttu-id="2c0cf-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2c0cf-110">Example 1</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="2c0cf-111">Ruft die Consumergruppe \` "MyConsumerGroupName" im Ereignishub \` \` "MyEventHubName" ab, der im Namespace "MyNamespaceName" mit der Ressourcengruppe \` \` \` \` "MyResourceGroupName" vorhanden \` ist.</span><span class="sxs-lookup"><span data-stu-id="2c0cf-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="2c0cf-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2c0cf-112">Example 2</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="2c0cf-113">Ruft eine Liste der Consumergruppen im Ereignishub \` "MyEventHubName" ab, der im Namespace "MyNamespaceName" mit der Ressourcengruppe \` \` \` \` "MyResourceGroupName" vorhanden \` ist.</span><span class="sxs-lookup"><span data-stu-id="2c0cf-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="2c0cf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c0cf-114">PARAMETERS</span></span>

### <span data-ttu-id="2c0cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c0cf-115">-DefaultProfile</span></span>
<span data-ttu-id="2c0cf-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2c0cf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c0cf-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="2c0cf-117">-EventHub</span></span>
<span data-ttu-id="2c0cf-118">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="2c0cf-118">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c0cf-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="2c0cf-119">-MaxCount</span></span>
<span data-ttu-id="2c0cf-120">Ermitteln Sie die maximale Anzahl von Consumergroups, die zurückgeben werden.</span><span class="sxs-lookup"><span data-stu-id="2c0cf-120">Determine the maximum number of ConsumerGroups  to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c0cf-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2c0cf-121">-Name</span></span>
<span data-ttu-id="2c0cf-122">ConsumerGroup Name</span><span class="sxs-lookup"><span data-stu-id="2c0cf-122">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c0cf-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2c0cf-123">-Namespace</span></span>
<span data-ttu-id="2c0cf-124">Namespacename</span><span class="sxs-lookup"><span data-stu-id="2c0cf-124">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c0cf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c0cf-125">-ResourceGroupName</span></span>
<span data-ttu-id="2c0cf-126">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="2c0cf-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c0cf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c0cf-127">CommonParameters</span></span>
<span data-ttu-id="2c0cf-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c0cf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c0cf-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c0cf-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c0cf-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2c0cf-130">INPUTS</span></span>

### <span data-ttu-id="2c0cf-131">System.String</span><span class="sxs-lookup"><span data-stu-id="2c0cf-131">System.String</span></span>

## <span data-ttu-id="2c0cf-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2c0cf-132">OUTPUTS</span></span>

### <span data-ttu-id="2c0cf-133">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="2c0cf-133">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="2c0cf-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2c0cf-134">NOTES</span></span>

## <span data-ttu-id="2c0cf-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2c0cf-135">RELATED LINKS</span></span>
