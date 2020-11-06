---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 5b88ce6edc92cb6483b8d6df95599fcea854f805
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496589"
---
# <span data-ttu-id="569db-101">Remove-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="569db-101">Remove-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="569db-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="569db-102">SYNOPSIS</span></span>
<span data-ttu-id="569db-103">Löscht die angegebene Event Hubs-Verbrauchergruppe.</span><span class="sxs-lookup"><span data-stu-id="569db-103">Deletes the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="569db-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="569db-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="569db-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="569db-105">DESCRIPTION</span></span>
<span data-ttu-id="569db-106">Das Remove-AzureRmEventHubConsumerGroup-Cmdlet entfernt die angegebene Consumer-Gruppe aus dem angegebenen Ereignis-Hub und löscht sie.</span><span class="sxs-lookup"><span data-stu-id="569db-106">The Remove-AzureRmEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="569db-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="569db-107">EXAMPLES</span></span>

### <span data-ttu-id="569db-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="569db-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="569db-109">Löscht die Consumer \` -Gruppen \` -MyConsumerGroupName aus dem \` Event \` -Hub-MyEventHubName, der auf den \` mynamespacename-Namespace beschränkt ist \` .</span><span class="sxs-lookup"><span data-stu-id="569db-109">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

## <span data-ttu-id="569db-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="569db-110">PARAMETERS</span></span>

### <span data-ttu-id="569db-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="569db-111">-DefaultProfile</span></span>
<span data-ttu-id="569db-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="569db-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="569db-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="569db-113">-EventHub</span></span>
<span data-ttu-id="569db-114">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="569db-114">EventHub Name</span></span>

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

### <span data-ttu-id="569db-115">-Name</span><span class="sxs-lookup"><span data-stu-id="569db-115">-Name</span></span>
<span data-ttu-id="569db-116">Consumergroup-Name</span><span class="sxs-lookup"><span data-stu-id="569db-116">ConsumerGroup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="569db-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="569db-117">-Namespace</span></span>
<span data-ttu-id="569db-118">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="569db-118">Namespace Name</span></span>

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

### <span data-ttu-id="569db-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="569db-119">-ResourceGroupName</span></span>
<span data-ttu-id="569db-120">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="569db-120">Resource Group Name</span></span>

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

### <span data-ttu-id="569db-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="569db-121">-Confirm</span></span>
<span data-ttu-id="569db-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="569db-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="569db-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="569db-123">-WhatIf</span></span>
<span data-ttu-id="569db-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="569db-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="569db-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="569db-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="569db-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="569db-126">CommonParameters</span></span>
<span data-ttu-id="569db-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="569db-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="569db-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="569db-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="569db-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="569db-129">INPUTS</span></span>

### <span data-ttu-id="569db-130">System. String</span><span class="sxs-lookup"><span data-stu-id="569db-130">System.String</span></span>


## <span data-ttu-id="569db-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="569db-131">OUTPUTS</span></span>

### <span data-ttu-id="569db-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="569db-132">System.Object</span></span>

## <span data-ttu-id="569db-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="569db-133">NOTES</span></span>

## <span data-ttu-id="569db-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="569db-134">RELATED LINKS</span></span>
