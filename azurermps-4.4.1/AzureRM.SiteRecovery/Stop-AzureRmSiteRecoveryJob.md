---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: CFEA76B4-684C-4C2A-9806-36DC133AEE80
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Stop-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Stop-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 79ad35a00fcd0aef62e99a217071589e10f973c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481486"
---
# <span data-ttu-id="ea038-101">Stop-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="ea038-101">Stop-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="ea038-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ea038-102">SYNOPSIS</span></span>
<span data-ttu-id="ea038-103">Beendet einen Wiederherstellungsauftrag für die Website.</span><span class="sxs-lookup"><span data-stu-id="ea038-103">Stops a Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea038-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea038-104">SYNTAX</span></span>

### <span data-ttu-id="ea038-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="ea038-105">ByObject (Default)</span></span>
```
Stop-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea038-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ea038-106">ByName</span></span>
```
Stop-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea038-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ea038-107">DESCRIPTION</span></span>
<span data-ttu-id="ea038-108">Das Cmdlet " **Stop-AzureRmSiteRecoveryJob** " beendet einen Azure Site Recovery-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="ea038-108">The **Stop-AzureRmSiteRecoveryJob** cmdlet stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="ea038-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ea038-109">EXAMPLES</span></span>

## <span data-ttu-id="ea038-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea038-110">PARAMETERS</span></span>

### <span data-ttu-id="ea038-111">-Job</span><span class="sxs-lookup"><span data-stu-id="ea038-111">-Job</span></span>
<span data-ttu-id="ea038-112">Gibt das zu beendende Wiederherstellungsauftrags Objekt der Website an.</span><span class="sxs-lookup"><span data-stu-id="ea038-112">Specifies the Site Recovery job object to stop.</span></span>

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

### <span data-ttu-id="ea038-113">-Name</span><span class="sxs-lookup"><span data-stu-id="ea038-113">-Name</span></span>
<span data-ttu-id="ea038-114">Gibt den eindeutigen Namen für den zu beendenden Standort Wiederherstellungsauftrag an.</span><span class="sxs-lookup"><span data-stu-id="ea038-114">Specifies the unique name for the Site Recovery job to stop.</span></span>

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

### <span data-ttu-id="ea038-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea038-115">-DefaultProfile</span></span>
<span data-ttu-id="ea038-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ea038-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea038-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea038-117">CommonParameters</span></span>
<span data-ttu-id="ea038-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea038-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea038-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea038-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea038-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ea038-120">INPUTS</span></span>

### <span data-ttu-id="ea038-121">ASRJob</span><span class="sxs-lookup"><span data-stu-id="ea038-121">ASRJob</span></span>
<span data-ttu-id="ea038-122">Der Parameter ' Job ' akzeptiert den Wert vom Typ ' ASRJob ' aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ea038-122">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="ea038-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ea038-123">OUTPUTS</span></span>

### <span data-ttu-id="ea038-124">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ea038-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ea038-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="ea038-125">NOTES</span></span>

## <span data-ttu-id="ea038-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ea038-126">RELATED LINKS</span></span>

[<span data-ttu-id="ea038-127">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="ea038-127">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="ea038-128">Neustart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="ea038-128">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="ea038-129">Lebenslauf-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="ea038-129">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)
