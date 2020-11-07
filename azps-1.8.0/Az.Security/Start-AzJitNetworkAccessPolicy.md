---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Start-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: cc25282105b8a45e75984ffbdc272743dd88220e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659425"
---
# <span data-ttu-id="1bd49-101">Start-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1bd49-101">Start-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="1bd49-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1bd49-102">SYNOPSIS</span></span>
<span data-ttu-id="1bd49-103">Ruft eine temporäre Netzwerkzugriffsanforderung auf.</span><span class="sxs-lookup"><span data-stu-id="1bd49-103">Invokes a temporary network access request.</span></span>

## <span data-ttu-id="1bd49-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bd49-104">SYNTAX</span></span>

### <span data-ttu-id="1bd49-105">ResourceGroupLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="1bd49-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bd49-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1bd49-106">ResourceId</span></span>
```
Start-AzJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bd49-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="1bd49-107">InputObject</span></span>
```
Start-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bd49-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1bd49-108">DESCRIPTION</span></span>
<span data-ttu-id="1bd49-109">Ruft eine temporäre Netzwerkzugriffsanforderung auf.</span><span class="sxs-lookup"><span data-stu-id="1bd49-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="1bd49-110">Die Anforderung wird anhand der konfigurierten JIT-Netzwerkzugriffsrichtlinie überprüft, und wenn permittet, wird eine Netzwerkverbindung entsprechend der Anforderung des Benutzers geöffnet.</span><span class="sxs-lookup"><span data-stu-id="1bd49-110">The request is validated against the configured JIT network access policy and if permittet, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="1bd49-111">Die Anforderung wird in der Richtlinie für die spätere Überprüfung loged und wird beendet, wenn die angegebene Dauer überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="1bd49-111">The request will be loged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="1bd49-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1bd49-112">EXAMPLES</span></span>

### <span data-ttu-id="1bd49-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1bd49-113">Example 1</span></span>
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

<span data-ttu-id="1bd49-114">Öffnet eine Netzwerkverbindung gemäß den angegebenen Verbindungs Anforderungsdaten.</span><span class="sxs-lookup"><span data-stu-id="1bd49-114">Opens up a network connection according to the specified connection request data.</span></span>

## <span data-ttu-id="1bd49-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="1bd49-115">PARAMETERS</span></span>

### <span data-ttu-id="1bd49-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bd49-116">-DefaultProfile</span></span>
<span data-ttu-id="1bd49-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1bd49-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bd49-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1bd49-118">-InputObject</span></span>
<span data-ttu-id="1bd49-119">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="1bd49-119">Input Object.</span></span>

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

### <span data-ttu-id="1bd49-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="1bd49-120">-Location</span></span>
<span data-ttu-id="1bd49-121">Lage.</span><span class="sxs-lookup"><span data-stu-id="1bd49-121">Location.</span></span>

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

### <span data-ttu-id="1bd49-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1bd49-122">-Name</span></span>
<span data-ttu-id="1bd49-123">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="1bd49-123">Resource name.</span></span>

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

### <span data-ttu-id="1bd49-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bd49-124">-ResourceGroupName</span></span>
<span data-ttu-id="1bd49-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1bd49-125">Resource group name.</span></span>

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

### <span data-ttu-id="1bd49-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1bd49-126">-ResourceId</span></span>
<span data-ttu-id="1bd49-127">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="1bd49-127">Resource ID.</span></span>

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

### <span data-ttu-id="1bd49-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1bd49-128">-VirtualMachine</span></span>
<span data-ttu-id="1bd49-129">Automatische Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="1bd49-129">Automatic Provisioning.</span></span>

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

### <span data-ttu-id="1bd49-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1bd49-130">-Confirm</span></span>
<span data-ttu-id="1bd49-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1bd49-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bd49-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bd49-132">-WhatIf</span></span>
<span data-ttu-id="1bd49-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1bd49-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1bd49-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1bd49-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bd49-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bd49-135">CommonParameters</span></span>
<span data-ttu-id="1bd49-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bd49-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bd49-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bd49-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bd49-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1bd49-138">INPUTS</span></span>

### <span data-ttu-id="1bd49-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1bd49-139">System.String</span></span>

### <span data-ttu-id="1bd49-140">Microsoft. Azure. Commands. Security. Cmdlets. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicyInitiateInputObject</span><span class="sxs-lookup"><span data-stu-id="1bd49-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span></span>

## <span data-ttu-id="1bd49-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1bd49-141">OUTPUTS</span></span>

### <span data-ttu-id="1bd49-142">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1bd49-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="1bd49-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="1bd49-143">NOTES</span></span>

## <span data-ttu-id="1bd49-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1bd49-144">RELATED LINKS</span></span>
