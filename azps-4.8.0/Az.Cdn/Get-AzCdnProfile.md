---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
ms.openlocfilehash: 1af77b3fec469b9bb60d5531c89534d5de11b4f0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008368"
---
# <span data-ttu-id="328b7-101">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="328b7-101">Get-AzCdnProfile</span></span>

## <span data-ttu-id="328b7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="328b7-102">SYNOPSIS</span></span>
<span data-ttu-id="328b7-103">Ruft ein CDN-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="328b7-103">Gets a CDN profile.</span></span>

## <span data-ttu-id="328b7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="328b7-104">SYNTAX</span></span>

```
Get-AzCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="328b7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="328b7-105">DESCRIPTION</span></span>
<span data-ttu-id="328b7-106">Das Cmdlet " **Get-AzCdnProfile** " Ruft ein Azure Content Delivery Network (CDN)-Profil und die zugehörigen Informationen ab.</span><span class="sxs-lookup"><span data-stu-id="328b7-106">The **Get-AzCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="328b7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="328b7-107">EXAMPLES</span></span>

## <span data-ttu-id="328b7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="328b7-108">PARAMETERS</span></span>

### <span data-ttu-id="328b7-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="328b7-109">-DefaultProfile</span></span>
<span data-ttu-id="328b7-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="328b7-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="328b7-111">-Profilname</span><span class="sxs-lookup"><span data-stu-id="328b7-111">-ProfileName</span></span>
<span data-ttu-id="328b7-112">Gibt den Namen des Profils an.</span><span class="sxs-lookup"><span data-stu-id="328b7-112">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="328b7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="328b7-113">-ResourceGroupName</span></span>
<span data-ttu-id="328b7-114">Gibt den Namen der Ressourcengruppe an, zu der das Profil gehört.</span><span class="sxs-lookup"><span data-stu-id="328b7-114">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="328b7-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="328b7-115">CommonParameters</span></span>
<span data-ttu-id="328b7-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="328b7-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="328b7-117">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="328b7-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="328b7-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="328b7-118">INPUTS</span></span>

### <span data-ttu-id="328b7-119">System. String</span><span class="sxs-lookup"><span data-stu-id="328b7-119">System.String</span></span>

## <span data-ttu-id="328b7-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="328b7-120">OUTPUTS</span></span>

### <span data-ttu-id="328b7-121">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="328b7-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="328b7-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="328b7-122">NOTES</span></span>

## <span data-ttu-id="328b7-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="328b7-123">RELATED LINKS</span></span>

[<span data-ttu-id="328b7-124">Neu – AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="328b7-124">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="328b7-125">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="328b7-125">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="328b7-126">Satz-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="328b7-126">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


