---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 80b3a5ce4cb38222993e69181519a864c578cf67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502421"
---
# <span data-ttu-id="c441d-101">Remove-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="c441d-101">Remove-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="c441d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c441d-102">SYNOPSIS</span></span>
<span data-ttu-id="c441d-103">Entfernt das Abonnement für ein Thema aus dem angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="c441d-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c441d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c441d-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c441d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c441d-105">DESCRIPTION</span></span>
<span data-ttu-id="c441d-106">Das Cmdlet **Remove-AzureRmServiceBusSubscription** entfernt das Abonnement für ein Thema aus dem angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="c441d-106">The **Remove-AzureRmServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="c441d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c441d-107">EXAMPLES</span></span>

### <span data-ttu-id="c441d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c441d-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="c441d-109">Entfernt das Abonnement `SB-TopicSubscription-Example1` für das Thema `SB-Topic_exampl1` im angegebenen ServiceBus `SB-Example1` -Namespace.</span><span class="sxs-lookup"><span data-stu-id="c441d-109">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="c441d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c441d-110">PARAMETERS</span></span>

### <span data-ttu-id="c441d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c441d-111">-DefaultProfile</span></span>
<span data-ttu-id="c441d-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c441d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c441d-113">-Name</span><span class="sxs-lookup"><span data-stu-id="c441d-113">-Name</span></span>
<span data-ttu-id="c441d-114">Name des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="c441d-114">Subscription Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c441d-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c441d-115">-Namespace</span></span>
<span data-ttu-id="c441d-116">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="c441d-116">Namespace Name.</span></span>

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

### <span data-ttu-id="c441d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c441d-117">-ResourceGroupName</span></span>
<span data-ttu-id="c441d-118">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="c441d-118">The name of the resource group</span></span>

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

### <span data-ttu-id="c441d-119">-Topic</span><span class="sxs-lookup"><span data-stu-id="c441d-119">-Topic</span></span>
<span data-ttu-id="c441d-120">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="c441d-120">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c441d-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c441d-121">-Confirm</span></span>
<span data-ttu-id="c441d-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c441d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c441d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c441d-123">-WhatIf</span></span>
<span data-ttu-id="c441d-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c441d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c441d-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c441d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c441d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c441d-126">CommonParameters</span></span>
<span data-ttu-id="c441d-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c441d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c441d-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c441d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c441d-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c441d-129">INPUTS</span></span>

### <span data-ttu-id="c441d-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c441d-130">-ResourceGroup</span></span>
 <span data-ttu-id="c441d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c441d-131">System.String</span></span>

### <span data-ttu-id="c441d-132">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="c441d-132">-NamespaceName</span></span>
 <span data-ttu-id="c441d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c441d-133">System.String</span></span>

### <span data-ttu-id="c441d-134">-Topicname</span><span class="sxs-lookup"><span data-stu-id="c441d-134">-TopicName</span></span>
 <span data-ttu-id="c441d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c441d-135">System.String</span></span>

### <span data-ttu-id="c441d-136">-Abonnementname</span><span class="sxs-lookup"><span data-stu-id="c441d-136">-SubscriptionName</span></span>
 <span data-ttu-id="c441d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c441d-137">System.String</span></span>

## <span data-ttu-id="c441d-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c441d-138">OUTPUTS</span></span>

### <span data-ttu-id="c441d-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c441d-139">System.Boolean</span></span>

## <span data-ttu-id="c441d-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="c441d-140">NOTES</span></span>

## <span data-ttu-id="c441d-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c441d-141">RELATED LINKS</span></span>

