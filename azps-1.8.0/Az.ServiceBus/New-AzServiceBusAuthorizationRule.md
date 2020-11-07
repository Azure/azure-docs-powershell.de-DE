---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: 62edcb426fe62f834b876b0dd4e2006712f81348
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659396"
---
# <span data-ttu-id="5f277-101">New-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5f277-101">New-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="5f277-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5f277-102">SYNOPSIS</span></span>
<span data-ttu-id="5f277-103">Erstellt eine neue Autorisierungsregel für den angegebenen ServiceBus-Namespace oder die angegebene Warteschlange oder das entsprechende Thema.</span><span class="sxs-lookup"><span data-stu-id="5f277-103">Creates a new authorization rule for the specified Service Bus given Namespace or Queue or Topic.</span></span>

## <span data-ttu-id="5f277-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f277-104">SYNTAX</span></span>

### <span data-ttu-id="5f277-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5f277-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f277-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="5f277-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5f277-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="5f277-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5f277-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f277-108">DESCRIPTION</span></span>
<span data-ttu-id="5f277-109">Das Cmdlet **New-AzServiceBusAuthorizationRule** erstellt eine neue Autorisierungsregel für den angegebenen ServiceBus-Namespace oder-Wartebereich oder das angegebene Thema.</span><span class="sxs-lookup"><span data-stu-id="5f277-109">The **New-AzServiceBusAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="5f277-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5f277-110">EXAMPLES</span></span>

### <span data-ttu-id="5f277-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5f277-111">Example 1</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="5f277-112">Erstellt `AuthoRule1` mit **Listen** -und **Sende** rechten für den Namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="5f277-112">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="5f277-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5f277-113">Example 2</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="5f277-114">Erstellt `AuthoRule1` mit **Listen** -und **Sende** rechten für die Warteschlange `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="5f277-114">Creates `AuthoRule1` with **Listen** and **Send** rights for the queue `SBQueue`.</span></span>

### <span data-ttu-id="5f277-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5f277-115">Example 3</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="5f277-116">Erstellt `AuthoRule1` mit **Listen** -und **Sende** rechten für das Thema `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="5f277-116">Creates `AuthoRule1` with **Listen** and **Send** rights for the topic `SBTopic`.</span></span>

## <span data-ttu-id="5f277-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f277-117">PARAMETERS</span></span>

### <span data-ttu-id="5f277-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f277-118">-DefaultProfile</span></span>
<span data-ttu-id="5f277-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5f277-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f277-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5f277-120">-Name</span></span>
<span data-ttu-id="5f277-121">AuthorizationRule-Name</span><span class="sxs-lookup"><span data-stu-id="5f277-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="5f277-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5f277-122">-Namespace</span></span>
<span data-ttu-id="5f277-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="5f277-123">Namespace Name</span></span>

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

### <span data-ttu-id="5f277-124">-Queue</span><span class="sxs-lookup"><span data-stu-id="5f277-124">-Queue</span></span>
<span data-ttu-id="5f277-125">Warteschlangen Name</span><span class="sxs-lookup"><span data-stu-id="5f277-125">Queue Name</span></span>

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

### <span data-ttu-id="5f277-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f277-126">-ResourceGroupName</span></span>
<span data-ttu-id="5f277-127">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="5f277-127">Resource Group Name</span></span>

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

### <span data-ttu-id="5f277-128">-Rechte</span><span class="sxs-lookup"><span data-stu-id="5f277-128">-Rights</span></span>
<span data-ttu-id="5f277-129">Rechte wie "Abhören", "Senden", "verwalten"</span><span class="sxs-lookup"><span data-stu-id="5f277-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="5f277-130">-Topic</span><span class="sxs-lookup"><span data-stu-id="5f277-130">-Topic</span></span>
<span data-ttu-id="5f277-131">Name des Themas</span><span class="sxs-lookup"><span data-stu-id="5f277-131">Topic Name</span></span>

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

### <span data-ttu-id="5f277-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5f277-132">-Confirm</span></span>
<span data-ttu-id="5f277-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5f277-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f277-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f277-134">-WhatIf</span></span>
<span data-ttu-id="5f277-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f277-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f277-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5f277-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f277-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f277-137">CommonParameters</span></span>
<span data-ttu-id="5f277-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f277-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f277-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f277-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f277-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5f277-140">INPUTS</span></span>

### <span data-ttu-id="5f277-141">System. String</span><span class="sxs-lookup"><span data-stu-id="5f277-141">System.String</span></span>

### <span data-ttu-id="5f277-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="5f277-142">System.String[]</span></span>

## <span data-ttu-id="5f277-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5f277-143">OUTPUTS</span></span>

### <span data-ttu-id="5f277-144">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="5f277-144">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="5f277-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="5f277-145">NOTES</span></span>

## <span data-ttu-id="5f277-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5f277-146">RELATED LINKS</span></span>
