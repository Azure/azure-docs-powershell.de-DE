---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
ms.openlocfilehash: e82e455d603ca4fd5d577e18337c93a2368fbcf5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945316"
---
# <span data-ttu-id="b3230-101">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="b3230-101">Get-AzCdnProfile</span></span>

## <span data-ttu-id="b3230-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3230-102">SYNOPSIS</span></span>
<span data-ttu-id="b3230-103">Ruft ein CDN-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="b3230-103">Gets a CDN profile.</span></span>

## <span data-ttu-id="b3230-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3230-104">SYNTAX</span></span>

```
Get-AzCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3230-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b3230-105">DESCRIPTION</span></span>
<span data-ttu-id="b3230-106">Das **Get-AzCdnProfile-Cmdlet** ruft ein Azure Content Delivery Network (CDN)-Profil und die zugehörigen Informationen ab.</span><span class="sxs-lookup"><span data-stu-id="b3230-106">The **Get-AzCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="b3230-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b3230-107">EXAMPLES</span></span>

## <span data-ttu-id="b3230-108">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b3230-108">PARAMETERS</span></span>

### <span data-ttu-id="b3230-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3230-109">-DefaultProfile</span></span>
<span data-ttu-id="b3230-110">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="b3230-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3230-111">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="b3230-111">-ProfileName</span></span>
<span data-ttu-id="b3230-112">Gibt den Namen des Profils an.</span><span class="sxs-lookup"><span data-stu-id="b3230-112">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="b3230-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3230-113">-ResourceGroupName</span></span>
<span data-ttu-id="b3230-114">Gibt den Namen der Ressourcengruppe an, zu der das Profil gehört.</span><span class="sxs-lookup"><span data-stu-id="b3230-114">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="b3230-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3230-115">CommonParameters</span></span>
<span data-ttu-id="b3230-116">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3230-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3230-117">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3230-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3230-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b3230-118">INPUTS</span></span>

### <span data-ttu-id="b3230-119">System.String</span><span class="sxs-lookup"><span data-stu-id="b3230-119">System.String</span></span>

## <span data-ttu-id="b3230-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b3230-120">OUTPUTS</span></span>

### <span data-ttu-id="b3230-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="b3230-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="b3230-122">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b3230-122">NOTES</span></span>

## <span data-ttu-id="b3230-123">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b3230-123">RELATED LINKS</span></span>

[<span data-ttu-id="b3230-124">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="b3230-124">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="b3230-125">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="b3230-125">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="b3230-126">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="b3230-126">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


