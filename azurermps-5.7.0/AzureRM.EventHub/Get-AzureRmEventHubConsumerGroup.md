---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 445d20453b9f3d99e4ff5c72e118b287f0a83898
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502589"
---
# <span data-ttu-id="14d89-101">Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="14d89-101">Get-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="14d89-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="14d89-102">SYNOPSIS</span></span>
<span data-ttu-id="14d89-103">Ruft die Details einer angegebenen Event Hubs-Verbrauchergruppe ab oder ruft eine Liste von Verbrauchergruppen in einem Ereignis-Hub ab.</span><span class="sxs-lookup"><span data-stu-id="14d89-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14d89-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="14d89-104">SYNTAX</span></span>

```
Get-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14d89-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14d89-105">DESCRIPTION</span></span>
<span data-ttu-id="14d89-106">Das Get-AzureRmEventHubConsumerGroup-Cmdlet ruft entweder die Details einer angegebenen Event Hubs-Verbrauchergruppe oder eine Liste von Verbrauchergruppen in einem bestimmten Ereignis-Hub ab.</span><span class="sxs-lookup"><span data-stu-id="14d89-106">The Get-AzureRmEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="14d89-107">Wenn der Name einer Consumer-Gruppe bereitgestellt wird, werden die Details einer einzelnen Consumer-Gruppe zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="14d89-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="14d89-108">Wenn der Name einer Consumer-Gruppe nicht angegeben wird, wird eine Liste der Verbrauchergruppen im angegebenen Ereignis-Hub zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="14d89-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="14d89-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="14d89-109">EXAMPLES</span></span>

### <span data-ttu-id="14d89-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="14d89-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="14d89-111">Ruft die Gruppe der \` Consumer \` -MyConsumerGroupName im MyEventHubName des Ereignis Hubs ab \` \` , die im Namespace \` mynamespacename \` mit Ressourcengruppe MyResourceGroupName vorhanden ist \` \` .</span><span class="sxs-lookup"><span data-stu-id="14d89-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="14d89-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="14d89-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="14d89-113">Ruft eine Liste der Verbrauchergruppen im MyEventHubName des Ereignis Hubs ab \` \` , die im Namespace \` mynamespacename \` mit Ressourcengruppe MyResourceGroupName vorhanden ist \` \` .</span><span class="sxs-lookup"><span data-stu-id="14d89-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="14d89-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="14d89-114">PARAMETERS</span></span>

### <span data-ttu-id="14d89-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14d89-115">-DefaultProfile</span></span>
<span data-ttu-id="14d89-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="14d89-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14d89-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="14d89-117">-EventHub</span></span>
<span data-ttu-id="14d89-118">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="14d89-118">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d89-119">-Name</span><span class="sxs-lookup"><span data-stu-id="14d89-119">-Name</span></span>
<span data-ttu-id="14d89-120">Consumergroup-Name</span><span class="sxs-lookup"><span data-stu-id="14d89-120">ConsumerGroup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d89-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="14d89-121">-Namespace</span></span>
<span data-ttu-id="14d89-122">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="14d89-122">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d89-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14d89-123">-ResourceGroupName</span></span>
<span data-ttu-id="14d89-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="14d89-124">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14d89-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14d89-125">CommonParameters</span></span>
<span data-ttu-id="14d89-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14d89-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="14d89-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14d89-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14d89-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="14d89-128">INPUTS</span></span>

### <span data-ttu-id="14d89-129">System. String</span><span class="sxs-lookup"><span data-stu-id="14d89-129">System.String</span></span>


## <span data-ttu-id="14d89-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="14d89-130">OUTPUTS</span></span>

### <span data-ttu-id="14d89-131">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="14d89-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="14d89-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="14d89-132">NOTES</span></span>

## <span data-ttu-id="14d89-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="14d89-133">RELATED LINKS</span></span>
