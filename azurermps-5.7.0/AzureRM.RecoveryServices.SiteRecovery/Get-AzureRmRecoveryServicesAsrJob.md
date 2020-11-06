---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 233a6a7c7fd7b2bfe96ed9cc0df6a88bdb9d8747
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478309"
---
# <span data-ttu-id="8067d-101">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="8067d-101">Get-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="8067d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8067d-102">SYNOPSIS</span></span>
<span data-ttu-id="8067d-103">Ruft die Details des angegebenen ASR-Auftrags oder der Liste der zuletzt verwendeten ASR-Aufträge im Recovery Services Vault ab.</span><span class="sxs-lookup"><span data-stu-id="8067d-103">Gets the details of the specified ASR job or the list of recent ASR jobs in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8067d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8067d-104">SYNTAX</span></span>

### <span data-ttu-id="8067d-105">ByParam (Standard)</span><span class="sxs-lookup"><span data-stu-id="8067d-105">ByParam (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8067d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8067d-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8067d-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="8067d-107">ByObject</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8067d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8067d-108">DESCRIPTION</span></span>
<span data-ttu-id="8067d-109">Das Cmdlet " **Get-AzureRmRecoveryServicesAsrJob** " ruft Azure Site Recovery-Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="8067d-109">The **Get-AzureRmRecoveryServicesAsrJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="8067d-110">Sie können dieses Cmdlet verwenden, um die ASR-Aufträge im Speicher für Wiederherstellungsdienste anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8067d-110">You can use this cmdlet to view the ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="8067d-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8067d-111">EXAMPLES</span></span>

### <span data-ttu-id="8067d-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8067d-112">Example 1</span></span>
```
PS C:\> $jobs = Get-AzureRmRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

<span data-ttu-id="8067d-113">Gibt alle Aufträge für ein bestimmtes ASR-Objekt zurück (Verweis auf das ASR-Objekt wie repliziertes Element oder Wiederherstellungsplan anhand seiner ID).</span><span class="sxs-lookup"><span data-stu-id="8067d-113">Returns all the jobs on a particular ASR object(reference the ASR object such as replicated item or recovery plan by its ID.)</span></span> 

## <span data-ttu-id="8067d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="8067d-114">PARAMETERS</span></span>

### <span data-ttu-id="8067d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8067d-115">-DefaultProfile</span></span>
<span data-ttu-id="8067d-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8067d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="8067d-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="8067d-117">-EndTime</span></span>
<span data-ttu-id="8067d-118">Gibt die Endzeit für die Aufträge an.</span><span class="sxs-lookup"><span data-stu-id="8067d-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="8067d-119">Dieses Cmdlet ruft alle Aufträge ab, die vor der angegebenen Zeit gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="8067d-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="8067d-120">Verwenden Sie das Get-Date-Cmdlet, um ein **DateTime** -Objekt für diesen Parameter abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8067d-120">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="8067d-121">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="8067d-121">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="8067d-122">-Job</span><span class="sxs-lookup"><span data-stu-id="8067d-122">-Job</span></span>
<span data-ttu-id="8067d-123">Gibt das ASR-Auftragsobjekt an, für das aktualisierte Details abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8067d-123">Specifies the ASR job object to get updated details for.</span></span>

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

### <span data-ttu-id="8067d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="8067d-124">-Name</span></span>
<span data-ttu-id="8067d-125">Geben Sie den ASR-Auftrag nach Name an.</span><span class="sxs-lookup"><span data-stu-id="8067d-125">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="8067d-126">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="8067d-126">-StartTime</span></span>
<span data-ttu-id="8067d-127">Gibt die Startzeit für die Aufträge an.</span><span class="sxs-lookup"><span data-stu-id="8067d-127">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="8067d-128">Dieses Cmdlet ruft alle Aufträge ab, die nach der angegebenen Zeit gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="8067d-128">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="8067d-129">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="8067d-129">-State</span></span>
<span data-ttu-id="8067d-130">Gibt den Status für einen ASR-Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="8067d-130">Specifies the state for a ASR job.</span></span>
<span data-ttu-id="8067d-131">Dieses Cmdlet ruft alle Aufträge ab, die dem angegebenen Zustand entsprechen.</span><span class="sxs-lookup"><span data-stu-id="8067d-131">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="8067d-132">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8067d-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8067d-133">NotStarted</span><span class="sxs-lookup"><span data-stu-id="8067d-133">NotStarted</span></span>
- <span data-ttu-id="8067d-134">InProgress</span><span class="sxs-lookup"><span data-stu-id="8067d-134">InProgress</span></span>
- <span data-ttu-id="8067d-135">Erfolgreich</span><span class="sxs-lookup"><span data-stu-id="8067d-135">Succeeded</span></span>
- <span data-ttu-id="8067d-136">Anderen</span><span class="sxs-lookup"><span data-stu-id="8067d-136">Other</span></span>
- <span data-ttu-id="8067d-137">Fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="8067d-137">Failed</span></span>
- <span data-ttu-id="8067d-138">Storniert</span><span class="sxs-lookup"><span data-stu-id="8067d-138">Cancelled</span></span>
- <span data-ttu-id="8067d-139">Ausgesetzt</span><span class="sxs-lookup"><span data-stu-id="8067d-139">Suspended</span></span>

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

### <span data-ttu-id="8067d-140">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="8067d-140">-TargetObjectId</span></span>
<span data-ttu-id="8067d-141">Gibt die ID des Objekts an.</span><span class="sxs-lookup"><span data-stu-id="8067d-141">Specifies the ID of the object.</span></span> <span data-ttu-id="8067d-142">Wird verwendet, um nach Aufträgen für das angegebene Objekt zu suchen.</span><span class="sxs-lookup"><span data-stu-id="8067d-142">Used to search for jobs on the specified object.</span></span>

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

### <span data-ttu-id="8067d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8067d-143">CommonParameters</span></span>
<span data-ttu-id="8067d-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8067d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8067d-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8067d-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8067d-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8067d-146">INPUTS</span></span>

### <span data-ttu-id="8067d-147">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8067d-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8067d-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8067d-148">OUTPUTS</span></span>

### <span data-ttu-id="8067d-149">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="8067d-149">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8067d-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="8067d-150">NOTES</span></span>

## <span data-ttu-id="8067d-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8067d-151">RELATED LINKS</span></span>

[<span data-ttu-id="8067d-152">Neustart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="8067d-152">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="8067d-153">Lebenslauf-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="8067d-153">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="8067d-154">Stopp-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="8067d-154">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
