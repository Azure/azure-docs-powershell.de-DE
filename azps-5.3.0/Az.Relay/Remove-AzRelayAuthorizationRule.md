---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayAuthorizationRule.md
ms.openlocfilehash: f99330a7611964e8db3d41f4ece56bb247c1c403
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378116"
---
# <span data-ttu-id="dd7af-101">Remove-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="dd7af-101">Remove-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="dd7af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd7af-102">SYNOPSIS</span></span>
<span data-ttu-id="dd7af-103">Entfernt die Autorisierungsregel für eine HybridVerbindung aus den angegebenen Relayentitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="dd7af-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="dd7af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd7af-104">SYNTAX</span></span>

### <span data-ttu-id="dd7af-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="dd7af-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd7af-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="dd7af-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd7af-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="dd7af-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd7af-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd7af-108">DESCRIPTION</span></span>
<span data-ttu-id="dd7af-109">Das **Cmdlet "Remove-AzRelayAuthorizationRule"** entfernt die Autorisierungsregel der angegebenen Relayentitäten (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="dd7af-109">The **Remove-AzRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="dd7af-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dd7af-110">EXAMPLES</span></span>

### <span data-ttu-id="dd7af-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dd7af-111">Example 1</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="dd7af-112">Entfernt die `AuthoRule1` Autorisierungsregel des `TestNameSpace-Relay1` Namespaces.</span><span class="sxs-lookup"><span data-stu-id="dd7af-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="dd7af-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="dd7af-113">Example 2</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="dd7af-114">Entfernt die `AuthoRule1` Autorisierungsregel für "WcfRelay" `TestWcfRelay` aus dem `TestNameSpace-Relay1` Namespace.</span><span class="sxs-lookup"><span data-stu-id="dd7af-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="dd7af-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="dd7af-115">Example 3</span></span>
```
PS C:\> Remove-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="dd7af-116">Entfernt die `AuthoRule1` Autorisierungsregel für HybridConnection `TestHybridConnection` aus dem `TestNameSpace-Relay1` Namespace.</span><span class="sxs-lookup"><span data-stu-id="dd7af-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="dd7af-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd7af-117">PARAMETERS</span></span>

### <span data-ttu-id="dd7af-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd7af-118">-DefaultProfile</span></span>
<span data-ttu-id="dd7af-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dd7af-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd7af-120">-Force</span><span class="sxs-lookup"><span data-stu-id="dd7af-120">-Force</span></span>
<span data-ttu-id="dd7af-121">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="dd7af-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="dd7af-122">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="dd7af-122">-HybridConnection</span></span>
<span data-ttu-id="dd7af-123">HybridConnection-Name.</span><span class="sxs-lookup"><span data-stu-id="dd7af-123">HybridConnection Name.</span></span>

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

### <span data-ttu-id="dd7af-124">-Name</span><span class="sxs-lookup"><span data-stu-id="dd7af-124">-Name</span></span>
<span data-ttu-id="dd7af-125">AuthorizationRule Name.</span><span class="sxs-lookup"><span data-stu-id="dd7af-125">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="dd7af-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dd7af-126">-Namespace</span></span>
<span data-ttu-id="dd7af-127">Namespacename.</span><span class="sxs-lookup"><span data-stu-id="dd7af-127">Namespace Name.</span></span>

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

### <span data-ttu-id="dd7af-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd7af-128">-PassThru</span></span>
<span data-ttu-id="dd7af-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="dd7af-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="dd7af-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd7af-130">-ResourceGroupName</span></span>
<span data-ttu-id="dd7af-131">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="dd7af-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="dd7af-132">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="dd7af-132">-WcfRelay</span></span>
<span data-ttu-id="dd7af-133">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="dd7af-133">WcfRelay Name.</span></span>

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

### <span data-ttu-id="dd7af-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd7af-134">-Confirm</span></span>
<span data-ttu-id="dd7af-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dd7af-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd7af-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="dd7af-136">-WhatIf</span></span>
<span data-ttu-id="dd7af-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dd7af-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd7af-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd7af-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd7af-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd7af-139">CommonParameters</span></span>
<span data-ttu-id="dd7af-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd7af-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd7af-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd7af-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd7af-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dd7af-142">INPUTS</span></span>

### <span data-ttu-id="dd7af-143">System.String</span><span class="sxs-lookup"><span data-stu-id="dd7af-143">System.String</span></span>

## <span data-ttu-id="dd7af-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dd7af-144">OUTPUTS</span></span>

### <span data-ttu-id="dd7af-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dd7af-145">System.Boolean</span></span>

## <span data-ttu-id="dd7af-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dd7af-146">NOTES</span></span>

## <span data-ttu-id="dd7af-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dd7af-147">RELATED LINKS</span></span>
