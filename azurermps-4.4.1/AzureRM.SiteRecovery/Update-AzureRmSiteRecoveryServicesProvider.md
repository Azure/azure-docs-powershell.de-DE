---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 48DCC0DC-1D59-4C30-9E1F-BBED7F94844F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 31eda861294d4c678e141da8f40d1f5d6c5a4ca1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663819"
---
# <span data-ttu-id="47ea1-101">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="47ea1-101">Update-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="47ea1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="47ea1-102">SYNOPSIS</span></span>
<span data-ttu-id="47ea1-103">Aktualisiert die vom Azure Site Recovery Services-Anbieter empfangenen Informationen.</span><span class="sxs-lookup"><span data-stu-id="47ea1-103">Updates the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47ea1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="47ea1-104">SYNTAX</span></span>

```
Update-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47ea1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47ea1-105">DESCRIPTION</span></span>
<span data-ttu-id="47ea1-106">Mit dem Cmdlet **Update-AzureRmSiteRecoveryServicesProvider** werden die vom Azure Site Recovery Services-Anbieter empfangenen Informationen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="47ea1-106">The **Update-AzureRmSiteRecoveryServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span>
<span data-ttu-id="47ea1-107">Mit diesem Cmdlet können Sie eine Aktualisierung der vom Wiederherstellungsdienste-Anbieter empfangenen Informationen auslösen.</span><span class="sxs-lookup"><span data-stu-id="47ea1-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="47ea1-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="47ea1-108">EXAMPLES</span></span>

## <span data-ttu-id="47ea1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="47ea1-109">PARAMETERS</span></span>

### <span data-ttu-id="47ea1-110">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="47ea1-110">-ServicesProvider</span></span>
<span data-ttu-id="47ea1-111">Gibt das Azure Site Recovery Services-Anbieterobjekt an.</span><span class="sxs-lookup"><span data-stu-id="47ea1-111">Specifies the Azure Site Recovery Services Provider object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47ea1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47ea1-112">-DefaultProfile</span></span>
<span data-ttu-id="47ea1-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="47ea1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47ea1-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47ea1-114">CommonParameters</span></span>
<span data-ttu-id="47ea1-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47ea1-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47ea1-116">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47ea1-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47ea1-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="47ea1-117">INPUTS</span></span>

### <span data-ttu-id="47ea1-118">ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="47ea1-118">ASRRecoveryServicesProvider</span></span>
<span data-ttu-id="47ea1-119">Der Parameter "ServicesProvider" akzeptiert den Wert vom Typ "ASRRecoveryServicesProvider" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="47ea1-119">Parameter 'ServicesProvider' accepts value of type 'ASRRecoveryServicesProvider' from the pipeline</span></span>

## <span data-ttu-id="47ea1-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="47ea1-120">OUTPUTS</span></span>

## <span data-ttu-id="47ea1-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="47ea1-121">NOTES</span></span>

## <span data-ttu-id="47ea1-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="47ea1-122">RELATED LINKS</span></span>

[<span data-ttu-id="47ea1-123">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="47ea1-123">Get-AzureRmSiteRecoveryServicesProvider</span></span>](./Get-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="47ea1-124">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="47ea1-124">Remove-AzureRmSiteRecoveryServicesProvider</span></span>](./Remove-AzureRmSiteRecoveryServicesProvider.md)
