---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 48DCC0DC-1D59-4C30-9E1F-BBED7F94844F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/update-azurermsiterecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 7e1a043d1fd34ceae673111f2f7e0b892e419172
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500389"
---
# <span data-ttu-id="3e9d9-101">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="3e9d9-101">Update-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="3e9d9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3e9d9-102">SYNOPSIS</span></span>
<span data-ttu-id="3e9d9-103">Aktualisiert die vom Azure Site Recovery Services-Anbieter empfangenen Informationen.</span><span class="sxs-lookup"><span data-stu-id="3e9d9-103">Updates the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e9d9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e9d9-104">SYNTAX</span></span>

```
Update-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e9d9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3e9d9-105">DESCRIPTION</span></span>
<span data-ttu-id="3e9d9-106">Mit dem Cmdlet **Update-AzureRmSiteRecoveryServicesProvider** werden die vom Azure Site Recovery Services-Anbieter empfangenen Informationen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3e9d9-106">The **Update-AzureRmSiteRecoveryServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span>
<span data-ttu-id="3e9d9-107">Mit diesem Cmdlet können Sie eine Aktualisierung der vom Wiederherstellungsdienste-Anbieter empfangenen Informationen auslösen.</span><span class="sxs-lookup"><span data-stu-id="3e9d9-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="3e9d9-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3e9d9-108">EXAMPLES</span></span>

## <span data-ttu-id="3e9d9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e9d9-109">PARAMETERS</span></span>

### <span data-ttu-id="3e9d9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e9d9-110">-DefaultProfile</span></span>
<span data-ttu-id="3e9d9-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3e9d9-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e9d9-112">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="3e9d9-112">-ServicesProvider</span></span>
<span data-ttu-id="3e9d9-113">Gibt das Azure Site Recovery Services-Anbieterobjekt an.</span><span class="sxs-lookup"><span data-stu-id="3e9d9-113">Specifies the Azure Site Recovery Services Provider object.</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e9d9-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e9d9-114">CommonParameters</span></span>
<span data-ttu-id="3e9d9-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e9d9-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e9d9-116">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e9d9-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e9d9-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3e9d9-117">INPUTS</span></span>

### <span data-ttu-id="3e9d9-118">ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="3e9d9-118">ASRRecoveryServicesProvider</span></span>
<span data-ttu-id="3e9d9-119">Der Parameter "ServicesProvider" akzeptiert den Wert vom Typ "ASRRecoveryServicesProvider" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="3e9d9-119">Parameter 'ServicesProvider' accepts value of type 'ASRRecoveryServicesProvider' from the pipeline</span></span>

## <span data-ttu-id="3e9d9-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3e9d9-120">OUTPUTS</span></span>

## <span data-ttu-id="3e9d9-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="3e9d9-121">NOTES</span></span>

## <span data-ttu-id="3e9d9-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3e9d9-122">RELATED LINKS</span></span>

[<span data-ttu-id="3e9d9-123">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="3e9d9-123">Get-AzureRmSiteRecoveryServicesProvider</span></span>](./Get-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="3e9d9-124">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="3e9d9-124">Remove-AzureRmSiteRecoveryServicesProvider</span></span>](./Remove-AzureRmSiteRecoveryServicesProvider.md)
