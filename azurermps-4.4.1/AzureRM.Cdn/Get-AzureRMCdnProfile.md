---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
ms.openlocfilehash: 726e84e1fe43e90ebf16241a017dadb2af5584b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503250"
---
# <span data-ttu-id="eed6c-101">Get-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="eed6c-101">Get-AzureRmCdnProfile</span></span>

## <span data-ttu-id="eed6c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eed6c-102">SYNOPSIS</span></span>
<span data-ttu-id="eed6c-103">Ruft ein CDN-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="eed6c-103">Gets a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eed6c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eed6c-104">SYNTAX</span></span>

```
Get-AzureRmCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eed6c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eed6c-105">DESCRIPTION</span></span>
<span data-ttu-id="eed6c-106">Das Cmdlet " **Get-AzureRMCdnProfile** " Ruft ein Azure Content Delivery Network (CDN)-Profil und die zugehörigen Informationen ab.</span><span class="sxs-lookup"><span data-stu-id="eed6c-106">The **Get-AzureRMCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="eed6c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eed6c-107">EXAMPLES</span></span>

## <span data-ttu-id="eed6c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="eed6c-108">PARAMETERS</span></span>

### <span data-ttu-id="eed6c-109">-Profilname</span><span class="sxs-lookup"><span data-stu-id="eed6c-109">-ProfileName</span></span>
<span data-ttu-id="eed6c-110">Gibt den Namen des Profils an.</span><span class="sxs-lookup"><span data-stu-id="eed6c-110">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="eed6c-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eed6c-111">-ResourceGroupName</span></span>
<span data-ttu-id="eed6c-112">Gibt den Namen der Ressourcengruppe an, zu der das Profil gehört.</span><span class="sxs-lookup"><span data-stu-id="eed6c-112">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="eed6c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eed6c-113">-DefaultProfile</span></span>
<span data-ttu-id="eed6c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eed6c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eed6c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eed6c-115">CommonParameters</span></span>
<span data-ttu-id="eed6c-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eed6c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eed6c-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eed6c-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eed6c-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eed6c-118">INPUTS</span></span>

## <span data-ttu-id="eed6c-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eed6c-119">OUTPUTS</span></span>

###  
<span data-ttu-id="eed6c-120">Dieses Cmdlet gibt ein Profilobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="eed6c-120">This cmdlet returns a profile object.</span></span>

## <span data-ttu-id="eed6c-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="eed6c-121">NOTES</span></span>

## <span data-ttu-id="eed6c-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eed6c-122">RELATED LINKS</span></span>

[<span data-ttu-id="eed6c-123">Neu – AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="eed6c-123">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="eed6c-124">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="eed6c-124">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="eed6c-125">Satz-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="eed6c-125">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


