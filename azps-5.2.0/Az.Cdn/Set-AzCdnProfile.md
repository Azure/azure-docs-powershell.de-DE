---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
ms.openlocfilehash: 341d46e5dd4ceefaf8baa76a71de462559115a5d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306395"
---
# <span data-ttu-id="38d92-101">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="38d92-101">Set-AzCdnProfile</span></span>

## <span data-ttu-id="38d92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38d92-102">SYNOPSIS</span></span>
<span data-ttu-id="38d92-103">Aktualisiert ein CDN-Profil.</span><span class="sxs-lookup"><span data-stu-id="38d92-103">Updates a CDN profile.</span></span>

## <span data-ttu-id="38d92-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38d92-104">SYNTAX</span></span>

```
Set-AzCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38d92-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38d92-105">DESCRIPTION</span></span>
<span data-ttu-id="38d92-106">Das **Set-AzCdnProfile-Cmdlet** aktualisiert ein Azure Content Delivery Network (CDN)-Profil.</span><span class="sxs-lookup"><span data-stu-id="38d92-106">The **Set-AzCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="38d92-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="38d92-107">EXAMPLES</span></span>

## <span data-ttu-id="38d92-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38d92-108">PARAMETERS</span></span>

### <span data-ttu-id="38d92-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="38d92-109">-CdnProfile</span></span>
<span data-ttu-id="38d92-110">Gibt das Profil an, das dieses Cmdlet aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="38d92-110">Specifies the profile that this cmdlet updates.</span></span>

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

### <span data-ttu-id="38d92-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38d92-111">-DefaultProfile</span></span>
<span data-ttu-id="38d92-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="38d92-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38d92-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38d92-113">-Confirm</span></span>
<span data-ttu-id="38d92-114">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="38d92-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38d92-115">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="38d92-115">-WhatIf</span></span>
<span data-ttu-id="38d92-116">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="38d92-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38d92-117">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="38d92-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38d92-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38d92-118">CommonParameters</span></span>
<span data-ttu-id="38d92-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38d92-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38d92-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38d92-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38d92-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="38d92-121">INPUTS</span></span>

### <span data-ttu-id="38d92-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="38d92-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="38d92-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="38d92-123">OUTPUTS</span></span>

### <span data-ttu-id="38d92-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="38d92-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="38d92-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="38d92-125">NOTES</span></span>

## <span data-ttu-id="38d92-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="38d92-126">RELATED LINKS</span></span>

[<span data-ttu-id="38d92-127">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="38d92-127">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="38d92-128">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="38d92-128">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="38d92-129">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="38d92-129">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)


