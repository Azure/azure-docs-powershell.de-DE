---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 2001E040-5551-40C3-81D2-9A8334DE02BF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7692d4407df8fb4af8647ee0b4490abe73b2c937
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005764"
---
# <span data-ttu-id="c11d8-101">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="c11d8-101">Get-AzureStorSimpleJob</span></span>

## <span data-ttu-id="c11d8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c11d8-102">SYNOPSIS</span></span>
<span data-ttu-id="c11d8-103">Ruft StorSimple-Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="c11d8-103">Gets StorSimple jobs.</span></span>

## <span data-ttu-id="c11d8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c11d8-104">SYNTAX</span></span>

```
Get-AzureStorSimpleJob [-DeviceName <String>] [-InstanceId <String>] [-Status <String>] [-Type <String>]
 [-From <DateTime>] [-To <DateTime>] [-Skip <Int32>] [-First <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c11d8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c11d8-105">DESCRIPTION</span></span>
<span data-ttu-id="c11d8-106">Das Cmdlet " **Get-AzureStorSimpleJob** " ruft Azure StorSimple-Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="c11d8-106">The **Get-AzureStorSimpleJob** cmdlet gets Azure StorSimple jobs.</span></span>
<span data-ttu-id="c11d8-107">Geben Sie eine Instanz-ID an, um einen bestimmten Job zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c11d8-107">Specify an instance ID to get a specific job.</span></span>
<span data-ttu-id="c11d8-108">Geben Sie andere Parameter an, um die von diesem Cmdlet abgerufenen Aufträge zu begrenzen.</span><span class="sxs-lookup"><span data-stu-id="c11d8-108">Specify other parameters to limit the jobs that this cmdlet gets.</span></span>

<span data-ttu-id="c11d8-109">Dieses Cmdlet gibt maximal 200-Aufträge zurück.</span><span class="sxs-lookup"><span data-stu-id="c11d8-109">This cmdlet returns a maximum of 200 jobs.</span></span>
<span data-ttu-id="c11d8-110">Wenn mehr als 200-Aufträge vorhanden sind, rufen Sie die verbleibenden Aufträge mithilfe des *First* -und *Skip* -Parameters ab.</span><span class="sxs-lookup"><span data-stu-id="c11d8-110">If more than 200 jobs exist, get the remaining jobs by using the *First* and *Skip* parameters.</span></span>
<span data-ttu-id="c11d8-111">Wenn Sie einen Wert von 100 für *Skip* und 50 für *First* angeben, gibt dieses Cmdlet nicht die ersten 100 Ergebnisse zurück.</span><span class="sxs-lookup"><span data-stu-id="c11d8-111">If you specify a value of 100 for *Skip* and 50 for *First* , this cmdlet does not return the first 100 results.</span></span>
<span data-ttu-id="c11d8-112">Nach dem 100 werden die nächsten 50-Ergebnisse zurückgegeben, die übersprungen werden.</span><span class="sxs-lookup"><span data-stu-id="c11d8-112">It returns the next 50 results after the 100 that it skips.</span></span>

## <span data-ttu-id="c11d8-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c11d8-113">EXAMPLES</span></span>

### <span data-ttu-id="c11d8-114">Beispiel 1: Abrufen eines Auftrags mithilfe einer ID</span><span class="sxs-lookup"><span data-stu-id="c11d8-114">Example 1: Get a job by using an ID</span></span>
```
PS C:\>Get-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d"
BackupPolicy             : 
BackupTimeStamp          : 1/1/0001 12:00:00 AM
BackupType               : CloudSnapshot
DataStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.DataStatistics
Device                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Entity                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
ErrorDetails             : {}
HideProgressDetails      : False
InstanceId               : 574f47e0-44e9-495c-b8a5-0203c57ebf6d
IsInstantRestoreComplete : False
IsJobCancellable         : True
JobDetails               : Microsoft.WindowsAzure.Management.StorSimple.Models.JobStatusInfo
Name                     : 26447caf-59bb-41c9-a028-3224d296c7dc
Progress                 : 100
SourceDevice             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceEntity             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceVolume             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Status                   : Completed
TimeStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeStatistics
Type                     : Backup
Volume                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
```

<span data-ttu-id="c11d8-115">Dieser Befehl ruft Informationen für den Auftrag ab, der die angegebene ID aufweist.</span><span class="sxs-lookup"><span data-stu-id="c11d8-115">This command gets information for the job that has the specified ID.</span></span>

### <span data-ttu-id="c11d8-116">Beispiel 2: Abrufen von Aufträgen mit einem Gerätenamen</span><span class="sxs-lookup"><span data-stu-id="c11d8-116">Example 2: Get jobs by using a device name</span></span>
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "8600-Bravo 001" -First 2
InstanceId                           Type                         Status                                          DeviceName                                      StartTime                                       Progress                                       
----------                           ----                         ------                                          ----------                                      ---------                                       --------                                       
1997c33f-bfcc-4d08-9aba-28068340a1f9 Backup                       Running                                         8600-Bravo 001                                  4/15/2015 1:30:02 PM                            92                                             
85074062-ef6a-408a-b6c9-2a0904bb99ca Backup                       Completed                                       8600-Bravo 001                                  4/15/2015 1:30:02 PM                            100
```

