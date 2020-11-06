---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Start-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Start-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Start-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: 62dccdc3b55caa5d63036ed3298caa5a01514342
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501069"
---
# <span data-ttu-id="2e6a7-101">Start-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2e6a7-101">Start-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="2e6a7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2e6a7-102">SYNOPSIS</span></span>
<span data-ttu-id="2e6a7-103">Ruft eine temporäre Netzwerkzugriffsanforderung auf.</span><span class="sxs-lookup"><span data-stu-id="2e6a7-103">Invokes a temporary network access request.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e6a7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e6a7-104">SYNTAX</span></span>

### <span data-ttu-id="2e6a7-105">ResourceGroupLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="2e6a7-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e6a7-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e6a7-106">ResourceId</span></span>
```
Start-AzureRmJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e6a7-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="2e6a7-107">InputObject</span></span>
```
Start-AzureRmJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e6a7-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2e6a7-108">DESCRIPTION</span></span>
<span data-ttu-id="2e6a7-109">Ruft eine temporäre Netzwerkzugriffsanforderung auf.</span><span class="sxs-lookup"><span data-stu-id="2e6a7-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="2e6a7-110">Die Anforderung wird anhand der konfigurierten JIT-Netzwerkzugriffsrichtlinie überprüft, und wenn permittet, wird eine Netzwerkverbindung entsprechend der Anforderung des Benutzers geöffnet.</span><span class="sxs-lookup"><span data-stu-id="2e6a7-110">The request is validated against the configured JIT network access policy and if permittet, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="2e6a7-111">Die Anforderung wird in der Richtlinie für die spätere Überprüfung loged und wird beendet, wenn die angegebene Dauer überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="2e6a7-111">The request will be loged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="2e6a7-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2e6a7-112">EXAMPLES</span></span>

### <span data-ttu-id="2e6a7-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2e6a7-113">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -Kind "Basic" -VirtualMachine $vms

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.S
                    ecurity/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                    Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="2e6a7-114">Öffnet eine Netzwerkverbindung gemäß den angegebenen Verbindungs Anforderungsdaten.</span><span class="sxs-lookup"><span data-stu-id="2e6a7-114">Opens up a network connection according to the specified connection request data.</span></span>

## <span data-ttu-id="2e6a7-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e6a7-115">PARAMETERS</span></span>

### <span data-ttu-id="2e6a7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e6a7-116">-DefaultProfile</span></span>
<span data-ttu-id="2e6a7-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2e6a7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e6a7-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2e6a7-118">-InputObject</span></span>
<span data-ttu-id="2e6a7-119">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="2e6a7-119">Input Object.</span></span>

```yaml
Type: PSSecurityJitNetworkAccessPolicyInitiateInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6a7-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="2e6a7-120">-Location</span></span>
<span data-ttu-id="2e6a7-121">Lage.</span><span class="sxs-lookup"><span data-stu-id="2e6a7-121">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e6a7-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2e6a7-122">-Name</span></span>
<span data-ttu-id="2e6a7-123">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="2e6a7-123">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e6a7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e6a7-124">-ResourceGroupName</span></span>
<span data-ttu-id="2e6a7-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2e6a7-125">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e6a7-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2e6a7-126">-ResourceId</span></span>
<span data-ttu-id="2e6a7-127">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="2e6a7-127">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6a7-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2e6a7-128">-VirtualMachine</span></span>
<span data-ttu-id="2e6a7-129">Automatische Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="2e6a7-129">Automatic Provisioning.</span></span>

```yaml
Type: PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e6a7-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2e6a7-130">-Confirm</span></span>
<span data-ttu-id="2e6a7-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2e6a7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e6a7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e6a7-132">-WhatIf</span></span>
<span data-ttu-id="2e6a7-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2e6a7-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2e6a7-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2e6a7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e6a7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e6a7-135">CommonParameters</span></span>
<span data-ttu-id="2e6a7-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e6a7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e6a7-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e6a7-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e6a7-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2e6a7-138">INPUTS</span></span>

### <span data-ttu-id="2e6a7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2e6a7-139">System.String</span></span>
<span data-ttu-id="2e6a7-140">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine []</span><span class="sxs-lookup"><span data-stu-id="2e6a7-140">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]</span></span>

## <span data-ttu-id="2e6a7-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2e6a7-141">OUTPUTS</span></span>

### <span data-ttu-id="2e6a7-142">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2e6a7-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="2e6a7-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="2e6a7-143">NOTES</span></span>

## <span data-ttu-id="2e6a7-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2e6a7-144">RELATED LINKS</span></span>
