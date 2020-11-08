---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Add-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: daccafa4d0100d333d2e686e8b03bb21d8a38736
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165608"
---
# <span data-ttu-id="a3d9c-101">Add-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="a3d9c-101">Add-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="a3d9c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a3d9c-102">SYNOPSIS</span></span>
<span data-ttu-id="a3d9c-103">Erzwingt die angegebenen Regeln für die in der Anforderung aufgelisteten NSG (en).</span><span class="sxs-lookup"><span data-stu-id="a3d9c-103">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="a3d9c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3d9c-104">SYNTAX</span></span>

### <span data-ttu-id="a3d9c-105">ResourceGroupLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="a3d9c-105">ResourceGroupLevelResource (Default)</span></span>
```
Add-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3d9c-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a3d9c-106">DESCRIPTION</span></span>
<span data-ttu-id="a3d9c-107">Adaptive Netzwerk Härten werden automatisch vom Azure Security Center berechnet, verwenden Sie dieses Cmdlet, um die angegebenen Regeln für die in der Anforderung aufgelisteten NSG (s) zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="a3d9c-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to enforces the given rules on the NSG(s) listed in the request.</span></span>

## <span data-ttu-id="a3d9c-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a3d9c-108">EXAMPLES</span></span>

### <span data-ttu-id="a3d9c-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a3d9c-109">Example 1</span></span>
```powershell
PS C:\> $anh = Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines | Select -First 1
PS C:\> Add-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869 -Rules $anh.Properties.Rules -NetworkSecurityGroups $anh.Properties.EffectiveNetworkSecurityGroups[0].NetworkSecurityGroups

True
```
<span data-ttu-id="a3d9c-110">Erzwingt die angegebenen Regeln für die in der Anforderung aufgelisteten NSG (en).</span><span class="sxs-lookup"><span data-stu-id="a3d9c-110">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="a3d9c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3d9c-111">PARAMETERS</span></span>

### <span data-ttu-id="a3d9c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3d9c-112">-DefaultProfile</span></span>
<span data-ttu-id="a3d9c-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a3d9c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3d9c-114">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="a3d9c-114">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="a3d9c-115">Der Name der adaptiven Netzwerk Härtungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="a3d9c-115">The name of the Adaptive Network Hardening resource.</span></span>

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

### <span data-ttu-id="a3d9c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3d9c-116">-ResourceGroupName</span></span>
<span data-ttu-id="a3d9c-117">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a3d9c-117">Resource group name.</span></span>

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

### <span data-ttu-id="a3d9c-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a3d9c-118">-ResourceName</span></span>
<span data-ttu-id="a3d9c-119">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="a3d9c-119">Resource name.</span></span>

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

### <span data-ttu-id="a3d9c-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="a3d9c-120">-ResourceNamespace</span></span>
<span data-ttu-id="a3d9c-121">Der Namespace der Ressource.</span><span class="sxs-lookup"><span data-stu-id="a3d9c-121">The Namespace of the resource.</span></span>

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

### <span data-ttu-id="a3d9c-122">-</span><span class="sxs-lookup"><span data-stu-id="a3d9c-122">-ResourceType</span></span>
<span data-ttu-id="a3d9c-123">Der Typ der Ressource.</span><span class="sxs-lookup"><span data-stu-id="a3d9c-123">The type of the resource.</span></span>

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

### <span data-ttu-id="a3d9c-124">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="a3d9c-124">-SubscriptionId</span></span>
<span data-ttu-id="a3d9c-125">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="a3d9c-125">Azure subscription ID.</span></span>

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

### <span data-ttu-id="a3d9c-126">-Regeln</span><span class="sxs-lookup"><span data-stu-id="a3d9c-126">-Rules</span></span>
<span data-ttu-id="a3d9c-127">Die zu erzwingenden Regeln.</span><span class="sxs-lookup"><span data-stu-id="a3d9c-127">The rules to enforce.</span></span>

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

### <span data-ttu-id="a3d9c-128">-NetworkSecurityGroups</span><span class="sxs-lookup"><span data-stu-id="a3d9c-128">-NetworkSecurityGroups</span></span>
<span data-ttu-id="a3d9c-129">Die Azure-Ressourcen-IDs der effektiven Netzwerk Sicherheitsgruppen, die mit den erstellten Sicherheitsregeln aus den Regeln für adaptive Netzwerk Härtung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a3d9c-129">The Azure resource IDs of the effective network security groups that will be updated with the created security rules from the Adaptive Network Hardening rules.</span></span>

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

### <span data-ttu-id="a3d9c-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3d9c-130">-PassThru</span></span>
<span data-ttu-id="a3d9c-131">Zurückgeben eines Werts, der auf Erfolg oder Fehler hinweist</span><span class="sxs-lookup"><span data-stu-id="a3d9c-131">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="a3d9c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3d9c-132">CommonParameters</span></span>
<span data-ttu-id="a3d9c-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3d9c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3d9c-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3d9c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3d9c-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a3d9c-135">INPUTS</span></span>

### <span data-ttu-id="a3d9c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a3d9c-136">System.String</span></span>

### <span data-ttu-id="a3d9c-137">Microsoft. Azure. Commands. SecurityCenter. Models. AdaptiveNetworkHardenings. PSSecurityAdaptiveNetworkHardeningsRule</span><span class="sxs-lookup"><span data-stu-id="a3d9c-137">Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule</span></span>

## <span data-ttu-id="a3d9c-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a3d9c-138">OUTPUTS</span></span>

### <span data-ttu-id="a3d9c-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a3d9c-139">System.Boolean</span></span>

## <span data-ttu-id="a3d9c-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="a3d9c-140">NOTES</span></span>

## <span data-ttu-id="a3d9c-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a3d9c-141">RELATED LINKS</span></span>