---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 098c61be4eaf405d3c3a031601b48f20de1e234a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478930"
---
# <span data-ttu-id="a8ba5-101">New-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a8ba5-101">New-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="a8ba5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a8ba5-102">SYNOPSIS</span></span>
<span data-ttu-id="a8ba5-103">Erstellt eine neue Autorisierungsregel für die angegebene ServiceBus-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="a8ba5-103">Creates a new authorization rule for the specified Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8ba5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8ba5-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Queue <String>
 -Name <String> [-Rights] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8ba5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8ba5-105">DESCRIPTION</span></span>
<span data-ttu-id="a8ba5-106">Das Cmdlet **New-AzureRmServiceBusQueueAuthorizationRule** erstellt eine neue Autorisierungsregel für die angegebene ServiceBus-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="a8ba5-106">The **New-AzureRmServiceBusQueueAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus queue.</span></span>

## <span data-ttu-id="a8ba5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a8ba5-107">EXAMPLES</span></span>

### <span data-ttu-id="a8ba5-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a8ba5-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="a8ba5-109">Erstellt eine Autorisierungsregel `SBAuthoRule1` mit **Listen-und sende** rechten für die Warteschlange `SB-Queue_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="a8ba5-109">Creates authorization rule `SBAuthoRule1` with **Listen and Send** rights for the queue `SB-Queue_exampl1`.</span></span>

## <span data-ttu-id="a8ba5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8ba5-110">PARAMETERS</span></span>

### <span data-ttu-id="a8ba5-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a8ba5-111">-ResourceGroup</span></span>
<span data-ttu-id="a8ba5-112">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a8ba5-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="a8ba5-113">-Rechte</span><span class="sxs-lookup"><span data-stu-id="a8ba5-113">-Rights</span></span>
<span data-ttu-id="a8ba5-114">Gibt die Rechte an; Zum Beispiel</span><span class="sxs-lookup"><span data-stu-id="a8ba5-114">Specifies the rights; for example,</span></span>  
<span data-ttu-id="a8ba5-115">@ ("Abhören"; "Senden"; "verwalten")</span><span class="sxs-lookup"><span data-stu-id="a8ba5-115">@("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ba5-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a8ba5-116">-Confirm</span></span>
<span data-ttu-id="a8ba5-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a8ba5-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8ba5-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8ba5-118">-WhatIf</span></span>
<span data-ttu-id="a8ba5-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a8ba5-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8ba5-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a8ba5-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8ba5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8ba5-121">-DefaultProfile</span></span>
<span data-ttu-id="a8ba5-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a8ba5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8ba5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a8ba5-123">-Name</span></span>
<span data-ttu-id="a8ba5-124">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="a8ba5-124">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ba5-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a8ba5-125">-Namespace</span></span>
<span data-ttu-id="a8ba5-126">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="a8ba5-126">Namespace Name.</span></span>

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

### <span data-ttu-id="a8ba5-127">-Queue</span><span class="sxs-lookup"><span data-stu-id="a8ba5-127">-Queue</span></span>
<span data-ttu-id="a8ba5-128">Name der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="a8ba5-128">Queue Name.</span></span>

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

### <span data-ttu-id="a8ba5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8ba5-129">CommonParameters</span></span>
<span data-ttu-id="a8ba5-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8ba5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8ba5-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8ba5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8ba5-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a8ba5-132">INPUTS</span></span>

### <span data-ttu-id="a8ba5-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a8ba5-133">-ResourceGroup</span></span>
 <span data-ttu-id="a8ba5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a8ba5-134">System.String</span></span>
 

### <span data-ttu-id="a8ba5-135">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="a8ba5-135">-NamespaceName</span></span>
 <span data-ttu-id="a8ba5-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a8ba5-136">System.String</span></span>
 

### <span data-ttu-id="a8ba5-137">-Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="a8ba5-137">-QueueName</span></span>
 <span data-ttu-id="a8ba5-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a8ba5-138">System.String</span></span>
 

### <span data-ttu-id="a8ba5-139">-Authorizationrulename</span><span class="sxs-lookup"><span data-stu-id="a8ba5-139">-AuthorizationRuleName</span></span>
 <span data-ttu-id="a8ba5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a8ba5-140">System.String</span></span>

## <span data-ttu-id="a8ba5-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a8ba5-141">OUTPUTS</span></span>

### <span data-ttu-id="a8ba5-142">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="a8ba5-142">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="a8ba5-143">ID:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/ResourceGroups/default-ServiceBus-westus/Providers/Microsoft.ServiceBus/Namespaces/SB-example1/Queues/SB-Queue_exampl1/authorizati onrules/SBAuthoRule1 Typ: Microsoft. ServiceBus/authorizationrules Name: SBAuthoRule1 Ort: West US Tags: Rights: {Listen, senden}</span><span class="sxs-lookup"><span data-stu-id="a8ba5-143">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onRules/SBAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="a8ba5-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="a8ba5-144">NOTES</span></span>

## <span data-ttu-id="a8ba5-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a8ba5-145">RELATED LINKS</span></span>

