---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: afef81ad904ccd5bf53f0b2a09bb10511e71fca1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503989"
---
# <span data-ttu-id="4fe07-101">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="4fe07-101">Get-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="4fe07-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4fe07-102">SYNOPSIS</span></span>
<span data-ttu-id="4fe07-103">Ruft die Details des angegebenen ASR-Auftrags oder der Liste der zuletzt verwendeten ASR-Aufträge im Recovery Services Vault ab.</span><span class="sxs-lookup"><span data-stu-id="4fe07-103">Gets the details of the specified ASR job or the list of recent ASR jobs in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fe07-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fe07-104">SYNTAX</span></span>

### <span data-ttu-id="4fe07-105">ByParam (Standard)</span><span class="sxs-lookup"><span data-stu-id="4fe07-105">ByParam (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [<CommonParameters>]
```

### <span data-ttu-id="4fe07-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4fe07-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="4fe07-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="4fe07-107">ByObject</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Job <ASRJob> [<CommonParameters>]
```

## <span data-ttu-id="4fe07-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4fe07-108">DESCRIPTION</span></span>
<span data-ttu-id="4fe07-109">Das Cmdlet " **Get-AzureRmRecoveryServicesAsrJob** " ruft Azure Site Recovery-Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="4fe07-109">The **Get-AzureRmRecoveryServicesAsrJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="4fe07-110">Sie können dieses Cmdlet verwenden, um die ASR-Aufträge im Speicher für Wiederherstellungsdienste anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4fe07-110">You can use this cmdlet to view the ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="4fe07-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4fe07-111">EXAMPLES</span></span>

### <span data-ttu-id="4fe07-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4fe07-112">Example 1</span></span>
```
PS C:\> $jobs = Get-AzureRmRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

<span data-ttu-id="4fe07-113">Gibt alle Aufträge für ein bestimmtes ASR-Objekt zurück (Verweis auf das ASR-Objekt wie repliziertes Element oder Wiederherstellungsplan anhand seiner ID).</span><span class="sxs-lookup"><span data-stu-id="4fe07-113">Returns all the jobs on a particular ASR object(reference the ASR object such as replicated item or recovery plan by its ID.)</span></span> 

## <span data-ttu-id="4fe07-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="4fe07-114">PARAMETERS</span></span>

### <span data-ttu-id="4fe07-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="4fe07-115">-EndTime</span></span>
<span data-ttu-id="4fe07-116">Gibt die Endzeit für die Aufträge an.</span><span class="sxs-lookup"><span data-stu-id="4fe07-116">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="4fe07-117">Dieses Cmdlet ruft alle Aufträge ab, die vor der angegebenen Zeit gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="4fe07-117">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="4fe07-118">Verwenden Sie das Get-Date-Cmdlet, um ein **DateTime** -Objekt für diesen Parameter abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4fe07-118">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="4fe07-119">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="4fe07-119">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fe07-120">-Job</span><span class="sxs-lookup"><span data-stu-id="4fe07-120">-Job</span></span>
<span data-ttu-id="4fe07-121">Gibt das ASR-Auftragsobjekt an, für das aktualisierte Details abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4fe07-121">Specifies the ASR job object to get updated details for.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4fe07-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4fe07-122">-Name</span></span>
<span data-ttu-id="4fe07-123">Geben Sie den ASR-Auftrag nach Name an.</span><span class="sxs-lookup"><span data-stu-id="4fe07-123">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="4fe07-124">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="4fe07-124">-StartTime</span></span>
<span data-ttu-id="4fe07-125">Gibt die Startzeit für die Aufträge an.</span><span class="sxs-lookup"><span data-stu-id="4fe07-125">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="4fe07-126">Dieses Cmdlet ruft alle Aufträge ab, die nach der angegebenen Zeit gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="4fe07-126">This cmdlet gets all jobs that started after the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fe07-127">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="4fe07-127">-State</span></span>
<span data-ttu-id="4fe07-128">Gibt den Status für einen ASR-Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="4fe07-128">Specifies the state for a ASR job.</span></span>
<span data-ttu-id="4fe07-129">Dieses Cmdlet ruft alle Aufträge ab, die dem angegebenen Zustand entsprechen.</span><span class="sxs-lookup"><span data-stu-id="4fe07-129">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="4fe07-130">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4fe07-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4fe07-131">NotStarted</span><span class="sxs-lookup"><span data-stu-id="4fe07-131">NotStarted</span></span>
- <span data-ttu-id="4fe07-132">InProgress</span><span class="sxs-lookup"><span data-stu-id="4fe07-132">InProgress</span></span>
- <span data-ttu-id="4fe07-133">Erfolgreich</span><span class="sxs-lookup"><span data-stu-id="4fe07-133">Succeeded</span></span>
- <span data-ttu-id="4fe07-134">Anderen</span><span class="sxs-lookup"><span data-stu-id="4fe07-134">Other</span></span>
- <span data-ttu-id="4fe07-135">Fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="4fe07-135">Failed</span></span>
- <span data-ttu-id="4fe07-136">Storniert</span><span class="sxs-lookup"><span data-stu-id="4fe07-136">Cancelled</span></span>
- <span data-ttu-id="4fe07-137">Ausgesetzt</span><span class="sxs-lookup"><span data-stu-id="4fe07-137">Suspended</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fe07-138">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="4fe07-138">-TargetObjectId</span></span>
<span data-ttu-id="4fe07-139">Gibt die ID des Objekts an.</span><span class="sxs-lookup"><span data-stu-id="4fe07-139">Specifies the ID of the object.</span></span> <span data-ttu-id="4fe07-140">Wird verwendet, um nach Aufträgen für das angegebene Objekt zu suchen.</span><span class="sxs-lookup"><span data-stu-id="4fe07-140">Used to search for jobs on the specified object.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fe07-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fe07-141">CommonParameters</span></span>
<span data-ttu-id="4fe07-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fe07-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fe07-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fe07-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fe07-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4fe07-144">INPUTS</span></span>

### <span data-ttu-id="4fe07-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="4fe07-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4fe07-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4fe07-146">OUTPUTS</span></span>

### <span data-ttu-id="4fe07-147">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4fe07-147">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4fe07-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="4fe07-148">NOTES</span></span>

## <span data-ttu-id="4fe07-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4fe07-149">RELATED LINKS</span></span>

[<span data-ttu-id="4fe07-150">Neustart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="4fe07-150">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="4fe07-151">Lebenslauf-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="4fe07-151">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="4fe07-152">Stopp-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="4fe07-152">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
