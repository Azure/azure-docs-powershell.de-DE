---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayAuthorizationRule.md
ms.openlocfilehash: af83820d33b9f36d93cc7623001d22a6cb5e0212
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166153"
---
# <span data-ttu-id="23e93-101">Get-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="23e93-101">Get-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="23e93-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="23e93-102">SYNOPSIS</span></span>
<span data-ttu-id="23e93-103">Ruft die Beschreibung einer angegebenen Autorisierungsregel für eine bestimmte Relay-Entitäten (Namespace/WcfRelay/HybridConnection) ab.</span><span class="sxs-lookup"><span data-stu-id="23e93-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="23e93-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="23e93-104">SYNTAX</span></span>

### <span data-ttu-id="23e93-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="23e93-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23e93-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="23e93-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23e93-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="23e93-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23e93-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23e93-108">DESCRIPTION</span></span>
<span data-ttu-id="23e93-109">Das Cmdlet " **Get-AzRelayAuthorizationRule** " Ruft die Beschreibung der angegebenen Autorisierungsregel in den angegebenen Relay-Entitäten ab (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="23e93-109">The **Get-AzRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="23e93-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="23e93-110">EXAMPLES</span></span>

### <span data-ttu-id="23e93-111">Beispiel 1: Namespace</span><span class="sxs-lookup"><span data-stu-id="23e93-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut
         hoRule1
```

<span data-ttu-id="23e93-112">Gibt die angegebene Autorisierungsregel Beschreibung für einen angegebenen Namespace zurück.</span><span class="sxs-lookup"><span data-stu-id="23e93-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="23e93-113">Beispiel 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="23e93-113">Example 2: WcfRelay</span></span>
```powershell
PS C:\>Get-AzWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
         1/authorizationRules/AuthoRule1
```

<span data-ttu-id="23e93-114">Gibt die angegebene Autorisierungsregel Beschreibung für eine bestimmte WcfRelay zurück.</span><span class="sxs-lookup"><span data-stu-id="23e93-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="23e93-115">Beispiel 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="23e93-115">Example 3: HybridConnection</span></span>
```powershell
PS C:\> Get-AzRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test
         HybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="23e93-116">Gibt die angegebene Autorisierungsregel Beschreibung für eine bestimmte HybridConnection zurück.</span><span class="sxs-lookup"><span data-stu-id="23e93-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="23e93-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="23e93-117">PARAMETERS</span></span>

### <span data-ttu-id="23e93-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23e93-118">-DefaultProfile</span></span>
<span data-ttu-id="23e93-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="23e93-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23e93-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="23e93-120">-HybridConnection</span></span>
<span data-ttu-id="23e93-121">HybridConnection-Name.</span><span class="sxs-lookup"><span data-stu-id="23e93-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="23e93-122">-Name</span><span class="sxs-lookup"><span data-stu-id="23e93-122">-Name</span></span>
<span data-ttu-id="23e93-123">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="23e93-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="23e93-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="23e93-124">-Namespace</span></span>
<span data-ttu-id="23e93-125">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="23e93-125">Namespace Name.</span></span>

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

### <span data-ttu-id="23e93-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23e93-126">-ResourceGroupName</span></span>
<span data-ttu-id="23e93-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="23e93-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="23e93-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="23e93-128">-WcfRelay</span></span>
<span data-ttu-id="23e93-129">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="23e93-129">WcfRelay Name.</span></span>

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

### <span data-ttu-id="23e93-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23e93-130">CommonParameters</span></span>
<span data-ttu-id="23e93-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23e93-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23e93-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23e93-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23e93-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="23e93-133">INPUTS</span></span>

### <span data-ttu-id="23e93-134">System. String</span><span class="sxs-lookup"><span data-stu-id="23e93-134">System.String</span></span>

## <span data-ttu-id="23e93-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="23e93-135">OUTPUTS</span></span>

### <span data-ttu-id="23e93-136">Microsoft. Azure. Commands. Relay. Models. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="23e93-136">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="23e93-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="23e93-137">NOTES</span></span>

## <span data-ttu-id="23e93-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="23e93-138">RELATED LINKS</span></span>
