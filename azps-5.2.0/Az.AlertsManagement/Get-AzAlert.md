---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: 94cb37a6f98195534e7effcbff8c19b2613923d8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371760"
---
# <span data-ttu-id="11302-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="11302-101">Get-AzAlert</span></span>

## <span data-ttu-id="11302-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11302-102">SYNOPSIS</span></span>
<span data-ttu-id="11302-103">Erhalten von Benachrichtigungsinformationen</span><span class="sxs-lookup"><span data-stu-id="11302-103">Get Alerts Information</span></span>

## <span data-ttu-id="11302-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="11302-104">SYNTAX</span></span>

### <span data-ttu-id="11302-105">AlertsListByFilter (Standard)</span><span class="sxs-lookup"><span data-stu-id="11302-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11302-106">AlertById</span><span class="sxs-lookup"><span data-stu-id="11302-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11302-107">AlertsListByTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="11302-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11302-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11302-108">DESCRIPTION</span></span>
<span data-ttu-id="11302-109">**Das Cmdlet "Get-AzAlert"** wird ausgelöste Warnungsinstanzen.</span><span class="sxs-lookup"><span data-stu-id="11302-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="11302-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="11302-110">EXAMPLES</span></span>

### <span data-ttu-id="11302-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="11302-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="11302-112">Listet alle Warnungen mit dem Schweregrad "Sev2" und der Bedingung "Überwacht ausgelöst" auf.</span><span class="sxs-lookup"><span data-stu-id="11302-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="11302-113">Wenn Sie "IncludeContext" auf "true" festlegen, schließen Sie eine benutzerdefinierte Benachrichtigungsnutzlast ein.</span><span class="sxs-lookup"><span data-stu-id="11302-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="11302-114">Verwenden Format-List, um die vollständigen Details jeder Benachrichtigung in der Liste zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="11302-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="11302-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="11302-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="11302-116">Erhalten von Warnungsdetails nach ID (GUID) oder Ressourcen-ID (vollständige ARM-ID)</span><span class="sxs-lookup"><span data-stu-id="11302-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

### <span data-ttu-id="11302-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="11302-117">Example 3</span></span>

