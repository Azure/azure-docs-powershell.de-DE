---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: edb22cc9945ca665b2e24a4488bf3335faac4f50
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380427"
---
# <span data-ttu-id="ebe02-101">Update-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="ebe02-101">Update-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="ebe02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebe02-102">SYNOPSIS</span></span>
<span data-ttu-id="ebe02-103">Aktualisiert eine Azure NetApp Files (ANF)-Momentaufnahmerichtlinie für die optionalen Zusatzmodifizierer.</span><span class="sxs-lookup"><span data-stu-id="ebe02-103">Updates an Azure NetApp Files (ANF) snapshot policy to the optional modifiers provided.</span></span>

## <span data-ttu-id="ebe02-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ebe02-104">SYNTAX</span></span>

### <span data-ttu-id="ebe02-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ebe02-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebe02-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebe02-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy -Name <String> [-Enabled <Boolean>]
 [-HourlySchedule <PSNetAppFilesHourlySchedule>] [-DailySchedule <PSNetAppFilesDailySchedule>]
 [-WeeklySchedule <PSNetAppFilesWeeklySchedule>] [-MonthlySchedule <PSNetAppFilesMonthlySchedule>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebe02-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebe02-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] -ResourceId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebe02-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebe02-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesSnapshotPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ebe02-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ebe02-109">DESCRIPTION</span></span>
<span data-ttu-id="ebe02-110">Das **Cmdlet "Update-AzNetAppFilesSnapshotPolicy"** ändert eine ANF-Momentaufnahmerichtlinie.</span><span class="sxs-lookup"><span data-stu-id="ebe02-110">The **Update-AzNetAppFilesSnapshotPolicy** cmdlet modifies an ANF snapshot policy.</span></span>

## <span data-ttu-id="ebe02-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ebe02-111">EXAMPLES</span></span>

### <span data-ttu-id="ebe02-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ebe02-112">Example 1</span></span>
```powershell
$hourlySchedule = @{
        Minute = 1
        SnapshotsToKeep = 3
    }
PS C:\> Update-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MySnapshotPolicy" -HourlySchedule $hourlySchedule
```

<span data-ttu-id="ebe02-113">Mit diesem Befehl wird die ANF-Sicherungsrichtlinie "MySnapshotPolicy" so geändert, dass die angegebene "HourlySchedule" vorkommt.</span><span class="sxs-lookup"><span data-stu-id="ebe02-113">This command changes the ANF backup policy "MySnapshotPolicy" to have the given HourlySchedule.</span></span>

## <span data-ttu-id="ebe02-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ebe02-114">PARAMETERS</span></span>

### <span data-ttu-id="ebe02-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ebe02-115">-AccountName</span></span>
<span data-ttu-id="ebe02-116">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="ebe02-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="ebe02-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="ebe02-117">-AccountObject</span></span>
<span data-ttu-id="ebe02-118">Das Konto für das neue Snapshotrichtlinienobjekt</span><span class="sxs-lookup"><span data-stu-id="ebe02-118">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="ebe02-119">-DailySchedule</span><span class="sxs-lookup"><span data-stu-id="ebe02-119">-DailySchedule</span></span>
<span data-ttu-id="ebe02-120">Hashtablearray, das den täglichen Zeitplan darstellt</span><span class="sxs-lookup"><span data-stu-id="ebe02-120">A hashtable array which represents the daily Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesDailySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebe02-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebe02-121">-DefaultProfile</span></span>
<span data-ttu-id="ebe02-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ebe02-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebe02-123">-Enabled</span><span class="sxs-lookup"><span data-stu-id="ebe02-123">-Enabled</span></span>
<span data-ttu-id="ebe02-124">Die Eigenschaft, die zu entscheiden ist, ob die Richtlinie aktiviert ist oder nicht</span><span class="sxs-lookup"><span data-stu-id="ebe02-124">The property to decide policy is enabled or not</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebe02-125">-HourlySchedule</span><span class="sxs-lookup"><span data-stu-id="ebe02-125">-HourlySchedule</span></span>
<span data-ttu-id="ebe02-126">Hashtablearray, das den Stundenplan darstellt</span><span class="sxs-lookup"><span data-stu-id="ebe02-126">A hashtable array which represents the hourly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesHourlySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebe02-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ebe02-127">-InputObject</span></span>
<span data-ttu-id="ebe02-128">Das zu entfernende Momentaufnahmeobjekt</span><span class="sxs-lookup"><span data-stu-id="ebe02-128">The snapshot object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebe02-129">-Location</span><span class="sxs-lookup"><span data-stu-id="ebe02-129">-Location</span></span>
<span data-ttu-id="ebe02-130">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="ebe02-130">The location of the resource</span></span>

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

### <span data-ttu-id="ebe02-131">-MonthlySchedule</span><span class="sxs-lookup"><span data-stu-id="ebe02-131">-MonthlySchedule</span></span>
<span data-ttu-id="ebe02-132">Hashtablearray, das den montly Schedule darstellt</span><span class="sxs-lookup"><span data-stu-id="ebe02-132">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesMonthlySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebe02-133">-Name</span><span class="sxs-lookup"><span data-stu-id="ebe02-133">-Name</span></span>
<span data-ttu-id="ebe02-134">Der Name der ANF-Momentaufnahmerichtlinie</span><span class="sxs-lookup"><span data-stu-id="ebe02-134">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: SnapshotPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebe02-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebe02-135">-ResourceGroupName</span></span>
<span data-ttu-id="ebe02-136">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="ebe02-136">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="ebe02-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ebe02-137">-ResourceId</span></span>
<span data-ttu-id="ebe02-138">Die Ressourcen-ID der ANF-Momentaufnahmerichtlinie</span><span class="sxs-lookup"><span data-stu-id="ebe02-138">The resource id of the ANF Snapshot Policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebe02-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="ebe02-139">-Tag</span></span>
<span data-ttu-id="ebe02-140">Hashtablearray, das Ressourcentags darstellt</span><span class="sxs-lookup"><span data-stu-id="ebe02-140">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="ebe02-141">-WeeklySchedule</span><span class="sxs-lookup"><span data-stu-id="ebe02-141">-WeeklySchedule</span></span>
<span data-ttu-id="ebe02-142">Hashtablearray, das den montly Schedule darstellt</span><span class="sxs-lookup"><span data-stu-id="ebe02-142">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesWeeklySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebe02-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ebe02-143">-Confirm</span></span>
<span data-ttu-id="ebe02-144">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ebe02-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebe02-145">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ebe02-145">-WhatIf</span></span>
<span data-ttu-id="ebe02-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ebe02-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebe02-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ebe02-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebe02-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebe02-148">CommonParameters</span></span>
<span data-ttu-id="ebe02-149">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebe02-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebe02-150">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ebe02-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebe02-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ebe02-151">INPUTS</span></span>

### <span data-ttu-id="ebe02-152">System.String</span><span class="sxs-lookup"><span data-stu-id="ebe02-152">System.String</span></span>

### <span data-ttu-id="ebe02-153">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="ebe02-153">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="ebe02-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="ebe02-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="ebe02-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ebe02-155">OUTPUTS</span></span>

### <span data-ttu-id="ebe02-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="ebe02-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="ebe02-157">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ebe02-157">NOTES</span></span>

## <span data-ttu-id="ebe02-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ebe02-158">RELATED LINKS</span></span>
