---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: D0336AB5-019F-4EFD-88D2-63E12BA1ED95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoverysite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoverySite.md
ms.openlocfilehash: 053cd7695768be44cf3cecc5964e037f12f0b84e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498782"
---
# <span data-ttu-id="0b016-101">New-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="0b016-101">New-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="0b016-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0b016-102">SYNOPSIS</span></span>
<span data-ttu-id="0b016-103">Erstellt eine Website Wiederherstellungs Website.</span><span class="sxs-lookup"><span data-stu-id="0b016-103">Creates a Site Recovery site.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b016-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b016-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoverySite -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b016-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b016-105">DESCRIPTION</span></span>
<span data-ttu-id="0b016-106">Das Cmdlet **New-AzureRmSiteRecoverySite** erstellt eine Azure Site Recovery-Website im aktuellen Tresor.</span><span class="sxs-lookup"><span data-stu-id="0b016-106">The **New-AzureRmSiteRecoverySite** cmdlet creates an Azure Site Recovery site in the current vault.</span></span>

## <span data-ttu-id="0b016-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b016-107">EXAMPLES</span></span>

## <span data-ttu-id="0b016-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b016-108">PARAMETERS</span></span>

### <span data-ttu-id="0b016-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b016-109">-DefaultProfile</span></span>
<span data-ttu-id="0b016-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0b016-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b016-111">-Name</span><span class="sxs-lookup"><span data-stu-id="0b016-111">-Name</span></span>
<span data-ttu-id="0b016-112">Gibt den Namen der Website an.</span><span class="sxs-lookup"><span data-stu-id="0b016-112">Specifies the name of the site.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b016-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b016-113">CommonParameters</span></span>
<span data-ttu-id="0b016-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b016-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b016-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b016-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b016-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0b016-116">INPUTS</span></span>

### <span data-ttu-id="0b016-117">Keine</span><span class="sxs-lookup"><span data-stu-id="0b016-117">None</span></span>
<span data-ttu-id="0b016-118">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="0b016-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0b016-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0b016-119">OUTPUTS</span></span>

## <span data-ttu-id="0b016-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="0b016-120">NOTES</span></span>

## <span data-ttu-id="0b016-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0b016-121">RELATED LINKS</span></span>

[<span data-ttu-id="0b016-122">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="0b016-122">Get-AzureRmSiteRecoverySite</span></span>](./Get-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="0b016-123">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="0b016-123">Remove-AzureRmSiteRecoverySite</span></span>](./Remove-AzureRmSiteRecoverySite.md)
