---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
ms.openlocfilehash: 98c41f8e9e1592cf0405f42701fc19f3badd9553
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364578"
---
# <span data-ttu-id="bfa3d-101">Get-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="bfa3d-101">Get-AzCdnOriginGroup</span></span>

## <span data-ttu-id="bfa3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfa3d-102">SYNOPSIS</span></span>
<span data-ttu-id="bfa3d-103">Ruft eine CDN-Origin-Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="bfa3d-103">Gets a CDN origin group</span></span>

## <span data-ttu-id="bfa3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bfa3d-104">SYNTAX</span></span>

### <span data-ttu-id="bfa3d-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bfa3d-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfa3d-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfa3d-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOriginGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfa3d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bfa3d-107">DESCRIPTION</span></span>
<span data-ttu-id="bfa3d-108">Das Get-AzCdnOriginGroup cmdlet ruft eine CDN-Origin-Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="bfa3d-108">The Get-AzCdnOriginGroup cmdlet retrieves a CDN origin group.</span></span>

## <span data-ttu-id="bfa3d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bfa3d-109">EXAMPLES</span></span>

### <span data-ttu-id="bfa3d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bfa3d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="bfa3d-111">Mit diesem Befehl wird die Origin-Gruppe innerhalb des angegebenen Endpunkts empfangen.</span><span class="sxs-lookup"><span data-stu-id="bfa3d-111">This command will get the origin group within the specified endpoint.</span></span>

## <span data-ttu-id="bfa3d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfa3d-112">PARAMETERS</span></span>

### <span data-ttu-id="bfa3d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfa3d-113">-DefaultProfile</span></span>
<span data-ttu-id="bfa3d-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bfa3d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfa3d-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="bfa3d-115">-EndpointName</span></span>
<span data-ttu-id="bfa3d-116">Name des Azure CDN-Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="bfa3d-116">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="bfa3d-117">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="bfa3d-117">-OriginGroupName</span></span>
<span data-ttu-id="bfa3d-118">Name der Azure CDN-Origin-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="bfa3d-118">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="bfa3d-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="bfa3d-119">-ProfileName</span></span>
<span data-ttu-id="bfa3d-120">Azure CDN-Profilname.</span><span class="sxs-lookup"><span data-stu-id="bfa3d-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="bfa3d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfa3d-121">-ResourceGroupName</span></span>
<span data-ttu-id="bfa3d-122">Die Ressourcengruppe des Azure CDN-Profils.</span><span class="sxs-lookup"><span data-stu-id="bfa3d-122">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="bfa3d-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bfa3d-123">-ResourceId</span></span>
<span data-ttu-id="bfa3d-124">Ressourcen-ID für die Origin-Gruppe</span><span class="sxs-lookup"><span data-stu-id="bfa3d-124">Resource Id for the the origin group</span></span>

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

### <span data-ttu-id="bfa3d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfa3d-125">CommonParameters</span></span>
<span data-ttu-id="bfa3d-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfa3d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfa3d-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bfa3d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfa3d-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bfa3d-128">INPUTS</span></span>

### <span data-ttu-id="bfa3d-129">Keine</span><span class="sxs-lookup"><span data-stu-id="bfa3d-129">None</span></span>

## <span data-ttu-id="bfa3d-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bfa3d-130">OUTPUTS</span></span>

### <span data-ttu-id="bfa3d-131">System.Object</span><span class="sxs-lookup"><span data-stu-id="bfa3d-131">System.Object</span></span>

## <span data-ttu-id="bfa3d-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bfa3d-132">NOTES</span></span>

## <span data-ttu-id="bfa3d-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bfa3d-133">RELATED LINKS</span></span>
