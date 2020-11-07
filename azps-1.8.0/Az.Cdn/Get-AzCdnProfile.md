---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
ms.openlocfilehash: 110528c1e7a9891381ebc8182a1e0b45267d87b6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661619"
---
# <span data-ttu-id="cf161-101">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="cf161-101">Get-AzCdnProfile</span></span>

## <span data-ttu-id="cf161-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cf161-102">SYNOPSIS</span></span>
<span data-ttu-id="cf161-103">Ruft ein CDN-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="cf161-103">Gets a CDN profile.</span></span>

## <span data-ttu-id="cf161-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf161-104">SYNTAX</span></span>

```
Get-AzCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf161-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cf161-105">DESCRIPTION</span></span>
<span data-ttu-id="cf161-106">Das Cmdlet " **Get-AzCdnProfile** " Ruft ein Azure Content Delivery Network (CDN)-Profil und die zugehörigen Informationen ab.</span><span class="sxs-lookup"><span data-stu-id="cf161-106">The **Get-AzCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="cf161-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cf161-107">EXAMPLES</span></span>

## <span data-ttu-id="cf161-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf161-108">PARAMETERS</span></span>

### <span data-ttu-id="cf161-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf161-109">-DefaultProfile</span></span>
<span data-ttu-id="cf161-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="cf161-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf161-111">-Profilname</span><span class="sxs-lookup"><span data-stu-id="cf161-111">-ProfileName</span></span>
<span data-ttu-id="cf161-112">Gibt den Namen des Profils an.</span><span class="sxs-lookup"><span data-stu-id="cf161-112">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="cf161-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf161-113">-ResourceGroupName</span></span>
<span data-ttu-id="cf161-114">Gibt den Namen der Ressourcengruppe an, zu der das Profil gehört.</span><span class="sxs-lookup"><span data-stu-id="cf161-114">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="cf161-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf161-115">CommonParameters</span></span>
<span data-ttu-id="cf161-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf161-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf161-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf161-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf161-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cf161-118">INPUTS</span></span>

### <span data-ttu-id="cf161-119">System. String</span><span class="sxs-lookup"><span data-stu-id="cf161-119">System.String</span></span>

## <span data-ttu-id="cf161-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cf161-120">OUTPUTS</span></span>

### <span data-ttu-id="cf161-121">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="cf161-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="cf161-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="cf161-122">NOTES</span></span>

## <span data-ttu-id="cf161-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cf161-123">RELATED LINKS</span></span>

[<span data-ttu-id="cf161-124">Neu – AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="cf161-124">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="cf161-125">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="cf161-125">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="cf161-126">Satz-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="cf161-126">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


