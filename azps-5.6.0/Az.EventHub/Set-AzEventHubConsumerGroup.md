---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/set-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
ms.openlocfilehash: 844b8a08a54409e4eb10cde9f063b65cb5587bae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947187"
---
# <span data-ttu-id="8fc0d-101">Set-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="8fc0d-101">Set-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="8fc0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fc0d-102">SYNOPSIS</span></span>
<span data-ttu-id="8fc0d-103">Aktualisiert die angegebene Ereignishub-Consumergruppe.</span><span class="sxs-lookup"><span data-stu-id="8fc0d-103">Updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="8fc0d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8fc0d-104">SYNTAX</span></span>

```
Set-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8fc0d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8fc0d-105">DESCRIPTION</span></span>
<span data-ttu-id="8fc0d-106">Das Set-AzEventHubConsumerGroup-Cmdlet aktualisiert die angegebene Ereignishub-Consumergruppe.</span><span class="sxs-lookup"><span data-stu-id="8fc0d-106">The Set-AzEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="8fc0d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8fc0d-107">EXAMPLES</span></span>

### <span data-ttu-id="8fc0d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8fc0d-108">Example 1</span></span>
```
PS C:\> Set-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="8fc0d-109">Legt die Benutzermetadaten der Consumergruppe \` MyConsumerGroupName \` auf "Testing" fest.</span><span class="sxs-lookup"><span data-stu-id="8fc0d-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="8fc0d-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8fc0d-110">PARAMETERS</span></span>

### <span data-ttu-id="8fc0d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fc0d-111">-DefaultProfile</span></span>
<span data-ttu-id="8fc0d-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8fc0d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fc0d-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="8fc0d-113">-EventHub</span></span>
<span data-ttu-id="8fc0d-114">EventHub-Name</span><span class="sxs-lookup"><span data-stu-id="8fc0d-114">EventHub Name</span></span>

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

### <span data-ttu-id="8fc0d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8fc0d-115">-Name</span></span>
<span data-ttu-id="8fc0d-116">ConsumerGroup Name</span><span class="sxs-lookup"><span data-stu-id="8fc0d-116">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fc0d-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8fc0d-117">-Namespace</span></span>
<span data-ttu-id="8fc0d-118">Namespacename</span><span class="sxs-lookup"><span data-stu-id="8fc0d-118">Namespace Name</span></span>

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

### <span data-ttu-id="8fc0d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fc0d-119">-ResourceGroupName</span></span>
<span data-ttu-id="8fc0d-120">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="8fc0d-120">Resource Group Name</span></span>

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

### <span data-ttu-id="8fc0d-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="8fc0d-121">-UserMetadata</span></span>
<span data-ttu-id="8fc0d-122">Benutzermetadaten für ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="8fc0d-122">User Metadata for ConsumerGroup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fc0d-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8fc0d-123">-Confirm</span></span>
<span data-ttu-id="8fc0d-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8fc0d-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc0d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fc0d-125">-WhatIf</span></span>
<span data-ttu-id="8fc0d-126">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8fc0d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fc0d-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8fc0d-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc0d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fc0d-128">CommonParameters</span></span>
<span data-ttu-id="8fc0d-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fc0d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fc0d-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fc0d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fc0d-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8fc0d-131">INPUTS</span></span>

### <span data-ttu-id="8fc0d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="8fc0d-132">System.String</span></span>

## <span data-ttu-id="8fc0d-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8fc0d-133">OUTPUTS</span></span>

### <span data-ttu-id="8fc0d-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="8fc0d-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="8fc0d-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8fc0d-135">NOTES</span></span>

## <span data-ttu-id="8fc0d-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8fc0d-136">RELATED LINKS</span></span>
