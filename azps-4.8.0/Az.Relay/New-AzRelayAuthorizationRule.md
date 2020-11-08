---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
ms.openlocfilehash: 39bba687e355b1742210fb0c37fc8f1a65d957a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174900"
---
# <span data-ttu-id="da4f4-101">New-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="da4f4-101">New-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="da4f4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="da4f4-102">SYNOPSIS</span></span>
<span data-ttu-id="da4f4-103">Erstellt eine neue Autorisierungsregel für die angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="da4f4-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="da4f4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="da4f4-104">SYNTAX</span></span>

### <span data-ttu-id="da4f4-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="da4f4-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da4f4-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="da4f4-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da4f4-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="da4f4-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da4f4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="da4f4-108">DESCRIPTION</span></span>
<span data-ttu-id="da4f4-109">Das Cmdlet **New-AzRelayAuthorizationRule** erstellt eine neue Autorisierungsregel für die angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="da4f4-109">The **New-AzRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="da4f4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="da4f4-110">EXAMPLES</span></span>

### <span data-ttu-id="da4f4-111">Beispiel 1: Namespace</span><span class="sxs-lookup"><span data-stu-id="da4f4-111">Example 1: Namespace</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="da4f4-112">Erstellt `AuthoRule1` mit **Listen** rechten für den Namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="da4f4-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="da4f4-113">Beispiel 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="da4f4-113">Example 2: WcfRelay</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="da4f4-114">Erstellt eine Autorisierungsregel `AuthoRule1` mit **Listen** rechten für das WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="da4f4-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="da4f4-115">Beispiel 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="da4f4-115">Example 3: HybridConnection</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="da4f4-116">Erstellt `AuthoRule1` mit **Listen** rechten für die Hybrid Verbindung `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="da4f4-116">Creates `AuthoRule1` with **Listen** rights for the Hybrid Connection `TestHybridConnection`.</span></span>

## <span data-ttu-id="da4f4-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="da4f4-117">PARAMETERS</span></span>

### <span data-ttu-id="da4f4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da4f4-118">-DefaultProfile</span></span>
<span data-ttu-id="da4f4-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="da4f4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da4f4-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="da4f4-120">-HybridConnection</span></span>
<span data-ttu-id="da4f4-121">HybridConnection-Name.</span><span class="sxs-lookup"><span data-stu-id="da4f4-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="da4f4-122">-Name</span><span class="sxs-lookup"><span data-stu-id="da4f4-122">-Name</span></span>
<span data-ttu-id="da4f4-123">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="da4f4-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="da4f4-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="da4f4-124">-Namespace</span></span>
<span data-ttu-id="da4f4-125">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="da4f4-125">Namespace Name.</span></span>

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

### <span data-ttu-id="da4f4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da4f4-126">-ResourceGroupName</span></span>
<span data-ttu-id="da4f4-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="da4f4-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="da4f4-128">-Rechte</span><span class="sxs-lookup"><span data-stu-id="da4f4-128">-Rights</span></span>
<span data-ttu-id="da4f4-129">Rechte wie "Abhören", "Senden", "verwalten"</span><span class="sxs-lookup"><span data-stu-id="da4f4-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="da4f4-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="da4f4-130">-WcfRelay</span></span>
<span data-ttu-id="da4f4-131">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="da4f4-131">WcfRelay Name.</span></span>

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

### <span data-ttu-id="da4f4-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="da4f4-132">-Confirm</span></span>
<span data-ttu-id="da4f4-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="da4f4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da4f4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da4f4-134">-WhatIf</span></span>
<span data-ttu-id="da4f4-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="da4f4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da4f4-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="da4f4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da4f4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da4f4-137">CommonParameters</span></span>
<span data-ttu-id="da4f4-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da4f4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da4f4-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da4f4-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da4f4-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="da4f4-140">INPUTS</span></span>

### <span data-ttu-id="da4f4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="da4f4-141">System.String</span></span>

### <span data-ttu-id="da4f4-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="da4f4-142">System.String[]</span></span>

## <span data-ttu-id="da4f4-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="da4f4-143">OUTPUTS</span></span>

### <span data-ttu-id="da4f4-144">Microsoft. Azure. Commands. Relay. Models. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="da4f4-144">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="da4f4-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="da4f4-145">NOTES</span></span>

## <span data-ttu-id="da4f4-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="da4f4-146">RELATED LINKS</span></span>
