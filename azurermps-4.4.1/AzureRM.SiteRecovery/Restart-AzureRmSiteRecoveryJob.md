---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 5A70AC55-27B4-421E-8EB0-1C7B8DFD3537
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Restart-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Restart-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 1b17284a5b0dfbdc8ee031df714c9f9f03533697
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500682"
---
# <span data-ttu-id="185c8-101">Restart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="185c8-101">Restart-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="185c8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="185c8-102">SYNOPSIS</span></span>
<span data-ttu-id="185c8-103">Startet einen Azure Site Recovery-Auftrag neu.</span><span class="sxs-lookup"><span data-stu-id="185c8-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="185c8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="185c8-104">SYNTAX</span></span>

### <span data-ttu-id="185c8-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="185c8-105">ByObject (Default)</span></span>
```
Restart-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="185c8-106">ByName</span><span class="sxs-lookup"><span data-stu-id="185c8-106">ByName</span></span>
```
Restart-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="185c8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="185c8-107">DESCRIPTION</span></span>
<span data-ttu-id="185c8-108">Mit dem Cmdlet " **Restart-AzureRmSiteRecoveryJob** " wird ein Azure Site Recovery-Auftrag neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="185c8-108">The **Restart-AzureRmSiteRecoveryJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="185c8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="185c8-109">EXAMPLES</span></span>

## <span data-ttu-id="185c8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="185c8-110">PARAMETERS</span></span>

### <span data-ttu-id="185c8-111">-Job</span><span class="sxs-lookup"><span data-stu-id="185c8-111">-Job</span></span>
<span data-ttu-id="185c8-112">Gibt das Auftragsobjekt für die Standortwiederherstellung an.</span><span class="sxs-lookup"><span data-stu-id="185c8-112">Specifies the Site Recovery job object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="185c8-113">-Name</span><span class="sxs-lookup"><span data-stu-id="185c8-113">-Name</span></span>
<span data-ttu-id="185c8-114">Gibt den eindeutigen Namen für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="185c8-114">Specifies the unique name for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="185c8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="185c8-115">-DefaultProfile</span></span>
<span data-ttu-id="185c8-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="185c8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="185c8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="185c8-117">CommonParameters</span></span>
<span data-ttu-id="185c8-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="185c8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="185c8-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="185c8-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="185c8-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="185c8-120">INPUTS</span></span>

### <span data-ttu-id="185c8-121">ASRJob</span><span class="sxs-lookup"><span data-stu-id="185c8-121">ASRJob</span></span>
<span data-ttu-id="185c8-122">Der Parameter ' Job ' akzeptiert den Wert vom Typ ' ASRJob ' aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="185c8-122">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="185c8-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="185c8-123">OUTPUTS</span></span>

### <span data-ttu-id="185c8-124">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="185c8-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="185c8-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="185c8-125">NOTES</span></span>

## <span data-ttu-id="185c8-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="185c8-126">RELATED LINKS</span></span>

[<span data-ttu-id="185c8-127">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="185c8-127">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="185c8-128">Lebenslauf-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="185c8-128">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="185c8-129">Stopp-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="185c8-129">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
