---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/new-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: 08560730438fe5bca85a78e8a7f75f427c07de0d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932243"
---
# <span data-ttu-id="ecd90-101">New-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ecd90-101">New-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="ecd90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecd90-102">SYNOPSIS</span></span>
<span data-ttu-id="ecd90-103">Erstellt eine neue Autorisierungsregel für den angegebenen Service Bus, der namespace oder Queue oder Topic enthält.</span><span class="sxs-lookup"><span data-stu-id="ecd90-103">Creates a new authorization rule for the specified Service Bus given Namespace or Queue or Topic.</span></span>

## <span data-ttu-id="ecd90-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ecd90-104">SYNTAX</span></span>

### <span data-ttu-id="ecd90-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ecd90-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecd90-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ecd90-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ecd90-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ecd90-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ecd90-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ecd90-108">DESCRIPTION</span></span>
<span data-ttu-id="ecd90-109">Das **Cmdlet New-AzServiceBusAuthorizationRule** erstellt eine neue Autorisierungsregel für den angegebenen Service Bus-Namespace oder die angegebene Warteschlange oder das angegebene Thema.</span><span class="sxs-lookup"><span data-stu-id="ecd90-109">The **New-AzServiceBusAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="ecd90-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ecd90-110">EXAMPLES</span></span>

### <span data-ttu-id="ecd90-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ecd90-111">Example 1</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="ecd90-112">Erstellt `AuthoRule1` mit den Rechten **"Anhören"** und **"Senden"** für den -Namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="ecd90-112">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="ecd90-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ecd90-113">Example 2</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="ecd90-114">Erstellt `AuthoRule1` mit den Rechten **"Anhören"** **und "Senden"** für die `SBQueue` Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="ecd90-114">Creates `AuthoRule1` with **Listen** and **Send** rights for the queue `SBQueue`.</span></span>

### <span data-ttu-id="ecd90-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ecd90-115">Example 3</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="ecd90-116">Erstellt `AuthoRule1` mit den Rechten **"Anhören"** und "Senden" für das Thema  `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="ecd90-116">Creates `AuthoRule1` with **Listen** and **Send** rights for the topic `SBTopic`.</span></span>

## <span data-ttu-id="ecd90-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ecd90-117">PARAMETERS</span></span>

### <span data-ttu-id="ecd90-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecd90-118">-DefaultProfile</span></span>
<span data-ttu-id="ecd90-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ecd90-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecd90-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ecd90-120">-Name</span></span>
<span data-ttu-id="ecd90-121">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="ecd90-121">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecd90-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ecd90-122">-Namespace</span></span>
<span data-ttu-id="ecd90-123">Namespacename</span><span class="sxs-lookup"><span data-stu-id="ecd90-123">Namespace Name</span></span>

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

### <span data-ttu-id="ecd90-124">-Queue</span><span class="sxs-lookup"><span data-stu-id="ecd90-124">-Queue</span></span>
<span data-ttu-id="ecd90-125">Warteschlangenname</span><span class="sxs-lookup"><span data-stu-id="ecd90-125">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecd90-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecd90-126">-ResourceGroupName</span></span>
<span data-ttu-id="ecd90-127">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="ecd90-127">Resource Group Name</span></span>

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

### <span data-ttu-id="ecd90-128">-Rechte</span><span class="sxs-lookup"><span data-stu-id="ecd90-128">-Rights</span></span>
<span data-ttu-id="ecd90-129">Rechte, z. B. "Zuhören", "Senden", "Verwalten"</span><span class="sxs-lookup"><span data-stu-id="ecd90-129">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecd90-130">-Topic</span><span class="sxs-lookup"><span data-stu-id="ecd90-130">-Topic</span></span>
<span data-ttu-id="ecd90-131">Topic Name</span><span class="sxs-lookup"><span data-stu-id="ecd90-131">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecd90-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ecd90-132">-Confirm</span></span>
<span data-ttu-id="ecd90-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ecd90-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecd90-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecd90-134">-WhatIf</span></span>
<span data-ttu-id="ecd90-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ecd90-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecd90-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ecd90-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecd90-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecd90-137">CommonParameters</span></span>
<span data-ttu-id="ecd90-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecd90-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecd90-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecd90-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecd90-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ecd90-140">INPUTS</span></span>

### <span data-ttu-id="ecd90-141">System.String</span><span class="sxs-lookup"><span data-stu-id="ecd90-141">System.String</span></span>

### <span data-ttu-id="ecd90-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="ecd90-142">System.String[]</span></span>

## <span data-ttu-id="ecd90-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ecd90-143">OUTPUTS</span></span>

### <span data-ttu-id="ecd90-144">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="ecd90-144">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="ecd90-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ecd90-145">NOTES</span></span>

## <span data-ttu-id="ecd90-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ecd90-146">RELATED LINKS</span></span>
