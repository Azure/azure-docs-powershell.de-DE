---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/get-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
ms.openlocfilehash: bed3165eee350f55470c0cbca575226e77ec9d71
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943828"
---
# <span data-ttu-id="ed026-101">Get-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ed026-101">Get-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="ed026-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed026-102">SYNOPSIS</span></span>
<span data-ttu-id="ed026-103">Ruft die Beschreibung einer angegebenen Autorisierungsregel für eine bestimmte Relay-Entität ab (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="ed026-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="ed026-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed026-104">SYNTAX</span></span>

### <span data-ttu-id="ed026-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ed026-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed026-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ed026-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed026-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ed026-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed026-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed026-108">DESCRIPTION</span></span>
<span data-ttu-id="ed026-109">Das **Get-AzRelayAuthorizationRule-Cmdlet** ruft die Beschreibung der angegebenen Autorisierungsregel in den angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection) ab.</span><span class="sxs-lookup"><span data-stu-id="ed026-109">The **Get-AzRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="ed026-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ed026-110">EXAMPLES</span></span>

### <span data-ttu-id="ed026-111">Beispiel 1: Namespace</span><span class="sxs-lookup"><span data-stu-id="ed026-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut
         hoRule1
```

<span data-ttu-id="ed026-112">Gibt die angegebene Beschreibung der Autorisierungsregel für einen angegebenen Namespace zurück.</span><span class="sxs-lookup"><span data-stu-id="ed026-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="ed026-113">Beispiel 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="ed026-113">Example 2: WcfRelay</span></span>
```powershell
PS C:\>Get-AzWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
         1/authorizationRules/AuthoRule1
```

<span data-ttu-id="ed026-114">Gibt die angegebene Beschreibung der Autorisierungsregel für ein bestimmtes WcfRelay zurück.</span><span class="sxs-lookup"><span data-stu-id="ed026-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="ed026-115">Beispiel 3: HybridVerbinden</span><span class="sxs-lookup"><span data-stu-id="ed026-115">Example 3: HybridConnection</span></span>
```powershell
PS C:\> Get-AzRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test
         HybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="ed026-116">Gibt die angegebene Beschreibung der Autorisierungsregel für eine gegebene HybridVerbindeung zurück.</span><span class="sxs-lookup"><span data-stu-id="ed026-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="ed026-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ed026-117">PARAMETERS</span></span>

### <span data-ttu-id="ed026-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed026-118">-DefaultProfile</span></span>
<span data-ttu-id="ed026-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed026-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed026-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="ed026-120">-HybridConnection</span></span>
<span data-ttu-id="ed026-121">HybridVerbindeungsname.</span><span class="sxs-lookup"><span data-stu-id="ed026-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="ed026-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ed026-122">-Name</span></span>
<span data-ttu-id="ed026-123">AuthorizationRule Name.</span><span class="sxs-lookup"><span data-stu-id="ed026-123">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed026-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ed026-124">-Namespace</span></span>
<span data-ttu-id="ed026-125">Namespacename.</span><span class="sxs-lookup"><span data-stu-id="ed026-125">Namespace Name.</span></span>

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

### <span data-ttu-id="ed026-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed026-126">-ResourceGroupName</span></span>
<span data-ttu-id="ed026-127">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="ed026-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="ed026-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="ed026-128">-WcfRelay</span></span>
<span data-ttu-id="ed026-129">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="ed026-129">WcfRelay Name.</span></span>

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

### <span data-ttu-id="ed026-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed026-130">CommonParameters</span></span>
<span data-ttu-id="ed026-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed026-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed026-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed026-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed026-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ed026-133">INPUTS</span></span>

### <span data-ttu-id="ed026-134">System.String</span><span class="sxs-lookup"><span data-stu-id="ed026-134">System.String</span></span>

## <span data-ttu-id="ed026-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ed026-135">OUTPUTS</span></span>

### <span data-ttu-id="ed026-136">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="ed026-136">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="ed026-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ed026-137">NOTES</span></span>

## <span data-ttu-id="ed026-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ed026-138">RELATED LINKS</span></span>
