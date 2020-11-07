---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: e3a5cbe95bf524a70194cfce7e0b8bb80b701dec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658396"
---
# <span data-ttu-id="374a4-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="374a4-101">Get-AzAlert</span></span>

## <span data-ttu-id="374a4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="374a4-102">SYNOPSIS</span></span>
<span data-ttu-id="374a4-103">Abrufen von Benachrichtigungsinformationen</span><span class="sxs-lookup"><span data-stu-id="374a4-103">Get Alerts Information</span></span>

## <span data-ttu-id="374a4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="374a4-104">SYNTAX</span></span>

### <span data-ttu-id="374a4-105">AlertsListByFilter (Standard)</span><span class="sxs-lookup"><span data-stu-id="374a4-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="374a4-106">AlertById</span><span class="sxs-lookup"><span data-stu-id="374a4-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="374a4-107">AlertsListByTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="374a4-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="374a4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="374a4-108">DESCRIPTION</span></span>
<span data-ttu-id="374a4-109">**Get-AzAlert-** Cmdlet ruft ausgelöste Warnungsinstanzen ab.</span><span class="sxs-lookup"><span data-stu-id="374a4-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="374a4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="374a4-110">EXAMPLES</span></span>

### <span data-ttu-id="374a4-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="374a4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="374a4-112">Auflisten aller Benachrichtigungen mit Sev2-Schweregrad und ausgelöster Monitor Bedingung.</span><span class="sxs-lookup"><span data-stu-id="374a4-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="374a4-113">Wenn Include auf true festgelegt wird, wird die benutzerdefinierte Nutzlast von Alert berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="374a4-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="374a4-114">Verwenden Sie Format-List, um die vollständigen Details jeder Benachrichtigung in der Liste abzurufen.</span><span class="sxs-lookup"><span data-stu-id="374a4-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="374a4-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="374a4-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="374a4-116">Abrufen von Warnungsdetails nach ID (GUID) oder Ressourcen-ID (vollständige Arm-ID)</span><span class="sxs-lookup"><span data-stu-id="374a4-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

## <span data-ttu-id="374a4-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="374a4-117">PARAMETERS</span></span>

### <span data-ttu-id="374a4-118">-Warnungs-Nr.</span><span class="sxs-lookup"><span data-stu-id="374a4-118">-AlertId</span></span>
<span data-ttu-id="374a4-119">Eindeutiger Bezeichner der Benachrichtigungs-ID.</span><span class="sxs-lookup"><span data-stu-id="374a4-119">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="374a4-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="374a4-120">-AlertRuleId</span></span>
<span data-ttu-id="374a4-121">Filtern nach Warnungsregel-ID</span><span class="sxs-lookup"><span data-stu-id="374a4-121">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="374a4-122">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="374a4-122">-CustomTimeRange</span></span>
<span data-ttu-id="374a4-123">Unterstütztes Format – \< Anfangs-und Endzeit \> / \< \> , wobei die Zeit im ISO-8601-Format liegt</span><span class="sxs-lookup"><span data-stu-id="374a4-123">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="374a4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="374a4-124">-DefaultProfile</span></span>
<span data-ttu-id="374a4-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="374a4-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="374a4-126">-Include</span><span class="sxs-lookup"><span data-stu-id="374a4-126">-IncludeContext</span></span>
<span data-ttu-id="374a4-127">Kontext (benutzerdefinierte Nutzlast) der Benachrichtigung einbeziehen</span><span class="sxs-lookup"><span data-stu-id="374a4-127">Include context (custom payload) of alert</span></span>

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

### <span data-ttu-id="374a4-128">-IncludeEgressConfig</span><span class="sxs-lookup"><span data-stu-id="374a4-128">-IncludeEgressConfig</span></span>
<span data-ttu-id="374a4-129">EgressConfig einbeziehen</span><span class="sxs-lookup"><span data-stu-id="374a4-129">Include EgressConfig</span></span>

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