<span data-ttu-id="11302-118">Erhalten Sie Benachrichtigungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="11302-118">Get Alerts Information.</span></span> <span data-ttu-id="11302-119">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="11302-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzAlert -IncludeContext $true -TimeRange '1h'
```

## <span data-ttu-id="11302-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11302-120">PARAMETERS</span></span>

### <span data-ttu-id="11302-121">-AlertId</span><span class="sxs-lookup"><span data-stu-id="11302-121">-AlertId</span></span>
<span data-ttu-id="11302-122">Eindeutiger Bezeichner der Warnung/Ressourcen-ID einer Warnung.</span><span class="sxs-lookup"><span data-stu-id="11302-122">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11302-123">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="11302-123">-AlertRuleId</span></span>
<span data-ttu-id="11302-124">Filtern nach Warnungsregel-ID</span><span class="sxs-lookup"><span data-stu-id="11302-124">Filter on Alert Rule Id</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11302-125">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="11302-125">-CustomTimeRange</span></span>
<span data-ttu-id="11302-126">Unterstütztes Format – \<start-time\> / \<end-time\> Uhrzeit im ISO-8601-Format</span><span class="sxs-lookup"><span data-stu-id="11302-126">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11302-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11302-127">-DefaultProfile</span></span>
<span data-ttu-id="11302-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="11302-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11302-129">-IncludeContext</span><span class="sxs-lookup"><span data-stu-id="11302-129">-IncludeContext</span></span>
<span data-ttu-id="11302-130">Schließen Sie den Kontext (benutzerdefinierte Nutzlast) einer Warnung ein.</span><span class="sxs-lookup"><span data-stu-id="11302-130">Include context (custom payload) of alert</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11302-131">-IncludeEgressConfig</span><span class="sxs-lookup"><span data-stu-id="11302-131">-IncludeEgressConfig</span></span>
<span data-ttu-id="11302-132">Include EgressConfig</span><span class="sxs-lookup"><span data-stu-id="11302-132">Include EgressConfig</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11302-133">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="11302-133">-MonitorCondition</span></span>
<span data-ttu-id="11302-134">Filter on Monitor Condition</span><span class="sxs-lookup"><span data-stu-id="11302-134">Filter on Monitor Condition</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11302-135">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="11302-135">-MonitorService</span></span>
<span data-ttu-id="11302-136">Filtern nach moniterer Dienst</span><span class="sxs-lookup"><span data-stu-id="11302-136">Filter on Moniter Service</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11302-137">-PageCount</span><span class="sxs-lookup"><span data-stu-id="11302-137">-PageCount</span></span>
<span data-ttu-id="11302-138">Die Anzahl der Warnungen, die auf einer Seite abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="11302-138">Number of alerts to be fetched in a page.</span></span>

```yaml
Type: System.Int32
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11302-139">-Select</span><span class="sxs-lookup"><span data-stu-id="11302-139">-Select</span></span>
<span data-ttu-id="11302-140">Projektiert die erforderlichen Felder aus dem Wesentlichen heraus.</span><span class="sxs-lookup"><span data-stu-id="11302-140">Project the required fields out of essentials.</span></span>
<span data-ttu-id="11302-141">Die erwartete Eingabe ist durch Kommas getrennt.</span><span class="sxs-lookup"><span data-stu-id="11302-141">Expected input is comma-separated.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11302-142">-Schweregrad</span><span class="sxs-lookup"><span data-stu-id="11302-142">-Severity</span></span>
<span data-ttu-id="11302-143">Filtern nach Schweregrad der Warnung</span><span class="sxs-lookup"><span data-stu-id="11302-143">Filter on Severity of alert</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11302-144">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="11302-144">-SmartGroupId</span></span>
<span data-ttu-id="11302-145">Filtern aller Benachrichtigungen mit der Intelligenten Gruppen-ID</span><span class="sxs-lookup"><span data-stu-id="11302-145">Filter all the alerts having the Smart Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11302-146">-SortBy</span><span class="sxs-lookup"><span data-stu-id="11302-146">-SortBy</span></span>
<span data-ttu-id="11302-147">Warnungseigenschaft, die beim Sortieren verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="11302-147">Alert property to use while sorting</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11302-148">-SortOrder</span><span class="sxs-lookup"><span data-stu-id="11302-148">-SortOrder</span></span>
<span data-ttu-id="11302-149">Sortierreihenfolge</span><span class="sxs-lookup"><span data-stu-id="11302-149">Sort Order</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11302-150">-State</span><span class="sxs-lookup"><span data-stu-id="11302-150">-State</span></span>
<span data-ttu-id="11302-151">Filtern nach Benachrichtigungsstatus</span><span class="sxs-lookup"><span data-stu-id="11302-151">Filter on State of alert</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11302-152">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="11302-152">-TargetResourceGroup</span></span>
<span data-ttu-id="11302-153">Filtern Sie nach dem Namen der Ressourcengruppe der zu warnende Zielressource.</span><span class="sxs-lookup"><span data-stu-id="11302-153">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11302-154">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="11302-154">-TargetResourceId</span></span>
<span data-ttu-id="11302-155">Filtern Sie nach der Ressourcen-ID der zu warnende Zielressource.</span><span class="sxs-lookup"><span data-stu-id="11302-155">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11302-156">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="11302-156">-TargetResourceType</span></span>
<span data-ttu-id="11302-157">Filtern Sie nach dem Ressourcentyp der zu warnende Zielressource.</span><span class="sxs-lookup"><span data-stu-id="11302-157">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11302-158">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="11302-158">-TimeRange</span></span>
<span data-ttu-id="11302-159">Unterstützte Zeitbereichswerte – 1h, 1d, 7d, 30d (Standard ist 1d)</span><span class="sxs-lookup"><span data-stu-id="11302-159">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

```yaml
Type: System.String
Parameter Sets: AlertsListByFilter, AlertsListByTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11302-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11302-160">CommonParameters</span></span>
<span data-ttu-id="11302-161">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11302-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11302-162">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11302-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11302-163">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="11302-163">INPUTS</span></span>

### <span data-ttu-id="11302-164">Keine</span><span class="sxs-lookup"><span data-stu-id="11302-164">None</span></span>

## <span data-ttu-id="11302-165">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="11302-165">OUTPUTS</span></span>

### <span data-ttu-id="11302-166">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span><span class="sxs-lookup"><span data-stu-id="11302-166">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="11302-167">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="11302-167">NOTES</span></span>

## <span data-ttu-id="11302-168">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="11302-168">RELATED LINKS</span></span>
