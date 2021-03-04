---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 980b680130ca319612bbbf28e787ebd99c4bf8bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928875"
---
# <span data-ttu-id="99025-101">Get-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="99025-101">Get-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="99025-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99025-102">SYNOPSIS</span></span>
<span data-ttu-id="99025-103">Ruft die JIT-Netzwerkzugriffsrichtlinien ab.</span><span class="sxs-lookup"><span data-stu-id="99025-103">Gets the JIT network access policies</span></span>

## <span data-ttu-id="99025-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99025-104">SYNTAX</span></span>

### <span data-ttu-id="99025-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="99025-105">SubscriptionScope (Default)</span></span>
```
Get-AzJitNetworkAccessPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99025-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="99025-106">ResourceGroupScope</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="99025-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="99025-107">ResourceGroupLevelResource</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99025-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="99025-108">ResourceId</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="99025-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="99025-109">DESCRIPTION</span></span>
<span data-ttu-id="99025-110">Mit just In Time (JIT)-Netzwerkzugriffsrichtlinien können Sie eine Richtlinie definieren, die es einfachen Benutzern ermöglicht, eine temporäre Netzwerkverbindung mit einer VM zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="99025-110">Just In Time (JIT) network access policies let you define a policy the will allow simple users to create a temporary network connection to a VM.</span></span>
<span data-ttu-id="99025-111">Die Richtlinie definiert, welche Ports, Protokoll- und Quell-IP-Adressen eine Verbindung mit einer VM anfordern können, und die maximale Dauer, bevor die Verbindung automatisch geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="99025-111">The policy defines what ports, protocol and source IP addresses can request a connection to a VM and the max duration before the connection will be closed automatically.</span></span>
<span data-ttu-id="99025-112">In der Richtlinie sehen Sie auch die Verbindungsanforderung, die mit dieser Richtlinie gestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="99025-112">In the policy you can also see the connection request that were made with this policy.</span></span> 

## <span data-ttu-id="99025-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="99025-113">EXAMPLES</span></span>

### <span data-ttu-id="99025-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="99025-114">Example 1</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/northeurope/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="99025-115">Alle Zugriffspolizistinnen und -polizistinnen für das JIT-Netzwerk in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="99025-115">Get all the JIT network access polices on a subscription</span></span>

### <span data-ttu-id="99025-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="99025-116">Example 2</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy -ResourceGroupName "myService1"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/northeurope/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="99025-117">Alle Zugriffspolisen für das JIT-Netzwerk in der Ressourcengruppe "myService1"</span><span class="sxs-lookup"><span data-stu-id="99025-117">Get all the JIT network access polices on the "myService1" resource group</span></span>

### <span data-ttu-id="99025-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="99025-118">Example 3</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="99025-119">Ruft eine bestimmte JIT-Netzwerkzugriffsrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="99025-119">Gets a specific JIT network access policy</span></span>

## <span data-ttu-id="99025-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="99025-120">PARAMETERS</span></span>

### <span data-ttu-id="99025-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99025-121">-DefaultProfile</span></span>
<span data-ttu-id="99025-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="99025-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99025-123">-Location</span><span class="sxs-lookup"><span data-stu-id="99025-123">-Location</span></span>
<span data-ttu-id="99025-124">Ort.</span><span class="sxs-lookup"><span data-stu-id="99025-124">Location.</span></span>

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

### <span data-ttu-id="99025-125">-Name</span><span class="sxs-lookup"><span data-stu-id="99025-125">-Name</span></span>
<span data-ttu-id="99025-126">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="99025-126">Resource name.</span></span>

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

### <span data-ttu-id="99025-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99025-127">-ResourceGroupName</span></span>
<span data-ttu-id="99025-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="99025-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99025-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99025-129">-ResourceId</span></span>
<span data-ttu-id="99025-130">Die Ressourcen-ID der Jit-Netzwerkzugriffsrichtlinienressource.</span><span class="sxs-lookup"><span data-stu-id="99025-130">The resource id of the jit Network Access Policy resource.</span></span>

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

### <span data-ttu-id="99025-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99025-131">CommonParameters</span></span>
<span data-ttu-id="99025-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99025-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99025-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99025-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99025-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="99025-134">INPUTS</span></span>

### <span data-ttu-id="99025-135">System.String</span><span class="sxs-lookup"><span data-stu-id="99025-135">System.String</span></span>

## <span data-ttu-id="99025-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="99025-136">OUTPUTS</span></span>

### <span data-ttu-id="99025-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="99025-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="99025-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="99025-138">NOTES</span></span>

## <span data-ttu-id="99025-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="99025-139">RELATED LINKS</span></span>
