---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/powershell/module/az.monitor/add-azautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
ms.openlocfilehash: b761422a3a2c81d1070dbc5852ca67e2ac91117c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932795"
---
# <span data-ttu-id="23547-101">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="23547-101">Add-AzAutoscaleSetting</span></span>

## <span data-ttu-id="23547-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23547-102">SYNOPSIS</span></span>
<span data-ttu-id="23547-103">Erstellt eine Einstellung für die automatische Skalierung.</span><span class="sxs-lookup"><span data-stu-id="23547-103">Creates an Autoscale setting.</span></span>

## <span data-ttu-id="23547-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23547-104">SYNTAX</span></span>

### <span data-ttu-id="23547-105">UpdateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="23547-105">UpdateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -InputObject <PSAutoscaleSetting> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23547-106">CreateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="23547-106">CreateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -Location <String> -Name <String> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23547-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="23547-107">DESCRIPTION</span></span>
<span data-ttu-id="23547-108">Das **Add-AzAutoscaleSetting-Cmdlet** erstellt eine Einstellung für die automatische Skalierung.</span><span class="sxs-lookup"><span data-stu-id="23547-108">The **Add-AzAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>
<span data-ttu-id="23547-109">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h. es kann eine Bestätigung vom Benutzer anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="23547-109">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="23547-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="23547-110">EXAMPLES</span></span>

### <span data-ttu-id="23547-111">Beispiel 1: Erstellen einer Einstellung für die automatische Skalierung</span><span class="sxs-lookup"><span data-stu-id="23547-111">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDay "1", "2", "3" -ScheduleHour 5, 10, 15 -ScheduleMinute 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroupName "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfile $Profile1, $Profile2
```

<span data-ttu-id="23547-112">Die ersten beiden Befehle verwenden [New-AzAutoscaleRule,](https://docs.microsoft.com/powershell/module/az.monitor/new-azautoscalerule) um zwei Regeln für die automatische Skalierung zu erstellen, $Rule 1 und $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="23547-112">The first two commands use [New-AzAutoscaleRule](https://docs.microsoft.com/powershell/module/az.monitor/new-azautoscalerule) to create two Autoscale rules, $Rule1 and $Rule2.</span></span>
<span data-ttu-id="23547-113">Für den dritten und vierten Befehl wird [New-AzAutoscaleProfile](https://docs.microsoft.com/powershell/module/az.monitor/new-azautoscaleprofile) zum Erstellen von Profilen für die automatische Skalierung $Profile 1 und $Profile 2 mithilfe von $Rule 1 und $Rule 2 verwendet.</span><span class="sxs-lookup"><span data-stu-id="23547-113">The third and fourth commands use [New-AzAutoscaleProfile](https://docs.microsoft.com/powershell/module/az.monitor/new-azautoscaleprofile) to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>
<span data-ttu-id="23547-114">Der letzte Befehl erstellt mithilfe der Profile in $Profile 1 und $Profile 2 eine Einstellung für die automatische Skalierung.</span><span class="sxs-lookup"><span data-stu-id="23547-114">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="23547-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="23547-115">PARAMETERS</span></span>

### <span data-ttu-id="23547-116">-AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="23547-116">-AutoscaleProfile</span></span>
<span data-ttu-id="23547-117">Gibt eine Liste der Profile an, die der Einstellung "Autoscale" hinzugefügt werden, oder $Null, um kein Profil hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="23547-117">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23547-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23547-118">-DefaultProfile</span></span>
<span data-ttu-id="23547-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="23547-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23547-120">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="23547-120">-DisableSetting</span></span>
<span data-ttu-id="23547-121">Deaktiviert eine vorhandene Einstellung für die automatische Skalierung.</span><span class="sxs-lookup"><span data-stu-id="23547-121">Disables an existing Autoscale setting.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23547-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23547-122">-InputObject</span></span>
<span data-ttu-id="23547-123">Die vollständige Spezifikation eines AutoscaleSettings</span><span class="sxs-lookup"><span data-stu-id="23547-123">The complete spec of an AutoscaleSetting</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting
Parameter Sets: UpdateAutoscaleSetting
Aliases: SettingSpec

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23547-124">-Location</span><span class="sxs-lookup"><span data-stu-id="23547-124">-Location</span></span>
<span data-ttu-id="23547-125">Gibt die Position der Einstellung für die automatische Skalierung an.</span><span class="sxs-lookup"><span data-stu-id="23547-125">Specifies the location of the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23547-126">-Name</span><span class="sxs-lookup"><span data-stu-id="23547-126">-Name</span></span>
<span data-ttu-id="23547-127">Gibt den Namen der autoscale-Einstellung an, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="23547-127">Specifies the name of the Autoscale setting to create.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23547-128">-Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="23547-128">-Notification</span></span>
<span data-ttu-id="23547-129">Gibt eine Liste von durch Kommas getrennten Benachrichtigungen an.</span><span class="sxs-lookup"><span data-stu-id="23547-129">Specifies a list of comma-separated notifications.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23547-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23547-130">-ResourceGroupName</span></span>
<span data-ttu-id="23547-131">Gibt den Namen der Ressourcengruppe für die Ressource an, die der Einstellung Autoscale zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="23547-131">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23547-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="23547-132">-TargetResourceId</span></span>
<span data-ttu-id="23547-133">Gibt die ID der Ressource an, die automatisch entskaliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="23547-133">Specifies the ID of the resource to autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23547-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="23547-134">-Confirm</span></span>
<span data-ttu-id="23547-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="23547-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23547-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23547-136">-WhatIf</span></span>
<span data-ttu-id="23547-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="23547-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="23547-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="23547-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23547-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23547-139">CommonParameters</span></span>
<span data-ttu-id="23547-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23547-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23547-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23547-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23547-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="23547-142">INPUTS</span></span>

### <span data-ttu-id="23547-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="23547-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span></span>

### <span data-ttu-id="23547-144">System.String</span><span class="sxs-lookup"><span data-stu-id="23547-144">System.String</span></span>

### <span data-ttu-id="23547-145">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="23547-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="23547-146">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="23547-146">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="23547-147">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="23547-147">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="23547-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="23547-148">OUTPUTS</span></span>

### <span data-ttu-id="23547-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="23547-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="23547-150">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="23547-150">NOTES</span></span>

## <span data-ttu-id="23547-151">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="23547-151">RELATED LINKS</span></span>

[<span data-ttu-id="23547-152">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="23547-152">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="23547-153">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="23547-153">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="23547-154">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="23547-154">New-AzAutoscaleRule</span></span>](./New-AzAutoscaleRule.md)

[<span data-ttu-id="23547-155">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="23547-155">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


