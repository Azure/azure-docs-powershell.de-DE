---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: b71c9a5da3c89916b18bdb5446f311e3d71615bf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845207"
---
# <span data-ttu-id="b7b8e-101">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="b7b8e-101">Get-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="b7b8e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b7b8e-102">SYNOPSIS</span></span>
<span data-ttu-id="b7b8e-103">Ruft die Details des angegebenen ASR-Auftrags oder der Liste der zuletzt verwendeten ASR-Aufträge im Recovery Services Vault ab.</span><span class="sxs-lookup"><span data-stu-id="b7b8e-103">Gets the details of the specified ASR job or the list of recent ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="b7b8e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7b8e-104">SYNTAX</span></span>

### <span data-ttu-id="b7b8e-105">ByParam (Standard)</span><span class="sxs-lookup"><span data-stu-id="b7b8e-105">ByParam (Default)</span></span>
```
Get-AzRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7b8e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b7b8e-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7b8e-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="b7b8e-107">ByObject</span></span>
```
Get-AzRecoveryServicesAsrJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7b8e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7b8e-108">DESCRIPTION</span></span>
<span data-ttu-id="b7b8e-109">Das Cmdlet " **Get-AzRecoveryServicesAsrJob** " ruft Azure Site Recovery-Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="b7b8e-109">The **Get-AzRecoveryServicesAsrJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="b7b8e-110">Sie können dieses Cmdlet verwenden, um die ASR-Aufträge im Speicher für Wiederherstellungsdienste anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b7b8e-110">You can use this cmdlet to view the ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="b7b8e-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b7b8e-111">EXAMPLES</span></span>

### <span data-ttu-id="b7b8e-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b7b8e-112">Example 1</span></span>
```
PS C:\> $jobs = Get-AzRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

<span data-ttu-id="b7b8e-113">Gibt alle Aufträge für ein bestimmtes ASR-Objekt zurück (Verweis auf das ASR-Objekt wie repliziertes Element oder Wiederherstellungsplan anhand seiner ID).</span><span class="sxs-lookup"><span data-stu-id="b7b8e-113">Returns all the jobs on a particular ASR object(reference the ASR object such as replicated item or recovery plan by its ID.)</span></span> 

## <span data-ttu-id="b7b8e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7b8e-114">PARAMETERS</span></span>

### <span data-ttu-id="b7b8e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7b8e-115">-DefaultProfile</span></span>
<span data-ttu-id="b7b8e-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b7b8e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7b8e-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="b7b8e-117">-EndTime</span></span>
<span data-ttu-id="b7b8e-118">Gibt die Endzeit für die Aufträge an.</span><span class="sxs-lookup"><span data-stu-id="b7b8e-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="b7b8e-119">Dieses Cmdlet ruft alle Aufträge ab, die vor der angegebenen Zeit gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="b7b8e-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="b7b8e-120">Verwenden Sie das Get-Date-Cmdlet, um ein **DateTime** -Objekt für diesen Parameter abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b7b8e-120">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="b7b8e-121">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="b7b8e-121">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7b8e-122">-Job</span><span class="sxs-lookup"><span data-stu-id="b7b8e-122">-Job</span></span>
<span data-ttu-id="b7b8e-123">Gibt das ASR-Auftragsobjekt an, für das aktualisierte Details abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b7b8e-123">Specifies the ASR job object to get updated details for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7b8e-124">-Name</span><span class="sxs-lookup"><span data-stu-id="b7b8e-124">-Name</span></span>
<span data-ttu-id="b7b8e-125">Geben Sie den ASR-Auftrag nach Name an.</span><span class="sxs-lookup"><span data-stu-id="b7b8e-125">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="b7b8e-126">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="b7b8e-126">-StartTime</span></span>
<span data-ttu-id="b7b8e-127">Gibt die Startzeit für die Aufträge an.</span><span class="sxs-lookup"><span data-stu-id="b7b8e-127">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="b7b8e-128">Dieses Cmdlet ruft alle Aufträge ab, die nach der angegebenen Zeit gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="b7b8e-128">This cmdlet gets all jobs that started after the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7b8e-129">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="b7b8e-129">-State</span></span>
<span data-ttu-id="b7b8e-130">Gibt den Status für einen ASR-Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="b7b8e-130">Specifies the state for a ASR job.</span></span>
<span data-ttu-id="b7b8e-131">Dieses Cmdlet ruft alle Aufträge ab, die dem angegebenen Zustand entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b7b8e-131">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="b7b8e-132">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b7b8e-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b7b8e-133">NotStarted</span><span class="sxs-lookup"><span data-stu-id="b7b8e-133">NotStarted</span></span>
- <span data-ttu-id="b7b8e-134">InProgress</span><span class="sxs-lookup"><span data-stu-id="b7b8e-134">InProgress</span></span>
- <span data-ttu-id="b7b8e-135">Erfolgreich</span><span class="sxs-lookup"><span data-stu-id="b7b8e-135">Succeeded</span></span>
- <span data-ttu-id="b7b8e-136">Anderen</span><span class="sxs-lookup"><span data-stu-id="b7b8e-136">Other</span></span>
- <span data-ttu-id="b7b8e-137">Fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="b7b8e-137">Failed</span></span>
- <span data-ttu-id="b7b8e-138">Storniert</span><span class="sxs-lookup"><span data-stu-id="b7b8e-138">Cancelled</span></span>
- <span data-ttu-id="b7b8e-139">Ausgesetzt</span><span class="sxs-lookup"><span data-stu-id="b7b8e-139">Suspended</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7b8e-140">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="b7b8e-140">-TargetObjectId</span></span>
<span data-ttu-id="b7b8e-141">Gibt die ID des Objekts an.</span><span class="sxs-lookup"><span data-stu-id="b7b8e-141">Specifies the ID of the object.</span></span> <span data-ttu-id="b7b8e-142">Wird verwendet, um nach Aufträgen für das angegebene Objekt zu suchen.</span><span class="sxs-lookup"><span data-stu-id="b7b8e-142">Used to search for jobs on the specified object.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7b8e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7b8e-143">CommonParameters</span></span>
<span data-ttu-id="b7b8e-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7b8e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7b8e-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7b8e-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7b8e-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b7b8e-146">INPUTS</span></span>

### <span data-ttu-id="b7b8e-147">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b7b8e-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b7b8e-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b7b8e-148">OUTPUTS</span></span>

### <span data-ttu-id="b7b8e-149">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b7b8e-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b7b8e-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="b7b8e-150">NOTES</span></span>

## <span data-ttu-id="b7b8e-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b7b8e-151">RELATED LINKS</span></span>

[<span data-ttu-id="b7b8e-152">Neustart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="b7b8e-152">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="b7b8e-153">Lebenslauf-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="b7b8e-153">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="b7b8e-154">Stopp-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="b7b8e-154">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
