---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: C4C624DB-BBE8-4F94-BDC6-C012482F7271
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: f09ca4bb6c033b954542d6c734b27bf5f2236d87
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476574"
---
# <span data-ttu-id="f051a-101">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="f051a-101">Remove-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="f051a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f051a-102">SYNOPSIS</span></span>
<span data-ttu-id="f051a-103">Entfernt eine Replikationsrichtlinie für die Standortwiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="f051a-103">Removes a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f051a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f051a-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryPolicy -Policy <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f051a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f051a-105">DESCRIPTION</span></span>
<span data-ttu-id="f051a-106">Das Cmdlet **Remove-AzureRMSiteRecoveryPolicy** entfernt eine Azure Site Recovery-Replikationsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="f051a-106">The **Remove-AzureRMSiteRecoveryPolicy** cmdlet removes an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="f051a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f051a-107">EXAMPLES</span></span>

## <span data-ttu-id="f051a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f051a-108">PARAMETERS</span></span>

### <span data-ttu-id="f051a-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f051a-109">-DefaultProfile</span></span>
<span data-ttu-id="f051a-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f051a-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f051a-111">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="f051a-111">-Policy</span></span>
<span data-ttu-id="f051a-112">Gibt das Website Wiederherstellungsrichtlinien Objekt an.</span><span class="sxs-lookup"><span data-stu-id="f051a-112">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f051a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f051a-113">CommonParameters</span></span>
<span data-ttu-id="f051a-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f051a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f051a-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f051a-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f051a-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f051a-116">INPUTS</span></span>

### <span data-ttu-id="f051a-117">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="f051a-117">ASRPolicy</span></span>
<span data-ttu-id="f051a-118">Der Parameter "Richtlinie" akzeptiert den Wert vom Typ "ASRPolicy" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="f051a-118">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="f051a-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f051a-119">OUTPUTS</span></span>

## <span data-ttu-id="f051a-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="f051a-120">NOTES</span></span>

## <span data-ttu-id="f051a-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f051a-121">RELATED LINKS</span></span>

[<span data-ttu-id="f051a-122">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="f051a-122">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="f051a-123">Neu – AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="f051a-123">New-AzureRmSiteRecoveryPolicy</span></span>](./New-AzureRmSiteRecoveryPolicy.md)
