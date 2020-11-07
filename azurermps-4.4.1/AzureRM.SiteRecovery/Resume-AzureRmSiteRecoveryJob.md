---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3F827EA0-7CF9-49F8-93BB-B15078A8BBB7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Resume-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Resume-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 5514d7cec58c2ecad7a4b9c79b3d4d2ad77a5ef3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663516"
---
# <span data-ttu-id="728af-101">Resume-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="728af-101">Resume-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="728af-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="728af-102">SYNOPSIS</span></span>
<span data-ttu-id="728af-103">Setzt einen angehaltene Website Wiederherstellungsauftrag fort.</span><span class="sxs-lookup"><span data-stu-id="728af-103">Resumes a suspended Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="728af-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="728af-104">SYNTAX</span></span>

### <span data-ttu-id="728af-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="728af-105">ByObject (Default)</span></span>
```
Resume-AzureRmSiteRecoveryJob -Job <ASRJob> [-Comments <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="728af-106">ByName</span><span class="sxs-lookup"><span data-stu-id="728af-106">ByName</span></span>
```
Resume-AzureRmSiteRecoveryJob -Name <String> [-Comments <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="728af-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="728af-107">DESCRIPTION</span></span>
<span data-ttu-id="728af-108">Mit dem Cmdlet **Resume-AzureRmSiteRecoveryJob** wird ein angehaltene Azure Site Recovery-Auftrag fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="728af-108">The **Resume-AzureRmSiteRecoveryJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="728af-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="728af-109">EXAMPLES</span></span>

## <span data-ttu-id="728af-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="728af-110">PARAMETERS</span></span>

### <span data-ttu-id="728af-111">-Kommentare</span><span class="sxs-lookup"><span data-stu-id="728af-111">-Comments</span></span>
<span data-ttu-id="728af-112">Gibt die Kommentare für das Auftragsprotokoll an.</span><span class="sxs-lookup"><span data-stu-id="728af-112">Specifies the comments for the job log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="728af-113">-Job</span><span class="sxs-lookup"><span data-stu-id="728af-113">-Job</span></span>
<span data-ttu-id="728af-114">Gibt das Auftragsobjekt für die Standortwiederherstellung an.</span><span class="sxs-lookup"><span data-stu-id="728af-114">Specifies the Site Recovery job object.</span></span>

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

### <span data-ttu-id="728af-115">-Name</span><span class="sxs-lookup"><span data-stu-id="728af-115">-Name</span></span>
<span data-ttu-id="728af-116">Gibt den eindeutigen Namen für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="728af-116">Specifies the unique name for the job.</span></span>

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

### <span data-ttu-id="728af-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="728af-117">-DefaultProfile</span></span>
<span data-ttu-id="728af-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="728af-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="728af-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="728af-119">CommonParameters</span></span>
<span data-ttu-id="728af-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="728af-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="728af-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="728af-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="728af-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="728af-122">INPUTS</span></span>

### <span data-ttu-id="728af-123">ASRJob</span><span class="sxs-lookup"><span data-stu-id="728af-123">ASRJob</span></span>
<span data-ttu-id="728af-124">Der Parameter ' Job ' akzeptiert den Wert vom Typ ' ASRJob ' aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="728af-124">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="728af-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="728af-125">OUTPUTS</span></span>

### <span data-ttu-id="728af-126">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="728af-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="728af-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="728af-127">NOTES</span></span>

## <span data-ttu-id="728af-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="728af-128">RELATED LINKS</span></span>

[<span data-ttu-id="728af-129">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="728af-129">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="728af-130">Neustart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="728af-130">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="728af-131">Stopp-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="728af-131">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
