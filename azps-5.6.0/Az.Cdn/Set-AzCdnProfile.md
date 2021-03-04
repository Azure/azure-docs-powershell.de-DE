---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/powershell/module/az.cdn/set-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
ms.openlocfilehash: 88e10d5f887d290139ee465217756c598bef0a3c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930363"
---
# <span data-ttu-id="8bb85-101">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="8bb85-101">Set-AzCdnProfile</span></span>

## <span data-ttu-id="8bb85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bb85-102">SYNOPSIS</span></span>
<span data-ttu-id="8bb85-103">Aktualisiert ein CDN-Profil.</span><span class="sxs-lookup"><span data-stu-id="8bb85-103">Updates a CDN profile.</span></span>

## <span data-ttu-id="8bb85-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8bb85-104">SYNTAX</span></span>

```
Set-AzCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8bb85-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8bb85-105">DESCRIPTION</span></span>
<span data-ttu-id="8bb85-106">Das **Cmdlet Set-AzCdnProfile** aktualisiert ein Azure Content Delivery Network (CDN)-Profil.</span><span class="sxs-lookup"><span data-stu-id="8bb85-106">The **Set-AzCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="8bb85-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8bb85-107">EXAMPLES</span></span>

## <span data-ttu-id="8bb85-108">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8bb85-108">PARAMETERS</span></span>

### <span data-ttu-id="8bb85-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="8bb85-109">-CdnProfile</span></span>
<span data-ttu-id="8bb85-110">Gibt das Profil an, das dieses Cmdlet aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="8bb85-110">Specifies the profile that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8bb85-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bb85-111">-DefaultProfile</span></span>
<span data-ttu-id="8bb85-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="8bb85-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8bb85-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8bb85-113">-Confirm</span></span>
<span data-ttu-id="8bb85-114">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8bb85-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bb85-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bb85-115">-WhatIf</span></span>
<span data-ttu-id="8bb85-116">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8bb85-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bb85-117">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8bb85-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bb85-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bb85-118">CommonParameters</span></span>
<span data-ttu-id="8bb85-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bb85-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bb85-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8bb85-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bb85-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8bb85-121">INPUTS</span></span>

### <span data-ttu-id="8bb85-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="8bb85-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="8bb85-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8bb85-123">OUTPUTS</span></span>

### <span data-ttu-id="8bb85-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="8bb85-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="8bb85-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8bb85-125">NOTES</span></span>

## <span data-ttu-id="8bb85-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8bb85-126">RELATED LINKS</span></span>

[<span data-ttu-id="8bb85-127">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="8bb85-127">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="8bb85-128">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="8bb85-128">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="8bb85-129">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="8bb85-129">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)


