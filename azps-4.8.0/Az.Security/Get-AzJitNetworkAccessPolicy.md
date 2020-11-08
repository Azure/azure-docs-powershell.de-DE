---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: c385ca902764d6bf9afa3808d718c2ceb5d1357c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174190"
---
# <span data-ttu-id="d069f-101">Get-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d069f-101">Get-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="d069f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d069f-102">SYNOPSIS</span></span>
<span data-ttu-id="d069f-103">Ruft die JIT-Netzwerkzugriffsrichtlinien ab.</span><span class="sxs-lookup"><span data-stu-id="d069f-103">Gets the JIT network access policies</span></span>

## <span data-ttu-id="d069f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d069f-104">SYNTAX</span></span>

### <span data-ttu-id="d069f-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="d069f-105">SubscriptionScope (Default)</span></span>
```
Get-AzJitNetworkAccessPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d069f-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="d069f-106">ResourceGroupScope</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d069f-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="d069f-107">ResourceGroupLevelResource</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d069f-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d069f-108">ResourceId</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d069f-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d069f-109">DESCRIPTION</span></span>
<span data-ttu-id="d069f-110">Just-in-time (JIT)-Netzwerkzugriffsrichtlinien können Sie eine Richtlinie definieren, mit der einfache Benutzer eine temporäre Netzwerkverbindung mit einem virtuellen Computer erstellen können.</span><span class="sxs-lookup"><span data-stu-id="d069f-110">Just In Time (JIT) network access policies let you define a policy the will allow simple users to create a temporary network connection to a VM.</span></span>
<span data-ttu-id="d069f-111">Die Richtlinie definiert, welche Ports, Protokoll-und Quell-IP-Adressen eine Verbindung mit einem virtuellen Computer anfordern können, und die maximale Dauer, bevor die Verbindung automatisch geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="d069f-111">The policy defines what ports, protocol and source IP addresses can request a connection to a VM and the max duration before the connection will be closed automatically.</span></span>
<span data-ttu-id="d069f-112">In der Richtlinie können Sie auch die Verbindungsanforderung sehen, die mit dieser Richtlinie vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="d069f-112">In the policy you can also see the connection request that were made with this policy.</span></span> 

## <span data-ttu-id="d069f-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d069f-113">EXAMPLES</span></span>

### <span data-ttu-id="d069f-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d069f-114">Example 1</span></span>
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

<span data-ttu-id="d069f-115">Abrufen aller JIT-Netzwerkzugriffsrichtlinien für ein Abonnement</span><span class="sxs-lookup"><span data-stu-id="d069f-115">Get all the JIT network access polices on a subscription</span></span>

### <span data-ttu-id="d069f-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d069f-116">Example 2</span></span>
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

<span data-ttu-id="d069f-117">Abrufen aller JIT-Netzwerkzugriffsrichtlinien für die Ressourcengruppe "myService1"</span><span class="sxs-lookup"><span data-stu-id="d069f-117">Get all the JIT network access polices on the "myService1" resource group</span></span>

### <span data-ttu-id="d069f-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d069f-118">Example 3</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="d069f-119">Ruft eine bestimmte JIT-Netzwerkzugriffsrichtlinie ab</span><span class="sxs-lookup"><span data-stu-id="d069f-119">Gets a specific JIT network access policy</span></span>

## <span data-ttu-id="d069f-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="d069f-120">PARAMETERS</span></span>

### <span data-ttu-id="d069f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d069f-121">-DefaultProfile</span></span>
<span data-ttu-id="d069f-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d069f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d069f-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="d069f-123">-Location</span></span>
<span data-ttu-id="d069f-124">Lage.</span><span class="sxs-lookup"><span data-stu-id="d069f-124">Location.</span></span>

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

### <span data-ttu-id="d069f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d069f-125">-Name</span></span>
<span data-ttu-id="d069f-126">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="d069f-126">Resource name.</span></span>

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

### <span data-ttu-id="d069f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d069f-127">-ResourceGroupName</span></span>
<span data-ttu-id="d069f-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d069f-128">Resource group name.</span></span>

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

### <span data-ttu-id="d069f-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d069f-129">-ResourceId</span></span>
<span data-ttu-id="d069f-130">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="d069f-130">Resource ID.</span></span>

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

### <span data-ttu-id="d069f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d069f-131">CommonParameters</span></span>
<span data-ttu-id="d069f-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d069f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d069f-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d069f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d069f-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d069f-134">INPUTS</span></span>

### <span data-ttu-id="d069f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d069f-135">System.String</span></span>

## <span data-ttu-id="d069f-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d069f-136">OUTPUTS</span></span>

### <span data-ttu-id="d069f-137">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d069f-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="d069f-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="d069f-138">NOTES</span></span>

## <span data-ttu-id="d069f-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d069f-139">RELATED LINKS</span></span>
