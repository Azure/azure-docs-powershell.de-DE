---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: a40fba16bd7d361544ca10867d2c575965447c12
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996284"
---
# <span data-ttu-id="e1eda-101">Set-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e1eda-101">Set-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="e1eda-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e1eda-102">SYNOPSIS</span></span>
<span data-ttu-id="e1eda-103">Aktualisiert die JIT-Netzwerkzugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="e1eda-103">Updates JIT network access policy.</span></span>

## <span data-ttu-id="e1eda-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1eda-104">SYNTAX</span></span>

```
Set-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1eda-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1eda-105">DESCRIPTION</span></span>
<span data-ttu-id="e1eda-106">Aktualisiert die JIT-Netzwerkzugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="e1eda-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="e1eda-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e1eda-107">EXAMPLES</span></span>

### <span data-ttu-id="e1eda-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e1eda-108">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="e1eda-109">Aktualisiert eine JIT-Netzwerkzugriffsrichtlinie mit neuen VM-Regeln.</span><span class="sxs-lookup"><span data-stu-id="e1eda-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="e1eda-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1eda-110">PARAMETERS</span></span>

### <span data-ttu-id="e1eda-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1eda-111">-DefaultProfile</span></span>
<span data-ttu-id="e1eda-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e1eda-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1eda-113">-Art</span><span class="sxs-lookup"><span data-stu-id="e1eda-113">-Kind</span></span>
<span data-ttu-id="e1eda-114">Art.</span><span class="sxs-lookup"><span data-stu-id="e1eda-114">Kind.</span></span>

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

### <span data-ttu-id="e1eda-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="e1eda-115">-Location</span></span>
<span data-ttu-id="e1eda-116">Lage.</span><span class="sxs-lookup"><span data-stu-id="e1eda-116">Location.</span></span>

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

### <span data-ttu-id="e1eda-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e1eda-117">-Name</span></span>
<span data-ttu-id="e1eda-118">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="e1eda-118">Resource name.</span></span>

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

### <span data-ttu-id="e1eda-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1eda-119">-ResourceGroupName</span></span>
<span data-ttu-id="e1eda-120">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e1eda-120">Resource group name.</span></span>

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

### <span data-ttu-id="e1eda-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e1eda-121">-VirtualMachine</span></span>
<span data-ttu-id="e1eda-122">Virtual Machines.</span><span class="sxs-lookup"><span data-stu-id="e1eda-122">Virtual Machines.</span></span>

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

### <span data-ttu-id="e1eda-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e1eda-123">-Confirm</span></span>
<span data-ttu-id="e1eda-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e1eda-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1eda-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1eda-125">-WhatIf</span></span>
<span data-ttu-id="e1eda-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e1eda-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1eda-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e1eda-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1eda-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1eda-128">CommonParameters</span></span>
<span data-ttu-id="e1eda-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1eda-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1eda-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1eda-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1eda-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e1eda-131">INPUTS</span></span>

### <span data-ttu-id="e1eda-132">Keine</span><span class="sxs-lookup"><span data-stu-id="e1eda-132">None</span></span>

## <span data-ttu-id="e1eda-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e1eda-133">OUTPUTS</span></span>

### <span data-ttu-id="e1eda-134">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e1eda-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="e1eda-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="e1eda-135">NOTES</span></span>

## <span data-ttu-id="e1eda-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e1eda-136">RELATED LINKS</span></span>
