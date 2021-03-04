---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Start-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 674f88a30ea036fc496cd6931b3d856a20a25c0a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936008"
---
# <span data-ttu-id="a5437-101">Start-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a5437-101">Start-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="a5437-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5437-102">SYNOPSIS</span></span>
<span data-ttu-id="a5437-103">Ruft eine temporäre Netzwerkzugriffsanforderung auf.</span><span class="sxs-lookup"><span data-stu-id="a5437-103">Invokes a temporary network access request.</span></span>

## <span data-ttu-id="a5437-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5437-104">SYNTAX</span></span>

### <span data-ttu-id="a5437-105">ResourceGroupLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="a5437-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5437-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5437-106">ResourceId</span></span>
```
Start-AzJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5437-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="a5437-107">InputObject</span></span>
```
Start-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5437-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5437-108">DESCRIPTION</span></span>
<span data-ttu-id="a5437-109">Ruft eine temporäre Netzwerkzugriffsanforderung auf.</span><span class="sxs-lookup"><span data-stu-id="a5437-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="a5437-110">Die Anforderung wird anhand der konfigurierten JIT-Netzwerkzugriffsrichtlinie überprüft, und wenn dies zulässig ist, wird entsprechend der Anforderung des Benutzers eine Netzwerkverbindung geöffnet.</span><span class="sxs-lookup"><span data-stu-id="a5437-110">The request is validated against the configured JIT network access policy and if permitted, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="a5437-111">Die Anforderung wird zur späteren Überprüfung in der Richtlinie protokolliert und beendet, wenn die angegebene Dauer überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="a5437-111">The request will be logged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="a5437-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a5437-112">EXAMPLES</span></span>

### <span data-ttu-id="a5437-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a5437-113">Example 1</span></span>
```powershell
$MyResource = Get-AzResource -Id /subscriptions/xxxxxxx-xxxxx-xxxxx-xxxxxxx/resourceGroups/PolicyDemo/providers/Microsoft.Compute/virtualMachines/PolicyDemoVM1
$JitPolicy = (@{
        id    = $MyResource.ResourceId; 
        ports = (@{
                number                     = 22
                endTimeUtc                 = Get-Date (Get-Date -AsUTC).AddHours(1) -Format O
                allowedSourceAddressPrefix = @($MyPublicIP) 
            })
    })
$ActivationVM = @($JitPolicy)
Start-AzJitNetworkAccessPolicy -ResourceGroupName $($MyResource.ResourceGroupName) -Location $MyResource.Location -Name "default" -VirtualMachine $ActivationVM

```

<span data-ttu-id="a5437-114">Öffnet eine Netzwerkverbindung für 1 Stunde über Port 22 über meine öffentliche IP (nicht angezeigt).</span><span class="sxs-lookup"><span data-stu-id="a5437-114">Opens up a network connection for 1 hour over port 22 from my public IP (not shown).</span></span>

## <span data-ttu-id="a5437-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a5437-115">PARAMETERS</span></span>

### <span data-ttu-id="a5437-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5437-116">-DefaultProfile</span></span>
<span data-ttu-id="a5437-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a5437-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5437-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5437-118">-InputObject</span></span>
<span data-ttu-id="a5437-119">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="a5437-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5437-120">-Location</span><span class="sxs-lookup"><span data-stu-id="a5437-120">-Location</span></span>
<span data-ttu-id="a5437-121">Ort.</span><span class="sxs-lookup"><span data-stu-id="a5437-121">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5437-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a5437-122">-Name</span></span>
<span data-ttu-id="a5437-123">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="a5437-123">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5437-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5437-124">-ResourceGroupName</span></span>
<span data-ttu-id="a5437-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a5437-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5437-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5437-126">-ResourceId</span></span>
<span data-ttu-id="a5437-127">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a5437-127">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5437-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a5437-128">-VirtualMachine</span></span>
<span data-ttu-id="a5437-129">Automatische Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="a5437-129">Automatic Provisioning.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5437-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a5437-130">-Confirm</span></span>
<span data-ttu-id="a5437-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a5437-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5437-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5437-132">-WhatIf</span></span>
<span data-ttu-id="a5437-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a5437-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5437-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a5437-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5437-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5437-135">CommonParameters</span></span>
<span data-ttu-id="a5437-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5437-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5437-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5437-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5437-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a5437-138">INPUTS</span></span>

### <span data-ttu-id="a5437-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a5437-139">System.String</span></span>

### <span data-ttu-id="a5437-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span><span class="sxs-lookup"><span data-stu-id="a5437-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span></span>

## <span data-ttu-id="a5437-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a5437-141">OUTPUTS</span></span>

### <span data-ttu-id="a5437-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a5437-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="a5437-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a5437-143">NOTES</span></span>

## <span data-ttu-id="a5437-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a5437-144">RELATED LINKS</span></span>
