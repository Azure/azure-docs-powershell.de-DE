---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: 87b53048ede0a5b2484da18ccd0a2f6a531aa92b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946899"
---
# <span data-ttu-id="a381e-101">Get-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="a381e-101">Get-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="a381e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a381e-102">SYNOPSIS</span></span>
<span data-ttu-id="a381e-103">Ruft eine Liste der adaptiven Netzwerksicherheitsressourcen im Bereich einer erweiterten Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="a381e-103">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="a381e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a381e-104">SYNTAX</span></span>

### <span data-ttu-id="a381e-105">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="a381e-105">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```
## <span data-ttu-id="a381e-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a381e-106">DESCRIPTION</span></span>
<span data-ttu-id="a381e-107">Adaptive Netzwerkeinstellungen werden automatisch vom Azure Security Center berechnet. Verwenden Sie dieses Cmdlet, um eine Liste der Adaptive Network Hardenings-Ressourcen im Bereich einer erweiterten Ressource zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a381e-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="a381e-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a381e-108">EXAMPLES</span></span>

### <span data-ttu-id="a381e-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a381e-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```

<span data-ttu-id="a381e-110">Ruft eine Liste der adaptiven Netzwerksicherheitsressourcen im Bereich einer erweiterten Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="a381e-110">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

### <span data-ttu-id="a381e-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a381e-111">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```
<span data-ttu-id="a381e-112">Erhalten einer einzigen adaptiven Netzwerkinteignungsressource</span><span class="sxs-lookup"><span data-stu-id="a381e-112">Get  a single Adaptive Network Hardenings resource</span></span>

## <span data-ttu-id="a381e-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a381e-113">PARAMETERS</span></span>

### <span data-ttu-id="a381e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a381e-114">-DefaultProfile</span></span>
<span data-ttu-id="a381e-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a381e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a381e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a381e-116">-ResourceGroupName</span></span>
<span data-ttu-id="a381e-117">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a381e-117">Resource group name.</span></span>

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

### <span data-ttu-id="a381e-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a381e-118">-ResourceName</span></span>
<span data-ttu-id="a381e-119">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="a381e-119">Resource name.</span></span>

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

### <span data-ttu-id="a381e-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="a381e-120">-ResourceNamespace</span></span>
<span data-ttu-id="a381e-121">Der Namespace der Ressource.</span><span class="sxs-lookup"><span data-stu-id="a381e-121">The Namespace of the resource.</span></span>

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

### <span data-ttu-id="a381e-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="a381e-122">-ResourceType</span></span>
<span data-ttu-id="a381e-123">Der Typ der Ressource.</span><span class="sxs-lookup"><span data-stu-id="a381e-123">The type of the resource.</span></span>

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

### <span data-ttu-id="a381e-124">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="a381e-124">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="a381e-125">Der Name der Adaptive Network Hardening-Ressource.</span><span class="sxs-lookup"><span data-stu-id="a381e-125">The name of the Adaptive Network Hardening resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AdaptiveNetworkHardeningResourceName
Aliases:

Required: false
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a381e-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a381e-126">-SubscriptionId</span></span>
<span data-ttu-id="a381e-127">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="a381e-127">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: false
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="a381e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a381e-128">CommonParameters</span></span>
<span data-ttu-id="a381e-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a381e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a381e-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a381e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a381e-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a381e-131">INPUTS</span></span>

### <span data-ttu-id="a381e-132">System.String</span><span class="sxs-lookup"><span data-stu-id="a381e-132">System.String</span></span>

## <span data-ttu-id="a381e-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a381e-133">OUTPUTS</span></span>

### <span data-ttu-id="a381e-134">Microsoft.Azure.Commands.Security.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardenings</span><span class="sxs-lookup"><span data-stu-id="a381e-134">Microsoft.Azure.Commands.Security.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardenings</span></span>

## <span data-ttu-id="a381e-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a381e-135">NOTES</span></span>

## <span data-ttu-id="a381e-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a381e-136">RELATED LINKS</span></span>