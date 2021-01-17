---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Start-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 0efde69aec3b30c58aee8c42aeb1703215219c2e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471990"
---
# <span data-ttu-id="eb30a-101">Start-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eb30a-101">Start-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="eb30a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb30a-102">SYNOPSIS</span></span>
<span data-ttu-id="eb30a-103">Ruft eine temporäre Netzwerkzugriffsanforderung auf.</span><span class="sxs-lookup"><span data-stu-id="eb30a-103">Invokes a temporary network access request.</span></span>

## <span data-ttu-id="eb30a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb30a-104">SYNTAX</span></span>

### <span data-ttu-id="eb30a-105">ResourceGroupLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="eb30a-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb30a-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb30a-106">ResourceId</span></span>
```
Start-AzJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb30a-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="eb30a-107">InputObject</span></span>
```
Start-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb30a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eb30a-108">DESCRIPTION</span></span>
<span data-ttu-id="eb30a-109">Ruft eine temporäre Netzwerkzugriffsanforderung auf.</span><span class="sxs-lookup"><span data-stu-id="eb30a-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="eb30a-110">Die Anforderung wird anhand der konfigurierten Richtlinie für den Zugriff auf das JIT-Netzwerk überprüft und, sofern zulässig, entsprechend der Anforderung des Benutzers eine Netzwerkverbindung geöffnet.</span><span class="sxs-lookup"><span data-stu-id="eb30a-110">The request is validated against the configured JIT network access policy and if permitted, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="eb30a-111">Die Anforderung wird zur späteren Überprüfung in der Richtlinie protokolliert und beendet, wenn die angegebene Dauer überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="eb30a-111">The request will be logged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="eb30a-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="eb30a-112">EXAMPLES</span></span>

### <span data-ttu-id="eb30a-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="eb30a-113">Example 1</span></span>
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

<span data-ttu-id="eb30a-114">Öffnet eine Netzwerkverbindung für eine Stunde über Port 22 von meiner öffentlichen IP (nicht angezeigt).</span><span class="sxs-lookup"><span data-stu-id="eb30a-114">Opens up a network connection for 1 hour over port 22 from my public IP (not shown).</span></span>

## <span data-ttu-id="eb30a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb30a-115">PARAMETERS</span></span>

### <span data-ttu-id="eb30a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb30a-116">-DefaultProfile</span></span>
<span data-ttu-id="eb30a-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb30a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb30a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb30a-118">-InputObject</span></span>
<span data-ttu-id="eb30a-119">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="eb30a-119">Input Object.</span></span>

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

### <span data-ttu-id="eb30a-120">-Location</span><span class="sxs-lookup"><span data-stu-id="eb30a-120">-Location</span></span>
<span data-ttu-id="eb30a-121">"Ort" aus.</span><span class="sxs-lookup"><span data-stu-id="eb30a-121">Location.</span></span>

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

### <span data-ttu-id="eb30a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="eb30a-122">-Name</span></span>
<span data-ttu-id="eb30a-123">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="eb30a-123">Resource name.</span></span>

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

### <span data-ttu-id="eb30a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb30a-124">-ResourceGroupName</span></span>
<span data-ttu-id="eb30a-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="eb30a-125">Resource group name.</span></span>

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

### <span data-ttu-id="eb30a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb30a-126">-ResourceId</span></span>
<span data-ttu-id="eb30a-127">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="eb30a-127">Resource ID.</span></span>

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

### <span data-ttu-id="eb30a-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="eb30a-128">-VirtualMachine</span></span>
<span data-ttu-id="eb30a-129">Automatische Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="eb30a-129">Automatic Provisioning.</span></span>

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

### <span data-ttu-id="eb30a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb30a-130">-Confirm</span></span>
<span data-ttu-id="eb30a-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eb30a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb30a-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="eb30a-132">-WhatIf</span></span>
<span data-ttu-id="eb30a-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eb30a-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb30a-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eb30a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb30a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb30a-135">CommonParameters</span></span>
<span data-ttu-id="eb30a-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb30a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb30a-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb30a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb30a-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="eb30a-138">INPUTS</span></span>

### <span data-ttu-id="eb30a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="eb30a-139">System.String</span></span>

### <span data-ttu-id="eb30a-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span><span class="sxs-lookup"><span data-stu-id="eb30a-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span></span>

## <span data-ttu-id="eb30a-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="eb30a-141">OUTPUTS</span></span>

### <span data-ttu-id="eb30a-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eb30a-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="eb30a-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="eb30a-143">NOTES</span></span>

## <span data-ttu-id="eb30a-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="eb30a-144">RELATED LINKS</span></span>
