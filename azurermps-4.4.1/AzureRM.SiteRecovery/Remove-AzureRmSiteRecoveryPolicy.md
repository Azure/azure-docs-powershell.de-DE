---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: C4C624DB-BBE8-4F94-BDC6-C012482F7271
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: 3b01e089271cc131af5a4258c46836a87104ef62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662889"
---
# <span data-ttu-id="d95b9-101">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="d95b9-101">Remove-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="d95b9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d95b9-102">SYNOPSIS</span></span>
<span data-ttu-id="d95b9-103">Entfernt eine Replikationsrichtlinie für die Standortwiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="d95b9-103">Removes a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d95b9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d95b9-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryPolicy -Policy <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d95b9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d95b9-105">DESCRIPTION</span></span>
<span data-ttu-id="d95b9-106">Das Cmdlet **Remove-AzureRMSiteRecoveryPolicy** entfernt eine Azure Site Recovery-Replikationsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="d95b9-106">The **Remove-AzureRMSiteRecoveryPolicy** cmdlet removes an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="d95b9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d95b9-107">EXAMPLES</span></span>

## <span data-ttu-id="d95b9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d95b9-108">PARAMETERS</span></span>

### <span data-ttu-id="d95b9-109">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="d95b9-109">-Policy</span></span>
<span data-ttu-id="d95b9-110">Gibt das Website Wiederherstellungsrichtlinien Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d95b9-110">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d95b9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d95b9-111">-DefaultProfile</span></span>
<span data-ttu-id="d95b9-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d95b9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d95b9-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d95b9-113">CommonParameters</span></span>
<span data-ttu-id="d95b9-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d95b9-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d95b9-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d95b9-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d95b9-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d95b9-116">INPUTS</span></span>

### <span data-ttu-id="d95b9-117">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="d95b9-117">ASRPolicy</span></span>
<span data-ttu-id="d95b9-118">Der Parameter "Richtlinie" akzeptiert den Wert vom Typ "ASRPolicy" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="d95b9-118">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="d95b9-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d95b9-119">OUTPUTS</span></span>

## <span data-ttu-id="d95b9-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="d95b9-120">NOTES</span></span>

## <span data-ttu-id="d95b9-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d95b9-121">RELATED LINKS</span></span>

[<span data-ttu-id="d95b9-122">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="d95b9-122">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="d95b9-123">Neu – AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="d95b9-123">New-AzureRmSiteRecoveryPolicy</span></span>](./New-AzureRmSiteRecoveryPolicy.md)
