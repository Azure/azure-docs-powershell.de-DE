---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 3ad94696ea10d791ebe2930b6c054e00b9e69d18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651160"
---
# <span data-ttu-id="dc742-101">Remove-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="dc742-101">Remove-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="dc742-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dc742-102">SYNOPSIS</span></span>
<span data-ttu-id="dc742-103">Entfernt die NetworkRuleSet für den angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="dc742-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="dc742-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc742-104">SYNTAX</span></span>

### <span data-ttu-id="dc742-105">NetworkRuleSetPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="dc742-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc742-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dc742-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc742-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc742-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc742-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc742-108">DESCRIPTION</span></span>
<span data-ttu-id="dc742-109">Entfernt die NetworkRuleSet für den angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="dc742-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="dc742-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dc742-110">EXAMPLES</span></span>

### <span data-ttu-id="dc742-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dc742-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="dc742-112">Name: standardmäßige Standardeinstellung: Allow ID:/Subscriptions/SubscriptionId/resourceGroups/ResourceGroup/Providers/Microsoft.EventHub/Namespaces/EventHub-Namespace-1375/networkRuleSets/default Type: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="dc742-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 


<span data-ttu-id="dc742-113">Löscht die NetworkRuleSet für den angegebenen Namespace "Eventhub-Namespace1-1375"</span><span class="sxs-lookup"><span data-stu-id="dc742-113">Deletes the NetworkRuleSet for the Given "Eventhub-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="dc742-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="dc742-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -InputObject $result1375
```

<span data-ttu-id="dc742-115">Löscht die NetworkRuleSet mit Inputobject</span><span class="sxs-lookup"><span data-stu-id="dc742-115">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="dc742-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="dc742-116">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="dc742-117">Name: standardmäßige Standardeinstellung: Allow ID:/Subscriptions/SubscriptionId/resourceGroups/ResourceGroup/Providers/Microsoft.EventHub/Namespaces/EventHub-Namespace-1375/networkRuleSets/default Type: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="dc742-117">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="dc742-118">Löscht die NetworkRuleSet mit der "Resourcen-Nr" des Namespaces.</span><span class="sxs-lookup"><span data-stu-id="dc742-118">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="dc742-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc742-119">PARAMETERS</span></span>

### <span data-ttu-id="dc742-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc742-120">-AsJob</span></span>
<span data-ttu-id="dc742-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="dc742-121">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc742-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc742-122">-DefaultProfile</span></span>
<span data-ttu-id="dc742-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dc742-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc742-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dc742-124">-InputObject</span></span>
<span data-ttu-id="dc742-125">Namespace-Objekt</span><span class="sxs-lookup"><span data-stu-id="dc742-125">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc742-126">-Name</span><span class="sxs-lookup"><span data-stu-id="dc742-126">-Name</span></span>
<span data-ttu-id="dc742-127">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="dc742-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc742-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc742-128">-PassThru</span></span>
<span data-ttu-id="dc742-129">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="dc742-129">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc742-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc742-130">-ResourceGroupName</span></span>
<span data-ttu-id="dc742-131">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="dc742-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc742-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="dc742-132">-ResourceId</span></span>
<span data-ttu-id="dc742-133">Namespace-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="dc742-133">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc742-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dc742-134">-Confirm</span></span>
<span data-ttu-id="dc742-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dc742-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc742-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc742-136">-WhatIf</span></span>
<span data-ttu-id="dc742-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dc742-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc742-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dc742-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc742-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc742-139">CommonParameters</span></span>
<span data-ttu-id="dc742-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc742-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="dc742-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc742-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc742-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dc742-142">INPUTS</span></span>

### <span data-ttu-id="dc742-143">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="dc742-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="dc742-144">System. String</span><span class="sxs-lookup"><span data-stu-id="dc742-144">System.String</span></span>

## <span data-ttu-id="dc742-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dc742-145">OUTPUTS</span></span>

### <span data-ttu-id="dc742-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dc742-146">System.Boolean</span></span>

## <span data-ttu-id="dc742-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="dc742-147">NOTES</span></span>

## <span data-ttu-id="dc742-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dc742-148">RELATED LINKS</span></span>