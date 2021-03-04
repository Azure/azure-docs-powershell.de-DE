---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
ms.openlocfilehash: f79b3b4e8347c485230141416461c1f320d3d7b4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941968"
---
# <span data-ttu-id="e89e5-101">Get-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="e89e5-101">Get-AzCdnOriginGroup</span></span>

## <span data-ttu-id="e89e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e89e5-102">SYNOPSIS</span></span>
<span data-ttu-id="e89e5-103">Ruft eine CDN-Ursprungsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="e89e5-103">Gets a CDN origin group</span></span>

## <span data-ttu-id="e89e5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e89e5-104">SYNTAX</span></span>

### <span data-ttu-id="e89e5-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e89e5-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e89e5-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e89e5-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOriginGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e89e5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e89e5-107">DESCRIPTION</span></span>
<span data-ttu-id="e89e5-108">Das Get-AzCdnOriginGroup-Cmdlet ruft eine CDN-Ursprungsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="e89e5-108">The Get-AzCdnOriginGroup cmdlet retrieves a CDN origin group.</span></span>

## <span data-ttu-id="e89e5-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e89e5-109">EXAMPLES</span></span>

### <span data-ttu-id="e89e5-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e89e5-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="e89e5-111">Mit diesem Befehl wird die Ursprungsgruppe innerhalb des angegebenen Endpunkts empfangen.</span><span class="sxs-lookup"><span data-stu-id="e89e5-111">This command will get the origin group within the specified endpoint.</span></span>

## <span data-ttu-id="e89e5-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e89e5-112">PARAMETERS</span></span>

### <span data-ttu-id="e89e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e89e5-113">-DefaultProfile</span></span>
<span data-ttu-id="e89e5-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e89e5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e89e5-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e89e5-115">-EndpointName</span></span>
<span data-ttu-id="e89e5-116">Azure CDN-Endpunktname.</span><span class="sxs-lookup"><span data-stu-id="e89e5-116">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e89e5-117">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="e89e5-117">-OriginGroupName</span></span>
<span data-ttu-id="e89e5-118">Azure CDN-Ursprungsgruppenname.</span><span class="sxs-lookup"><span data-stu-id="e89e5-118">Azure CDN origin group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e89e5-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="e89e5-119">-ProfileName</span></span>
<span data-ttu-id="e89e5-120">Azure CDN-Profilname.</span><span class="sxs-lookup"><span data-stu-id="e89e5-120">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e89e5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e89e5-121">-ResourceGroupName</span></span>
<span data-ttu-id="e89e5-122">Die Ressourcengruppe des Azure CDN-Profils.</span><span class="sxs-lookup"><span data-stu-id="e89e5-122">The resource group of the Azure CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e89e5-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e89e5-123">-ResourceId</span></span>
<span data-ttu-id="e89e5-124">Ressourcen-ID für die Ursprungsgruppe</span><span class="sxs-lookup"><span data-stu-id="e89e5-124">Resource Id for the the origin group</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e89e5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e89e5-125">CommonParameters</span></span>
<span data-ttu-id="e89e5-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e89e5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e89e5-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e89e5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e89e5-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e89e5-128">INPUTS</span></span>

### <span data-ttu-id="e89e5-129">Keine</span><span class="sxs-lookup"><span data-stu-id="e89e5-129">None</span></span>

## <span data-ttu-id="e89e5-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e89e5-130">OUTPUTS</span></span>

### <span data-ttu-id="e89e5-131">System.Object</span><span class="sxs-lookup"><span data-stu-id="e89e5-131">System.Object</span></span>

## <span data-ttu-id="e89e5-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e89e5-132">NOTES</span></span>

## <span data-ttu-id="e89e5-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e89e5-133">RELATED LINKS</span></span>
