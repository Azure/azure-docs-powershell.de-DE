---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: db6520ae16d114fdcad85daf3e0742589fa0fbbe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162409"
---
# <span data-ttu-id="a07a2-101">Get-AzCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="a07a2-101">Get-AzCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="a07a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a07a2-102">SYNOPSIS</span></span>
<span data-ttu-id="a07a2-103">Ruft die unterstützten Optimierungstypen für ein CDN-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="a07a2-103">Gets the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="a07a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a07a2-104">SYNTAX</span></span>

### <span data-ttu-id="a07a2-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a07a2-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a07a2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a07a2-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a07a2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a07a2-107">DESCRIPTION</span></span>
<span data-ttu-id="a07a2-108">Das **Cmdlet "Get-AzCdnProfileSupportedOptimizationType"** ruft die unterstützten Optimierungstypen für das aktuelle Profil ab.</span><span class="sxs-lookup"><span data-stu-id="a07a2-108">The **Get-AzCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="a07a2-109">Ein Benutzer kann einen Endpunkt mit einem Optimierungstyp aus den aufgelisteten Werten erstellen.</span><span class="sxs-lookup"><span data-stu-id="a07a2-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="a07a2-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a07a2-110">EXAMPLES</span></span>

### <span data-ttu-id="a07a2-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a07a2-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="a07a2-112">Holen Sie sich die unterstützten Optimierungstypen für ein CDN-Profil.</span><span class="sxs-lookup"><span data-stu-id="a07a2-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="a07a2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a07a2-113">PARAMETERS</span></span>

### <span data-ttu-id="a07a2-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="a07a2-114">-CdnProfile</span></span>
<span data-ttu-id="a07a2-115">Das Azure CDN-Profilobjekt.</span><span class="sxs-lookup"><span data-stu-id="a07a2-115">The Azure CDN profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a07a2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a07a2-116">-DefaultProfile</span></span>
<span data-ttu-id="a07a2-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a07a2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a07a2-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="a07a2-118">-ProfileName</span></span>
<span data-ttu-id="a07a2-119">Der Name des Profils.</span><span class="sxs-lookup"><span data-stu-id="a07a2-119">The name of the profile.</span></span>

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

### <span data-ttu-id="a07a2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a07a2-120">-ResourceGroupName</span></span>
<span data-ttu-id="a07a2-121">Die Ressourcengruppe, zu der das Profil gehört.</span><span class="sxs-lookup"><span data-stu-id="a07a2-121">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="a07a2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a07a2-122">CommonParameters</span></span>
<span data-ttu-id="a07a2-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a07a2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a07a2-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a07a2-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a07a2-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a07a2-125">INPUTS</span></span>

### <span data-ttu-id="a07a2-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="a07a2-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="a07a2-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a07a2-127">OUTPUTS</span></span>

### <span data-ttu-id="a07a2-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span><span class="sxs-lookup"><span data-stu-id="a07a2-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="a07a2-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a07a2-129">NOTES</span></span>

## <span data-ttu-id="a07a2-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a07a2-130">RELATED LINKS</span></span>
