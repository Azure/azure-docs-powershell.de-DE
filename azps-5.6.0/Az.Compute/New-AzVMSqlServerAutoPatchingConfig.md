---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 3433d6bf5d3886978b75024e34c873e38230212b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944237"
---
# <span data-ttu-id="80d34-101">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="80d34-101">New-AzVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="80d34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80d34-102">SYNOPSIS</span></span>
<span data-ttu-id="80d34-103">Erstellt ein Konfigurationsobjekt für das automatische Patchen auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="80d34-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="80d34-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="80d34-104">SYNTAX</span></span>

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## <span data-ttu-id="80d34-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="80d34-105">DESCRIPTION</span></span>
<span data-ttu-id="80d34-106">Das **Cmdlet New-AzVMSqlServerAutoPatchingConfig** erstellt ein Konfigurationsobjekt für das automatische Patchen auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="80d34-106">The **New-AzVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="80d34-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="80d34-107">EXAMPLES</span></span>

### <span data-ttu-id="80d34-108">Beispiel 1: Erstellen eines Konfigurationsobjekts zum Konfigurieren des automatischen Patchens</span><span class="sxs-lookup"><span data-stu-id="80d34-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="80d34-109">Mit diesem Befehl wird ein Konfigurationsobjekt zum Patchen erstellt.</span><span class="sxs-lookup"><span data-stu-id="80d34-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="80d34-110">Der Befehl gibt den Wochentag und das Wartungsfenster an.</span><span class="sxs-lookup"><span data-stu-id="80d34-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="80d34-111">Diese Konfiguration ermöglicht das Patchen, das diese Werte verwendet.</span><span class="sxs-lookup"><span data-stu-id="80d34-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="80d34-112">Der Befehl speichert das Ergebnis in der $AutoBackupConfig Variablen.</span><span class="sxs-lookup"><span data-stu-id="80d34-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="80d34-113">Sie können dieses Konfigurationselement für andere Cmdlets angeben, z. B. Set-AzVMSqlServerExtension cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80d34-113">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="80d34-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="80d34-114">PARAMETERS</span></span>

### <span data-ttu-id="80d34-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="80d34-115">-DayOfWeek</span></span>
<span data-ttu-id="80d34-116">Gibt den Wochentag an, an dem Updates installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="80d34-116">Specifies the day of the week when updates should be installed.</span></span>
<span data-ttu-id="80d34-117">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="80d34-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="80d34-118">Sonntag</span><span class="sxs-lookup"><span data-stu-id="80d34-118">Sunday</span></span>
- <span data-ttu-id="80d34-119">Montag</span><span class="sxs-lookup"><span data-stu-id="80d34-119">Monday</span></span>
- <span data-ttu-id="80d34-120">Dienstag</span><span class="sxs-lookup"><span data-stu-id="80d34-120">Tuesday</span></span>
- <span data-ttu-id="80d34-121">Mittwoch</span><span class="sxs-lookup"><span data-stu-id="80d34-121">Wednesday</span></span>
- <span data-ttu-id="80d34-122">Donnerstag</span><span class="sxs-lookup"><span data-stu-id="80d34-122">Thursday</span></span>
- <span data-ttu-id="80d34-123">Freitag</span><span class="sxs-lookup"><span data-stu-id="80d34-123">Friday</span></span>
- <span data-ttu-id="80d34-124">Samstag</span><span class="sxs-lookup"><span data-stu-id="80d34-124">Saturday</span></span>
- <span data-ttu-id="80d34-125">Jeden Tag</span><span class="sxs-lookup"><span data-stu-id="80d34-125">Everyday</span></span>

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

### <span data-ttu-id="80d34-126">-Enable</span><span class="sxs-lookup"><span data-stu-id="80d34-126">-Enable</span></span>
<span data-ttu-id="80d34-127">Gibt an, dass das automatische Patchen für den virtuellen Computer aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="80d34-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="80d34-128">Wenn Sie das automatische Patchen aktivieren, versetzt das Cmdlet Windows Update in den interaktiven Modus.</span><span class="sxs-lookup"><span data-stu-id="80d34-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="80d34-129">Wenn Sie das automatische Patchen deaktivieren, werden die Windows Update-Einstellungen nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="80d34-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="80d34-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="80d34-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="80d34-131">Gibt die Dauer des Wartungsfensters in Minuten an.</span><span class="sxs-lookup"><span data-stu-id="80d34-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="80d34-132">Automatisches Patchen verhindert das Ausführen einer Aktion, die sich auf die Verfügbarkeit eines virtuellen Computers außerhalb dieses Fensters auswirken kann.</span><span class="sxs-lookup"><span data-stu-id="80d34-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="80d34-133">Geben Sie ein Vielfaches von 30 Minuten an.</span><span class="sxs-lookup"><span data-stu-id="80d34-133">Specify a multiple of 30 minutes.</span></span>

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

### <span data-ttu-id="80d34-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="80d34-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="80d34-135">Gibt die Stunde des Tages an, zu der das Wartungsfenster beginnt.</span><span class="sxs-lookup"><span data-stu-id="80d34-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="80d34-136">Dieses Mal wird festgelegt, wann Updates mit der Installation beginnen.</span><span class="sxs-lookup"><span data-stu-id="80d34-136">This time defines when updates start to install.</span></span>

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

### <span data-ttu-id="80d34-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="80d34-137">-PatchCategory</span></span>
<span data-ttu-id="80d34-138">Gibt an, ob wichtige Updates einbezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="80d34-138">Specifies whether important updates should be included.</span></span>

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

### <span data-ttu-id="80d34-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80d34-139">CommonParameters</span></span>
<span data-ttu-id="80d34-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80d34-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80d34-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80d34-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80d34-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="80d34-142">INPUTS</span></span>

### <span data-ttu-id="80d34-143">Keine</span><span class="sxs-lookup"><span data-stu-id="80d34-143">None</span></span>

## <span data-ttu-id="80d34-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="80d34-144">OUTPUTS</span></span>

### <span data-ttu-id="80d34-145">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="80d34-145">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

## <span data-ttu-id="80d34-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="80d34-146">NOTES</span></span>

## <span data-ttu-id="80d34-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="80d34-147">RELATED LINKS</span></span>

[<span data-ttu-id="80d34-148">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="80d34-148">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="80d34-149">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="80d34-149">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


