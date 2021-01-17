---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Start-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: b992f3a41278ba66c54eeefc0b548eef76b50980
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368036"
---
# <span data-ttu-id="bf5af-101">Start-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bf5af-101">Start-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="bf5af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf5af-102">SYNOPSIS</span></span>
<span data-ttu-id="bf5af-103">Ruft eine temporäre Netzwerkzugriffsanforderung auf.</span><span class="sxs-lookup"><span data-stu-id="bf5af-103">Invokes a temporary network access request.</span></span>

## <span data-ttu-id="bf5af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf5af-104">SYNTAX</span></span>

### <span data-ttu-id="bf5af-105">ResourceGroupLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="bf5af-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf5af-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf5af-106">ResourceId</span></span>
```
Start-AzJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf5af-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="bf5af-107">InputObject</span></span>
```
Start-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf5af-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bf5af-108">DESCRIPTION</span></span>
<span data-ttu-id="bf5af-109">Ruft eine temporäre Netzwerkzugriffsanforderung auf.</span><span class="sxs-lookup"><span data-stu-id="bf5af-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="bf5af-110">Die Anforderung wird anhand der konfigurierten Richtlinie für den Zugriff auf das JIT-Netzwerk überprüft und, sofern zulässig, entsprechend der Anforderung des Benutzers eine Netzwerkverbindung geöffnet.</span><span class="sxs-lookup"><span data-stu-id="bf5af-110">The request is validated against the configured JIT network access policy and if permitted, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="bf5af-111">Die Anforderung wird zur späteren Überprüfung in der Richtlinie protokolliert und beendet, wenn die angegebene Dauer überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="bf5af-111">The request will be logged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="bf5af-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bf5af-112">EXAMPLES</span></span>

### <span data-ttu-id="bf5af-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bf5af-113">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -Kind "Basic" -VirtualMachine $vms

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.S
                    ecurity/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                    Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="bf5af-114">Öffnet eine Netzwerkverbindung entsprechend den angegebenen Verbindungsanforderungsdaten.</span><span class="sxs-lookup"><span data-stu-id="bf5af-114">Opens up a network connection according to the specified connection request data.</span></span>

## <span data-ttu-id="bf5af-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf5af-115">PARAMETERS</span></span>

### <span data-ttu-id="bf5af-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf5af-116">-DefaultProfile</span></span>
<span data-ttu-id="bf5af-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bf5af-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf5af-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf5af-118">-InputObject</span></span>
<span data-ttu-id="bf5af-119">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="bf5af-119">Input Object.</span></span>

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

### <span data-ttu-id="bf5af-120">-Location</span><span class="sxs-lookup"><span data-stu-id="bf5af-120">-Location</span></span>
<span data-ttu-id="bf5af-121">"Ort" aus.</span><span class="sxs-lookup"><span data-stu-id="bf5af-121">Location.</span></span>

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

### <span data-ttu-id="bf5af-122">-Name</span><span class="sxs-lookup"><span data-stu-id="bf5af-122">-Name</span></span>
<span data-ttu-id="bf5af-123">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="bf5af-123">Resource name.</span></span>

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

### <span data-ttu-id="bf5af-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf5af-124">-ResourceGroupName</span></span>
<span data-ttu-id="bf5af-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="bf5af-125">Resource group name.</span></span>

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

### <span data-ttu-id="bf5af-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf5af-126">-ResourceId</span></span>
<span data-ttu-id="bf5af-127">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="bf5af-127">Resource ID.</span></span>

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

### <span data-ttu-id="bf5af-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="bf5af-128">-VirtualMachine</span></span>
<span data-ttu-id="bf5af-129">Automatische Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="bf5af-129">Automatic Provisioning.</span></span>

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

### <span data-ttu-id="bf5af-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bf5af-130">-Confirm</span></span>
<span data-ttu-id="bf5af-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bf5af-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf5af-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="bf5af-132">-WhatIf</span></span>
<span data-ttu-id="bf5af-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bf5af-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bf5af-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bf5af-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf5af-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf5af-135">CommonParameters</span></span>
<span data-ttu-id="bf5af-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf5af-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf5af-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf5af-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf5af-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bf5af-138">INPUTS</span></span>

### <span data-ttu-id="bf5af-139">System.String</span><span class="sxs-lookup"><span data-stu-id="bf5af-139">System.String</span></span>

### <span data-ttu-id="bf5af-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span><span class="sxs-lookup"><span data-stu-id="bf5af-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span></span>

## <span data-ttu-id="bf5af-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bf5af-141">OUTPUTS</span></span>

### <span data-ttu-id="bf5af-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bf5af-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="bf5af-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bf5af-143">NOTES</span></span>

## <span data-ttu-id="bf5af-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bf5af-144">RELATED LINKS</span></span>
