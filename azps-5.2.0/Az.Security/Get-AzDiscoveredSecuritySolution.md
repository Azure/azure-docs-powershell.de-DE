---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzDiscoveredSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
ms.openlocfilehash: 1fbe9e790966a92c38ba79b56221e5e6083b649c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296495"
---
# <span data-ttu-id="5bebe-101">Get-AzDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="5bebe-101">Get-AzDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="5bebe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bebe-102">SYNOPSIS</span></span>
<span data-ttu-id="5bebe-103">Ruft Sicherheitslösungen ab, die vom Azure Security Center ermittelt wurden</span><span class="sxs-lookup"><span data-stu-id="5bebe-103">Gets security solutions that were discovered by Azure Security Center</span></span>

## <span data-ttu-id="5bebe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5bebe-104">SYNTAX</span></span>

### <span data-ttu-id="5bebe-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="5bebe-105">SubscriptionScope (Default)</span></span>
```
Get-AzDiscoveredSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bebe-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="5bebe-106">ResourceGroupLevelResource</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bebe-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5bebe-107">ResourceId</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5bebe-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5bebe-108">DESCRIPTION</span></span>
<span data-ttu-id="5bebe-109">Sicherheitslösungen werden automatisch vom Azure Security Center ermittelt. Verwenden Sie dieses Cmdlet, um die ermittelten Sicherheitslösungen</span><span class="sxs-lookup"><span data-stu-id="5bebe-109">Security solutions are automatically discovered by Azure Security Center, use this cmdlet to view the discovered security solutions</span></span>

## <span data-ttu-id="5bebe-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5bebe-110">EXAMPLES</span></span>

### <span data-ttu-id="5bebe-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5bebe-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDiscoveredSecuritySolution
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="5bebe-112">Holen Sie sich alle erkannten Sicherheitslösungen im Abonnement</span><span class="sxs-lookup"><span data-stu-id="5bebe-112">Get all the discovered security solutions in the subscription</span></span>

### <span data-ttu-id="5bebe-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5bebe-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDiscoveredSecuritySolution -ResourceGroupName "myService1" -Location "centralus" -Name "ContosoWAF2"
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="5bebe-114">Erhalten einer bestimmten ermittelten Sicherheitslösung</span><span class="sxs-lookup"><span data-stu-id="5bebe-114">Get a specific discovered security solution</span></span>

## <span data-ttu-id="5bebe-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bebe-115">PARAMETERS</span></span>

### <span data-ttu-id="5bebe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bebe-116">-DefaultProfile</span></span>
<span data-ttu-id="5bebe-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5bebe-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bebe-118">-Location</span><span class="sxs-lookup"><span data-stu-id="5bebe-118">-Location</span></span>
<span data-ttu-id="5bebe-119">"Ort" aus.</span><span class="sxs-lookup"><span data-stu-id="5bebe-119">Location.</span></span>

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

### <span data-ttu-id="5bebe-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5bebe-120">-Name</span></span>
<span data-ttu-id="5bebe-121">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="5bebe-121">Resource name.</span></span>

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

### <span data-ttu-id="5bebe-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bebe-122">-ResourceGroupName</span></span>
<span data-ttu-id="5bebe-123">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="5bebe-123">Resource group name.</span></span>

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

### <span data-ttu-id="5bebe-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5bebe-124">-ResourceId</span></span>
<span data-ttu-id="5bebe-125">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="5bebe-125">Resource ID.</span></span>

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

### <span data-ttu-id="5bebe-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bebe-126">CommonParameters</span></span>
<span data-ttu-id="5bebe-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bebe-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bebe-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5bebe-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bebe-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5bebe-129">INPUTS</span></span>

### <span data-ttu-id="5bebe-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5bebe-130">System.String</span></span>

## <span data-ttu-id="5bebe-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5bebe-131">OUTPUTS</span></span>

### <span data-ttu-id="5bebe-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="5bebe-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="5bebe-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5bebe-133">NOTES</span></span>

## <span data-ttu-id="5bebe-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5bebe-134">RELATED LINKS</span></span>
