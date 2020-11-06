---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/resume-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: e6c384f56e7af9bacad40dfbc1fbf87d26dd8320
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482818"
---
# <span data-ttu-id="1a8ba-101">Resume-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="1a8ba-101">Resume-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="1a8ba-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1a8ba-102">SYNOPSIS</span></span>
<span data-ttu-id="1a8ba-103">Setzt einen angehenden Azure Site Recovery-Auftrag fort.</span><span class="sxs-lookup"><span data-stu-id="1a8ba-103">Resumes a suspended Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a8ba-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a8ba-104">SYNTAX</span></span>

### <span data-ttu-id="1a8ba-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="1a8ba-105">ByObject (Default)</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a8ba-106">ByName</span><span class="sxs-lookup"><span data-stu-id="1a8ba-106">ByName</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -Name <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a8ba-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1a8ba-107">DESCRIPTION</span></span>
<span data-ttu-id="1a8ba-108">Mit dem Cmdlet **Resume-AzureRmRecoveryServicesAsrJob** wird ein angehaltene Azure Site Recovery-Auftrag fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="1a8ba-108">The **Resume-AzureRmRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="1a8ba-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1a8ba-109">EXAMPLES</span></span>

### <span data-ttu-id="1a8ba-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1a8ba-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="1a8ba-111">Fortsetzen des angegebenen Auftrags, wenn er sich in einem warte-oder angehalten-Zustand befindet und das aktualisierte ASR-Auftragsobjekt zurückgibt, das dem ASR-Auftrag entspricht.</span><span class="sxs-lookup"><span data-stu-id="1a8ba-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="1a8ba-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a8ba-112">PARAMETERS</span></span>

### <span data-ttu-id="1a8ba-113">-Kommentar</span><span class="sxs-lookup"><span data-stu-id="1a8ba-113">-Comment</span></span>
<span data-ttu-id="1a8ba-114">Kommentare für das Auftragsprotokoll.</span><span class="sxs-lookup"><span data-stu-id="1a8ba-114">Comments for the job log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Comments

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a8ba-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1a8ba-115">-Confirm</span></span>
<span data-ttu-id="1a8ba-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1a8ba-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a8ba-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a8ba-117">-DefaultProfile</span></span>
<span data-ttu-id="1a8ba-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1a8ba-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="1a8ba-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1a8ba-119">-InputObject</span></span>
<span data-ttu-id="1a8ba-120">Das Eingabeobjekt für das Cmdlet: das ASR-Auftragsobjekt, das dem Auftrag entspricht, der fortgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1a8ba-120">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: Job

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a8ba-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1a8ba-121">-Name</span></span>
<span data-ttu-id="1a8ba-122">Geben Sie den ASR-Auftrag nach Name an.</span><span class="sxs-lookup"><span data-stu-id="1a8ba-122">Specify the ASR job by name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a8ba-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a8ba-123">-WhatIf</span></span>
<span data-ttu-id="1a8ba-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1a8ba-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a8ba-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1a8ba-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a8ba-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a8ba-126">CommonParameters</span></span>
<span data-ttu-id="1a8ba-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a8ba-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a8ba-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a8ba-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a8ba-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1a8ba-129">INPUTS</span></span>

### <span data-ttu-id="1a8ba-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1a8ba-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1a8ba-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1a8ba-131">OUTPUTS</span></span>

### <span data-ttu-id="1a8ba-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1a8ba-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1a8ba-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="1a8ba-133">NOTES</span></span>

## <span data-ttu-id="1a8ba-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1a8ba-134">RELATED LINKS</span></span>

[<span data-ttu-id="1a8ba-135">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="1a8ba-135">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="1a8ba-136">Neustart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="1a8ba-136">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="1a8ba-137">Stopp-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="1a8ba-137">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
