---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
ms.openlocfilehash: 3da9950f2dfdf38bc4e1b461ffd1fcf409b445e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650581"
---
# <span data-ttu-id="20125-101">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="20125-101">Add-AzAutoscaleSetting</span></span>

## <span data-ttu-id="20125-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="20125-102">SYNOPSIS</span></span>
<span data-ttu-id="20125-103">Erstellt eine AutoScale-Einstellung.</span><span class="sxs-lookup"><span data-stu-id="20125-103">Creates an Autoscale setting.</span></span>

## <span data-ttu-id="20125-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="20125-104">SYNTAX</span></span>

### <span data-ttu-id="20125-105">UpdateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="20125-105">UpdateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -InputObject <PSAutoscaleSetting> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20125-106">CreateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="20125-106">CreateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -Location <String> -Name <String> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20125-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20125-107">DESCRIPTION</span></span>
<span data-ttu-id="20125-108">Das Cmdlet **Add-AzAutoscaleSetting** erstellt eine AutoScale-Einstellung.</span><span class="sxs-lookup"><span data-stu-id="20125-108">The **Add-AzAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>
<span data-ttu-id="20125-109">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="20125-109">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="20125-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="20125-110">EXAMPLES</span></span>

### <span data-ttu-id="20125-111">Beispiel 1: Erstellen einer AutoScale-Einstellung</span><span class="sxs-lookup"><span data-stu-id="20125-111">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDay "1", "2", "3" -ScheduleHour 5, 10, 15 -ScheduleMinute 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroupName "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfile $Profile1, $Profile2
```

<span data-ttu-id="20125-112">Die ersten beiden Befehle verwenden New-AzAutoscaleRule, um zwei AutoScale-Regeln zu erstellen, $Rule 1 und $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="20125-112">The first two commands use New-AzAutoscaleRule to create two Autoscale rules, $Rule1 and $Rule2.</span></span>
<span data-ttu-id="20125-113">Der dritte und der vierte Befehl verwenden New-AzAutoscaleProfile zum Erstellen von AutoScale-Profilen, $Profile 1 und $Profile 2 unter Verwendung von $Rule 1 und $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="20125-113">The third and fourth commands use New-AzAutoscaleProfile to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>
<span data-ttu-id="20125-114">Der endgültige Befehl erstellt eine AutoScale-Einstellung mit den Profilen in $Profile 1 und $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="20125-114">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="20125-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="20125-115">PARAMETERS</span></span>

### <span data-ttu-id="20125-116">-AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="20125-116">-AutoscaleProfile</span></span>
<span data-ttu-id="20125-117">Gibt eine Liste von Profilen an, die der Einstellung "AutoSkalieren" hinzugefügt werden sollen, oder $NULL, kein Profil hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="20125-117">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

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

### <span data-ttu-id="20125-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20125-118">-DefaultProfile</span></span>
<span data-ttu-id="20125-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="20125-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20125-120">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="20125-120">-DisableSetting</span></span>
<span data-ttu-id="20125-121">Deaktiviert eine vorhandene AutoScale-Einstellung.</span><span class="sxs-lookup"><span data-stu-id="20125-121">Disables an existing Autoscale setting.</span></span>

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

### <span data-ttu-id="20125-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="20125-122">-InputObject</span></span>
<span data-ttu-id="20125-123">Die vollständige Spezifikation eines AutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="20125-123">The complete spec of an AutoscaleSetting</span></span>

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

### <span data-ttu-id="20125-124">-Standort</span><span class="sxs-lookup"><span data-stu-id="20125-124">-Location</span></span>
<span data-ttu-id="20125-125">Gibt die Position der Einstellung "AutoScale" an.</span><span class="sxs-lookup"><span data-stu-id="20125-125">Specifies the location of the Autoscale setting.</span></span>

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

### <span data-ttu-id="20125-126">-Name</span><span class="sxs-lookup"><span data-stu-id="20125-126">-Name</span></span>
<span data-ttu-id="20125-127">Gibt den Namen der zu erstellende AutoScale-Einstellung an.</span><span class="sxs-lookup"><span data-stu-id="20125-127">Specifies the name of the Autoscale setting to create.</span></span>

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

### <span data-ttu-id="20125-128">-Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="20125-128">-Notification</span></span>
<span data-ttu-id="20125-129">Gibt eine Liste mit durch Kommas getrennten Benachrichtigungen an.</span><span class="sxs-lookup"><span data-stu-id="20125-129">Specifies a list of comma-separated notifications.</span></span>

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

### <span data-ttu-id="20125-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20125-130">-ResourceGroupName</span></span>
<span data-ttu-id="20125-131">Gibt den Namen der Ressourcengruppe für die Ressource an, die mit der Einstellung "AutoScale" verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="20125-131">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

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

### <span data-ttu-id="20125-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="20125-132">-TargetResourceId</span></span>
<span data-ttu-id="20125-133">Gibt die ID der Ressource an, die von der autoskala abgestuft wird.</span><span class="sxs-lookup"><span data-stu-id="20125-133">Specifies the ID of the resource to autoscale.</span></span>

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

### <span data-ttu-id="20125-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="20125-134">-Confirm</span></span>
<span data-ttu-id="20125-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="20125-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20125-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20125-136">-WhatIf</span></span>
<span data-ttu-id="20125-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="20125-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20125-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="20125-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20125-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20125-139">CommonParameters</span></span>
<span data-ttu-id="20125-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20125-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20125-141">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20125-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20125-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="20125-142">INPUTS</span></span>

### <span data-ttu-id="20125-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="20125-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span></span>

### <span data-ttu-id="20125-144">System. String</span><span class="sxs-lookup"><span data-stu-id="20125-144">System.String</span></span>

### <span data-ttu-id="20125-145">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="20125-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="20125-146">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Management. Monitor. Management. Models. AutoscaleProfile, Microsoft. Azure. PowerShell. Cmdlets. Monitor, Version = 1.0.0.0, Kultur = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="20125-146">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="20125-147">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Management. Monitor. Management. Models. AutoscaleNotification, Microsoft. Azure. PowerShell. Cmdlets. Monitor, Version = 1.0.0.0, Kultur = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="20125-147">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="20125-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="20125-148">OUTPUTS</span></span>

### <span data-ttu-id="20125-149">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="20125-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="20125-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="20125-150">NOTES</span></span>

## <span data-ttu-id="20125-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="20125-151">RELATED LINKS</span></span>

[<span data-ttu-id="20125-152">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="20125-152">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="20125-153">Neu – AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="20125-153">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="20125-154">Neu – AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="20125-154">New-AzAutoscaleRule</span></span>](./New-AzAutoscaleRule.md)

[<span data-ttu-id="20125-155">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="20125-155">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


