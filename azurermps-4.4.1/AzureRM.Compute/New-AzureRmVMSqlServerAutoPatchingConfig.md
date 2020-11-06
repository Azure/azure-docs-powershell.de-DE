---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
Module Name: Azure
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 17d99840bffb9063ad61dec00d4b7d5983118399
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505162"
---
# <span data-ttu-id="e3834-101">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="e3834-101">New-AzureVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="e3834-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e3834-102">SYNOPSIS</span></span>
<span data-ttu-id="e3834-103">Erstellt ein Konfigurationsobjekt für das automatische Patchen auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="e3834-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3834-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3834-104">SYNTAX</span></span>

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e3834-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3834-105">DESCRIPTION</span></span>
<span data-ttu-id="e3834-106">Mit dem Cmdlet **New-AzureVMSqlServerAutoPatchingConfig** wird ein Configuration-Objekt für das automatische Patchen auf einem virtuellen Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="e3834-106">The **New-AzureVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="e3834-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e3834-107">EXAMPLES</span></span>

### <span data-ttu-id="e3834-108">Beispiel 1: Erstellen eines Konfigurationsobjekts zum Konfigurieren des automatischen Patches</span><span class="sxs-lookup"><span data-stu-id="e3834-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="e3834-109">Mit diesem Befehl wird ein Configuration-Objekt für Patches erstellt.</span><span class="sxs-lookup"><span data-stu-id="e3834-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="e3834-110">Der Befehl gibt den Wochentag an und definiert das Wartungsfenster.</span><span class="sxs-lookup"><span data-stu-id="e3834-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="e3834-111">Diese Konfiguration ermöglicht das Patchen, das diese Werte verwendet.</span><span class="sxs-lookup"><span data-stu-id="e3834-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="e3834-112">Der Befehl speichert das Ergebnis in der $AutoBackupConfig-Variablen.</span><span class="sxs-lookup"><span data-stu-id="e3834-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="e3834-113">Sie können dieses Konfigurationselement für andere Cmdlets angeben, beispielsweise das Cmdlet "Set-AzureRmVMSqlServerExtension".</span><span class="sxs-lookup"><span data-stu-id="e3834-113">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="e3834-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3834-114">PARAMETERS</span></span>

### <span data-ttu-id="e3834-115">-Enable</span><span class="sxs-lookup"><span data-stu-id="e3834-115">-Enable</span></span>
<span data-ttu-id="e3834-116">Gibt an, dass automatisiertes Patchen für den virtuellen Computer aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e3834-116">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="e3834-117">Wenn Sie das automatische Patchen aktivieren, setzt das Cmdlet Windows Update in den interaktiven Modus.</span><span class="sxs-lookup"><span data-stu-id="e3834-117">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="e3834-118">Wenn Sie das automatische Patchen deaktivieren, werden die Windows Update-Einstellungen nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="e3834-118">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="e3834-119">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="e3834-119">-DayOfWeek</span></span>
<span data-ttu-id="e3834-120">Gibt den Wochentag an, zu dem Updates installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e3834-120">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="e3834-121">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e3834-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e3834-122">Sonntag</span><span class="sxs-lookup"><span data-stu-id="e3834-122">Sunday</span></span>
- <span data-ttu-id="e3834-123">Montag</span><span class="sxs-lookup"><span data-stu-id="e3834-123">Monday</span></span>
- <span data-ttu-id="e3834-124">Dienstag</span><span class="sxs-lookup"><span data-stu-id="e3834-124">Tuesday</span></span>
- <span data-ttu-id="e3834-125">Mittwoch</span><span class="sxs-lookup"><span data-stu-id="e3834-125">Wednesday</span></span>
- <span data-ttu-id="e3834-126">Donnerstag</span><span class="sxs-lookup"><span data-stu-id="e3834-126">Thursday</span></span>
- <span data-ttu-id="e3834-127">Freitag</span><span class="sxs-lookup"><span data-stu-id="e3834-127">Friday</span></span>
- <span data-ttu-id="e3834-128">Samstag</span><span class="sxs-lookup"><span data-stu-id="e3834-128">Saturday</span></span>
- <span data-ttu-id="e3834-129">Alltags</span><span class="sxs-lookup"><span data-stu-id="e3834-129">Everyday</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3834-130">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="e3834-130">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="e3834-131">Gibt die Stunde des Tages an, an dem das Wartungsfenster gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="e3834-131">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="e3834-132">Dieses Mal wird definiert, wann Updates zu installieren beginnen.</span><span class="sxs-lookup"><span data-stu-id="e3834-132">This time defines when updates start to install.</span></span>

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

### <span data-ttu-id="e3834-133">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="e3834-133">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="e3834-134">Gibt die Dauer in Minuten des Wartungsfensters an.</span><span class="sxs-lookup"><span data-stu-id="e3834-134">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="e3834-135">Durch automatisches Patchen wird verhindert, dass eine Aktion ausgeführt wird, die sich auf die Verfügbarkeit einer virtuellen Maschine außerhalb dieses Fensters auswirkt.</span><span class="sxs-lookup"><span data-stu-id="e3834-135">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="e3834-136">Geben Sie ein Vielfaches von 30 Minuten an.</span><span class="sxs-lookup"><span data-stu-id="e3834-136">Specify a multiple of 30 minutes.</span></span>

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

### <span data-ttu-id="e3834-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="e3834-137">-PatchCategory</span></span>
<span data-ttu-id="e3834-138">Gibt an, ob wichtige Updates enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="e3834-138">Specifies whether important updates should be included.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3834-139">-Information</span><span class="sxs-lookup"><span data-stu-id="e3834-139">-InformationAction</span></span>
<span data-ttu-id="e3834-140">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="e3834-140">@{Text=}</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3834-141">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e3834-141">-InformationVariable</span></span>
<span data-ttu-id="e3834-142">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="e3834-142">@{Text=}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3834-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3834-143">CommonParameters</span></span>
<span data-ttu-id="e3834-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3834-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3834-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3834-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3834-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e3834-146">INPUTS</span></span>

## <span data-ttu-id="e3834-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e3834-147">OUTPUTS</span></span>

### <span data-ttu-id="e3834-148">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="e3834-148">AutoPatchingSettings</span></span>
<span data-ttu-id="e3834-149">Dieses Cmdlet gibt das Objekt zurück, das Einstellungen für automatisiertes Patchen enthält.</span><span class="sxs-lookup"><span data-stu-id="e3834-149">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="e3834-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="e3834-150">NOTES</span></span>

## <span data-ttu-id="e3834-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e3834-151">RELATED LINKS</span></span>

[<span data-ttu-id="e3834-152">Neu – AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="e3834-152">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="e3834-153">Satz-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="e3834-153">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


