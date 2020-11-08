---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
ms.openlocfilehash: cb898921b7fdfddddc95fc88d49dade4654c7ad2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007976"
---
# <span data-ttu-id="65d61-101">Set-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="65d61-101">Set-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="65d61-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="65d61-102">SYNOPSIS</span></span>
<span data-ttu-id="65d61-103">Aktualisiert die angegebene Event Hubs-Verbrauchergruppe.</span><span class="sxs-lookup"><span data-stu-id="65d61-103">Updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="65d61-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="65d61-104">SYNTAX</span></span>

```
Set-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="65d61-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65d61-105">DESCRIPTION</span></span>
<span data-ttu-id="65d61-106">Das Set-AzEventHubConsumerGroup-Cmdlet aktualisiert die angegebene Event Hubs-Verbrauchergruppe.</span><span class="sxs-lookup"><span data-stu-id="65d61-106">The Set-AzEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="65d61-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="65d61-107">EXAMPLES</span></span>

### <span data-ttu-id="65d61-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="65d61-108">Example 1</span></span>
```
PS C:\> Set-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="65d61-109">Legt die Benutzer Metadaten der Verbrauchergruppe \` MyConsumerGroupName \` auf "testen" fest.</span><span class="sxs-lookup"><span data-stu-id="65d61-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="65d61-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="65d61-110">PARAMETERS</span></span>

### <span data-ttu-id="65d61-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65d61-111">-DefaultProfile</span></span>
<span data-ttu-id="65d61-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="65d61-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65d61-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="65d61-113">-EventHub</span></span>
<span data-ttu-id="65d61-114">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="65d61-114">EventHub Name</span></span>

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

### <span data-ttu-id="65d61-115">-Name</span><span class="sxs-lookup"><span data-stu-id="65d61-115">-Name</span></span>
<span data-ttu-id="65d61-116">Consumergroup-Name</span><span class="sxs-lookup"><span data-stu-id="65d61-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="65d61-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="65d61-117">-Namespace</span></span>
<span data-ttu-id="65d61-118">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="65d61-118">Namespace Name</span></span>

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

### <span data-ttu-id="65d61-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65d61-119">-ResourceGroupName</span></span>
<span data-ttu-id="65d61-120">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="65d61-120">Resource Group Name</span></span>

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

### <span data-ttu-id="65d61-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="65d61-121">-UserMetadata</span></span>
<span data-ttu-id="65d61-122">Benutzer Metadaten für consumergroup</span><span class="sxs-lookup"><span data-stu-id="65d61-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="65d61-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="65d61-123">-Confirm</span></span>
<span data-ttu-id="65d61-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="65d61-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65d61-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65d61-125">-WhatIf</span></span>
<span data-ttu-id="65d61-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="65d61-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65d61-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="65d61-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65d61-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65d61-128">CommonParameters</span></span>
<span data-ttu-id="65d61-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65d61-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65d61-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65d61-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65d61-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="65d61-131">INPUTS</span></span>

### <span data-ttu-id="65d61-132">System. String</span><span class="sxs-lookup"><span data-stu-id="65d61-132">System.String</span></span>

## <span data-ttu-id="65d61-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="65d61-133">OUTPUTS</span></span>

### <span data-ttu-id="65d61-134">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="65d61-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="65d61-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="65d61-135">NOTES</span></span>

## <span data-ttu-id="65d61-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="65d61-136">RELATED LINKS</span></span>
