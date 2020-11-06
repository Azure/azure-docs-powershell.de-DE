---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
ms.openlocfilehash: 8c5c614a041ff0e4ab9bc4fdc0aea944901d1efc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481574"
---
# <span data-ttu-id="ec6b5-101">Remove-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="ec6b5-101">Remove-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="ec6b5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ec6b5-102">SYNOPSIS</span></span>
<span data-ttu-id="ec6b5-103">Entfernt die Warteschlange aus dem angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="ec6b5-103">Removes the queue from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec6b5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec6b5-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusQueue -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec6b5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec6b5-105">DESCRIPTION</span></span>
<span data-ttu-id="ec6b5-106">Das Cmdlet **Remove-AzureRmServiceBusQueue** entfernt die Warteschlange aus dem angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="ec6b5-106">The **Remove-AzureRmServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="ec6b5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ec6b5-107">EXAMPLES</span></span>

### <span data-ttu-id="ec6b5-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ec6b5-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="ec6b5-109">Entfernt die Warteschlange `SB-Queue_exampl1` aus dem Namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="ec6b5-109">Removes the queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="ec6b5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec6b5-110">PARAMETERS</span></span>

### <span data-ttu-id="ec6b5-111">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ec6b5-111">-Confirm</span></span>
<span data-ttu-id="ec6b5-112">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ec6b5-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec6b5-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec6b5-113">-WhatIf</span></span>
<span data-ttu-id="ec6b5-114">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ec6b5-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec6b5-115">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ec6b5-115">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec6b5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec6b5-116">-DefaultProfile</span></span>
<span data-ttu-id="ec6b5-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ec6b5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec6b5-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ec6b5-118">-Name</span></span>
<span data-ttu-id="ec6b5-119">Name der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="ec6b5-119">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec6b5-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ec6b5-120">-Namespace</span></span>
<span data-ttu-id="ec6b5-121">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="ec6b5-121">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec6b5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec6b5-122">-ResourceGroupName</span></span>
<span data-ttu-id="ec6b5-123">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="ec6b5-123">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec6b5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec6b5-124">CommonParameters</span></span>
<span data-ttu-id="ec6b5-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec6b5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec6b5-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec6b5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec6b5-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ec6b5-127">INPUTS</span></span>

### <span data-ttu-id="ec6b5-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ec6b5-128">-ResourceGroup</span></span>
 <span data-ttu-id="ec6b5-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ec6b5-129">System.String</span></span>

### <span data-ttu-id="ec6b5-130">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="ec6b5-130">-NamespaceName</span></span>
 <span data-ttu-id="ec6b5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ec6b5-131">System.String</span></span>

### <span data-ttu-id="ec6b5-132">-Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="ec6b5-132">-QueueName</span></span>
 <span data-ttu-id="ec6b5-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ec6b5-133">System.String</span></span>

## <span data-ttu-id="ec6b5-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ec6b5-134">OUTPUTS</span></span>

### <span data-ttu-id="ec6b5-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="ec6b5-135">System.Object</span></span>

## <span data-ttu-id="ec6b5-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="ec6b5-136">NOTES</span></span>

## <span data-ttu-id="ec6b5-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ec6b5-137">RELATED LINKS</span></span>

