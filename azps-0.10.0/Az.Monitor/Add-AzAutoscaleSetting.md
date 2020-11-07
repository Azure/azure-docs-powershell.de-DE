---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
ms.openlocfilehash: 6efcc4ad0a957fb2e6124d9688163f08de318b70
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843827"
---
# <span data-ttu-id="46fcf-101">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="46fcf-101">Add-AzAutoscaleSetting</span></span>

## <span data-ttu-id="46fcf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46fcf-102">SYNOPSIS</span></span>
<span data-ttu-id="46fcf-103">Erstellt eine AutoScale-Einstellung.</span><span class="sxs-lookup"><span data-stu-id="46fcf-103">Creates an Autoscale setting.</span></span>

## <span data-ttu-id="46fcf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46fcf-104">SYNTAX</span></span>

### <span data-ttu-id="46fcf-105">UpdateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="46fcf-105">UpdateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -InputObject <PSAutoscaleSetting> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46fcf-106">CreateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="46fcf-106">CreateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -Location <String> -Name <String> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46fcf-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46fcf-107">DESCRIPTION</span></span>
<span data-ttu-id="46fcf-108">Das Cmdlet **Add-AzAutoscaleSetting** erstellt eine AutoScale-Einstellung.</span><span class="sxs-lookup"><span data-stu-id="46fcf-108">The **Add-AzAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>
<span data-ttu-id="46fcf-109">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="46fcf-109">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="46fcf-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46fcf-110">EXAMPLES</span></span>

### <span data-ttu-id="46fcf-111">Beispiel 1: Erstellen einer AutoScale-Einstellung</span><span class="sxs-lookup"><span data-stu-id="46fcf-111">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDay "1", "2", "3" -ScheduleHour 5, 10, 15 -ScheduleMinute 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroupName "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfile $Profile1, $Profile2
```

<span data-ttu-id="46fcf-112">Die ersten beiden Befehle verwenden New-AzAutoscaleRule, um zwei AutoScale-Regeln zu erstellen, $Rule 1 und $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="46fcf-112">The first two commands use New-AzAutoscaleRule to create two Autoscale rules, $Rule1 and $Rule2.</span></span>
<span data-ttu-id="46fcf-113">Der dritte und der vierte Befehl verwenden New-AzAutoscaleProfile zum Erstellen von AutoScale-Profilen, $Profile 1 und $Profile 2 unter Verwendung von $Rule 1 und $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="46fcf-113">The third and fourth commands use New-AzAutoscaleProfile to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>
<span data-ttu-id="46fcf-114">Der endgültige Befehl erstellt eine AutoScale-Einstellung mit den Profilen in $Profile 1 und $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="46fcf-114">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="46fcf-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="46fcf-115">PARAMETERS</span></span>

### <span data-ttu-id="46fcf-116">-AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="46fcf-116">-AutoscaleProfile</span></span>
<span data-ttu-id="46fcf-117">Gibt eine Liste von Profilen an, die der Einstellung "AutoSkalieren" hinzugefügt werden sollen, oder $NULL, kein Profil hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="46fcf-117">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

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

### <span data-ttu-id="46fcf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46fcf-118">-DefaultProfile</span></span>
<span data-ttu-id="46fcf-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="46fcf-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46fcf-120">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="46fcf-120">-DisableSetting</span></span>
<span data-ttu-id="46fcf-121">Deaktiviert eine vorhandene AutoScale-Einstellung.</span><span class="sxs-lookup"><span data-stu-id="46fcf-121">Disables an existing Autoscale setting.</span></span>

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

### <span data-ttu-id="46fcf-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="46fcf-122">-InputObject</span></span>
<span data-ttu-id="46fcf-123">Die vollständige Spezifikation eines AutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="46fcf-123">The complete spec of an AutoscaleSetting</span></span>

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

### <span data-ttu-id="46fcf-124">-Standort</span><span class="sxs-lookup"><span data-stu-id="46fcf-124">-Location</span></span>
<span data-ttu-id="46fcf-125">Gibt die Position der Einstellung "AutoScale" an.</span><span class="sxs-lookup"><span data-stu-id="46fcf-125">Specifies the location of the Autoscale setting.</span></span>

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

### <span data-ttu-id="46fcf-126">-Name</span><span class="sxs-lookup"><span data-stu-id="46fcf-126">-Name</span></span>
<span data-ttu-id="46fcf-127">Gibt den Namen der zu erstellende AutoScale-Einstellung an.</span><span class="sxs-lookup"><span data-stu-id="46fcf-127">Specifies the name of the Autoscale setting to create.</span></span>

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

### <span data-ttu-id="46fcf-128">-Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="46fcf-128">-Notification</span></span>
<span data-ttu-id="46fcf-129">Gibt eine Liste mit durch Kommas getrennten Benachrichtigungen an.</span><span class="sxs-lookup"><span data-stu-id="46fcf-129">Specifies a list of comma-separated notifications.</span></span>

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

### <span data-ttu-id="46fcf-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46fcf-130">-ResourceGroupName</span></span>
<span data-ttu-id="46fcf-131">Gibt den Namen der Ressourcengruppe für die Ressource an, die mit der Einstellung "AutoScale" verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="46fcf-131">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

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

### <span data-ttu-id="46fcf-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="46fcf-132">-TargetResourceId</span></span>
<span data-ttu-id="46fcf-133">Gibt die ID der Ressource an, die von der autoskala abgestuft wird.</span><span class="sxs-lookup"><span data-stu-id="46fcf-133">Specifies the ID of the resource to autoscale.</span></span>

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

### <span data-ttu-id="46fcf-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="46fcf-134">-Confirm</span></span>
<span data-ttu-id="46fcf-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46fcf-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46fcf-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46fcf-136">-WhatIf</span></span>
<span data-ttu-id="46fcf-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46fcf-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46fcf-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46fcf-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46fcf-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46fcf-139">CommonParameters</span></span>
<span data-ttu-id="46fcf-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46fcf-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46fcf-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46fcf-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46fcf-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46fcf-142">INPUTS</span></span>

### <span data-ttu-id="46fcf-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="46fcf-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span></span>

### <span data-ttu-id="46fcf-144">System. String</span><span class="sxs-lookup"><span data-stu-id="46fcf-144">System.String</span></span>

### <span data-ttu-id="46fcf-145">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="46fcf-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="46fcf-146">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Management. Monitor. Management. Models. AutoscaleProfile, Microsoft. Azure. PowerShell. Cmdlets. Monitor, Version = 1.0.0.0, Kultur = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="46fcf-146">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="46fcf-147">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Management. Monitor. Management. Models. AutoscaleNotification, Microsoft. Azure. PowerShell. Cmdlets. Monitor, Version = 1.0.0.0, Kultur = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="46fcf-147">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="46fcf-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46fcf-148">OUTPUTS</span></span>

### <span data-ttu-id="46fcf-149">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="46fcf-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="46fcf-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="46fcf-150">NOTES</span></span>

## <span data-ttu-id="46fcf-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46fcf-151">RELATED LINKS</span></span>

[<span data-ttu-id="46fcf-152">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="46fcf-152">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="46fcf-153">Neu – AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="46fcf-153">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="46fcf-154">Neu – AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="46fcf-154">New-AzAutoscaleRule</span></span>](./New-AzAutoscaleRule.md)

[<span data-ttu-id="46fcf-155">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="46fcf-155">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


