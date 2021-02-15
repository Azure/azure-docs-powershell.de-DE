---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
ms.openlocfilehash: 25a81344d9d8d5b8af8eed907bce7977408515ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151732"
---
# <span data-ttu-id="16d20-101">New-AzFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="16d20-101">New-AzFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="16d20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16d20-102">SYNOPSIS</span></span>
<span data-ttu-id="16d20-103">Erstellen einer neuen Anwendungsregel für die Azure-Firewallrichtlinie</span><span class="sxs-lookup"><span data-stu-id="16d20-103">Create a new Azure Firewall Policy Application Rule</span></span>

## <span data-ttu-id="16d20-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16d20-104">SYNTAX</span></span>

### <span data-ttu-id="16d20-105">SourceAddressAndTargetFqdn (Standard)</span><span class="sxs-lookup"><span data-stu-id="16d20-105">SourceAddressAndTargetFqdn (Default)</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16d20-106">SourceAddressAndFqdnTag</span><span class="sxs-lookup"><span data-stu-id="16d20-106">SourceAddressAndFqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16d20-107">SourceAddressAndWebCategory</span><span class="sxs-lookup"><span data-stu-id="16d20-107">SourceAddressAndWebCategory</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -WebCategory <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16d20-108">SourceAddressAndTargetUrl</span><span class="sxs-lookup"><span data-stu-id="16d20-108">SourceAddressAndTargetUrl</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -TargetUrl <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16d20-109">SourceIpGroupAndTargetUrl</span><span class="sxs-lookup"><span data-stu-id="16d20-109">SourceIpGroupAndTargetUrl</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -TargetUrl <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16d20-110">SourceIpGroupAndTargetFqdn</span><span class="sxs-lookup"><span data-stu-id="16d20-110">SourceIpGroupAndTargetFqdn</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16d20-111">SourceIpGroupAndFqdnTag</span><span class="sxs-lookup"><span data-stu-id="16d20-111">SourceIpGroupAndFqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16d20-112">SourceIpGroupAndWebCategory</span><span class="sxs-lookup"><span data-stu-id="16d20-112">SourceIpGroupAndWebCategory</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -WebCategory <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16d20-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="16d20-113">DESCRIPTION</span></span>
<span data-ttu-id="16d20-114">Das **Cmdlet "New-AzFirewallPolicyApplicationRule"** erstellt eine Anwendungsregel für eine Azure-Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="16d20-114">The **New-AzFirewallPolicyApplicationRule** cmdlet creates an Application Rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="16d20-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="16d20-115">EXAMPLES</span></span>

### <span data-ttu-id="16d20-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="16d20-116">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -TargetFqdn "*.ro", "*.com"
```

<span data-ttu-id="16d20-117">In diesem Beispiel wird eine Anwendungsregel mit der Quelladresse, dem Protokoll und den Zielfqdns erstellt.</span><span class="sxs-lookup"><span data-stu-id="16d20-117">This example creates an application rule with the source address, protocol and the target fqdns.</span></span>

### <span data-ttu-id="16d20-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="16d20-118">Example 2</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -WebCategory "DatingAndPersonals", "Tasteless"
```

<span data-ttu-id="16d20-119">In diesem Beispiel wird eine Anwendungsregel mit quelladresse, protokoll- und webkategorien erstellt.</span><span class="sxs-lookup"><span data-stu-id="16d20-119">This example creates an application rule with the source address, protocol and web categories.</span></span>

## <span data-ttu-id="16d20-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16d20-120">PARAMETERS</span></span>

### <span data-ttu-id="16d20-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16d20-121">-DefaultProfile</span></span>
<span data-ttu-id="16d20-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="16d20-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16d20-123">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="16d20-123">-Description</span></span>
<span data-ttu-id="16d20-124">Beschreibung der Regel</span><span class="sxs-lookup"><span data-stu-id="16d20-124">The description of the rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16d20-125">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="16d20-125">-FqdnTag</span></span>
<span data-ttu-id="16d20-126">Die FQDN-Tags der Regel</span><span class="sxs-lookup"><span data-stu-id="16d20-126">The FQDN Tags of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndFqdnTag, SourceIpGroupAndFqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16d20-127">-Name</span><span class="sxs-lookup"><span data-stu-id="16d20-127">-Name</span></span>
<span data-ttu-id="16d20-128">Der Name der Anwendungsregel</span><span class="sxs-lookup"><span data-stu-id="16d20-128">The name of the Application Rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16d20-129">-Protocol</span><span class="sxs-lookup"><span data-stu-id="16d20-129">-Protocol</span></span>
<span data-ttu-id="16d20-130">Die Protokolle der Regel</span><span class="sxs-lookup"><span data-stu-id="16d20-130">The protocols of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetFqdn, SourceAddressAndWebCategory, SourceIpGroupAndTargetFqdn, SourceIpGroupAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16d20-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="16d20-131">-SourceAddress</span></span>
<span data-ttu-id="16d20-132">Die Quelladressen der Regel</span><span class="sxs-lookup"><span data-stu-id="16d20-132">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetFqdn, SourceAddressAndFqdnTag, SourceAddressAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16d20-133">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="16d20-133">-SourceIpGroup</span></span>
<span data-ttu-id="16d20-134">Die Quell-IP-Gruppen der Regel</span><span class="sxs-lookup"><span data-stu-id="16d20-134">The source ipgroups of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceIpGroupAndTargetFqdn, SourceIpGroupAndFqdnTag, SourceIpGroupAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16d20-135">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="16d20-135">-TargetFqdn</span></span>
<span data-ttu-id="16d20-136">Die ziel-FQDNs der Regel</span><span class="sxs-lookup"><span data-stu-id="16d20-136">The target FQDNs of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetFqdn, SourceIpGroupAndTargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16d20-137">-WebCategory</span><span class="sxs-lookup"><span data-stu-id="16d20-137">-WebCategory</span></span>
<span data-ttu-id="16d20-138">Die Webkategorien der Regel</span><span class="sxs-lookup"><span data-stu-id="16d20-138">The Web Categories of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndWebCategory, SourceIpGroupAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16d20-139">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="16d20-139">-TargetUrl</span></span>
<span data-ttu-id="16d20-140">Die Ziel-URL der Regel</span><span class="sxs-lookup"><span data-stu-id="16d20-140">The Target Url of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetUrl, SourceIpGroupAndTargetUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16d20-141">-TerminateTLS</span><span class="sxs-lookup"><span data-stu-id="16d20-141">-TerminateTLS</span></span>
<span data-ttu-id="16d20-142">Steht für das Beenden von TLS</span><span class="sxs-lookup"><span data-stu-id="16d20-142">Indicates terminating TLS</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16d20-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16d20-143">CommonParameters</span></span>
<span data-ttu-id="16d20-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16d20-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16d20-145">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16d20-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16d20-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="16d20-146">INPUTS</span></span>

### <span data-ttu-id="16d20-147">Keine</span><span class="sxs-lookup"><span data-stu-id="16d20-147">None</span></span>

## <span data-ttu-id="16d20-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="16d20-148">OUTPUTS</span></span>

### <span data-ttu-id="16d20-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="16d20-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="16d20-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="16d20-150">NOTES</span></span>

## <span data-ttu-id="16d20-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="16d20-151">RELATED LINKS</span></span>
