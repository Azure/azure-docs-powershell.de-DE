---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
ms.openlocfilehash: a345b69fdc6695706f61a85c2926392c9f522aeb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478698"
---
# <span data-ttu-id="7cc6f-101">Get-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="7cc6f-101">Get-AzureRmCdnProfile</span></span>

## <span data-ttu-id="7cc6f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7cc6f-102">SYNOPSIS</span></span>
<span data-ttu-id="7cc6f-103">Ruft ein CDN-Profil ab.</span><span class="sxs-lookup"><span data-stu-id="7cc6f-103">Gets a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cc6f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7cc6f-104">SYNTAX</span></span>

```
Get-AzureRmCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cc6f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7cc6f-105">DESCRIPTION</span></span>
<span data-ttu-id="7cc6f-106">Das Cmdlet " **Get-AzureRMCdnProfile** " Ruft ein Azure Content Delivery Network (CDN)-Profil und die zugehörigen Informationen ab.</span><span class="sxs-lookup"><span data-stu-id="7cc6f-106">The **Get-AzureRMCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="7cc6f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7cc6f-107">EXAMPLES</span></span>

## <span data-ttu-id="7cc6f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7cc6f-108">PARAMETERS</span></span>

### <span data-ttu-id="7cc6f-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cc6f-109">-DefaultProfile</span></span>
<span data-ttu-id="7cc6f-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7cc6f-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cc6f-111">-Profilname</span><span class="sxs-lookup"><span data-stu-id="7cc6f-111">-ProfileName</span></span>
<span data-ttu-id="7cc6f-112">Gibt den Namen des Profils an.</span><span class="sxs-lookup"><span data-stu-id="7cc6f-112">Specifies the name of the profile.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cc6f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cc6f-113">-ResourceGroupName</span></span>
<span data-ttu-id="7cc6f-114">Gibt den Namen der Ressourcengruppe an, zu der das Profil gehört.</span><span class="sxs-lookup"><span data-stu-id="7cc6f-114">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cc6f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cc6f-115">CommonParameters</span></span>
<span data-ttu-id="7cc6f-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cc6f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cc6f-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cc6f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cc6f-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7cc6f-118">INPUTS</span></span>

### <span data-ttu-id="7cc6f-119">Keine</span><span class="sxs-lookup"><span data-stu-id="7cc6f-119">None</span></span>
<span data-ttu-id="7cc6f-120">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="7cc6f-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7cc6f-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7cc6f-121">OUTPUTS</span></span>

###  
<span data-ttu-id="7cc6f-122">Dieses Cmdlet gibt ein Profilobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="7cc6f-122">This cmdlet returns a profile object.</span></span>

## <span data-ttu-id="7cc6f-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="7cc6f-123">NOTES</span></span>

## <span data-ttu-id="7cc6f-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7cc6f-124">RELATED LINKS</span></span>

[<span data-ttu-id="7cc6f-125">Neu – AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="7cc6f-125">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="7cc6f-126">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="7cc6f-126">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="7cc6f-127">Satz-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="7cc6f-127">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


