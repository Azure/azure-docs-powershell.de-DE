---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 6fe89822af5be532674e22dd3e1c1edd583fced4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008617"
---
# <span data-ttu-id="037c9-101">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="037c9-101">New-AzVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="037c9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="037c9-102">SYNOPSIS</span></span>
<span data-ttu-id="037c9-103">Erstellt ein Konfigurationsobjekt für das automatische Patchen auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="037c9-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="037c9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="037c9-104">SYNTAX</span></span>

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## <span data-ttu-id="037c9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="037c9-105">DESCRIPTION</span></span>
<span data-ttu-id="037c9-106">Mit dem Cmdlet **New-AzVMSqlServerAutoPatchingConfig** wird ein Configuration-Objekt für das automatische Patchen auf einem virtuellen Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="037c9-106">The **New-AzVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="037c9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="037c9-107">EXAMPLES</span></span>

### <span data-ttu-id="037c9-108">Beispiel 1: Erstellen eines Konfigurationsobjekts zum Konfigurieren des automatischen Patches</span><span class="sxs-lookup"><span data-stu-id="037c9-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="037c9-109">Mit diesem Befehl wird ein Configuration-Objekt für Patches erstellt.</span><span class="sxs-lookup"><span data-stu-id="037c9-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="037c9-110">Der Befehl gibt den Wochentag an und definiert das Wartungsfenster.</span><span class="sxs-lookup"><span data-stu-id="037c9-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="037c9-111">Diese Konfiguration ermöglicht das Patchen, das diese Werte verwendet.</span><span class="sxs-lookup"><span data-stu-id="037c9-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="037c9-112">Der Befehl speichert das Ergebnis in der $AutoBackupConfig-Variablen.</span><span class="sxs-lookup"><span data-stu-id="037c9-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="037c9-113">Sie können dieses Konfigurationselement für andere Cmdlets angeben, beispielsweise das Cmdlet "Set-AzVMSqlServerExtension".</span><span class="sxs-lookup"><span data-stu-id="037c9-113">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="037c9-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="037c9-114">PARAMETERS</span></span>

### <span data-ttu-id="037c9-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="037c9-115">-DayOfWeek</span></span>
<span data-ttu-id="037c9-116">Gibt den Wochentag an, zu dem Updates installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="037c9-116">Specifies the day of the week when updates should be installed.</span></span>
<span data-ttu-id="037c9-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="037c9-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="037c9-118">Sonntag</span><span class="sxs-lookup"><span data-stu-id="037c9-118">Sunday</span></span>
- <span data-ttu-id="037c9-119">Montag</span><span class="sxs-lookup"><span data-stu-id="037c9-119">Monday</span></span>
- <span data-ttu-id="037c9-120">Dienstag</span><span class="sxs-lookup"><span data-stu-id="037c9-120">Tuesday</span></span>
- <span data-ttu-id="037c9-121">Mittwoch</span><span class="sxs-lookup"><span data-stu-id="037c9-121">Wednesday</span></span>
- <span data-ttu-id="037c9-122">Donnerstag</span><span class="sxs-lookup"><span data-stu-id="037c9-122">Thursday</span></span>
- <span data-ttu-id="037c9-123">Freitag</span><span class="sxs-lookup"><span data-stu-id="037c9-123">Friday</span></span>
- <span data-ttu-id="037c9-124">Samstag</span><span class="sxs-lookup"><span data-stu-id="037c9-124">Saturday</span></span>
- <span data-ttu-id="037c9-125">Alltags</span><span class="sxs-lookup"><span data-stu-id="037c9-125">Everyday</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="037c9-126">-Enable</span><span class="sxs-lookup"><span data-stu-id="037c9-126">-Enable</span></span>
<span data-ttu-id="037c9-127">Gibt an, dass automatisiertes Patchen für den virtuellen Computer aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="037c9-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="037c9-128">Wenn Sie das automatische Patchen aktivieren, setzt das Cmdlet Windows Update in den interaktiven Modus.</span><span class="sxs-lookup"><span data-stu-id="037c9-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="037c9-129">Wenn Sie das automatische Patchen deaktivieren, werden die Windows Update-Einstellungen nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="037c9-129">If you disable automated patching, Windows Update settings do not change.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="037c9-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="037c9-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="037c9-131">Gibt die Dauer in Minuten des Wartungsfensters an.</span><span class="sxs-lookup"><span data-stu-id="037c9-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="037c9-132">Durch automatisches Patchen wird verhindert, dass eine Aktion ausgeführt wird, die sich auf die Verfügbarkeit einer virtuellen Maschine außerhalb dieses Fensters auswirkt.</span><span class="sxs-lookup"><span data-stu-id="037c9-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="037c9-133">Geben Sie ein Vielfaches von 30 Minuten an.</span><span class="sxs-lookup"><span data-stu-id="037c9-133">Specify a multiple of 30 minutes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="037c9-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="037c9-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="037c9-135">Gibt die Stunde des Tages an, an dem das Wartungsfenster gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="037c9-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="037c9-136">Dieses Mal wird definiert, wann Updates zu installieren beginnen.</span><span class="sxs-lookup"><span data-stu-id="037c9-136">This time defines when updates start to install.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="037c9-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="037c9-137">-PatchCategory</span></span>
<span data-ttu-id="037c9-138">Gibt an, ob wichtige Updates enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="037c9-138">Specifies whether important updates should be included.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Important

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="037c9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="037c9-139">CommonParameters</span></span>
<span data-ttu-id="037c9-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="037c9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="037c9-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="037c9-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="037c9-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="037c9-142">INPUTS</span></span>

### <span data-ttu-id="037c9-143">Keine</span><span class="sxs-lookup"><span data-stu-id="037c9-143">None</span></span>

## <span data-ttu-id="037c9-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="037c9-144">OUTPUTS</span></span>

### <span data-ttu-id="037c9-145">Microsoft. Azure. Commands. Compute. AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="037c9-145">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

## <span data-ttu-id="037c9-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="037c9-146">NOTES</span></span>

## <span data-ttu-id="037c9-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="037c9-147">RELATED LINKS</span></span>

[<span data-ttu-id="037c9-148">Neu – AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="037c9-148">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="037c9-149">Satz-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="037c9-149">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


