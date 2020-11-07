---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: be2b841511669ffa2ac3ffd416fd86072edcfb52
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664435"
---
# <span data-ttu-id="09430-101">New-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="09430-101">New-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="09430-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="09430-102">SYNOPSIS</span></span>
<span data-ttu-id="09430-103">Erstellt eine neue Autorisierungsregel für den angegebenen ServiceBus-Namespace oder die angegebene Warteschlange oder das entsprechende Thema.</span><span class="sxs-lookup"><span data-stu-id="09430-103">Creates a new authorization rule for the specified Service Bus given Namespace or Queue or Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09430-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="09430-104">SYNTAX</span></span>

### <span data-ttu-id="09430-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="09430-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09430-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="09430-106">QueueAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="09430-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="09430-107">TopicAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="09430-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09430-108">DESCRIPTION</span></span>
<span data-ttu-id="09430-109">Das Cmdlet **New-AzureRmServiceBusAuthorizationRule** erstellt eine neue Autorisierungsregel für den angegebenen ServiceBus-Namespace oder-Wartebereich oder das angegebene Thema.</span><span class="sxs-lookup"><span data-stu-id="09430-109">The **New-AzureRmServiceBusAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="09430-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="09430-110">EXAMPLES</span></span>

### <span data-ttu-id="09430-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="09430-111">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="09430-112">Erstellt `AuthoRule1` mit **Listen** -und **Sende** rechten für den Namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="09430-112">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="09430-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="09430-113">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="09430-114">Erstellt `AuthoRule1` mit **Listen** -und **Sende** rechten für die Warteschlange `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="09430-114">Creates `AuthoRule1` with **Listen** and **Send** rights for the queue `SBQueue`.</span></span>

### <span data-ttu-id="09430-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="09430-115">Example 3</span></span>
```
PS C:\> New-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="09430-116">Erstellt `AuthoRule1` mit **Listen** -und **Sende** rechten für das Thema `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="09430-116">Creates `AuthoRule1` with **Listen** and **Send** rights for the topic `SBTopic`.</span></span>

## <span data-ttu-id="09430-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="09430-117">PARAMETERS</span></span>

### <span data-ttu-id="09430-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="09430-118">-Confirm</span></span>
<span data-ttu-id="09430-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="09430-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09430-120">-Name</span><span class="sxs-lookup"><span data-stu-id="09430-120">-Name</span></span>
<span data-ttu-id="09430-121">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="09430-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="09430-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="09430-122">-Namespace</span></span>
<span data-ttu-id="09430-123">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="09430-123">Namespace Name.</span></span>

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

### <span data-ttu-id="09430-124">-Queue</span><span class="sxs-lookup"><span data-stu-id="09430-124">-Queue</span></span>
<span data-ttu-id="09430-125">Name der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="09430-125">Queue Name.</span></span>

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

### <span data-ttu-id="09430-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09430-126">-ResourceGroupName</span></span>
<span data-ttu-id="09430-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="09430-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="09430-128">-Rechte</span><span class="sxs-lookup"><span data-stu-id="09430-128">-Rights</span></span>
<span data-ttu-id="09430-129">Rechte wie "Abhören", "Senden", "verwalten"</span><span class="sxs-lookup"><span data-stu-id="09430-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="09430-130">-Topic</span><span class="sxs-lookup"><span data-stu-id="09430-130">-Topic</span></span>
<span data-ttu-id="09430-131">Name des Themas.</span><span class="sxs-lookup"><span data-stu-id="09430-131">Topic Name.</span></span>

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

### <span data-ttu-id="09430-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09430-132">-WhatIf</span></span>
<span data-ttu-id="09430-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="09430-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09430-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="09430-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09430-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09430-135">-DefaultProfile</span></span>
<span data-ttu-id="09430-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="09430-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09430-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09430-137">CommonParameters</span></span>
<span data-ttu-id="09430-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09430-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09430-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09430-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09430-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="09430-140">INPUTS</span></span>

### <span data-ttu-id="09430-141">System. String</span><span class="sxs-lookup"><span data-stu-id="09430-141">System.String</span></span>
<span data-ttu-id="09430-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="09430-142">System.String[]</span></span>

## <span data-ttu-id="09430-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="09430-143">OUTPUTS</span></span>

### <span data-ttu-id="09430-144">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="09430-144">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="09430-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="09430-145">NOTES</span></span>

## <span data-ttu-id="09430-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="09430-146">RELATED LINKS</span></span>