<span data-ttu-id="c11d8-117">Dieser Befehl ruft Informationen zu den Aufträgen für das Gerät mit dem Namen 8600-Bravo 001 ab.</span><span class="sxs-lookup"><span data-stu-id="c11d8-117">This command gets information for the jobs for the device named 8600-Bravo 001.</span></span>
<span data-ttu-id="c11d8-118">Der Befehl ruft die ersten beiden Aufträge für das Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="c11d8-118">The command gets the first two jobs for the device.</span></span>

### <span data-ttu-id="c11d8-119">Beispiel 3: Abrufen von abgeschlossenen Aufträgen</span><span class="sxs-lookup"><span data-stu-id="c11d8-119">Example 3: Get completed jobs</span></span>
```
PS C:\>Get-AzureStorSimpleJob -Status "Completed" -Skip 10 -First 2
```

<span data-ttu-id="c11d8-120">Dieser Befehl ruft abgeschlossene Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="c11d8-120">This command gets completed jobs.</span></span>
<span data-ttu-id="c11d8-121">Der Befehl ruft nur die ersten beiden Aufträge ab, nachdem er die ersten zehn Aufträge übersprungen hat.</span><span class="sxs-lookup"><span data-stu-id="c11d8-121">The command gets only the first two jobs after it skips the first ten jobs.</span></span>

### <span data-ttu-id="c11d8-122">Beispiel 4: Abrufen manueller Backup-Aufträge</span><span class="sxs-lookup"><span data-stu-id="c11d8-122">Example 4: Get manual backup jobs</span></span>
```
PS C:\>Get-AzureStorSimpleJob -Type "ManualBackup"
```

<span data-ttu-id="c11d8-123">Dieser Befehl ruft Aufträge des manuellen Sicherungstyps ab.</span><span class="sxs-lookup"><span data-stu-id="c11d8-123">This command gets jobs of the manual backup type.</span></span>

### <span data-ttu-id="c11d8-124">Beispiel 5: Abrufen von Aufträgen zwischen angegebenen Zeiten</span><span class="sxs-lookup"><span data-stu-id="c11d8-124">Example 5: Get jobs between specified times</span></span>
```
PS C:\>$StartTime = Get-Date -Year 2015 -Month 3 -Day 10
PS C:\> $EndTime = Get-Date -Year 2015 -Month 3 -Day 11 -Hour 12 -Minute 15
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" -From $StartTime -To $EndTime
```

<span data-ttu-id="c11d8-125">Die ersten beiden Befehle erstellen **DateTime** -Objekte mithilfe des Get-Date-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="c11d8-125">The first two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="c11d8-126">Die Befehle speichern die neuen Uhrzeiten in den $StartTime-und $EndTime Variablen.</span><span class="sxs-lookup"><span data-stu-id="c11d8-126">The commands store the new times in the $StartTime and $EndTime variables.</span></span>
<span data-ttu-id="c11d8-127">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="c11d8-127">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="c11d8-128">Der endgültige Befehl ruft Aufträge für das Gerät mit dem Namen Device07 zwischen den in $StartTime und $EndTime gespeicherten Zeiten ab.</span><span class="sxs-lookup"><span data-stu-id="c11d8-128">The final command gets jobs for the device named Device07 between the times stored in $StartTime and $EndTime.</span></span>

## <span data-ttu-id="c11d8-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="c11d8-129">PARAMETERS</span></span>

