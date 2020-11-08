---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: beba9c457378949dfe82811186bde84522b46ae5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003940"
---
# <span data-ttu-id="91cec-101">New-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="91cec-101">New-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="91cec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="91cec-102">SYNOPSIS</span></span>
<span data-ttu-id="91cec-103">Erstellt eine neue Autorisierungsregel für den angegebenen ServiceBus-Namespace oder die angegebene Warteschlange oder das entsprechende Thema.</span><span class="sxs-lookup"><span data-stu-id="91cec-103">Creates a new authorization rule for the specified Service Bus given Namespace or Queue or Topic.</span></span>

## <span data-ttu-id="91cec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="91cec-104">SYNTAX</span></span>

### <span data-ttu-id="91cec-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="91cec-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91cec-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="91cec-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91cec-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="91cec-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="91cec-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91cec-108">DESCRIPTION</span></span>
<span data-ttu-id="91cec-109">Das Cmdlet **New-AzServiceBusAuthorizationRule** erstellt eine neue Autorisierungsregel für den angegebenen ServiceBus-Namespace oder-Wartebereich oder das angegebene Thema.</span><span class="sxs-lookup"><span data-stu-id="91cec-109">The **New-AzServiceBusAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="91cec-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="91cec-110">EXAMPLES</span></span>

### <span data-ttu-id="91cec-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="91cec-111">Example 1</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="91cec-112">Erstellt `AuthoRule1` mit **Listen** -und **Sende** rechten für den Namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="91cec-112">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="91cec-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="91cec-113">Example 2</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="91cec-114">Erstellt `AuthoRule1` mit **Listen** -und **Sende** rechten für die Warteschlange `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="91cec-114">Creates `AuthoRule1` with **Listen** and **Send** rights for the queue `SBQueue`.</span></span>

### <span data-ttu-id="91cec-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="91cec-115">Example 3</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="91cec-116">Erstellt `AuthoRule1` mit **Listen** -und **Sende** rechten für das Thema `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="91cec-116">Creates `AuthoRule1` with **Listen** and **Send** rights for the topic `SBTopic`.</span></span>

## <span data-ttu-id="91cec-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="91cec-117">PARAMETERS</span></span>

### <span data-ttu-id="91cec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91cec-118">-DefaultProfile</span></span>
<span data-ttu-id="91cec-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="91cec-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91cec-120">-Name</span><span class="sxs-lookup"><span data-stu-id="91cec-120">-Name</span></span>
<span data-ttu-id="91cec-121">AuthorizationRule-Name</span><span class="sxs-lookup"><span data-stu-id="91cec-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="91cec-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="91cec-122">-Namespace</span></span>
<span data-ttu-id="91cec-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="91cec-123">Namespace Name</span></span>

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

### <span data-ttu-id="91cec-124">-Queue</span><span class="sxs-lookup"><span data-stu-id="91cec-124">-Queue</span></span>
<span data-ttu-id="91cec-125">Warteschlangen Name</span><span class="sxs-lookup"><span data-stu-id="91cec-125">Queue Name</span></span>

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

### <span data-ttu-id="91cec-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91cec-126">-ResourceGroupName</span></span>
<span data-ttu-id="91cec-127">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="91cec-127">Resource Group Name</span></span>

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

### <span data-ttu-id="91cec-128">-Rechte</span><span class="sxs-lookup"><span data-stu-id="91cec-128">-Rights</span></span>
<span data-ttu-id="91cec-129">Rechte wie "Abhören", "Senden", "verwalten"</span><span class="sxs-lookup"><span data-stu-id="91cec-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="91cec-130">-Topic</span><span class="sxs-lookup"><span data-stu-id="91cec-130">-Topic</span></span>
<span data-ttu-id="91cec-131">Name des Themas</span><span class="sxs-lookup"><span data-stu-id="91cec-131">Topic Name</span></span>

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

### <span data-ttu-id="91cec-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="91cec-132">-Confirm</span></span>
<span data-ttu-id="91cec-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="91cec-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91cec-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91cec-134">-WhatIf</span></span>
<span data-ttu-id="91cec-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="91cec-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91cec-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="91cec-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91cec-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91cec-137">CommonParameters</span></span>
<span data-ttu-id="91cec-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91cec-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91cec-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91cec-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91cec-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="91cec-140">INPUTS</span></span>

### <span data-ttu-id="91cec-141">System. String</span><span class="sxs-lookup"><span data-stu-id="91cec-141">System.String</span></span>

### <span data-ttu-id="91cec-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="91cec-142">System.String[]</span></span>

## <span data-ttu-id="91cec-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="91cec-143">OUTPUTS</span></span>

### <span data-ttu-id="91cec-144">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="91cec-144">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="91cec-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="91cec-145">NOTES</span></span>

## <span data-ttu-id="91cec-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="91cec-146">RELATED LINKS</span></span>
