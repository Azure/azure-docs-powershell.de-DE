---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
ms.openlocfilehash: c554caf7230b54db3e1161a20e001f9873f6dfff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497862"
---
# <span data-ttu-id="bf1e2-101">Set-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="bf1e2-101">Set-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="bf1e2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bf1e2-102">SYNOPSIS</span></span>
<span data-ttu-id="bf1e2-103">Aktualisiert einen CDN-Ursprungsserver.</span><span class="sxs-lookup"><span data-stu-id="bf1e2-103">Updates a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf1e2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf1e2-104">SYNTAX</span></span>

```
Set-AzureRmCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf1e2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf1e2-105">DESCRIPTION</span></span>
<span data-ttu-id="bf1e2-106">Das Cmdlet " **Satz-AzureRmCdnOrigin** " aktualisiert einen Server mit Azure Content Delivery Network (CDN).</span><span class="sxs-lookup"><span data-stu-id="bf1e2-106">The **Set-AzureRmCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="bf1e2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bf1e2-107">EXAMPLES</span></span>

## <span data-ttu-id="bf1e2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf1e2-108">PARAMETERS</span></span>

### <span data-ttu-id="bf1e2-109">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="bf1e2-109">-CdnOrigin</span></span>
<span data-ttu-id="bf1e2-110">Gibt den Ursprungsserver an, der vom Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="bf1e2-110">Specifies the origin server that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf1e2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf1e2-111">-DefaultProfile</span></span>
<span data-ttu-id="bf1e2-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bf1e2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf1e2-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf1e2-113">CommonParameters</span></span>
<span data-ttu-id="bf1e2-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf1e2-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf1e2-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf1e2-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf1e2-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bf1e2-116">INPUTS</span></span>

### <span data-ttu-id="bf1e2-117">PSOrigin</span><span class="sxs-lookup"><span data-stu-id="bf1e2-117">PSOrigin</span></span>
<span data-ttu-id="bf1e2-118">Der Parameter ' CdnOrigin' akzeptiert den Wert vom Typ ' PSOrigin' aus der Pipeline</span><span class="sxs-lookup"><span data-stu-id="bf1e2-118">Parameter 'CdnOrigin' accepts value of type 'PSOrigin' from the pipeline</span></span>

## <span data-ttu-id="bf1e2-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bf1e2-119">OUTPUTS</span></span>

### <span data-ttu-id="bf1e2-120">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="bf1e2-120">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="bf1e2-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="bf1e2-121">NOTES</span></span>

## <span data-ttu-id="bf1e2-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bf1e2-122">RELATED LINKS</span></span>

[<span data-ttu-id="bf1e2-123">Get-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="bf1e2-123">Get-AzureRmCdnOrigin</span></span>](./Get-AzureRmCdnOrigin.md)


