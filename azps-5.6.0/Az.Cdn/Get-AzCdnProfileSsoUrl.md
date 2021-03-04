---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
ms.openlocfilehash: c458973a5cff000cab13c4602e1a73234314c0d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924264"
---
# <span data-ttu-id="36aa8-101">Get-AzCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="36aa8-101">Get-AzCdnProfileSsoUrl</span></span>

## <span data-ttu-id="36aa8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36aa8-102">SYNOPSIS</span></span>
<span data-ttu-id="36aa8-103">Ruft die einmalige Anmelde-URL eines CDN-Profils ab.</span><span class="sxs-lookup"><span data-stu-id="36aa8-103">Gets the single sign-on URL of a CDN profile.</span></span>

## <span data-ttu-id="36aa8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36aa8-104">SYNTAX</span></span>

### <span data-ttu-id="36aa8-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="36aa8-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36aa8-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="36aa8-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36aa8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36aa8-107">DESCRIPTION</span></span>
<span data-ttu-id="36aa8-108">Das **Cmdlet Get-AzCdnProfileSsoUrl** ruft die einmalige Anmelde-URL des Azure Content Delivery Network (CDN)-Profils ab.</span><span class="sxs-lookup"><span data-stu-id="36aa8-108">The **Get-AzCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="36aa8-109">Mit dieser URL können Benutzer eine Verbindung mit einem ergänzenden Portal herstellen und zusätzliche Features von CDN verwenden.</span><span class="sxs-lookup"><span data-stu-id="36aa8-109">This URL lets users connect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="36aa8-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="36aa8-110">EXAMPLES</span></span>

## <span data-ttu-id="36aa8-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="36aa8-111">PARAMETERS</span></span>

### <span data-ttu-id="36aa8-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="36aa8-112">-CdnProfile</span></span>
<span data-ttu-id="36aa8-113">Gibt das CDN-Profil an.</span><span class="sxs-lookup"><span data-stu-id="36aa8-113">Specifies the CDN profile.</span></span>

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

### <span data-ttu-id="36aa8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36aa8-114">-DefaultProfile</span></span>
<span data-ttu-id="36aa8-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="36aa8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36aa8-116">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="36aa8-116">-ProfileName</span></span>
<span data-ttu-id="36aa8-117">Gibt den Namen des CDN-Profils an.</span><span class="sxs-lookup"><span data-stu-id="36aa8-117">Specifies the name of the CDN profile.</span></span>

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

### <span data-ttu-id="36aa8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36aa8-118">-ResourceGroupName</span></span>
<span data-ttu-id="36aa8-119">Gibt den Namen des Ressourcengruppennamens an, zu dem das Profil gehört.</span><span class="sxs-lookup"><span data-stu-id="36aa8-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

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

### <span data-ttu-id="36aa8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36aa8-120">CommonParameters</span></span>
<span data-ttu-id="36aa8-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36aa8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36aa8-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36aa8-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36aa8-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="36aa8-123">INPUTS</span></span>

### <span data-ttu-id="36aa8-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="36aa8-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="36aa8-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="36aa8-125">OUTPUTS</span></span>

### <span data-ttu-id="36aa8-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span><span class="sxs-lookup"><span data-stu-id="36aa8-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span></span>

## <span data-ttu-id="36aa8-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="36aa8-127">NOTES</span></span>

## <span data-ttu-id="36aa8-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="36aa8-128">RELATED LINKS</span></span>

[<span data-ttu-id="36aa8-129">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="36aa8-129">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)


