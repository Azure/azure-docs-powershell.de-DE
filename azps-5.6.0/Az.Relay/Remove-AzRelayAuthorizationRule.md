---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/remove-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
ms.openlocfilehash: 1284780428fdaacfc255faf2ac640565eec44950
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943768"
---
# <span data-ttu-id="f560d-101">Remove-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f560d-101">Remove-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="f560d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f560d-102">SYNOPSIS</span></span>
<span data-ttu-id="f560d-103">Entfernt die Autorisierungsregel einer HybridConnection aus den angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="f560d-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="f560d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f560d-104">SYNTAX</span></span>

### <span data-ttu-id="f560d-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f560d-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f560d-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f560d-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f560d-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f560d-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f560d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f560d-108">DESCRIPTION</span></span>
<span data-ttu-id="f560d-109">Das **Cmdlet Remove-AzRelayAuthorizationRule** entfernt die Autorisierungsregel der angegebenen Relay-Entitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="f560d-109">The **Remove-AzRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="f560d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f560d-110">EXAMPLES</span></span>

### <span data-ttu-id="f560d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f560d-111">Example 1</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="f560d-112">Entfernt die Autorisierungsregel `AuthoRule1` des `TestNameSpace-Relay1` Namespaces .</span><span class="sxs-lookup"><span data-stu-id="f560d-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="f560d-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f560d-113">Example 2</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="f560d-114">Entfernt die `AuthoRule1` Autorisierungsregel des WcfRelays `TestWcfRelay` aus dem -Namespace. `TestNameSpace-Relay1`</span><span class="sxs-lookup"><span data-stu-id="f560d-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="f560d-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="f560d-115">Example 3</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="f560d-116">Entfernt die `AuthoRule1` Autorisierungsregel der HybridConnection `TestHybridConnection` aus dem -Namespace. `TestNameSpace-Relay1`</span><span class="sxs-lookup"><span data-stu-id="f560d-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="f560d-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f560d-117">PARAMETERS</span></span>

### <span data-ttu-id="f560d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f560d-118">-DefaultProfile</span></span>
<span data-ttu-id="f560d-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f560d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f560d-120">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="f560d-120">-Force</span></span>
<span data-ttu-id="f560d-121">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="f560d-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f560d-122">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="f560d-122">-HybridConnection</span></span>
<span data-ttu-id="f560d-123">HybridVerbindeungsname.</span><span class="sxs-lookup"><span data-stu-id="f560d-123">HybridConnection Name.</span></span>

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

### <span data-ttu-id="f560d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f560d-124">-Name</span></span>
<span data-ttu-id="f560d-125">AuthorizationRule Name.</span><span class="sxs-lookup"><span data-stu-id="f560d-125">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="f560d-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f560d-126">-Namespace</span></span>
<span data-ttu-id="f560d-127">Namespacename.</span><span class="sxs-lookup"><span data-stu-id="f560d-127">Namespace Name.</span></span>

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

### <span data-ttu-id="f560d-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f560d-128">-PassThru</span></span>
<span data-ttu-id="f560d-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="f560d-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f560d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f560d-130">-ResourceGroupName</span></span>
<span data-ttu-id="f560d-131">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="f560d-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="f560d-132">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="f560d-132">-WcfRelay</span></span>
<span data-ttu-id="f560d-133">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="f560d-133">WcfRelay Name.</span></span>

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

### <span data-ttu-id="f560d-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f560d-134">-Confirm</span></span>
<span data-ttu-id="f560d-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f560d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f560d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f560d-136">-WhatIf</span></span>
<span data-ttu-id="f560d-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f560d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f560d-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f560d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f560d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f560d-139">CommonParameters</span></span>
<span data-ttu-id="f560d-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f560d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f560d-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f560d-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f560d-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f560d-142">INPUTS</span></span>

### <span data-ttu-id="f560d-143">System.String</span><span class="sxs-lookup"><span data-stu-id="f560d-143">System.String</span></span>

## <span data-ttu-id="f560d-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f560d-144">OUTPUTS</span></span>

### <span data-ttu-id="f560d-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f560d-145">System.Boolean</span></span>

## <span data-ttu-id="f560d-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f560d-146">NOTES</span></span>

## <span data-ttu-id="f560d-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f560d-147">RELATED LINKS</span></span>
