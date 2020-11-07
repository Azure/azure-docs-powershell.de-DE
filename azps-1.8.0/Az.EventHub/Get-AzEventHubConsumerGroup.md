---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
ms.openlocfilehash: 7f10df478851679afeb73157252d954f756f0c4c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661055"
---
# <span data-ttu-id="ab48c-101">Get-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="ab48c-101">Get-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="ab48c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ab48c-102">SYNOPSIS</span></span>
<span data-ttu-id="ab48c-103">Ruft die Details einer angegebenen Event Hubs-Verbrauchergruppe ab oder ruft eine Liste von Verbrauchergruppen in einem Ereignis-Hub ab.</span><span class="sxs-lookup"><span data-stu-id="ab48c-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

## <span data-ttu-id="ab48c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab48c-104">SYNTAX</span></span>

```
Get-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab48c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ab48c-105">DESCRIPTION</span></span>
<span data-ttu-id="ab48c-106">Das Get-AzEventHubConsumerGroup-Cmdlet ruft entweder die Details einer angegebenen Event Hubs-Verbrauchergruppe oder eine Liste von Verbrauchergruppen in einem bestimmten Ereignis-Hub ab.</span><span class="sxs-lookup"><span data-stu-id="ab48c-106">The Get-AzEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="ab48c-107">Wenn der Name einer Consumer-Gruppe bereitgestellt wird, werden die Details einer einzelnen Consumer-Gruppe zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ab48c-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="ab48c-108">Wenn der Name einer Consumer-Gruppe nicht angegeben wird, wird eine Liste der Verbrauchergruppen im angegebenen Ereignis-Hub zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ab48c-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="ab48c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ab48c-109">EXAMPLES</span></span>

### <span data-ttu-id="ab48c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ab48c-110">Example 1</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="ab48c-111">Ruft die Gruppe der \` Consumer \` -MyConsumerGroupName im MyEventHubName des Ereignis Hubs ab \` \` , die im Namespace \` mynamespacename \` mit Ressourcengruppe MyResourceGroupName vorhanden ist \` \` .</span><span class="sxs-lookup"><span data-stu-id="ab48c-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ab48c-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ab48c-112">Example 2</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="ab48c-113">Ruft eine Liste der Verbrauchergruppen im MyEventHubName des Ereignis Hubs ab \` \` , die im Namespace \` mynamespacename \` mit Ressourcengruppe MyResourceGroupName vorhanden ist \` \` .</span><span class="sxs-lookup"><span data-stu-id="ab48c-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="ab48c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab48c-114">PARAMETERS</span></span>

### <span data-ttu-id="ab48c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab48c-115">-DefaultProfile</span></span>
<span data-ttu-id="ab48c-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ab48c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab48c-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="ab48c-117">-EventHub</span></span>
<span data-ttu-id="ab48c-118">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="ab48c-118">EventHub Name</span></span>

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

### <span data-ttu-id="ab48c-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="ab48c-119">-MaxCount</span></span>
<span data-ttu-id="ab48c-120">Ermitteln Sie die maximale Anzahl der ConsumerGroups, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ab48c-120">Determine the maximum number of ConsumerGroups  to return.</span></span>

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

### <span data-ttu-id="ab48c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ab48c-121">-Name</span></span>
<span data-ttu-id="ab48c-122">Consumergroup-Name</span><span class="sxs-lookup"><span data-stu-id="ab48c-122">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="ab48c-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ab48c-123">-Namespace</span></span>
<span data-ttu-id="ab48c-124">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="ab48c-124">Namespace Name</span></span>

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

### <span data-ttu-id="ab48c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab48c-125">-ResourceGroupName</span></span>
<span data-ttu-id="ab48c-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="ab48c-126">Resource Group Name</span></span>

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

### <span data-ttu-id="ab48c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab48c-127">CommonParameters</span></span>
<span data-ttu-id="ab48c-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab48c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab48c-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab48c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab48c-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ab48c-130">INPUTS</span></span>

### <span data-ttu-id="ab48c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ab48c-131">System.String</span></span>

## <span data-ttu-id="ab48c-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ab48c-132">OUTPUTS</span></span>

### <span data-ttu-id="ab48c-133">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="ab48c-133">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="ab48c-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="ab48c-134">NOTES</span></span>

## <span data-ttu-id="ab48c-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ab48c-135">RELATED LINKS</span></span>
