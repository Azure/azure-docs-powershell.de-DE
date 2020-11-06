---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 516192dab6d075979a2d78cea72afaedb7a18231
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483113"
---
# <span data-ttu-id="2eabd-101">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="2eabd-101">New-AzureVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="2eabd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2eabd-102">SYNOPSIS</span></span>
<span data-ttu-id="2eabd-103">Erstellt ein Konfigurationsobjekt für das automatische Patchen auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="2eabd-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2eabd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2eabd-104">SYNTAX</span></span>

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## <span data-ttu-id="2eabd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2eabd-105">DESCRIPTION</span></span>
<span data-ttu-id="2eabd-106">Mit dem Cmdlet **New-AzureVMSqlServerAutoPatchingConfig** wird ein Configuration-Objekt für das automatische Patchen auf einem virtuellen Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="2eabd-106">The **New-AzureVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="2eabd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2eabd-107">EXAMPLES</span></span>

### <span data-ttu-id="2eabd-108">Beispiel 1: Erstellen eines Konfigurationsobjekts zum Konfigurieren des automatischen Patches</span><span class="sxs-lookup"><span data-stu-id="2eabd-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="2eabd-109">Mit diesem Befehl wird ein Configuration-Objekt für Patches erstellt.</span><span class="sxs-lookup"><span data-stu-id="2eabd-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="2eabd-110">Der Befehl gibt den Wochentag an und definiert das Wartungsfenster.</span><span class="sxs-lookup"><span data-stu-id="2eabd-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="2eabd-111">Diese Konfiguration ermöglicht das Patchen, das diese Werte verwendet.</span><span class="sxs-lookup"><span data-stu-id="2eabd-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="2eabd-112">Der Befehl speichert das Ergebnis in der $AutoBackupConfig-Variablen.</span><span class="sxs-lookup"><span data-stu-id="2eabd-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="2eabd-113">Sie können dieses Konfigurationselement für andere Cmdlets angeben, beispielsweise das Cmdlet "Set-AzureRmVMSqlServerExtension".</span><span class="sxs-lookup"><span data-stu-id="2eabd-113">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="2eabd-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2eabd-114">PARAMETERS</span></span>

### <span data-ttu-id="2eabd-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="2eabd-115">-DayOfWeek</span></span>
<span data-ttu-id="2eabd-116">Gibt den Wochentag an, zu dem Updates installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2eabd-116">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="2eabd-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2eabd-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2eabd-118">Sonntag</span><span class="sxs-lookup"><span data-stu-id="2eabd-118">Sunday</span></span>
- <span data-ttu-id="2eabd-119">Montag</span><span class="sxs-lookup"><span data-stu-id="2eabd-119">Monday</span></span>
- <span data-ttu-id="2eabd-120">Dienstag</span><span class="sxs-lookup"><span data-stu-id="2eabd-120">Tuesday</span></span>
- <span data-ttu-id="2eabd-121">Mittwoch</span><span class="sxs-lookup"><span data-stu-id="2eabd-121">Wednesday</span></span>
- <span data-ttu-id="2eabd-122">Donnerstag</span><span class="sxs-lookup"><span data-stu-id="2eabd-122">Thursday</span></span>
- <span data-ttu-id="2eabd-123">Freitag</span><span class="sxs-lookup"><span data-stu-id="2eabd-123">Friday</span></span>
- <span data-ttu-id="2eabd-124">Samstag</span><span class="sxs-lookup"><span data-stu-id="2eabd-124">Saturday</span></span>
- <span data-ttu-id="2eabd-125">Alltags</span><span class="sxs-lookup"><span data-stu-id="2eabd-125">Everyday</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eabd-126">-Enable</span><span class="sxs-lookup"><span data-stu-id="2eabd-126">-Enable</span></span>
<span data-ttu-id="2eabd-127">Gibt an, dass automatisiertes Patchen für den virtuellen Computer aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2eabd-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="2eabd-128">Wenn Sie das automatische Patchen aktivieren, setzt das Cmdlet Windows Update in den interaktiven Modus.</span><span class="sxs-lookup"><span data-stu-id="2eabd-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="2eabd-129">Wenn Sie das automatische Patchen deaktivieren, werden die Windows Update-Einstellungen nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="2eabd-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="2eabd-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="2eabd-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="2eabd-131">Gibt die Dauer in Minuten des Wartungsfensters an.</span><span class="sxs-lookup"><span data-stu-id="2eabd-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="2eabd-132">Durch automatisches Patchen wird verhindert, dass eine Aktion ausgeführt wird, die sich auf die Verfügbarkeit einer virtuellen Maschine außerhalb dieses Fensters auswirkt.</span><span class="sxs-lookup"><span data-stu-id="2eabd-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="2eabd-133">Geben Sie ein Vielfaches von 30 Minuten an.</span><span class="sxs-lookup"><span data-stu-id="2eabd-133">Specify a multiple of 30 minutes.</span></span>

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

### <span data-ttu-id="2eabd-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="2eabd-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="2eabd-135">Gibt die Stunde des Tages an, an dem das Wartungsfenster gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="2eabd-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="2eabd-136">Dieses Mal wird definiert, wann Updates zu installieren beginnen.</span><span class="sxs-lookup"><span data-stu-id="2eabd-136">This time defines when updates start to install.</span></span>

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

### <span data-ttu-id="2eabd-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="2eabd-137">-PatchCategory</span></span>
<span data-ttu-id="2eabd-138">Gibt an, ob wichtige Updates enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="2eabd-138">Specifies whether important updates should be included.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Important

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eabd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eabd-139">CommonParameters</span></span>
<span data-ttu-id="2eabd-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eabd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eabd-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2eabd-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eabd-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2eabd-142">INPUTS</span></span>

### <span data-ttu-id="2eabd-143">Keine</span><span class="sxs-lookup"><span data-stu-id="2eabd-143">None</span></span>
<span data-ttu-id="2eabd-144">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="2eabd-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2eabd-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2eabd-145">OUTPUTS</span></span>

### <span data-ttu-id="2eabd-146">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="2eabd-146">AutoPatchingSettings</span></span>
<span data-ttu-id="2eabd-147">Dieses Cmdlet gibt das Objekt zurück, das Einstellungen für automatisiertes Patchen enthält.</span><span class="sxs-lookup"><span data-stu-id="2eabd-147">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="2eabd-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="2eabd-148">NOTES</span></span>

## <span data-ttu-id="2eabd-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2eabd-149">RELATED LINKS</span></span>

[<span data-ttu-id="2eabd-150">Neu – AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="2eabd-150">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="2eabd-151">Satz-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="2eabd-151">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


