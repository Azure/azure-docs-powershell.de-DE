---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/add-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
ms.openlocfilehash: 60074271c37097e266e0c8e2ca1e4ee2a35e577d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842372"
---
# <span data-ttu-id="a9e79-101">Add-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="a9e79-101">Add-AzEventHubIPRule</span></span>

## <span data-ttu-id="a9e79-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9e79-102">SYNOPSIS</span></span>
<span data-ttu-id="a9e79-103">Hinzufügen einer einzelnen IP-Regel zum NetworkRuleSet des angegebenen Namespaces</span><span class="sxs-lookup"><span data-stu-id="a9e79-103">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="a9e79-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9e79-104">SYNTAX</span></span>

### <span data-ttu-id="a9e79-105">IPRulePropertiesParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a9e79-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9e79-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9e79-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9e79-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9e79-107">DESCRIPTION</span></span>
<span data-ttu-id="a9e79-108">Hinzufügen einer einzelnen IP-Regel zum NetworkRuleSet des angegebenen Namespaces</span><span class="sxs-lookup"><span data-stu-id="a9e79-108">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="a9e79-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9e79-109">EXAMPLES</span></span>

### <span data-ttu-id="a9e79-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a9e79-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="a9e79-111">Name: standardmäßige Standard: Allow ID:/Subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/Providers/Microsoft.Eventhub/Namespaces/Eventhub-Namespace-2389/networkRuleSets/default Typ: Microsoft. Eventhub/Namespaces/NetworkRuleSet IpRules: {11.22.33.44, allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="a9e79-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="a9e79-112">Fügen Sie die IPRule mit IpMask "11.22.33.44" hinzu, und die Aktion ermöglicht den angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="a9e79-112">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

### <span data-ttu-id="a9e79-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a9e79-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpRuleObject $ipruleobject
```
<span data-ttu-id="a9e79-114">Name: standardmäßige Standard: Allow ID:/Subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/Providers/Microsoft.Eventhub/Namespaces/Eventhub-Namespace-2389/networkRuleSets/default Typ: Microsoft. Eventhub/Namespaces/NetworkRuleSet IpRules: {11.22.33.44, allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="a9e79-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="a9e79-115">Fügen Sie die IPRule mit IpMask "11.22.33.44" hinzu, und die Aktion ermöglicht den angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="a9e79-115">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

## <span data-ttu-id="a9e79-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9e79-116">PARAMETERS</span></span>

### <span data-ttu-id="a9e79-117">– Aktion</span><span class="sxs-lookup"><span data-stu-id="a9e79-117">-Action</span></span>
<span data-ttu-id="a9e79-118">Die IP-Filter Aktion</span><span class="sxs-lookup"><span data-stu-id="a9e79-118">The IP Filter Action</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9e79-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9e79-119">-DefaultProfile</span></span>
<span data-ttu-id="a9e79-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a9e79-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9e79-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="a9e79-121">-IpMask</span></span>
<span data-ttu-id="a9e79-122">Subnet-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="a9e79-122">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9e79-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="a9e79-123">-IpRuleObject</span></span>
<span data-ttu-id="a9e79-124">IPRule-Konfigurationsobjekt, das hinzugefügt werden soll</span><span class="sxs-lookup"><span data-stu-id="a9e79-124">IPRule Configuration Object to be added</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9e79-125">-Name</span><span class="sxs-lookup"><span data-stu-id="a9e79-125">-Name</span></span>
<span data-ttu-id="a9e79-126">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="a9e79-126">Namespace Name</span></span>

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

### <span data-ttu-id="a9e79-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9e79-127">-ResourceGroupName</span></span>
<span data-ttu-id="a9e79-128">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="a9e79-128">Resource Group Name</span></span>

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

### <span data-ttu-id="a9e79-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a9e79-129">-Confirm</span></span>
<span data-ttu-id="a9e79-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a9e79-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9e79-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9e79-131">-WhatIf</span></span>
<span data-ttu-id="a9e79-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a9e79-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9e79-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a9e79-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9e79-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9e79-134">CommonParameters</span></span>
<span data-ttu-id="a9e79-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9e79-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a9e79-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9e79-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9e79-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9e79-137">INPUTS</span></span>

### <span data-ttu-id="a9e79-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a9e79-138">System.String</span></span>

### <span data-ttu-id="a9e79-139">Microsoft. Azure. Commands. EventHub. Models. PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="a9e79-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="a9e79-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9e79-140">OUTPUTS</span></span>

### <span data-ttu-id="a9e79-141">Microsoft. Azure. Commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="a9e79-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="a9e79-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9e79-142">NOTES</span></span>

## <span data-ttu-id="a9e79-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9e79-143">RELATED LINKS</span></span>
