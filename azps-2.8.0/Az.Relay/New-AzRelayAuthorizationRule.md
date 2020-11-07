---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
ms.openlocfilehash: dbfecc8eaca271cf025f84a3f042684075ee98b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823588"
---
# <span data-ttu-id="05705-101">New-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="05705-101">New-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="05705-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="05705-102">SYNOPSIS</span></span>
<span data-ttu-id="05705-103">Erstellt eine neue Autorisierungsregel für die angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="05705-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="05705-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="05705-104">SYNTAX</span></span>

### <span data-ttu-id="05705-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="05705-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05705-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="05705-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="05705-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="05705-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="05705-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="05705-108">DESCRIPTION</span></span>
<span data-ttu-id="05705-109">Das Cmdlet **New-AzRelayAuthorizationRule** erstellt eine neue Autorisierungsregel für die angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="05705-109">The **New-AzRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="05705-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="05705-110">EXAMPLES</span></span>

### <span data-ttu-id="05705-111">Beispiel 1 – Namespace</span><span class="sxs-lookup"><span data-stu-id="05705-111">Example 1 - Namespace</span></span>
```
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="05705-112">Erstellt `AuthoRule1` mit **Listen** rechten für den Namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="05705-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="05705-113">Beispiel 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="05705-113">Example 2 - WcfRelay</span></span>
```
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="05705-114">Erstellt eine Autorisierungsregel `AuthoRule1` mit **Listen** rechten für das WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="05705-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="05705-115">Beispiel 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="05705-115">Example 3 - HybridConnection</span></span>
```
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="05705-116">Erstellt `AuthoRule1` mit **Listen** rechten für die Hybrid Verbindung `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="05705-116">Creates `AuthoRule1` with **Listen** rights for the Hybrid Connection `TestHybridConnection`.</span></span>

## <span data-ttu-id="05705-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="05705-117">PARAMETERS</span></span>

### <span data-ttu-id="05705-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05705-118">-DefaultProfile</span></span>
<span data-ttu-id="05705-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="05705-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05705-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="05705-120">-HybridConnection</span></span>
<span data-ttu-id="05705-121">HybridConnection-Name.</span><span class="sxs-lookup"><span data-stu-id="05705-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="05705-122">-Name</span><span class="sxs-lookup"><span data-stu-id="05705-122">-Name</span></span>
<span data-ttu-id="05705-123">AuthorizationRule-Name.</span><span class="sxs-lookup"><span data-stu-id="05705-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="05705-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="05705-124">-Namespace</span></span>
<span data-ttu-id="05705-125">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="05705-125">Namespace Name.</span></span>

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

### <span data-ttu-id="05705-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05705-126">-ResourceGroupName</span></span>
<span data-ttu-id="05705-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="05705-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="05705-128">-Rechte</span><span class="sxs-lookup"><span data-stu-id="05705-128">-Rights</span></span>
<span data-ttu-id="05705-129">Rechte wie "Abhören", "Senden", "verwalten"</span><span class="sxs-lookup"><span data-stu-id="05705-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="05705-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="05705-130">-WcfRelay</span></span>
<span data-ttu-id="05705-131">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="05705-131">WcfRelay Name.</span></span>

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

### <span data-ttu-id="05705-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="05705-132">-Confirm</span></span>
<span data-ttu-id="05705-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="05705-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05705-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05705-134">-WhatIf</span></span>
<span data-ttu-id="05705-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="05705-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05705-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="05705-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05705-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05705-137">CommonParameters</span></span>
<span data-ttu-id="05705-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05705-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05705-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05705-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05705-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="05705-140">INPUTS</span></span>

### <span data-ttu-id="05705-141">System. String</span><span class="sxs-lookup"><span data-stu-id="05705-141">System.String</span></span>

### <span data-ttu-id="05705-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="05705-142">System.String[]</span></span>

## <span data-ttu-id="05705-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="05705-143">OUTPUTS</span></span>

### <span data-ttu-id="05705-144">Microsoft. Azure. Commands. Relay. Models. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="05705-144">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="05705-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="05705-145">NOTES</span></span>

## <span data-ttu-id="05705-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="05705-146">RELATED LINKS</span></span>
