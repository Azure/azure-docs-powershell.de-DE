---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: 72e3cf48f112c5e9bb07a8f7eb57dfe3d4c9ee07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482050"
---
# <span data-ttu-id="7505b-101">Set-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7505b-101">Set-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="7505b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7505b-102">SYNOPSIS</span></span>
<span data-ttu-id="7505b-103">Aktualisiert die JIT-Netzwerkzugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="7505b-103">Updates JIT network access policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7505b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7505b-104">SYNTAX</span></span>

```
Set-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7505b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7505b-105">DESCRIPTION</span></span>
<span data-ttu-id="7505b-106">Aktualisiert die JIT-Netzwerkzugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="7505b-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="7505b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7505b-107">EXAMPLES</span></span>

### <span data-ttu-id="7505b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7505b-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="7505b-109">Aktualisiert eine JIT-Netzwerkzugriffsrichtlinie mit neuen VM-Regeln.</span><span class="sxs-lookup"><span data-stu-id="7505b-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="7505b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7505b-110">PARAMETERS</span></span>

### <span data-ttu-id="7505b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7505b-111">-DefaultProfile</span></span>
<span data-ttu-id="7505b-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7505b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7505b-113">-Art</span><span class="sxs-lookup"><span data-stu-id="7505b-113">-Kind</span></span>
<span data-ttu-id="7505b-114">Art.</span><span class="sxs-lookup"><span data-stu-id="7505b-114">Kind.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7505b-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="7505b-115">-Location</span></span>
<span data-ttu-id="7505b-116">Lage.</span><span class="sxs-lookup"><span data-stu-id="7505b-116">Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7505b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7505b-117">-Name</span></span>
<span data-ttu-id="7505b-118">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="7505b-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7505b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7505b-119">-ResourceGroupName</span></span>
<span data-ttu-id="7505b-120">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7505b-120">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7505b-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7505b-121">-VirtualMachine</span></span>
<span data-ttu-id="7505b-122">Virutal-Computer.</span><span class="sxs-lookup"><span data-stu-id="7505b-122">Virutal Machines.</span></span>

```yaml
Type: PSSecurityJitNetworkAccessPolicyVirtualMachine[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7505b-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7505b-123">-Confirm</span></span>
<span data-ttu-id="7505b-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7505b-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7505b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7505b-125">-WhatIf</span></span>
<span data-ttu-id="7505b-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7505b-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7505b-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7505b-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7505b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7505b-128">CommonParameters</span></span>
<span data-ttu-id="7505b-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7505b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7505b-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7505b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7505b-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7505b-131">INPUTS</span></span>

### <span data-ttu-id="7505b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7505b-132">System.String</span></span>
<span data-ttu-id="7505b-133">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicyVirtualMachine []</span><span class="sxs-lookup"><span data-stu-id="7505b-133">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyVirtualMachine[]</span></span>

## <span data-ttu-id="7505b-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7505b-134">OUTPUTS</span></span>

### <span data-ttu-id="7505b-135">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7505b-135">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="7505b-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="7505b-136">NOTES</span></span>

## <span data-ttu-id="7505b-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7505b-137">RELATED LINKS</span></span>
