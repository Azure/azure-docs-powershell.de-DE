---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
ms.openlocfilehash: f53b02d54164b6cc4e3aad8cf07357e7f2e156e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503029"
---
# <span data-ttu-id="a9dfa-101">Get-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="a9dfa-101">Get-AzureRmCdnProfile</span></span>

## <span data-ttu-id="a9dfa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9dfa-102">SYNOPSIS</span></span>
<span data-ttu-id="a9dfa-103">Ruft ein CDN-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="a9dfa-103">Gets a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9dfa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9dfa-104">SYNTAX</span></span>

```
Get-AzureRmCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9dfa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9dfa-105">DESCRIPTION</span></span>
<span data-ttu-id="a9dfa-106">Das Cmdlet " **Get-AzureRMCdnProfile** " Ruft ein Azure Content Delivery Network (CDN)-Profil und die zugehörigen Informationen ab.</span><span class="sxs-lookup"><span data-stu-id="a9dfa-106">The **Get-AzureRMCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="a9dfa-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9dfa-107">EXAMPLES</span></span>

## <span data-ttu-id="a9dfa-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9dfa-108">PARAMETERS</span></span>

### <span data-ttu-id="a9dfa-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9dfa-109">-DefaultProfile</span></span>
<span data-ttu-id="a9dfa-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a9dfa-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9dfa-111">-Profilname</span><span class="sxs-lookup"><span data-stu-id="a9dfa-111">-ProfileName</span></span>
<span data-ttu-id="a9dfa-112">Gibt den Namen des Profils an.</span><span class="sxs-lookup"><span data-stu-id="a9dfa-112">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="a9dfa-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9dfa-113">-ResourceGroupName</span></span>
<span data-ttu-id="a9dfa-114">Gibt den Namen der Ressourcengruppe an, zu der das Profil gehört.</span><span class="sxs-lookup"><span data-stu-id="a9dfa-114">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="a9dfa-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9dfa-115">CommonParameters</span></span>
<span data-ttu-id="a9dfa-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9dfa-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9dfa-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9dfa-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9dfa-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9dfa-118">INPUTS</span></span>

### <span data-ttu-id="a9dfa-119">System. String</span><span class="sxs-lookup"><span data-stu-id="a9dfa-119">System.String</span></span>

## <span data-ttu-id="a9dfa-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9dfa-120">OUTPUTS</span></span>

### <span data-ttu-id="a9dfa-121">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="a9dfa-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="a9dfa-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9dfa-122">NOTES</span></span>

## <span data-ttu-id="a9dfa-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9dfa-123">RELATED LINKS</span></span>

[<span data-ttu-id="a9dfa-124">Neu – AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="a9dfa-124">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="a9dfa-125">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="a9dfa-125">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="a9dfa-126">Satz-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="a9dfa-126">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


