---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 0ce851373ac31aaef4c5664db7085f345e9b947d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844455"
---
# <span data-ttu-id="d8bdd-101">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="d8bdd-101">New-AzVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="d8bdd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d8bdd-102">SYNOPSIS</span></span>
<span data-ttu-id="d8bdd-103">Erstellt ein Konfigurationsobjekt für das automatische Patchen auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="d8bdd-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="d8bdd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8bdd-104">SYNTAX</span></span>

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>]
 [-MaintenanceWindowStartingHour <Int32>] [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="d8bdd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d8bdd-105">DESCRIPTION</span></span>
<span data-ttu-id="d8bdd-106">Mit dem Cmdlet **New-AzVMSqlServerAutoPatchingConfig** wird ein Configuration-Objekt für das automatische Patchen auf einem virtuellen Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="d8bdd-106">The **New-AzVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="d8bdd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d8bdd-107">EXAMPLES</span></span>

### <span data-ttu-id="d8bdd-108">Beispiel 1: Erstellen eines Konfigurationsobjekts zum Konfigurieren des automatischen Patches</span><span class="sxs-lookup"><span data-stu-id="d8bdd-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="d8bdd-109">Mit diesem Befehl wird ein Configuration-Objekt für Patches erstellt.</span><span class="sxs-lookup"><span data-stu-id="d8bdd-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="d8bdd-110">Der Befehl gibt den Wochentag an und definiert das Wartungsfenster.</span><span class="sxs-lookup"><span data-stu-id="d8bdd-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="d8bdd-111">Diese Konfiguration ermöglicht das Patchen, das diese Werte verwendet.</span><span class="sxs-lookup"><span data-stu-id="d8bdd-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="d8bdd-112">Der Befehl speichert das Ergebnis in der $AutoBackupConfig-Variablen.</span><span class="sxs-lookup"><span data-stu-id="d8bdd-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="d8bdd-113">Sie können dieses Konfigurationselement für andere Cmdlets angeben, beispielsweise das Cmdlet "Set-AzVMSqlServerExtension".</span><span class="sxs-lookup"><span data-stu-id="d8bdd-113">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="d8bdd-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8bdd-114">PARAMETERS</span></span>

### <span data-ttu-id="d8bdd-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="d8bdd-115">-DayOfWeek</span></span>
<span data-ttu-id="d8bdd-116">Gibt den Wochentag an, zu dem Updates installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d8bdd-116">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="d8bdd-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d8bdd-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d8bdd-118">Sonntag</span><span class="sxs-lookup"><span data-stu-id="d8bdd-118">Sunday</span></span>
- <span data-ttu-id="d8bdd-119">Montag</span><span class="sxs-lookup"><span data-stu-id="d8bdd-119">Monday</span></span>
- <span data-ttu-id="d8bdd-120">Dienstag</span><span class="sxs-lookup"><span data-stu-id="d8bdd-120">Tuesday</span></span>
- <span data-ttu-id="d8bdd-121">Mittwoch</span><span class="sxs-lookup"><span data-stu-id="d8bdd-121">Wednesday</span></span>
- <span data-ttu-id="d8bdd-122">Donnerstag</span><span class="sxs-lookup"><span data-stu-id="d8bdd-122">Thursday</span></span>
- <span data-ttu-id="d8bdd-123">Freitag</span><span class="sxs-lookup"><span data-stu-id="d8bdd-123">Friday</span></span>
- <span data-ttu-id="d8bdd-124">Samstag</span><span class="sxs-lookup"><span data-stu-id="d8bdd-124">Saturday</span></span>
- <span data-ttu-id="d8bdd-125">Alltags</span><span class="sxs-lookup"><span data-stu-id="d8bdd-125">Everyday</span></span>

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

### <span data-ttu-id="d8bdd-126">-Enable</span><span class="sxs-lookup"><span data-stu-id="d8bdd-126">-Enable</span></span>
<span data-ttu-id="d8bdd-127">Gibt an, dass automatisiertes Patchen für den virtuellen Computer aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d8bdd-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="d8bdd-128">Wenn Sie das automatische Patchen aktivieren, setzt das Cmdlet Windows Update in den interaktiven Modus.</span><span class="sxs-lookup"><span data-stu-id="d8bdd-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="d8bdd-129">Wenn Sie das automatische Patchen deaktivieren, werden die Windows Update-Einstellungen nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="d8bdd-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="d8bdd-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="d8bdd-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="d8bdd-131">Gibt die Dauer in Minuten des Wartungsfensters an.</span><span class="sxs-lookup"><span data-stu-id="d8bdd-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="d8bdd-132">Durch automatisches Patchen wird verhindert, dass eine Aktion ausgeführt wird, die sich auf die Verfügbarkeit einer virtuellen Maschine außerhalb dieses Fensters auswirkt.</span><span class="sxs-lookup"><span data-stu-id="d8bdd-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="d8bdd-133">Geben Sie ein Vielfaches von 30 Minuten an.</span><span class="sxs-lookup"><span data-stu-id="d8bdd-133">Specify a multiple of 30 minutes.</span></span>

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

### <span data-ttu-id="d8bdd-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="d8bdd-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="d8bdd-135">Gibt die Stunde des Tages an, an dem das Wartungsfenster gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="d8bdd-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="d8bdd-136">Dieses Mal wird definiert, wann Updates zu installieren beginnen.</span><span class="sxs-lookup"><span data-stu-id="d8bdd-136">This time defines when updates start to install.</span></span>

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

### <span data-ttu-id="d8bdd-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="d8bdd-137">-PatchCategory</span></span>
<span data-ttu-id="d8bdd-138">Gibt an, ob wichtige Updates enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="d8bdd-138">Specifies whether important updates should be included.</span></span>

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

### <span data-ttu-id="d8bdd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8bdd-139">CommonParameters</span></span>
<span data-ttu-id="d8bdd-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8bdd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8bdd-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8bdd-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8bdd-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d8bdd-142">INPUTS</span></span>

### <span data-ttu-id="d8bdd-143">Keine</span><span class="sxs-lookup"><span data-stu-id="d8bdd-143">None</span></span>
<span data-ttu-id="d8bdd-144">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="d8bdd-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d8bdd-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d8bdd-145">OUTPUTS</span></span>

### <span data-ttu-id="d8bdd-146">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="d8bdd-146">AutoPatchingSettings</span></span>
<span data-ttu-id="d8bdd-147">Dieses Cmdlet gibt das Objekt zurück, das Einstellungen für automatisiertes Patchen enthält.</span><span class="sxs-lookup"><span data-stu-id="d8bdd-147">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="d8bdd-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="d8bdd-148">NOTES</span></span>

## <span data-ttu-id="d8bdd-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d8bdd-149">RELATED LINKS</span></span>

[<span data-ttu-id="d8bdd-150">Neu – AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="d8bdd-150">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="d8bdd-151">Satz-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="d8bdd-151">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


