---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
ms.openlocfilehash: 28c6bf4d463331755121e8a1ea14bf7f93407017
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498809"
---
# <span data-ttu-id="78005-101">Remove-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="78005-101">Remove-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="78005-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="78005-102">SYNOPSIS</span></span>
<span data-ttu-id="78005-103">Entfernt die Warteschlange aus dem angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="78005-103">Removes the queue from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78005-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="78005-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78005-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="78005-105">DESCRIPTION</span></span>
<span data-ttu-id="78005-106">Das Cmdlet **Remove-AzureRmServiceBusQueue** entfernt die Warteschlange aus dem angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="78005-106">The **Remove-AzureRmServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="78005-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="78005-107">EXAMPLES</span></span>

### <span data-ttu-id="78005-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="78005-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="78005-109">Entfernt die Warteschlange `SB-Queue_exampl1` aus dem Namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="78005-109">Removes the queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="78005-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="78005-110">PARAMETERS</span></span>

### <span data-ttu-id="78005-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78005-111">-DefaultProfile</span></span>
<span data-ttu-id="78005-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="78005-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78005-113">-Name</span><span class="sxs-lookup"><span data-stu-id="78005-113">-Name</span></span>
<span data-ttu-id="78005-114">Name der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="78005-114">Queue Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78005-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="78005-115">-Namespace</span></span>
<span data-ttu-id="78005-116">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="78005-116">Namespace Name.</span></span>

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

### <span data-ttu-id="78005-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78005-117">-ResourceGroupName</span></span>
<span data-ttu-id="78005-118">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="78005-118">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78005-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="78005-119">-Confirm</span></span>
<span data-ttu-id="78005-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="78005-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78005-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78005-121">-WhatIf</span></span>
<span data-ttu-id="78005-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="78005-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78005-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="78005-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78005-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78005-124">CommonParameters</span></span>
<span data-ttu-id="78005-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78005-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78005-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78005-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78005-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="78005-127">INPUTS</span></span>

### <span data-ttu-id="78005-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="78005-128">-ResourceGroup</span></span>
 <span data-ttu-id="78005-129">System. String</span><span class="sxs-lookup"><span data-stu-id="78005-129">System.String</span></span>

### <span data-ttu-id="78005-130">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="78005-130">-NamespaceName</span></span>
 <span data-ttu-id="78005-131">System. String</span><span class="sxs-lookup"><span data-stu-id="78005-131">System.String</span></span>

### <span data-ttu-id="78005-132">-Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="78005-132">-QueueName</span></span>
 <span data-ttu-id="78005-133">System. String</span><span class="sxs-lookup"><span data-stu-id="78005-133">System.String</span></span>

## <span data-ttu-id="78005-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="78005-134">OUTPUTS</span></span>

### <span data-ttu-id="78005-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="78005-135">System.Object</span></span>

## <span data-ttu-id="78005-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="78005-136">NOTES</span></span>

## <span data-ttu-id="78005-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="78005-137">RELATED LINKS</span></span>

