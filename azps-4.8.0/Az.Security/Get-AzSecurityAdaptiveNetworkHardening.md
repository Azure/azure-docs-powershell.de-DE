---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: cd28e66466239bf7fb0478774c1914180d2ede42
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94164999"
---
# <span data-ttu-id="549f3-101">Get-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="549f3-101">Get-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="549f3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="549f3-102">SYNOPSIS</span></span>
<span data-ttu-id="549f3-103">Ruft eine Liste der adaptiven Netzwerk Härtungs Ressourcen im Umfang einer erweiterten Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="549f3-103">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="549f3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="549f3-104">SYNTAX</span></span>

### <span data-ttu-id="549f3-105">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="549f3-105">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```
## <span data-ttu-id="549f3-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="549f3-106">DESCRIPTION</span></span>
<span data-ttu-id="549f3-107">Adaptive Netzwerk Härten werden automatisch vom Azure Security Center berechnet, verwenden Sie dieses Cmdlet, um eine Liste der adaptiven Netzwerk Härtungs Ressourcen im Umfang einer erweiterten Ressource abzurufen.</span><span class="sxs-lookup"><span data-stu-id="549f3-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="549f3-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="549f3-108">EXAMPLES</span></span>

### <span data-ttu-id="549f3-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="549f3-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```

<span data-ttu-id="549f3-110">Ruft eine Liste der adaptiven Netzwerk Härtungs Ressourcen im Umfang einer erweiterten Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="549f3-110">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

### <span data-ttu-id="549f3-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="549f3-111">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```
<span data-ttu-id="549f3-112">Abrufen einer einzelnen Ressource für adaptive Netzwerk Härten</span><span class="sxs-lookup"><span data-stu-id="549f3-112">Get  a single Adaptive Network Hardenings resource</span></span>

## <span data-ttu-id="549f3-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="549f3-113">PARAMETERS</span></span>

### <span data-ttu-id="549f3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="549f3-114">-DefaultProfile</span></span>
<span data-ttu-id="549f3-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="549f3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="549f3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="549f3-116">-ResourceGroupName</span></span>
<span data-ttu-id="549f3-117">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="549f3-117">Resource group name.</span></span>

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

### <span data-ttu-id="549f3-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="549f3-118">-ResourceName</span></span>
<span data-ttu-id="549f3-119">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="549f3-119">Resource name.</span></span>

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

### <span data-ttu-id="549f3-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="549f3-120">-ResourceNamespace</span></span>
<span data-ttu-id="549f3-121">Der Namespace der Ressource.</span><span class="sxs-lookup"><span data-stu-id="549f3-121">The Namespace of the resource.</span></span>

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

### <span data-ttu-id="549f3-122">-</span><span class="sxs-lookup"><span data-stu-id="549f3-122">-ResourceType</span></span>
<span data-ttu-id="549f3-123">Der Typ der Ressource.</span><span class="sxs-lookup"><span data-stu-id="549f3-123">The type of the resource.</span></span>

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

### <span data-ttu-id="549f3-124">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="549f3-124">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="549f3-125">Der Name der adaptiven Netzwerk Härtungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="549f3-125">The name of the Adaptive Network Hardening resource.</span></span>

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

### <span data-ttu-id="549f3-126">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="549f3-126">-SubscriptionId</span></span>
<span data-ttu-id="549f3-127">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="549f3-127">Azure subscription ID.</span></span>

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
### <span data-ttu-id="549f3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="549f3-128">CommonParameters</span></span>
<span data-ttu-id="549f3-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="549f3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="549f3-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="549f3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="549f3-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="549f3-131">INPUTS</span></span>

### <span data-ttu-id="549f3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="549f3-132">System.String</span></span>

## <span data-ttu-id="549f3-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="549f3-133">OUTPUTS</span></span>

### <span data-ttu-id="549f3-134">Microsoft. Azure. Commands. Security. Models. AdaptiveNetworkHardenings. PSSecurityAdaptiveNetworkHardenings</span><span class="sxs-lookup"><span data-stu-id="549f3-134">Microsoft.Azure.Commands.Security.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardenings</span></span>

## <span data-ttu-id="549f3-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="549f3-135">NOTES</span></span>

## <span data-ttu-id="549f3-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="549f3-136">RELATED LINKS</span></span>