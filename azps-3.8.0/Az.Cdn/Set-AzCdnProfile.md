---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
ms.openlocfilehash: 341d46e5dd4ceefaf8baa76a71de462559115a5d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003034"
---
# <span data-ttu-id="03d99-101">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="03d99-101">Set-AzCdnProfile</span></span>

## <span data-ttu-id="03d99-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="03d99-102">SYNOPSIS</span></span>
<span data-ttu-id="03d99-103">Aktualisiert ein CDN-Profil.</span><span class="sxs-lookup"><span data-stu-id="03d99-103">Updates a CDN profile.</span></span>

## <span data-ttu-id="03d99-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="03d99-104">SYNTAX</span></span>

```
Set-AzCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03d99-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="03d99-105">DESCRIPTION</span></span>
<span data-ttu-id="03d99-106">Das Cmdlet " **Satz-AzCdnProfile** " aktualisiert ein Azure Content Delivery Network (CDN)-Profil.</span><span class="sxs-lookup"><span data-stu-id="03d99-106">The **Set-AzCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="03d99-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="03d99-107">EXAMPLES</span></span>

## <span data-ttu-id="03d99-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="03d99-108">PARAMETERS</span></span>

### <span data-ttu-id="03d99-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="03d99-109">-CdnProfile</span></span>
<span data-ttu-id="03d99-110">Gibt das Profil an, das vom Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="03d99-110">Specifies the profile that this cmdlet updates.</span></span>

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

### <span data-ttu-id="03d99-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03d99-111">-DefaultProfile</span></span>
<span data-ttu-id="03d99-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="03d99-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03d99-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="03d99-113">-Confirm</span></span>
<span data-ttu-id="03d99-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="03d99-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03d99-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03d99-115">-WhatIf</span></span>
<span data-ttu-id="03d99-116">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="03d99-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03d99-117">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="03d99-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03d99-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03d99-118">CommonParameters</span></span>
<span data-ttu-id="03d99-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03d99-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03d99-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03d99-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03d99-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="03d99-121">INPUTS</span></span>

### <span data-ttu-id="03d99-122">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="03d99-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="03d99-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="03d99-123">OUTPUTS</span></span>

### <span data-ttu-id="03d99-124">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="03d99-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="03d99-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="03d99-125">NOTES</span></span>

## <span data-ttu-id="03d99-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="03d99-126">RELATED LINKS</span></span>

[<span data-ttu-id="03d99-127">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="03d99-127">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="03d99-128">Neu – AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="03d99-128">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="03d99-129">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="03d99-129">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)


