---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7317DAC1-B535-4650-86BF-73E96F61EECD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23bb8e09fac8ec4fe0e8ff5b3c23ab995f03694c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006397"
---
# <span data-ttu-id="e5f50-101">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="e5f50-101">New-AzureVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="e5f50-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e5f50-102">SYNOPSIS</span></span>
<span data-ttu-id="e5f50-103">Erstellt ein Konfigurationsobjekt für das automatische Patchen virtueller Maschinen.</span><span class="sxs-lookup"><span data-stu-id="e5f50-103">Creates a configuration object for virtual machine automatic patching.</span></span>

## <span data-ttu-id="e5f50-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5f50-104">SYNTAX</span></span>

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e5f50-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5f50-105">DESCRIPTION</span></span>
<span data-ttu-id="e5f50-106">Das Cmdlet **New-AzureVMSqlServerAutoPatchingConfig** erstellt ein Configuration-Objekt für das automatische Patchen virtueller Maschinen.</span><span class="sxs-lookup"><span data-stu-id="e5f50-106">The **New-AzureVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for virtual machine automatic patching.</span></span>

## <span data-ttu-id="e5f50-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e5f50-107">EXAMPLES</span></span>

### <span data-ttu-id="e5f50-108">Beispiel 1: Erstellen eines Konfigurationsobjekts zum Konfigurieren des automatischen Patches</span><span class="sxs-lookup"><span data-stu-id="e5f50-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $APS = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
          Enable                        : True
          DayOfWeek                     : Thursday
          MaintenanceWindowStartingHour : 11
          MaintenanceWindowDuration     : 120
          PatchCategory                 : Important
