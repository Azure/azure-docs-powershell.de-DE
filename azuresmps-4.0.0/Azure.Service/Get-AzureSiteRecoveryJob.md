---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2957C0DE-3A2F-4337-A778-2B95654972E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d0b272732cf6c1e1b2025c8e7f48b58e4807cdb3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005801"
---
# <span data-ttu-id="0f6dd-101">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="0f6dd-101">Get-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="0f6dd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0f6dd-102">SYNOPSIS</span></span>
<span data-ttu-id="0f6dd-103">Ruft die Vorgangsinformationen für ein Website Wiederherstellungs Depot ab.</span><span class="sxs-lookup"><span data-stu-id="0f6dd-103">Gets the operation information for a Site Recovery vault.</span></span>

## <span data-ttu-id="0f6dd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f6dd-104">SYNTAX</span></span>

### <span data-ttu-id="0f6dd-105">ByParam (Standard)</span><span class="sxs-lookup"><span data-stu-id="0f6dd-105">ByParam (Default)</span></span>
```
Get-AzureSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0f6dd-106">ById</span><span class="sxs-lookup"><span data-stu-id="0f6dd-106">ById</span></span>
```
Get-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0f6dd-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="0f6dd-107">ByObject</span></span>
```
Get-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0f6dd-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f6dd-108">DESCRIPTION</span></span>
<span data-ttu-id="0f6dd-109">Das Cmdlet " **Get-AzureSiteRecoveryJob** " ruft Azure Site Recovery-Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="0f6dd-109">The **Get-AzureSiteRecoveryJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="0f6dd-110">Sie können dieses Cmdlet verwenden, um die Vorgangsinformationen für das aktuelle Standort Wiederherstellungs Depot anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0f6dd-110">You can use this cmdlet to view the operation information for the current Site Recovery vault.</span></span>

## <span data-ttu-id="0f6dd-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0f6dd-111">EXAMPLES</span></span>

### <span data-ttu-id="0f6dd-112">Beispiel 1: Abrufen eines Auftrags durch Angabe einer ID</span><span class="sxs-lookup"><span data-stu-id="0f6dd-112">Example 1: Get a job by specifying an ID</span></span>
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

<span data-ttu-id="0f6dd-113">Mit diesem Befehl wird der Azure Site Recovery-Auftrag mit der angegebenen ID abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0f6dd-113">This command gets the  Azure Site Recovery job that has the specified ID.</span></span>

### <span data-ttu-id="0f6dd-114">Beispiel 2: Abrufen eines Auftrags basierend auf der Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="0f6dd-114">Example 2: Gets a job based on time</span></span>
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

<span data-ttu-id="0f6dd-115">Dieser Befehl ruft Website Wiederherstellungsaufträge ab, die zwischen der angegebenen Startzeit und Endzeit liegen.</span><span class="sxs-lookup"><span data-stu-id="0f6dd-115">This command gets Site Recovery jobs that fall between the specified start time and end time.</span></span>

## <span data-ttu-id="0f6dd-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f6dd-116">PARAMETERS</span></span>

### <span data-ttu-id="0f6dd-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="0f6dd-117">-EndTime</span></span>
<span data-ttu-id="0f6dd-118">Gibt die Endzeit für die Aufträge an.</span><span class="sxs-lookup"><span data-stu-id="0f6dd-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="0f6dd-119">Dieses Cmdlet ruft alle Aufträge ab, die vor der angegebenen Zeit gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="0f6dd-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="0f6dd-120">Verwenden Sie das Cmdlet " **Get-Date** ", um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0f6dd-120">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="0f6dd-121">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="0f6dd-121">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="0f6dd-122">-ID</span><span class="sxs-lookup"><span data-stu-id="0f6dd-122">-Id</span></span>
<span data-ttu-id="0f6dd-123">Gibt die ID des abzurufenden Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="0f6dd-123">Specifies the ID of a job to get.</span></span>

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

### <span data-ttu-id="0f6dd-124">-Job</span><span class="sxs-lookup"><span data-stu-id="0f6dd-124">-Job</span></span>
<span data-ttu-id="0f6dd-125">Gibt einen Auftrag an, der abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="0f6dd-125">Specifies a job to get.</span></span>

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

### <span data-ttu-id="0f6dd-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="0f6dd-126">-Profile</span></span>
<span data-ttu-id="0f6dd-127">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="0f6dd-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0f6dd-128">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="0f6dd-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0f6dd-129">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="0f6dd-129">-StartTime</span></span>
<span data-ttu-id="0f6dd-130">Gibt die Startzeit für die Aufträge an.</span><span class="sxs-lookup"><span data-stu-id="0f6dd-130">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="0f6dd-131">Dieses Cmdlet ruft alle Aufträge ab, die nach der angegebenen Zeit gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="0f6dd-131">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="0f6dd-132">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="0f6dd-132">-State</span></span>
<span data-ttu-id="0f6dd-133">Gibt den Eingabestatus für einen Standort Wiederherstellungsauftrag an.</span><span class="sxs-lookup"><span data-stu-id="0f6dd-133">Specifies the input state for a Site Recovery job.</span></span>
<span data-ttu-id="0f6dd-134">Dieses Cmdlet ruft alle Aufträge ab, die dem angegebenen Zustand entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0f6dd-134">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="0f6dd-135">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0f6dd-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0f6dd-136">NotStarted</span><span class="sxs-lookup"><span data-stu-id="0f6dd-136">NotStarted</span></span>
- <span data-ttu-id="0f6dd-137">InProgress</span><span class="sxs-lookup"><span data-stu-id="0f6dd-137">InProgress</span></span>
- <span data-ttu-id="0f6dd-138">Erfolgreich</span><span class="sxs-lookup"><span data-stu-id="0f6dd-138">Succeeded</span></span>
- <span data-ttu-id="0f6dd-139">Anderen</span><span class="sxs-lookup"><span data-stu-id="0f6dd-139">Other</span></span>
- <span data-ttu-id="0f6dd-140">Fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="0f6dd-140">Failed</span></span>
- <span data-ttu-id="0f6dd-141">Storniert</span><span class="sxs-lookup"><span data-stu-id="0f6dd-141">Cancelled</span></span>
- <span data-ttu-id="0f6dd-142">Ausgesetzt</span><span class="sxs-lookup"><span data-stu-id="0f6dd-142">Suspended</span></span>

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

### <span data-ttu-id="0f6dd-143">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="0f6dd-143">-TargetObjectId</span></span>
<span data-ttu-id="0f6dd-144">Gibt die ID des Objekts an, das für den Auftrag vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="0f6dd-144">Specifies the ID of the object targeted by the job.</span></span>

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

### <span data-ttu-id="0f6dd-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f6dd-145">CommonParameters</span></span>
<span data-ttu-id="0f6dd-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f6dd-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f6dd-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f6dd-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f6dd-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0f6dd-148">INPUTS</span></span>

## <span data-ttu-id="0f6dd-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0f6dd-149">OUTPUTS</span></span>

## <span data-ttu-id="0f6dd-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="0f6dd-150">NOTES</span></span>

## <span data-ttu-id="0f6dd-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0f6dd-151">RELATED LINKS</span></span>

[<span data-ttu-id="0f6dd-152">Azure Site Recovery Services-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="0f6dd-152">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)

[<span data-ttu-id="0f6dd-153">Neustart-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="0f6dd-153">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="0f6dd-154">Lebenslauf-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="0f6dd-154">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)

[<span data-ttu-id="0f6dd-155">Stopp-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="0f6dd-155">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


