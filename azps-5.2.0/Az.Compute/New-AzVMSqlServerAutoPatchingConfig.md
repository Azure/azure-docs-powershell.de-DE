---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 6fe89822af5be532674e22dd3e1c1edd583fced4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293698"
---
# <span data-ttu-id="e87cf-101">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="e87cf-101">New-AzVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="e87cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e87cf-102">SYNOPSIS</span></span>
<span data-ttu-id="e87cf-103">Erstellt ein Konfigurationsobjekt für das automatische Patchen auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="e87cf-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="e87cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e87cf-104">SYNTAX</span></span>

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## <span data-ttu-id="e87cf-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e87cf-105">DESCRIPTION</span></span>
<span data-ttu-id="e87cf-106">Das **Cmdlet "New-AzVMSqlServerAutoPatchingConfig"** erstellt ein Konfigurationsobjekt für das automatische Patchen auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="e87cf-106">The **New-AzVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="e87cf-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e87cf-107">EXAMPLES</span></span>

### <span data-ttu-id="e87cf-108">Beispiel 1: Erstellen eines Konfigurationsobjekts zum Konfigurieren des automatischen Patchens</span><span class="sxs-lookup"><span data-stu-id="e87cf-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="e87cf-109">Mit diesem Befehl wird ein Konfigurationsobjekt zum Patchen erstellt.</span><span class="sxs-lookup"><span data-stu-id="e87cf-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="e87cf-110">Der Befehl gibt den Wochentag an und definiert das Wartungsfenster.</span><span class="sxs-lookup"><span data-stu-id="e87cf-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="e87cf-111">Diese Konfiguration ermöglicht Patching, das diese Werte verwendet.</span><span class="sxs-lookup"><span data-stu-id="e87cf-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="e87cf-112">Der Befehl speichert das Ergebnis in der $AutoBackupConfig Variable.</span><span class="sxs-lookup"><span data-stu-id="e87cf-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="e87cf-113">Sie können dieses Konfigurationselement für andere Cmdlets angeben, z. B. Set-AzVMSqlServerExtension Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e87cf-113">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="e87cf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e87cf-114">PARAMETERS</span></span>

### <span data-ttu-id="e87cf-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="e87cf-115">-DayOfWeek</span></span>
<span data-ttu-id="e87cf-116">Gibt den Wochentag an, an dem Updates installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e87cf-116">Specifies the day of the week when updates should be installed.</span></span>
<span data-ttu-id="e87cf-117">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="e87cf-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e87cf-118">Sonntag</span><span class="sxs-lookup"><span data-stu-id="e87cf-118">Sunday</span></span>
- <span data-ttu-id="e87cf-119">Montag</span><span class="sxs-lookup"><span data-stu-id="e87cf-119">Monday</span></span>
- <span data-ttu-id="e87cf-120">Dienstag</span><span class="sxs-lookup"><span data-stu-id="e87cf-120">Tuesday</span></span>
- <span data-ttu-id="e87cf-121">Mittwoch</span><span class="sxs-lookup"><span data-stu-id="e87cf-121">Wednesday</span></span>
- <span data-ttu-id="e87cf-122">Donnerstag</span><span class="sxs-lookup"><span data-stu-id="e87cf-122">Thursday</span></span>
- <span data-ttu-id="e87cf-123">Freitag</span><span class="sxs-lookup"><span data-stu-id="e87cf-123">Friday</span></span>
- <span data-ttu-id="e87cf-124">Samstag</span><span class="sxs-lookup"><span data-stu-id="e87cf-124">Saturday</span></span>
- <span data-ttu-id="e87cf-125">Jeden Tag</span><span class="sxs-lookup"><span data-stu-id="e87cf-125">Everyday</span></span>

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

### <span data-ttu-id="e87cf-126">-Enable</span><span class="sxs-lookup"><span data-stu-id="e87cf-126">-Enable</span></span>
<span data-ttu-id="e87cf-127">Gibt an, dass automatisches Patchen für den virtuellen Computer aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e87cf-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="e87cf-128">Wenn Sie automatisches Patchen aktivieren, versetzt das Cmdlet Windows Update in den interaktiven Modus.</span><span class="sxs-lookup"><span data-stu-id="e87cf-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="e87cf-129">Wenn Sie das automatische Patchen deaktivieren, ändern sich die Windows Update-Einstellungen nicht.</span><span class="sxs-lookup"><span data-stu-id="e87cf-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="e87cf-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="e87cf-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="e87cf-131">Gibt die Dauer (in Minuten) des Wartungsfensters an.</span><span class="sxs-lookup"><span data-stu-id="e87cf-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="e87cf-132">Automatisches Patchen verhindert das Ausführen einer Aktion, die sich auf die Verfügbarkeit eines virtuellen Computers außerhalb dieses Fensters auswirken kann.</span><span class="sxs-lookup"><span data-stu-id="e87cf-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="e87cf-133">Geben Sie ein Vielfaches von 30 Minuten an.</span><span class="sxs-lookup"><span data-stu-id="e87cf-133">Specify a multiple of 30 minutes.</span></span>

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

### <span data-ttu-id="e87cf-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="e87cf-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="e87cf-135">Gibt die Stunde des Tages an, zu der das Wartungsfenster gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="e87cf-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="e87cf-136">Dieses Mal wird festgelegt, wann updates mit der Installation beginnen.</span><span class="sxs-lookup"><span data-stu-id="e87cf-136">This time defines when updates start to install.</span></span>

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

### <span data-ttu-id="e87cf-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="e87cf-137">-PatchCategory</span></span>
<span data-ttu-id="e87cf-138">Gibt an, ob wichtige Updates einbezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e87cf-138">Specifies whether important updates should be included.</span></span>

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

### <span data-ttu-id="e87cf-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e87cf-139">CommonParameters</span></span>
<span data-ttu-id="e87cf-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e87cf-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e87cf-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e87cf-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e87cf-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e87cf-142">INPUTS</span></span>

### <span data-ttu-id="e87cf-143">Keine</span><span class="sxs-lookup"><span data-stu-id="e87cf-143">None</span></span>

## <span data-ttu-id="e87cf-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e87cf-144">OUTPUTS</span></span>

### <span data-ttu-id="e87cf-145">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="e87cf-145">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

## <span data-ttu-id="e87cf-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e87cf-146">NOTES</span></span>

## <span data-ttu-id="e87cf-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e87cf-147">RELATED LINKS</span></span>

[<span data-ttu-id="e87cf-148">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="e87cf-148">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="e87cf-149">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="e87cf-149">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


