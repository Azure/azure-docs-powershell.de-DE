---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: cfa7fc38fa8c7b66347ae3632b6d1ea94ca07c86
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159305"
---
# <span data-ttu-id="3874e-101">New-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="3874e-101">New-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="3874e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3874e-102">SYNOPSIS</span></span>
<span data-ttu-id="3874e-103">Erstellt eine neue Azure NetApp Files (ANF)-Momentaufnahmerichtlinie für ein ANF-Konto.</span><span class="sxs-lookup"><span data-stu-id="3874e-103">Creates a new Azure NetApp Files (ANF) snapshot policy for an ANF account.</span></span>

## <span data-ttu-id="3874e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3874e-104">SYNTAX</span></span>

### <span data-ttu-id="3874e-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3874e-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled] -HourlySchedule <PSNetAppFilesHourlySchedule>
 -DailySchedule <PSNetAppFilesDailySchedule> -WeeklySchedule <PSNetAppFilesWeeklySchedule>
 -MonthlySchedule <PSNetAppFilesMonthlySchedule> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3874e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3874e-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshotPolicy -Name <String> [-Enabled] -HourlySchedule <PSNetAppFilesHourlySchedule>
 -DailySchedule <PSNetAppFilesDailySchedule> -WeeklySchedule <PSNetAppFilesWeeklySchedule>
 -MonthlySchedule <PSNetAppFilesMonthlySchedule> [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3874e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3874e-107">DESCRIPTION</span></span>
<span data-ttu-id="3874e-108">Das **Cmdlet "New-AzNetAppFilesActiveDirectory"** erstellt eine neue Momentaufnahmerichtlinie für ein ANF-Konto.</span><span class="sxs-lookup"><span data-stu-id="3874e-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new snapshot policy for an ANF account.</span></span>

## <span data-ttu-id="3874e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3874e-109">EXAMPLES</span></span>

### <span data-ttu-id="3874e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3874e-110">Example 1</span></span>
```powershell
$hourlySchedule = @{        
        Minute = 2
        SnapshotsToKeep = 6
    }
    $dailySchedule = @{
        Hour = 1
        Minute = 2
        SnapshotsToKeep = 6
    }
    $weeklySchedule = @{
        Minute = 2    
        Hour = 1                
        Day = "Sunday,Monday"
        SnapshotsToKeep = 6
    }
    $monthlySchedule = @{
        Minute = 2    
        Hour = 1        
        DaysOfMonth = "2,11,21"
        SnapshotsToKeep = 6
    }
PS C:\> New-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MySnapshotPolicy" -Enabled -HourlySchedule $hourlySchedule -DailySchedule $dailySchedule -WeeklySchedule $weeklySchedule -MonthlySchedule $monthlySchedule
```

<span data-ttu-id="3874e-111">Mit diesem Befehl wird die neue ANF-Momentaufnahmerichtlinie für das ANF-Konto mit dem Namen "MyAccount" erstellt.</span><span class="sxs-lookup"><span data-stu-id="3874e-111">This command creates the new ANF snapshot policy for ANF account named account "MyAccount".</span></span>

## <span data-ttu-id="3874e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3874e-112">PARAMETERS</span></span>

### <span data-ttu-id="3874e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3874e-113">-AccountName</span></span>
<span data-ttu-id="3874e-114">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="3874e-114">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3874e-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="3874e-115">-AccountObject</span></span>
<span data-ttu-id="3874e-116">Das Konto für das neue Snapshotrichtlinienobjekt</span><span class="sxs-lookup"><span data-stu-id="3874e-116">The Account for the new Snapshot Policy object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3874e-117">-DailySchedule</span><span class="sxs-lookup"><span data-stu-id="3874e-117">-DailySchedule</span></span>
<span data-ttu-id="3874e-118">Hashtablearray, das den täglichen Zeitplan darstellt</span><span class="sxs-lookup"><span data-stu-id="3874e-118">A hashtable array which represents the daily Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesDailySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3874e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3874e-119">-DefaultProfile</span></span>
<span data-ttu-id="3874e-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3874e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3874e-121">-Enabled</span><span class="sxs-lookup"><span data-stu-id="3874e-121">-Enabled</span></span>
<span data-ttu-id="3874e-122">Die Eigenschaft, die zu entscheiden ist, ob die Richtlinie aktiviert ist oder nicht</span><span class="sxs-lookup"><span data-stu-id="3874e-122">The property to decide policy is enabled or not</span></span>

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

### <span data-ttu-id="3874e-123">-HourlySchedule</span><span class="sxs-lookup"><span data-stu-id="3874e-123">-HourlySchedule</span></span>
<span data-ttu-id="3874e-124">Hashtablearray, das den Stundenplan darstellt</span><span class="sxs-lookup"><span data-stu-id="3874e-124">A hashtable array which represents the hourly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesHourlySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3874e-125">-Location</span><span class="sxs-lookup"><span data-stu-id="3874e-125">-Location</span></span>
<span data-ttu-id="3874e-126">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="3874e-126">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3874e-127">-MonthlySchedule</span><span class="sxs-lookup"><span data-stu-id="3874e-127">-MonthlySchedule</span></span>
<span data-ttu-id="3874e-128">Hashtablearray, das den montly Schedule darstellt</span><span class="sxs-lookup"><span data-stu-id="3874e-128">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesMonthlySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3874e-129">-Name</span><span class="sxs-lookup"><span data-stu-id="3874e-129">-Name</span></span>
<span data-ttu-id="3874e-130">Der Name der ANF-Momentaufnahmerichtlinie</span><span class="sxs-lookup"><span data-stu-id="3874e-130">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SnapshotPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3874e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3874e-131">-ResourceGroupName</span></span>
<span data-ttu-id="3874e-132">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="3874e-132">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3874e-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="3874e-133">-Tag</span></span>
<span data-ttu-id="3874e-134">Hashtablearray, das Ressourcentags darstellt</span><span class="sxs-lookup"><span data-stu-id="3874e-134">A hashtable array which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3874e-135">-WeeklySchedule</span><span class="sxs-lookup"><span data-stu-id="3874e-135">-WeeklySchedule</span></span>
<span data-ttu-id="3874e-136">Hashtablearray, das den montly Schedule darstellt</span><span class="sxs-lookup"><span data-stu-id="3874e-136">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesWeeklySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3874e-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3874e-137">-Confirm</span></span>
<span data-ttu-id="3874e-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3874e-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3874e-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3874e-139">-WhatIf</span></span>
<span data-ttu-id="3874e-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3874e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3874e-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3874e-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3874e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3874e-142">CommonParameters</span></span>
<span data-ttu-id="3874e-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3874e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3874e-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3874e-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3874e-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3874e-145">INPUTS</span></span>

### <span data-ttu-id="3874e-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="3874e-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="3874e-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3874e-147">OUTPUTS</span></span>

### <span data-ttu-id="3874e-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="3874e-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="3874e-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3874e-149">NOTES</span></span>

## <span data-ttu-id="3874e-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3874e-150">RELATED LINKS</span></span>
