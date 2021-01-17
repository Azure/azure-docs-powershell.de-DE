---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
ms.openlocfilehash: 1af77b3fec469b9bb60d5531c89534d5de11b4f0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303232"
---
# <span data-ttu-id="21185-101">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="21185-101">Get-AzCdnProfile</span></span>

## <span data-ttu-id="21185-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21185-102">SYNOPSIS</span></span>
<span data-ttu-id="21185-103">Ruft ein CDN-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="21185-103">Gets a CDN profile.</span></span>

## <span data-ttu-id="21185-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21185-104">SYNTAX</span></span>

```
Get-AzCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21185-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="21185-105">DESCRIPTION</span></span>
<span data-ttu-id="21185-106">Das **Get-AzCdnProfile-Cmdlet** ruft ein Azure Content Delivery Network (CDN)-Profil und die zugehörigen Informationen ab.</span><span class="sxs-lookup"><span data-stu-id="21185-106">The **Get-AzCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="21185-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="21185-107">EXAMPLES</span></span>

## <span data-ttu-id="21185-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21185-108">PARAMETERS</span></span>

### <span data-ttu-id="21185-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21185-109">-DefaultProfile</span></span>
<span data-ttu-id="21185-110">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="21185-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21185-111">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="21185-111">-ProfileName</span></span>
<span data-ttu-id="21185-112">Gibt den Namen des Profils an.</span><span class="sxs-lookup"><span data-stu-id="21185-112">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21185-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21185-113">-ResourceGroupName</span></span>
<span data-ttu-id="21185-114">Gibt den Namen der Ressourcengruppe an, zu der das Profil gehört.</span><span class="sxs-lookup"><span data-stu-id="21185-114">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21185-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21185-115">CommonParameters</span></span>
<span data-ttu-id="21185-116">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21185-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21185-117">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21185-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21185-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="21185-118">INPUTS</span></span>

### <span data-ttu-id="21185-119">System.String</span><span class="sxs-lookup"><span data-stu-id="21185-119">System.String</span></span>

## <span data-ttu-id="21185-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="21185-120">OUTPUTS</span></span>

### <span data-ttu-id="21185-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="21185-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="21185-122">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="21185-122">NOTES</span></span>

## <span data-ttu-id="21185-123">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="21185-123">RELATED LINKS</span></span>

[<span data-ttu-id="21185-124">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="21185-124">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="21185-125">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="21185-125">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="21185-126">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="21185-126">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


