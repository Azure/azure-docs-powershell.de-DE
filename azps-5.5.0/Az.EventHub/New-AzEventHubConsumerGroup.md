---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
ms.openlocfilehash: ef03af9c452496d198aaaa073ee9fd967d851bb4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147913"
---
# <span data-ttu-id="08cd8-101">New-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="08cd8-101">New-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="08cd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08cd8-102">SYNOPSIS</span></span>
<span data-ttu-id="08cd8-103">Erstellt eine neue Consumergruppe für den angegebenen Ereignishub.</span><span class="sxs-lookup"><span data-stu-id="08cd8-103">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="08cd8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="08cd8-104">SYNTAX</span></span>

```
New-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08cd8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08cd8-105">DESCRIPTION</span></span>
<span data-ttu-id="08cd8-106">Erstellt eine neue Consumergruppe für den angegebenen Ereignishub.</span><span class="sxs-lookup"><span data-stu-id="08cd8-106">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="08cd8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="08cd8-107">EXAMPLES</span></span>

### <span data-ttu-id="08cd8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="08cd8-108">Example 1</span></span>
```
PS C:\> New-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="08cd8-109">Erstellt die Consumergruppe \` "MyConsumerGroupName" im Ereignishub \` \` "MyEventHubName", der auf den Namespace "MyNamespaceName" mit der Ressourcengruppe \` \` \` \` "MyResourceGroupName" begrenzt \` ist.</span><span class="sxs-lookup"><span data-stu-id="08cd8-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="08cd8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08cd8-110">PARAMETERS</span></span>

### <span data-ttu-id="08cd8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08cd8-111">-DefaultProfile</span></span>
<span data-ttu-id="08cd8-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08cd8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08cd8-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="08cd8-113">-EventHub</span></span>
<span data-ttu-id="08cd8-114">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="08cd8-114">EventHub Name</span></span>

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

### <span data-ttu-id="08cd8-115">-Name</span><span class="sxs-lookup"><span data-stu-id="08cd8-115">-Name</span></span>
<span data-ttu-id="08cd8-116">ConsumerGroup Name</span><span class="sxs-lookup"><span data-stu-id="08cd8-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="08cd8-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="08cd8-117">-Namespace</span></span>
<span data-ttu-id="08cd8-118">Namespacename</span><span class="sxs-lookup"><span data-stu-id="08cd8-118">Namespace Name</span></span>

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

### <span data-ttu-id="08cd8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08cd8-119">-ResourceGroupName</span></span>
<span data-ttu-id="08cd8-120">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="08cd8-120">Resource Group Name</span></span>

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

### <span data-ttu-id="08cd8-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="08cd8-121">-UserMetadata</span></span>
<span data-ttu-id="08cd8-122">Benutzermetadaten für ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="08cd8-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="08cd8-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="08cd8-123">-Confirm</span></span>
<span data-ttu-id="08cd8-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="08cd8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08cd8-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="08cd8-125">-WhatIf</span></span>
<span data-ttu-id="08cd8-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="08cd8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08cd8-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="08cd8-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08cd8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08cd8-128">CommonParameters</span></span>
<span data-ttu-id="08cd8-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08cd8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08cd8-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08cd8-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08cd8-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="08cd8-131">INPUTS</span></span>

### <span data-ttu-id="08cd8-132">System.String</span><span class="sxs-lookup"><span data-stu-id="08cd8-132">System.String</span></span>

## <span data-ttu-id="08cd8-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="08cd8-133">OUTPUTS</span></span>

### <span data-ttu-id="08cd8-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="08cd8-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="08cd8-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="08cd8-135">NOTES</span></span>

## <span data-ttu-id="08cd8-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="08cd8-136">RELATED LINKS</span></span>