### <span data-ttu-id="374a4-130">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="374a4-130">-MonitorCondition</span></span>
<span data-ttu-id="374a4-131">Filtern nach Monitor Bedingung</span><span class="sxs-lookup"><span data-stu-id="374a4-131">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="374a4-132">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="374a4-132">-MonitorService</span></span>
<span data-ttu-id="374a4-133">Filter für den Monitordienst</span><span class="sxs-lookup"><span data-stu-id="374a4-133">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="374a4-134">-PageCount</span><span class="sxs-lookup"><span data-stu-id="374a4-134">-PageCount</span></span>
<span data-ttu-id="374a4-135">Die Anzahl der Benachrichtigungen, die auf einer Seite abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="374a4-135">Number of alerts to be fetched in a page.</span></span>

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

### <span data-ttu-id="374a4-136">-Wählen Sie</span><span class="sxs-lookup"><span data-stu-id="374a4-136">-Select</span></span>
<span data-ttu-id="374a4-137">Projizieren Sie die erforderlichen Felder aus Essentials.</span><span class="sxs-lookup"><span data-stu-id="374a4-137">Project the required fields out of essentials.</span></span>
<span data-ttu-id="374a4-138">Die erwartete Eingabe ist durch Kommas getrennt.</span><span class="sxs-lookup"><span data-stu-id="374a4-138">Expected input is comma-separated.</span></span>

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

### <span data-ttu-id="374a4-139">-Schweregrad</span><span class="sxs-lookup"><span data-stu-id="374a4-139">-Severity</span></span>
<span data-ttu-id="374a4-140">Nach Schweregrad der Benachrichtigung Filtern</span><span class="sxs-lookup"><span data-stu-id="374a4-140">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="374a4-141">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="374a4-141">-SmartGroupId</span></span>
<span data-ttu-id="374a4-142">Filtern aller Warnungen mit der intelligenten Gruppen-ID</span><span class="sxs-lookup"><span data-stu-id="374a4-142">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="374a4-143">-Ordnennach</span><span class="sxs-lookup"><span data-stu-id="374a4-143">-SortBy</span></span>
<span data-ttu-id="374a4-144">Benachrichtigungs Eigenschaft, die beim Sortieren verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="374a4-144">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="374a4-145">-Sortierreihenfolge</span><span class="sxs-lookup"><span data-stu-id="374a4-145">-SortOrder</span></span>
<span data-ttu-id="374a4-146">Sortierreihenfolge</span><span class="sxs-lookup"><span data-stu-id="374a4-146">Sort Order</span></span>

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

### <span data-ttu-id="374a4-147">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="374a4-147">-State</span></span>
<span data-ttu-id="374a4-148">Nach Warnungsstatus Filtern</span><span class="sxs-lookup"><span data-stu-id="374a4-148">Filter on State of alert</span></span>

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

### <span data-ttu-id="374a4-149">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="374a4-149">-TargetResourceGroup</span></span>
<span data-ttu-id="374a4-150">Filtern nach Ressourcengruppenname der Zielressource für Alert.</span><span class="sxs-lookup"><span data-stu-id="374a4-150">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="374a4-151">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="374a4-151">-TargetResourceId</span></span>
<span data-ttu-id="374a4-152">Filtern Sie nach der Ressourcen-ID der Zielressource der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="374a4-152">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="374a4-153">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="374a4-153">-TargetResourceType</span></span>
<span data-ttu-id="374a4-154">Filtern Sie nach dem Ressourcentyp der Zielressource für Alert.</span><span class="sxs-lookup"><span data-stu-id="374a4-154">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="374a4-155">-Zeitraum</span><span class="sxs-lookup"><span data-stu-id="374a4-155">-TimeRange</span></span>
<span data-ttu-id="374a4-156">Unterstützte Zeitbereichs Werte – 1H, 1D, 7D, 30D (Standard ist 1D)</span><span class="sxs-lookup"><span data-stu-id="374a4-156">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="374a4-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="374a4-157">CommonParameters</span></span>
<span data-ttu-id="374a4-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="374a4-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="374a4-159">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="374a4-159">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="374a4-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="374a4-160">INPUTS</span></span>

### <span data-ttu-id="374a4-161">Keine</span><span class="sxs-lookup"><span data-stu-id="374a4-161">None</span></span>

## <span data-ttu-id="374a4-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="374a4-162">OUTPUTS</span></span>

### <span data-ttu-id="374a4-163">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSAlert</span><span class="sxs-lookup"><span data-stu-id="374a4-163">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="374a4-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="374a4-164">NOTES</span></span>

## <span data-ttu-id="374a4-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="374a4-165">RELATED LINKS</span></span>
