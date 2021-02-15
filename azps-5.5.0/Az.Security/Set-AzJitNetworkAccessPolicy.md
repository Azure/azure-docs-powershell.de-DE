---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 83aca2353102b85fd138422f249464b59a8666ca
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174172"
---
# <span data-ttu-id="2ca8a-101">Set-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2ca8a-101">Set-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="2ca8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ca8a-102">SYNOPSIS</span></span>
<span data-ttu-id="2ca8a-103">Aktualisiert die Richtlinie für den JIT-Netzwerkzugriff.</span><span class="sxs-lookup"><span data-stu-id="2ca8a-103">Updates JIT network access policy.</span></span>

## <span data-ttu-id="2ca8a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ca8a-104">SYNTAX</span></span>

```
Set-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ca8a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2ca8a-105">DESCRIPTION</span></span>
<span data-ttu-id="2ca8a-106">Aktualisiert die Richtlinie für den JIT-Netzwerkzugriff.</span><span class="sxs-lookup"><span data-stu-id="2ca8a-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="2ca8a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2ca8a-107">EXAMPLES</span></span>

### <span data-ttu-id="2ca8a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2ca8a-108">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="2ca8a-109">Aktualisiert eine JiT-Netzwerkzugriffsrichtlinie mit neuen VM-Regeln.</span><span class="sxs-lookup"><span data-stu-id="2ca8a-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="2ca8a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ca8a-110">PARAMETERS</span></span>

### <span data-ttu-id="2ca8a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ca8a-111">-DefaultProfile</span></span>
<span data-ttu-id="2ca8a-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2ca8a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ca8a-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="2ca8a-113">-Kind</span></span>
<span data-ttu-id="2ca8a-114">Art der Jit-Netzwerkzugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="2ca8a-114">Jit Network Access Policy Kind.</span></span>

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

### <span data-ttu-id="2ca8a-115">-Location</span><span class="sxs-lookup"><span data-stu-id="2ca8a-115">-Location</span></span>
<span data-ttu-id="2ca8a-116">"Ort" aus.</span><span class="sxs-lookup"><span data-stu-id="2ca8a-116">Location.</span></span>

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

### <span data-ttu-id="2ca8a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2ca8a-117">-Name</span></span>
<span data-ttu-id="2ca8a-118">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="2ca8a-118">Resource name.</span></span>

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

### <span data-ttu-id="2ca8a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ca8a-119">-ResourceGroupName</span></span>
<span data-ttu-id="2ca8a-120">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="2ca8a-120">Resource group name.</span></span>

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

### <span data-ttu-id="2ca8a-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2ca8a-121">-VirtualMachine</span></span>
<span data-ttu-id="2ca8a-122">Virtuelle Computer.</span><span class="sxs-lookup"><span data-stu-id="2ca8a-122">Virtual Machines.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyVirtualMachine[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca8a-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ca8a-123">-Confirm</span></span>
<span data-ttu-id="2ca8a-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2ca8a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ca8a-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2ca8a-125">-WhatIf</span></span>
<span data-ttu-id="2ca8a-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2ca8a-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ca8a-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2ca8a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ca8a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ca8a-128">CommonParameters</span></span>
<span data-ttu-id="2ca8a-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ca8a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ca8a-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ca8a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ca8a-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2ca8a-131">INPUTS</span></span>

### <span data-ttu-id="2ca8a-132">Keine</span><span class="sxs-lookup"><span data-stu-id="2ca8a-132">None</span></span>

## <span data-ttu-id="2ca8a-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2ca8a-133">OUTPUTS</span></span>

### <span data-ttu-id="2ca8a-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2ca8a-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="2ca8a-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2ca8a-135">NOTES</span></span>

## <span data-ttu-id="2ca8a-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2ca8a-136">RELATED LINKS</span></span>
