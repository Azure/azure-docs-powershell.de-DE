---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/new-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
ms.openlocfilehash: d0faea052141420db88f58fd6513c2d6822f56c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943799"
---
# <span data-ttu-id="08949-101">New-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="08949-101">New-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="08949-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08949-102">SYNOPSIS</span></span>
<span data-ttu-id="08949-103">Erstellt eine neue Autorisierungsregel für die angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="08949-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="08949-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="08949-104">SYNTAX</span></span>

### <span data-ttu-id="08949-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="08949-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08949-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="08949-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="08949-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="08949-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08949-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08949-108">DESCRIPTION</span></span>
<span data-ttu-id="08949-109">Das **Cmdlet New-AzRelayAuthorizationRule** erstellt eine neue Autorisierungsregel für die angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="08949-109">The **New-AzRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="08949-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="08949-110">EXAMPLES</span></span>

### <span data-ttu-id="08949-111">Beispiel 1: Namespace</span><span class="sxs-lookup"><span data-stu-id="08949-111">Example 1: Namespace</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="08949-112">Erstellt `AuthoRule1` mit **Listenrechten** für den -Namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="08949-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="08949-113">Beispiel 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="08949-113">Example 2: WcfRelay</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="08949-114">Erstellt eine `AuthoRule1` Autorisierungsregel mit **Listenberechtigungen** für wcfRelay. `TestWCFRelay1`</span><span class="sxs-lookup"><span data-stu-id="08949-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="08949-115">Beispiel 3: HybridVerbinden</span><span class="sxs-lookup"><span data-stu-id="08949-115">Example 3: HybridConnection</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="08949-116">Erstellt `AuthoRule1` mit **Listenrechten** für die Hybridverbindung `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="08949-116">Creates `AuthoRule1` with **Listen** rights for the Hybrid Connection `TestHybridConnection`.</span></span>

## <span data-ttu-id="08949-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="08949-117">PARAMETERS</span></span>

### <span data-ttu-id="08949-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08949-118">-DefaultProfile</span></span>
<span data-ttu-id="08949-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08949-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08949-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="08949-120">-HybridConnection</span></span>
<span data-ttu-id="08949-121">HybridVerbindeungsname.</span><span class="sxs-lookup"><span data-stu-id="08949-121">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08949-122">-Name</span><span class="sxs-lookup"><span data-stu-id="08949-122">-Name</span></span>
<span data-ttu-id="08949-123">AuthorizationRule Name.</span><span class="sxs-lookup"><span data-stu-id="08949-123">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08949-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="08949-124">-Namespace</span></span>
<span data-ttu-id="08949-125">Namespacename.</span><span class="sxs-lookup"><span data-stu-id="08949-125">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08949-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08949-126">-ResourceGroupName</span></span>
<span data-ttu-id="08949-127">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="08949-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="08949-128">-Rechte</span><span class="sxs-lookup"><span data-stu-id="08949-128">-Rights</span></span>
<span data-ttu-id="08949-129">Rechte, z. B. "Zuhören", "Senden", "Verwalten"</span><span class="sxs-lookup"><span data-stu-id="08949-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="08949-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="08949-130">-WcfRelay</span></span>
<span data-ttu-id="08949-131">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="08949-131">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08949-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="08949-132">-Confirm</span></span>
<span data-ttu-id="08949-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="08949-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08949-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08949-134">-WhatIf</span></span>
<span data-ttu-id="08949-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="08949-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08949-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="08949-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08949-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08949-137">CommonParameters</span></span>
<span data-ttu-id="08949-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08949-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08949-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08949-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08949-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="08949-140">INPUTS</span></span>

### <span data-ttu-id="08949-141">System.String</span><span class="sxs-lookup"><span data-stu-id="08949-141">System.String</span></span>

### <span data-ttu-id="08949-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="08949-142">System.String[]</span></span>

## <span data-ttu-id="08949-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="08949-143">OUTPUTS</span></span>

### <span data-ttu-id="08949-144">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="08949-144">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="08949-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="08949-145">NOTES</span></span>

## <span data-ttu-id="08949-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="08949-146">RELATED LINKS</span></span>
