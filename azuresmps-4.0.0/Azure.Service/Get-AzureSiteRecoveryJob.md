---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2957C0DE-3A2F-4337-A778-2B95654972E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8a7c99e2ce307d700e43094ffa9be47e5449acc0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411652"
---
# <span data-ttu-id="0b73e-101">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="0b73e-101">Get-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="0b73e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b73e-102">SYNOPSIS</span></span>
<span data-ttu-id="0b73e-103">Ruft die Vorgangsinformationen für einen Websitewiederherstellungstresor ab.</span><span class="sxs-lookup"><span data-stu-id="0b73e-103">Gets the operation information for a Site Recovery vault.</span></span>

## <span data-ttu-id="0b73e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b73e-104">SYNTAX</span></span>

### <span data-ttu-id="0b73e-105">ByParam (Standard)</span><span class="sxs-lookup"><span data-stu-id="0b73e-105">ByParam (Default)</span></span>
```
Get-AzureSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0b73e-106">ById</span><span class="sxs-lookup"><span data-stu-id="0b73e-106">ById</span></span>
```
Get-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0b73e-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="0b73e-107">ByObject</span></span>
```
Get-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0b73e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b73e-108">DESCRIPTION</span></span>
<span data-ttu-id="0b73e-109">Das **Cmdlet "Get-AzureSiteRecoveryJob"** ruft Azure Site Recovery-Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="0b73e-109">The **Get-AzureSiteRecoveryJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="0b73e-110">Mit diesem Cmdlet können Sie die Vorgangsinformationen für den aktuellen Websitewiederherstellungstresor anzeigen.</span><span class="sxs-lookup"><span data-stu-id="0b73e-110">You can use this cmdlet to view the operation information for the current Site Recovery vault.</span></span>

## <span data-ttu-id="0b73e-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0b73e-111">EXAMPLES</span></span>

### <span data-ttu-id="0b73e-112">Beispiel 1: Erhalten eines Auftrags durch Angeben einer ID</span><span class="sxs-lookup"><span data-stu-id="0b73e-112">Example 1: Get a job by specifying an ID</span></span>
```
PS C:\> Get-AzureSiteRecoveryJob -Id "033785cc-9f72-4f07-8e78-e4d1e942a7ae" 
Name             : SaveRecoveryPlan
ID               : 033785cc-9f72-4f07-8e78-e4d1e942a7ae
ClientRequestId  : d604206b-32e1-4d5b-9a23-32b118d14a1e-2015-02-20 07:20:42Z-P
State            : Succeeded
StateDescription : Completed
StartTime        : 20-02-2015 07:20:45 +05:30
EndTime          : 20-02-2015 07:20:46 +05:30
TargetObjectId   : cfb445bf-fd14-4b5d-b9ac-5154e1415ef2
TargetObjectType : RecoveryPlan
TargetObjectName : RP
AllowedActions   : {Cancel}
Tasks            : {Save a recovery plan task}
Errors           : {}
```

<span data-ttu-id="0b73e-113">Dieser Befehl ruft den Azure-Websitewiederherstellungsauftrag ab, der die angegebene ID hat.</span><span class="sxs-lookup"><span data-stu-id="0b73e-113">This command gets the  Azure Site Recovery job that has the specified ID.</span></span>

### <span data-ttu-id="0b73e-114">Beispiel 2: Ruft einen Auftrag basierend auf der Zeit ab.</span><span class="sxs-lookup"><span data-stu-id="0b73e-114">Example 2: Gets a job based on time</span></span>
```
PS C:\> Get-AzureSiteRecoveryJob -StartTime "20-02-2015 01:00:00" -EndTime "21-02-2015 01:00:00"
Name             : SaveRecoveryPlan
ID               : 033785cc-9f72-4f07-8e78-e4d1e942a7ae
ClientRequestId  : d604206b-32e1-4d5b-9a23-32b118d14a1e-2015-02-20 07:20:42Z-P
State            : Succeeded
StateDescription : Completed
StartTime        : 20-02-2015 07:20:45 +05:30
EndTime          : 20-02-2015 07:20:46 +05:30
TargetObjectId   : cfb445bf-fd14-4b5d-b9ac-5154e1415ef2
TargetObjectType : RecoveryPlan
TargetObjectName : RP
AllowedActions   : {Cancel}
Tasks            : {Save a recovery plan task}
Errors           : {}
```

<span data-ttu-id="0b73e-115">Dieser Befehl ruft Websitewiederherstellungsaufträge ab, die zwischen der angegebenen Start- und Endzeit liegen.</span><span class="sxs-lookup"><span data-stu-id="0b73e-115">This command gets Site Recovery jobs that fall between the specified start time and end time.</span></span>

## <span data-ttu-id="0b73e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b73e-116">PARAMETERS</span></span>

### <span data-ttu-id="0b73e-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="0b73e-117">-EndTime</span></span>
<span data-ttu-id="0b73e-118">Gibt die Endzeit für die Aufträge an.</span><span class="sxs-lookup"><span data-stu-id="0b73e-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="0b73e-119">Dieses Cmdlet ruft alle Aufträge ab, die vor dem angegebenen Zeitpunkt begonnen haben.</span><span class="sxs-lookup"><span data-stu-id="0b73e-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="0b73e-120">Verwenden Sie das Get-Date-Cmdlet, um ein **"DateTime"-Objekt** zu erhalten. </span><span class="sxs-lookup"><span data-stu-id="0b73e-120">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="0b73e-121">Weitere Informationen erhalten Sie, wenn Sie " `Get-Help Get-Date` eingeben" aus.</span><span class="sxs-lookup"><span data-stu-id="0b73e-121">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="0b73e-122">-ID</span><span class="sxs-lookup"><span data-stu-id="0b73e-122">-Id</span></span>
<span data-ttu-id="0b73e-123">Gibt die ID eines zu erhaltenden Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="0b73e-123">Specifies the ID of a job to get.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b73e-124">-Job</span><span class="sxs-lookup"><span data-stu-id="0b73e-124">-Job</span></span>
<span data-ttu-id="0b73e-125">Gibt einen Auftrag an, den Sie erhalten müssen.</span><span class="sxs-lookup"><span data-stu-id="0b73e-125">Specifies a job to get.</span></span>

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

### <span data-ttu-id="0b73e-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="0b73e-126">-Profile</span></span>
<span data-ttu-id="0b73e-127">Gibt das Azure-Profil an, aus dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="0b73e-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0b73e-128">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="0b73e-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b73e-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0b73e-129">-StartTime</span></span>
<span data-ttu-id="0b73e-130">Gibt die Startzeit für die Aufträge an.</span><span class="sxs-lookup"><span data-stu-id="0b73e-130">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="0b73e-131">Dieses Cmdlet ruft alle Aufträge ab, die nach der angegebenen Zeit gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="0b73e-131">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="0b73e-132">-State</span><span class="sxs-lookup"><span data-stu-id="0b73e-132">-State</span></span>
<span data-ttu-id="0b73e-133">Gibt den Eingabezustand für einen Websitewiederherstellungsauftrag an.</span><span class="sxs-lookup"><span data-stu-id="0b73e-133">Specifies the input state for a Site Recovery job.</span></span>
<span data-ttu-id="0b73e-134">Dieses Cmdlet ruft alle Aufträge ab, die dem angegebenen Zustand entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0b73e-134">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="0b73e-135">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="0b73e-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0b73e-136">NotStarted</span><span class="sxs-lookup"><span data-stu-id="0b73e-136">NotStarted</span></span>
- <span data-ttu-id="0b73e-137">InProgress</span><span class="sxs-lookup"><span data-stu-id="0b73e-137">InProgress</span></span>
- <span data-ttu-id="0b73e-138">Erfolgreich</span><span class="sxs-lookup"><span data-stu-id="0b73e-138">Succeeded</span></span>
- <span data-ttu-id="0b73e-139">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="0b73e-139">Other</span></span>
- <span data-ttu-id="0b73e-140">Fehler</span><span class="sxs-lookup"><span data-stu-id="0b73e-140">Failed</span></span>
- <span data-ttu-id="0b73e-141">Abgebrochen</span><span class="sxs-lookup"><span data-stu-id="0b73e-141">Cancelled</span></span>
- <span data-ttu-id="0b73e-142">Angehalten</span><span class="sxs-lookup"><span data-stu-id="0b73e-142">Suspended</span></span>

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

### <span data-ttu-id="0b73e-143">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="0b73e-143">-TargetObjectId</span></span>
<span data-ttu-id="0b73e-144">Gibt die ID des Objekts an, auf das der Auftrag ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="0b73e-144">Specifies the ID of the object targeted by the job.</span></span>

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

### <span data-ttu-id="0b73e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b73e-145">CommonParameters</span></span>
<span data-ttu-id="0b73e-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b73e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b73e-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b73e-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b73e-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0b73e-148">INPUTS</span></span>

## <span data-ttu-id="0b73e-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0b73e-149">OUTPUTS</span></span>

## <span data-ttu-id="0b73e-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0b73e-150">NOTES</span></span>

## <span data-ttu-id="0b73e-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0b73e-151">RELATED LINKS</span></span>



[<span data-ttu-id="0b73e-152">Restart-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="0b73e-152">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="0b73e-153">Resume-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="0b73e-153">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)

[<span data-ttu-id="0b73e-154">Stop-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="0b73e-154">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


