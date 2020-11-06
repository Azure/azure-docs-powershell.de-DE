---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
ms.openlocfilehash: c3d4ca61f0bbdc5dcea2eb41a9da0f5de1112719
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481569"
---
# <span data-ttu-id="cc772-101">Remove-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="cc772-101">Remove-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="cc772-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cc772-102">SYNOPSIS</span></span>
<span data-ttu-id="cc772-103">Entfernt das Abonnement für ein Thema aus dem angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="cc772-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc772-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc772-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc772-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cc772-105">DESCRIPTION</span></span>
<span data-ttu-id="cc772-106">Das Cmdlet **Remove-AzureRmServiceBusSubscription** entfernt das Abonnement für ein Thema aus dem angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="cc772-106">The **Remove-AzureRmServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="cc772-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cc772-107">EXAMPLES</span></span>

### <span data-ttu-id="cc772-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cc772-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="cc772-109">Entfernt das Abonnement `SB-TopicSubscription-Example1` für das Thema `SB-Topic_exampl1` im angegebenen ServiceBus `SB-Example1` -Namespace.</span><span class="sxs-lookup"><span data-stu-id="cc772-109">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="cc772-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc772-110">PARAMETERS</span></span>

### <span data-ttu-id="cc772-111">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cc772-111">-Confirm</span></span>
<span data-ttu-id="cc772-112">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cc772-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc772-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc772-113">-WhatIf</span></span>
<span data-ttu-id="cc772-114">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cc772-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc772-115">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cc772-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc772-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc772-116">-DefaultProfile</span></span>
<span data-ttu-id="cc772-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cc772-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc772-118">-Name</span><span class="sxs-lookup"><span data-stu-id="cc772-118">-Name</span></span>
<span data-ttu-id="cc772-119">Name des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="cc772-119">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc772-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cc772-120">-Namespace</span></span>
<span data-ttu-id="cc772-121">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="cc772-121">Namespace Name.</span></span>

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

### <span data-ttu-id="cc772-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc772-122">-ResourceGroupName</span></span>
<span data-ttu-id="cc772-123">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="cc772-123">The name of the resource group</span></span>

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

### <span data-ttu-id="cc772-124">-Topic</span><span class="sxs-lookup"><span data-stu-id="cc772-124">-Topic</span></span>
<span data-ttu-id="cc772-125">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="cc772-125">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc772-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc772-126">CommonParameters</span></span>
<span data-ttu-id="cc772-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc772-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc772-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc772-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc772-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cc772-129">INPUTS</span></span>

### <span data-ttu-id="cc772-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cc772-130">-ResourceGroup</span></span>
 <span data-ttu-id="cc772-131">System. String</span><span class="sxs-lookup"><span data-stu-id="cc772-131">System.String</span></span>

### <span data-ttu-id="cc772-132">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="cc772-132">-NamespaceName</span></span>
 <span data-ttu-id="cc772-133">System. String</span><span class="sxs-lookup"><span data-stu-id="cc772-133">System.String</span></span>

### <span data-ttu-id="cc772-134">-Topicname</span><span class="sxs-lookup"><span data-stu-id="cc772-134">-TopicName</span></span>
 <span data-ttu-id="cc772-135">System. String</span><span class="sxs-lookup"><span data-stu-id="cc772-135">System.String</span></span>

### <span data-ttu-id="cc772-136">-Abonnementname</span><span class="sxs-lookup"><span data-stu-id="cc772-136">-SubscriptionName</span></span>
 <span data-ttu-id="cc772-137">System. String</span><span class="sxs-lookup"><span data-stu-id="cc772-137">System.String</span></span>

## <span data-ttu-id="cc772-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cc772-138">OUTPUTS</span></span>

### <span data-ttu-id="cc772-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cc772-139">System.Boolean</span></span>

## <span data-ttu-id="cc772-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="cc772-140">NOTES</span></span>

## <span data-ttu-id="cc772-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cc772-141">RELATED LINKS</span></span>