```

<span data-ttu-id="e5f50-109">Mit diesem Befehl wird ein Configuration-Objekt erstellt, mit dem das automatische Patchen mithilfe von AzureVMSqlServerExtension konfiguriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="e5f50-109">This command creates configuration object that can be used to configure automatic patching using Set-AzureVMSqlServerExtension.</span></span>

## <span data-ttu-id="e5f50-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5f50-110">PARAMETERS</span></span>

### <span data-ttu-id="e5f50-111">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="e5f50-111">-DayOfWeek</span></span>
<span data-ttu-id="e5f50-112">Gibt den Wochentag an, zu dem Updates installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e5f50-112">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="e5f50-113">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e5f50-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e5f50-114">Sonntag</span><span class="sxs-lookup"><span data-stu-id="e5f50-114">Sunday</span></span>
- <span data-ttu-id="e5f50-115">Montag</span><span class="sxs-lookup"><span data-stu-id="e5f50-115">Monday</span></span>
- <span data-ttu-id="e5f50-116">Dienstag</span><span class="sxs-lookup"><span data-stu-id="e5f50-116">Tuesday</span></span>
- <span data-ttu-id="e5f50-117">Mittwoch</span><span class="sxs-lookup"><span data-stu-id="e5f50-117">Wednesday</span></span>
- <span data-ttu-id="e5f50-118">Donnerstag</span><span class="sxs-lookup"><span data-stu-id="e5f50-118">Thursday</span></span>
- <span data-ttu-id="e5f50-119">Freitag</span><span class="sxs-lookup"><span data-stu-id="e5f50-119">Friday</span></span>
- <span data-ttu-id="e5f50-120">Samstag</span><span class="sxs-lookup"><span data-stu-id="e5f50-120">Saturday</span></span>
- <span data-ttu-id="e5f50-121">Alltags</span><span class="sxs-lookup"><span data-stu-id="e5f50-121">Everyday</span></span>

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

### <span data-ttu-id="e5f50-122">-Enable</span><span class="sxs-lookup"><span data-stu-id="e5f50-122">-Enable</span></span>
<span data-ttu-id="e5f50-123">Gibt an, dass automatisiertes Patchen für den virtuellen Computer aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e5f50-123">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="e5f50-124">Wenn Sie das automatische Patchen aktivieren, wird Windows Update vom Cmdlet in den interaktiven Modus versetzt.</span><span class="sxs-lookup"><span data-stu-id="e5f50-124">If you enable automated patching the cmdlet will put Windows Update into interactive mode.</span></span>
<span data-ttu-id="e5f50-125">Wenn Sie das automatische Patchen deaktivieren, werden die Windows Update-Einstellungen nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="e5f50-125">If you disable automated patching, Windows Update settings will not change.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5f50-126">-Information</span><span class="sxs-lookup"><span data-stu-id="e5f50-126">-InformationAction</span></span>
<span data-ttu-id="e5f50-127">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="e5f50-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e5f50-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e5f50-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e5f50-129">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="e5f50-129">Continue</span></span>
- <span data-ttu-id="e5f50-130">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="e5f50-130">Ignore</span></span>
- <span data-ttu-id="e5f50-131">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="e5f50-131">Inquire</span></span>
- <span data-ttu-id="e5f50-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e5f50-132">SilentlyContinue</span></span>
- <span data-ttu-id="e5f50-133">Beenden</span><span class="sxs-lookup"><span data-stu-id="e5f50-133">Stop</span></span>
- <span data-ttu-id="e5f50-134">Anhalten</span><span class="sxs-lookup"><span data-stu-id="e5f50-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5f50-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e5f50-135">-InformationVariable</span></span>
<span data-ttu-id="e5f50-136">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="e5f50-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5f50-137">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="e5f50-137">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="e5f50-138">Gibt die Dauer des Wartungsfensters an.</span><span class="sxs-lookup"><span data-stu-id="e5f50-138">Specifies the duration of the maintenance window.</span></span>
<span data-ttu-id="e5f50-139">Durch automatisches Patchen wird eine Aktion verhindert, die sich auf die Verfügbarkeit eines virtuellen Computers außerhalb dieses Fensters auswirken kann.</span><span class="sxs-lookup"><span data-stu-id="e5f50-139">Automated patching will avoid performing an action that can impact a virtual machine availability outside of that window.</span></span>
<span data-ttu-id="e5f50-140">Es sind nur 30 Minuten Inkremente zulässig.</span><span class="sxs-lookup"><span data-stu-id="e5f50-140">Only 30 minutes increments are allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5f50-141">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="e5f50-141">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="e5f50-142">Gibt die Stunde des Tages an, an dem das Wartungsfenster gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="e5f50-142">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="e5f50-143">Dieses Mal wird definiert, wann Updates mit der Installation beginnen und auf die Stunde gerundet werden.</span><span class="sxs-lookup"><span data-stu-id="e5f50-143">This time defines when updates start installing and is rounded to the hour.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5f50-144">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="e5f50-144">-PatchCategory</span></span>
<span data-ttu-id="e5f50-145">Gibt an, ob wichtige Updates enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="e5f50-145">Specifies whether important updates should be included.</span></span>

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

### <span data-ttu-id="e5f50-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5f50-146">CommonParameters</span></span>
<span data-ttu-id="e5f50-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5f50-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5f50-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5f50-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5f50-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e5f50-149">INPUTS</span></span>

## <span data-ttu-id="e5f50-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e5f50-150">OUTPUTS</span></span>

### <span data-ttu-id="e5f50-151">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="e5f50-151">AutoPatchingSettings</span></span>
<span data-ttu-id="e5f50-152">Dieses Cmdlet gibt das Objekt zurück, das Einstellungen für automatisiertes Patchen enthält.</span><span class="sxs-lookup"><span data-stu-id="e5f50-152">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="e5f50-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="e5f50-153">NOTES</span></span>

## <span data-ttu-id="e5f50-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e5f50-154">RELATED LINKS</span></span>

[<span data-ttu-id="e5f50-155">Satz-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="e5f50-155">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)

[<span data-ttu-id="e5f50-156">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="e5f50-156">Remove-AzureVMSqlServerExtension</span></span>](./Remove-AzureVMSqlServerExtension.md)

[<span data-ttu-id="e5f50-157">Satz-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="e5f50-157">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)


