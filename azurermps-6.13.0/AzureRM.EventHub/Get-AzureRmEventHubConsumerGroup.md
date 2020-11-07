---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 205dc883f8f6e0481f88438137ca45ad7a99c4ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663145"
---
# <span data-ttu-id="d8088-101">Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="d8088-101">Get-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="d8088-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d8088-102">SYNOPSIS</span></span>
<span data-ttu-id="d8088-103">Ruft die Details einer angegebenen Event Hubs-Verbrauchergruppe ab oder ruft eine Liste von Verbrauchergruppen in einem Ereignis-Hub ab.</span><span class="sxs-lookup"><span data-stu-id="d8088-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8088-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8088-104">SYNTAX</span></span>

```
Get-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8088-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d8088-105">DESCRIPTION</span></span>
<span data-ttu-id="d8088-106">Das Get-AzureRmEventHubConsumerGroup-Cmdlet ruft entweder die Details einer angegebenen Event Hubs-Verbrauchergruppe oder eine Liste von Verbrauchergruppen in einem bestimmten Ereignis-Hub ab.</span><span class="sxs-lookup"><span data-stu-id="d8088-106">The Get-AzureRmEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="d8088-107">Wenn der Name einer Consumer-Gruppe bereitgestellt wird, werden die Details einer einzelnen Consumer-Gruppe zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d8088-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="d8088-108">Wenn der Name einer Consumer-Gruppe nicht angegeben wird, wird eine Liste der Verbrauchergruppen im angegebenen Ereignis-Hub zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d8088-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="d8088-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d8088-109">EXAMPLES</span></span>

### <span data-ttu-id="d8088-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d8088-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="d8088-111">Ruft die Gruppe der \` Consumer \` -MyConsumerGroupName im MyEventHubName des Ereignis Hubs ab \` \` , die im Namespace \` mynamespacename \` mit Ressourcengruppe MyResourceGroupName vorhanden ist \` \` .</span><span class="sxs-lookup"><span data-stu-id="d8088-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="d8088-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d8088-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="d8088-113">Ruft eine Liste der Verbrauchergruppen im MyEventHubName des Ereignis Hubs ab \` \` , die im Namespace \` mynamespacename \` mit Ressourcengruppe MyResourceGroupName vorhanden ist \` \` .</span><span class="sxs-lookup"><span data-stu-id="d8088-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="d8088-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8088-114">PARAMETERS</span></span>

### <span data-ttu-id="d8088-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8088-115">-DefaultProfile</span></span>
<span data-ttu-id="d8088-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d8088-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8088-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="d8088-117">-EventHub</span></span>
<span data-ttu-id="d8088-118">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="d8088-118">EventHub Name</span></span>

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

### <span data-ttu-id="d8088-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="d8088-119">-MaxCount</span></span>
<span data-ttu-id="d8088-120">Ermitteln Sie die maximale Anzahl der ConsumerGroups, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d8088-120">Determine the maximum number of ConsumerGroups  to return.</span></span>

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

### <span data-ttu-id="d8088-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d8088-121">-Name</span></span>
<span data-ttu-id="d8088-122">Consumergroup-Name</span><span class="sxs-lookup"><span data-stu-id="d8088-122">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="d8088-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d8088-123">-Namespace</span></span>
<span data-ttu-id="d8088-124">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="d8088-124">Namespace Name</span></span>

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

### <span data-ttu-id="d8088-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8088-125">-ResourceGroupName</span></span>
<span data-ttu-id="d8088-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="d8088-126">Resource Group Name</span></span>

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

### <span data-ttu-id="d8088-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8088-127">CommonParameters</span></span>
<span data-ttu-id="d8088-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8088-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8088-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8088-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8088-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d8088-130">INPUTS</span></span>

### <span data-ttu-id="d8088-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d8088-131">System.String</span></span>

## <span data-ttu-id="d8088-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d8088-132">OUTPUTS</span></span>

### <span data-ttu-id="d8088-133">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="d8088-133">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="d8088-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="d8088-134">NOTES</span></span>

## <span data-ttu-id="d8088-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d8088-135">RELATED LINKS</span></span>
