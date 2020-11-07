---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 9c263e4d31d5d186abb4a08f3849db072aec3721
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845587"
---
# <span data-ttu-id="91488-101">Remove-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="91488-101">Remove-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="91488-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="91488-102">SYNOPSIS</span></span>
<span data-ttu-id="91488-103">Entfernt die NetworkRuleSet für den angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="91488-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="91488-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="91488-104">SYNTAX</span></span>

### <span data-ttu-id="91488-105">NetworkRuleSetPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="91488-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91488-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="91488-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91488-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="91488-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91488-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91488-108">DESCRIPTION</span></span>
<span data-ttu-id="91488-109">Entfernt die NetworkRuleSet für den angegebenen Namespace.</span><span class="sxs-lookup"><span data-stu-id="91488-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="91488-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="91488-110">EXAMPLES</span></span>

### <span data-ttu-id="91488-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="91488-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="91488-112">Name: standardmäßige Standardeinstellung: Allow ID:/Subscriptions/SubscriptionId/resourceGroups/ResourceGroup/Providers/Microsoft.EventHub/Namespaces/EventHub-Namespace-1375/networkRuleSets/default Type: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="91488-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 


<span data-ttu-id="91488-113">Löscht die NetworkRuleSet für den angegebenen Namespace "Eventhub-Namespace1-1375"</span><span class="sxs-lookup"><span data-stu-id="91488-113">Deletes the NetworkRuleSet for the Given "Eventhub-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="91488-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="91488-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -InputObject $result1375
```

<span data-ttu-id="91488-115">Löscht die NetworkRuleSet mit Inputobject</span><span class="sxs-lookup"><span data-stu-id="91488-115">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="91488-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="91488-116">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="91488-117">Name: standardmäßige Standardeinstellung: Allow ID:/Subscriptions/SubscriptionId/resourceGroups/ResourceGroup/Providers/Microsoft.EventHub/Namespaces/EventHub-Namespace-1375/networkRuleSets/default Type: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="91488-117">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="91488-118">Löscht die NetworkRuleSet mit der "Resourcen-Nr" des Namespaces.</span><span class="sxs-lookup"><span data-stu-id="91488-118">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="91488-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="91488-119">PARAMETERS</span></span>

### <span data-ttu-id="91488-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91488-120">-AsJob</span></span>
<span data-ttu-id="91488-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="91488-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91488-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91488-122">-DefaultProfile</span></span>
<span data-ttu-id="91488-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="91488-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91488-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="91488-124">-InputObject</span></span>
<span data-ttu-id="91488-125">Namespace-Objekt</span><span class="sxs-lookup"><span data-stu-id="91488-125">Namespace Object</span></span>

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

### <span data-ttu-id="91488-126">-Name</span><span class="sxs-lookup"><span data-stu-id="91488-126">-Name</span></span>
<span data-ttu-id="91488-127">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="91488-127">Namespace Name</span></span>

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

### <span data-ttu-id="91488-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="91488-128">-PassThru</span></span>
<span data-ttu-id="91488-129">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="91488-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="91488-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91488-130">-ResourceGroupName</span></span>
<span data-ttu-id="91488-131">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="91488-131">Resource Group Name</span></span>

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

### <span data-ttu-id="91488-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="91488-132">-ResourceId</span></span>
<span data-ttu-id="91488-133">Namespace-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="91488-133">Namespace Resource Id</span></span>

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

### <span data-ttu-id="91488-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="91488-134">-Confirm</span></span>
<span data-ttu-id="91488-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="91488-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91488-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91488-136">-WhatIf</span></span>
<span data-ttu-id="91488-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="91488-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91488-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="91488-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91488-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91488-139">CommonParameters</span></span>
<span data-ttu-id="91488-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91488-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="91488-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91488-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91488-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="91488-142">INPUTS</span></span>

### <span data-ttu-id="91488-143">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="91488-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="91488-144">System. String</span><span class="sxs-lookup"><span data-stu-id="91488-144">System.String</span></span>

## <span data-ttu-id="91488-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="91488-145">OUTPUTS</span></span>

### <span data-ttu-id="91488-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="91488-146">System.Boolean</span></span>

## <span data-ttu-id="91488-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="91488-147">NOTES</span></span>

## <span data-ttu-id="91488-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="91488-148">RELATED LINKS</span></span>