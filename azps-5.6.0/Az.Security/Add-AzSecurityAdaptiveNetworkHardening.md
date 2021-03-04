---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Add-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: e0e634a4947953f65c3fd68c9cc3e40dfca17fd2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928880"
---
# <span data-ttu-id="91491-101">Add-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="91491-101">Add-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="91491-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91491-102">SYNOPSIS</span></span>
<span data-ttu-id="91491-103">Erzwingt die in der Anforderung aufgeführten Regeln für die NSG(n).</span><span class="sxs-lookup"><span data-stu-id="91491-103">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="91491-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91491-104">SYNTAX</span></span>

### <span data-ttu-id="91491-105">ResourceGroupLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="91491-105">ResourceGroupLevelResource (Default)</span></span>
```
Add-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91491-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="91491-106">DESCRIPTION</span></span>
<span data-ttu-id="91491-107">Adaptive Netzwerkeinstellungen werden automatisch vom Azure Security Center berechnet. Verwenden Sie dieses Cmdlet, um die in der Anforderung aufgeführten Regeln für die NSG(n) zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="91491-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to enforces the given rules on the NSG(s) listed in the request.</span></span>

## <span data-ttu-id="91491-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="91491-108">EXAMPLES</span></span>

### <span data-ttu-id="91491-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="91491-109">Example 1</span></span>
```powershell
PS C:\> $anh = Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines | Select -First 1
PS C:\> Add-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869 -Rules $anh.Properties.Rules -NetworkSecurityGroups $anh.Properties.EffectiveNetworkSecurityGroups[0].NetworkSecurityGroups

True
```
<span data-ttu-id="91491-110">Erzwingt die in der Anforderung aufgeführten Regeln für die NSG(n).</span><span class="sxs-lookup"><span data-stu-id="91491-110">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="91491-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="91491-111">PARAMETERS</span></span>

### <span data-ttu-id="91491-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91491-112">-DefaultProfile</span></span>
<span data-ttu-id="91491-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="91491-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91491-114">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="91491-114">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="91491-115">Der Name der Adaptive Network Hardening-Ressource.</span><span class="sxs-lookup"><span data-stu-id="91491-115">The name of the Adaptive Network Hardening resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AdaptiveNetworkHardeningResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91491-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91491-116">-ResourceGroupName</span></span>
<span data-ttu-id="91491-117">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="91491-117">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91491-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="91491-118">-ResourceName</span></span>
<span data-ttu-id="91491-119">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="91491-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91491-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="91491-120">-ResourceNamespace</span></span>
<span data-ttu-id="91491-121">Der Namespace der Ressource.</span><span class="sxs-lookup"><span data-stu-id="91491-121">The Namespace of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNamespace
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91491-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="91491-122">-ResourceType</span></span>
<span data-ttu-id="91491-123">Der Typ der Ressource.</span><span class="sxs-lookup"><span data-stu-id="91491-123">The type of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91491-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="91491-124">-SubscriptionId</span></span>
<span data-ttu-id="91491-125">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="91491-125">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91491-126">-Regeln</span><span class="sxs-lookup"><span data-stu-id="91491-126">-Rules</span></span>
<span data-ttu-id="91491-127">Die regeln, die erzwungen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="91491-127">The rules to enforce.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule
Parameter Sets: Rules
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91491-128">-NetworkSecurityGroups</span><span class="sxs-lookup"><span data-stu-id="91491-128">-NetworkSecurityGroups</span></span>
<span data-ttu-id="91491-129">Die Azure-Ressourcen-IDs der effektiven Netzwerksicherheitsgruppen, die mit den erstellten Sicherheitsregeln aus den Regeln für adaptive Netzwerksicherheit aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="91491-129">The Azure resource IDs of the effective network security groups that will be updated with the created security rules from the Adaptive Network Hardening rules.</span></span>

```yaml
Type: System.Collections.Generic.List<System.String>
Parameter Sets: NetworkSecurityGroups
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91491-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="91491-130">-PassThru</span></span>
<span data-ttu-id="91491-131">Zurückgeben eines Werts, der den Erfolg oder Fehler angibt</span><span class="sxs-lookup"><span data-stu-id="91491-131">Return a value indicating success or failure</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91491-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91491-132">CommonParameters</span></span>
<span data-ttu-id="91491-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91491-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91491-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91491-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91491-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="91491-135">INPUTS</span></span>

### <span data-ttu-id="91491-136">System.String</span><span class="sxs-lookup"><span data-stu-id="91491-136">System.String</span></span>

### <span data-ttu-id="91491-137">Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule</span><span class="sxs-lookup"><span data-stu-id="91491-137">Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule</span></span>

## <span data-ttu-id="91491-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="91491-138">OUTPUTS</span></span>

### <span data-ttu-id="91491-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="91491-139">System.Boolean</span></span>

## <span data-ttu-id="91491-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="91491-140">NOTES</span></span>

## <span data-ttu-id="91491-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="91491-141">RELATED LINKS</span></span>