### <span data-ttu-id="c11d8-130">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="c11d8-130">-DeviceName</span></span>
<span data-ttu-id="c11d8-131">Gibt den Namen eines StorSimple-Geräts an.</span><span class="sxs-lookup"><span data-stu-id="c11d8-131">Specifies the name of a StorSimple device.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11d8-132">-First</span><span class="sxs-lookup"><span data-stu-id="c11d8-132">-First</span></span>
<span data-ttu-id="c11d8-133">Ruft nur die angegebene Anzahl von Objekten ab.</span><span class="sxs-lookup"><span data-stu-id="c11d8-133">Gets only the specified number of objects.</span></span>
<span data-ttu-id="c11d8-134">Geben Sie die Anzahl der abzurufenden Objekte ein.</span><span class="sxs-lookup"><span data-stu-id="c11d8-134">Enter the number of objects to get.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11d8-135">-Ab</span><span class="sxs-lookup"><span data-stu-id="c11d8-135">-From</span></span>
<span data-ttu-id="c11d8-136">Gibt das Startdatum und die Startzeit für die Aufträge an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="c11d8-136">Specifies the start date and time for the jobs that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11d8-137">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="c11d8-137">-InstanceId</span></span>
<span data-ttu-id="c11d8-138">Gibt die ID des abzurufenden Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="c11d8-138">Specifies the ID of the job to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11d8-139">-Profil</span><span class="sxs-lookup"><span data-stu-id="c11d8-139">-Profile</span></span>
<span data-ttu-id="c11d8-140">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="c11d8-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c11d8-141">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="c11d8-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c11d8-142">-Skip</span><span class="sxs-lookup"><span data-stu-id="c11d8-142">-Skip</span></span>
<span data-ttu-id="c11d8-143">Ignoriert die angegebene Anzahl von Objekten und ruft dann die restlichen Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="c11d8-143">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="c11d8-144">Geben Sie die Anzahl der zu überspringenden Objekte ein.</span><span class="sxs-lookup"><span data-stu-id="c11d8-144">Enter the number of objects to skip.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11d8-145">-Status</span><span class="sxs-lookup"><span data-stu-id="c11d8-145">-Status</span></span>
<span data-ttu-id="c11d8-146">Gibt den Status an.</span><span class="sxs-lookup"><span data-stu-id="c11d8-146">Specifies the status.</span></span>
<span data-ttu-id="c11d8-147">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c11d8-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c11d8-148">Ausgeführt</span><span class="sxs-lookup"><span data-stu-id="c11d8-148">Running</span></span>
- <span data-ttu-id="c11d8-149">Abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="c11d8-149">Completed</span></span>
- <span data-ttu-id="c11d8-150">Storniert</span><span class="sxs-lookup"><span data-stu-id="c11d8-150">Cancelled</span></span>
- <span data-ttu-id="c11d8-151">Fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="c11d8-151">Failed</span></span>
- <span data-ttu-id="c11d8-152">Cancelling</span><span class="sxs-lookup"><span data-stu-id="c11d8-152">Canceling</span></span>
- <span data-ttu-id="c11d8-153">CompletedWithErrors</span><span class="sxs-lookup"><span data-stu-id="c11d8-153">CompletedWithErrors</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11d8-154">-To</span><span class="sxs-lookup"><span data-stu-id="c11d8-154">-To</span></span>
<span data-ttu-id="c11d8-155">Gibt das Enddatum und die Endzeit für die Aufträge an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="c11d8-155">Specifies the end date and time for the jobs that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11d8-156">-Typ</span><span class="sxs-lookup"><span data-stu-id="c11d8-156">-Type</span></span>
<span data-ttu-id="c11d8-157">Gibt den Auftragstyp an.</span><span class="sxs-lookup"><span data-stu-id="c11d8-157">Specifies the job type.</span></span>
<span data-ttu-id="c11d8-158">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c11d8-158">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c11d8-159">Backup</span><span class="sxs-lookup"><span data-stu-id="c11d8-159">Backup</span></span>
- <span data-ttu-id="c11d8-160">ManualBackup</span><span class="sxs-lookup"><span data-stu-id="c11d8-160">ManualBackup</span></span>
- <span data-ttu-id="c11d8-161">Wiederherstellungs</span><span class="sxs-lookup"><span data-stu-id="c11d8-161">Restore</span></span>
- <span data-ttu-id="c11d8-162">CloneWorkflow</span><span class="sxs-lookup"><span data-stu-id="c11d8-162">CloneWorkflow</span></span>
- <span data-ttu-id="c11d8-163">DeviceRestore</span><span class="sxs-lookup"><span data-stu-id="c11d8-163">DeviceRestore</span></span>
- <span data-ttu-id="c11d8-164">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="c11d8-164">Update</span></span>
- <span data-ttu-id="c11d8-165">SupportPackage</span><span class="sxs-lookup"><span data-stu-id="c11d8-165">SupportPackage</span></span>
- <span data-ttu-id="c11d8-166">VirtualApplianceProvisioning</span><span class="sxs-lookup"><span data-stu-id="c11d8-166">VirtualApplianceProvisioning</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11d8-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c11d8-167">CommonParameters</span></span>
<span data-ttu-id="c11d8-168">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c11d8-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c11d8-169">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c11d8-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c11d8-170">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c11d8-170">INPUTS</span></span>

### <span data-ttu-id="c11d8-171">Keine</span><span class="sxs-lookup"><span data-stu-id="c11d8-171">None</span></span>
<span data-ttu-id="c11d8-172">Sie können keine Eingabe an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="c11d8-172">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="c11d8-173">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c11d8-173">OUTPUTS</span></span>

### <span data-ttu-id="c11d8-174">IList \<DeviceJobDetails\> , DeviceJobDetails</span><span class="sxs-lookup"><span data-stu-id="c11d8-174">IList\<DeviceJobDetails\>, DeviceJobDetails</span></span>
<span data-ttu-id="c11d8-175">Dieses Cmdlet gibt eine Liste von Auftragsdetail Objekten zurück, oder wenn Sie den *InstanceId* -Parameter angeben, wird ein einzelnes Auftragsdetail Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c11d8-175">This cmdlet returns a list of job details objects, or, if you specify the *InstanceID* parameter, it returns a single job detail object.</span></span>

## <span data-ttu-id="c11d8-176">Notizen</span><span class="sxs-lookup"><span data-stu-id="c11d8-176">NOTES</span></span>

## <span data-ttu-id="c11d8-177">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c11d8-177">RELATED LINKS</span></span>

[<span data-ttu-id="c11d8-178">Stopp-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="c11d8-178">Stop-AzureStorSimpleJob</span></span>](./Stop-AzureStorSimpleJob.md)


