---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmAutoscaleSetting.md
ms.openlocfilehash: 08e7558bb357c930749cf4a93bfa428560c64395
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504561"
---
# <span data-ttu-id="4b6a3-101">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="4b6a3-101">Add-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="4b6a3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4b6a3-102">SYNOPSIS</span></span>
<span data-ttu-id="4b6a3-103">Erstellt eine AutoScale-Einstellung.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-103">Creates an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b6a3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b6a3-104">SYNTAX</span></span>

### <span data-ttu-id="4b6a3-105">UpdateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="4b6a3-105">UpdateAutoscaleSetting</span></span>
```
Add-AzureRmAutoscaleSetting -SettingSpec <PSAutoscaleSetting> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.AutoscaleProfile]>]
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b6a3-106">CreateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="4b6a3-106">CreateAutoscaleSetting</span></span>
```
Add-AzureRmAutoscaleSetting -Location <String> -Name <String> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b6a3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b6a3-107">DESCRIPTION</span></span>
<span data-ttu-id="4b6a3-108">Das Cmdlet **Add-AzureRmAutoscaleSetting** erstellt eine AutoScale-Einstellung.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-108">The **Add-AzureRmAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>

<span data-ttu-id="4b6a3-109">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-109">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="4b6a3-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4b6a3-110">EXAMPLES</span></span>

### <span data-ttu-id="4b6a3-111">Beispiel 1: Erstellen einer AutoScale-Einstellung</span><span class="sxs-lookup"><span data-stu-id="4b6a3-111">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzureRmAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroupName "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfiles $Profile1, $Profile2
```

<span data-ttu-id="4b6a3-112">Die ersten beiden Befehle verwenden New-AzureRmAutoscaleRule, um zwei AutoScale-Regeln zu erstellen, $Rule 1 und $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-112">The first two commands use New-AzureRmAutoscaleRule to create two Autoscale rules, $Rule1 and $Rule2.</span></span>

<span data-ttu-id="4b6a3-113">Der dritte und der vierte Befehl verwenden New-AzureRmAutoscaleProfile zum Erstellen von AutoScale-Profilen, $Profile 1 und $Profile 2 unter Verwendung von $Rule 1 und $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-113">The third and fourth commands use New-AzureRmAutoscaleProfile to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>

<span data-ttu-id="4b6a3-114">Der endgültige Befehl erstellt eine AutoScale-Einstellung mit den Profilen in $Profile 1 und $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-114">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="4b6a3-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b6a3-115">PARAMETERS</span></span>

### <span data-ttu-id="4b6a3-116">-AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="4b6a3-116">-AutoscaleProfile</span></span>
<span data-ttu-id="4b6a3-117">Gibt eine Liste von Profilen an, die der Einstellung "AutoSkalieren" hinzugefügt werden sollen, oder $NULL, kein Profil hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-117">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]
Parameter Sets: (All)
Aliases: AutoscaleProfiles

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b6a3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b6a3-118">-DefaultProfile</span></span>
<span data-ttu-id="4b6a3-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4b6a3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b6a3-120">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="4b6a3-120">-DisableSetting</span></span>
<span data-ttu-id="4b6a3-121">Deaktiviert eine vorhandene AutoScale-Einstellung.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-121">Disables an existing Autoscale setting.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b6a3-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="4b6a3-122">-Location</span></span>
<span data-ttu-id="4b6a3-123">Gibt die Position der Einstellung "AutoScale" an.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-123">Specifies the location of the Autoscale setting.</span></span>

```yaml
Type: String
Parameter Sets: CreateAutoscaleSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b6a3-124">-Name</span><span class="sxs-lookup"><span data-stu-id="4b6a3-124">-Name</span></span>
<span data-ttu-id="4b6a3-125">Gibt den Namen der zu erstellende AutoScale-Einstellung an.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-125">Specifies the name of the Autoscale setting to create.</span></span>

```yaml
Type: String
Parameter Sets: CreateAutoscaleSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b6a3-126">-Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="4b6a3-126">-Notification</span></span>
<span data-ttu-id="4b6a3-127">Gibt eine Liste mit durch Kommas getrennten Benachrichtigungen an.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-127">Specifies a list of comma-separated notifications.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]
Parameter Sets: (All)
Aliases: Notifications

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b6a3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b6a3-128">-ResourceGroupName</span></span>
<span data-ttu-id="4b6a3-129">Gibt den Namen der Ressourcengruppe für die Ressource an, die mit der Einstellung "AutoScale" verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-129">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b6a3-130">-SettingSpec</span><span class="sxs-lookup"><span data-stu-id="4b6a3-130">-SettingSpec</span></span>
<span data-ttu-id="4b6a3-131">Gibt ein **AutoscaleSetting** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-131">Specifies an **AutoscaleSetting** object.</span></span>
<span data-ttu-id="4b6a3-132">Sie können das Get-AzureRmAutoscaleSetting-Cmdlet verwenden, um ein **AutoscaleSetting** -Objekt abzurufen, oder Sie können eins in einem Windows PowerShell-Skript erstellen.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-132">You can use the Get-AzureRmAutoscaleSetting cmdlet to get an **AutoscaleSetting** object or you can construct one in a Windows PowerShell script.</span></span>

```yaml
Type: PSAutoscaleSetting
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the update semantics
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b6a3-133">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="4b6a3-133">-TargetResourceId</span></span>
<span data-ttu-id="4b6a3-134">Gibt die ID der Ressource an, die von der autoskala abgestuft wird.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-134">Specifies the ID of the resource to autoscale.</span></span>

```yaml
Type: String
Parameter Sets: CreateAutoscaleSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b6a3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b6a3-135">CommonParameters</span></span>
<span data-ttu-id="4b6a3-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b6a3-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b6a3-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b6a3-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4b6a3-138">INPUTS</span></span>

### <span data-ttu-id="4b6a3-139">Keine</span><span class="sxs-lookup"><span data-stu-id="4b6a3-139">None</span></span>
<span data-ttu-id="4b6a3-140">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="4b6a3-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4b6a3-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4b6a3-141">OUTPUTS</span></span>

### <span data-ttu-id="4b6a3-142">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="4b6a3-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="4b6a3-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="4b6a3-143">NOTES</span></span>

## <span data-ttu-id="4b6a3-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4b6a3-144">RELATED LINKS</span></span>

[<span data-ttu-id="4b6a3-145">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="4b6a3-145">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="4b6a3-146">Neu – AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="4b6a3-146">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="4b6a3-147">Neu – AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="4b6a3-147">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="4b6a3-148">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="4b6a3-148">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


