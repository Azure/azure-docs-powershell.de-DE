---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
ms.openlocfilehash: 98c41f8e9e1592cf0405f42701fc19f3badd9553
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171396"
---
# <span data-ttu-id="61153-101">Get-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="61153-101">Get-AzCdnOriginGroup</span></span>

## <span data-ttu-id="61153-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61153-102">SYNOPSIS</span></span>
<span data-ttu-id="61153-103">Ruft eine CDN-Origin-Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="61153-103">Gets a CDN origin group</span></span>

## <span data-ttu-id="61153-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61153-104">SYNTAX</span></span>

### <span data-ttu-id="61153-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="61153-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61153-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61153-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOriginGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61153-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="61153-107">DESCRIPTION</span></span>
<span data-ttu-id="61153-108">Das Get-AzCdnOriginGroup cmdlet ruft eine CDN-Origin-Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="61153-108">The Get-AzCdnOriginGroup cmdlet retrieves a CDN origin group.</span></span>

## <span data-ttu-id="61153-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="61153-109">EXAMPLES</span></span>

### <span data-ttu-id="61153-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="61153-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="61153-111">Mit diesem Befehl wird die Origin-Gruppe innerhalb des angegebenen Endpunkts empfangen.</span><span class="sxs-lookup"><span data-stu-id="61153-111">This command will get the origin group within the specified endpoint.</span></span>

## <span data-ttu-id="61153-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61153-112">PARAMETERS</span></span>

### <span data-ttu-id="61153-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61153-113">-DefaultProfile</span></span>
<span data-ttu-id="61153-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61153-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61153-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="61153-115">-EndpointName</span></span>
<span data-ttu-id="61153-116">Name des Azure CDN-Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="61153-116">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="61153-117">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="61153-117">-OriginGroupName</span></span>
<span data-ttu-id="61153-118">Name der Azure CDN-Origin-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="61153-118">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="61153-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="61153-119">-ProfileName</span></span>
<span data-ttu-id="61153-120">Azure CDN-Profilname.</span><span class="sxs-lookup"><span data-stu-id="61153-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="61153-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61153-121">-ResourceGroupName</span></span>
<span data-ttu-id="61153-122">Die Ressourcengruppe des Azure CDN-Profils.</span><span class="sxs-lookup"><span data-stu-id="61153-122">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="61153-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61153-123">-ResourceId</span></span>
<span data-ttu-id="61153-124">Ressourcen-ID für die Gruppe "Origin"</span><span class="sxs-lookup"><span data-stu-id="61153-124">Resource Id for the the origin group</span></span>

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

### <span data-ttu-id="61153-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61153-125">CommonParameters</span></span>
<span data-ttu-id="61153-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61153-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61153-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61153-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61153-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="61153-128">INPUTS</span></span>

### <span data-ttu-id="61153-129">Keine</span><span class="sxs-lookup"><span data-stu-id="61153-129">None</span></span>

## <span data-ttu-id="61153-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="61153-130">OUTPUTS</span></span>

### <span data-ttu-id="61153-131">System.Object</span><span class="sxs-lookup"><span data-stu-id="61153-131">System.Object</span></span>

## <span data-ttu-id="61153-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="61153-132">NOTES</span></span>

## <span data-ttu-id="61153-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="61153-133">RELATED LINKS</span></span>
