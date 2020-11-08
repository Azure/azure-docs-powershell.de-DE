---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlert.md
ms.openlocfilehash: 94cb37a6f98195534e7effcbff8c19b2613923d8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009487"
---
# <span data-ttu-id="35eab-101">Get-AzAlert</span><span class="sxs-lookup"><span data-stu-id="35eab-101">Get-AzAlert</span></span>

## <span data-ttu-id="35eab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="35eab-102">SYNOPSIS</span></span>
<span data-ttu-id="35eab-103">Abrufen von Benachrichtigungsinformationen</span><span class="sxs-lookup"><span data-stu-id="35eab-103">Get Alerts Information</span></span>

## <span data-ttu-id="35eab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="35eab-104">SYNTAX</span></span>

### <span data-ttu-id="35eab-105">AlertsListByFilter (Standard)</span><span class="sxs-lookup"><span data-stu-id="35eab-105">AlertsListByFilter (Default)</span></span>
```
Get-AzAlert [-TargetResourceType <String>] [-TargetResourceGroup <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-SmartGroupId <String>] [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>]
 [-SortBy <String>] [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35eab-106">AlertById</span><span class="sxs-lookup"><span data-stu-id="35eab-106">AlertById</span></span>
```
Get-AzAlert -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35eab-107">AlertsListByTargetResourceIdFilter</span><span class="sxs-lookup"><span data-stu-id="35eab-107">AlertsListByTargetResourceIdFilter</span></span>
```
Get-AzAlert [-TargetResourceId <String>] [-MonitorService <String>] [-MonitorCondition <String>]
 [-Severity <String>] [-State <String>] [-AlertRuleId <String>] [-SmartGroupId <String>]
 [-IncludeContext <Boolean>] [-IncludeEgressConfig <Boolean>] [-PageCount <Int32>] [-SortBy <String>]
 [-SortOrder <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-Select <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35eab-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="35eab-108">DESCRIPTION</span></span>
<span data-ttu-id="35eab-109">**Get-AzAlert-** Cmdlet ruft ausgelöste Warnungsinstanzen ab.</span><span class="sxs-lookup"><span data-stu-id="35eab-109">**Get-AzAlert** cmdlet gets fired alert instances.</span></span>

## <span data-ttu-id="35eab-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="35eab-110">EXAMPLES</span></span>

### <span data-ttu-id="35eab-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="35eab-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAlert -Severity "Sev2" -MonitorCondition "Fired" -IncludeContext true
```

<span data-ttu-id="35eab-112">Auflisten aller Benachrichtigungen mit Sev2-Schweregrad und ausgelöster Monitor Bedingung.</span><span class="sxs-lookup"><span data-stu-id="35eab-112">List all alerts with Sev2 severity and Fired monitor condition.</span></span> <span data-ttu-id="35eab-113">Wenn Include auf true festgelegt wird, wird die benutzerdefinierte Nutzlast von Alert berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="35eab-113">Setting IncludeContext to true, include custom payload of alert.</span></span>
<span data-ttu-id="35eab-114">Verwenden Sie Format-List, um die vollständigen Details jeder Benachrichtigung in der Liste abzurufen.</span><span class="sxs-lookup"><span data-stu-id="35eab-114">Use Format-List to get the complete details of each alert in list.</span></span>

### <span data-ttu-id="35eab-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="35eab-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAlert -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" | Format-List
```

<span data-ttu-id="35eab-116">Abrufen von Warnungsdetails nach ID (GUID) oder Ressourcen-ID (vollständige Arm-ID)</span><span class="sxs-lookup"><span data-stu-id="35eab-116">Get Alert details by Id (GUID) or Resource Id (Complete ARM Id)</span></span>

### <span data-ttu-id="35eab-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="35eab-117">Example 3</span></span>

<span data-ttu-id="35eab-118">Abrufen von Benachrichtigungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="35eab-118">Get Alerts Information.</span></span> <span data-ttu-id="35eab-119">automatisch</span><span class="sxs-lookup"><span data-stu-id="35eab-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzAlert -IncludeContext $true -TimeRange '1h'
```

## <span data-ttu-id="35eab-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="35eab-120">PARAMETERS</span></span>

### <span data-ttu-id="35eab-121">-Warnungs-Nr.</span><span class="sxs-lookup"><span data-stu-id="35eab-121">-AlertId</span></span>
<span data-ttu-id="35eab-122">Eindeutiger Bezeichner der Benachrichtigungs-ID.</span><span class="sxs-lookup"><span data-stu-id="35eab-122">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="35eab-123">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="35eab-123">-AlertRuleId</span></span>
<span data-ttu-id="35eab-124">Filtern nach Warnungsregel-ID</span><span class="sxs-lookup"><span data-stu-id="35eab-124">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="35eab-125">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="35eab-125">-CustomTimeRange</span></span>
<span data-ttu-id="35eab-126">Unterstütztes Format – \<start-time\> / \<end-time\> wobei die Zeit im ISO-8601-Format liegt</span><span class="sxs-lookup"><span data-stu-id="35eab-126">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="35eab-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35eab-127">-DefaultProfile</span></span>
<span data-ttu-id="35eab-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="35eab-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35eab-129">-Include</span><span class="sxs-lookup"><span data-stu-id="35eab-129">-IncludeContext</span></span>
<span data-ttu-id="35eab-130">Kontext (benutzerdefinierte Nutzlast) der Benachrichtigung einbeziehen</span><span class="sxs-lookup"><span data-stu-id="35eab-130">Include context (custom payload) of alert</span></span>

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

### <span data-ttu-id="35eab-131">-IncludeEgressConfig</span><span class="sxs-lookup"><span data-stu-id="35eab-131">-IncludeEgressConfig</span></span>
<span data-ttu-id="35eab-132">EgressConfig einbeziehen</span><span class="sxs-lookup"><span data-stu-id="35eab-132">Include EgressConfig</span></span>

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

### <span data-ttu-id="35eab-133">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="35eab-133">-MonitorCondition</span></span>
<span data-ttu-id="35eab-134">Filtern nach Monitor Bedingung</span><span class="sxs-lookup"><span data-stu-id="35eab-134">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="35eab-135">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="35eab-135">-MonitorService</span></span>
<span data-ttu-id="35eab-136">Filter für den Monitordienst</span><span class="sxs-lookup"><span data-stu-id="35eab-136">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="35eab-137">-PageCount</span><span class="sxs-lookup"><span data-stu-id="35eab-137">-PageCount</span></span>
<span data-ttu-id="35eab-138">Die Anzahl der Benachrichtigungen, die auf einer Seite abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="35eab-138">Number of alerts to be fetched in a page.</span></span>

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

### <span data-ttu-id="35eab-139">-Wählen Sie</span><span class="sxs-lookup"><span data-stu-id="35eab-139">-Select</span></span>
<span data-ttu-id="35eab-140">Projizieren Sie die erforderlichen Felder aus Essentials.</span><span class="sxs-lookup"><span data-stu-id="35eab-140">Project the required fields out of essentials.</span></span>
<span data-ttu-id="35eab-141">Die erwartete Eingabe ist durch Kommas getrennt.</span><span class="sxs-lookup"><span data-stu-id="35eab-141">Expected input is comma-separated.</span></span>

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

### <span data-ttu-id="35eab-142">-Schweregrad</span><span class="sxs-lookup"><span data-stu-id="35eab-142">-Severity</span></span>
<span data-ttu-id="35eab-143">Nach Schweregrad der Benachrichtigung Filtern</span><span class="sxs-lookup"><span data-stu-id="35eab-143">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="35eab-144">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="35eab-144">-SmartGroupId</span></span>
<span data-ttu-id="35eab-145">Filtern aller Warnungen mit der intelligenten Gruppen-ID</span><span class="sxs-lookup"><span data-stu-id="35eab-145">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="35eab-146">-Ordnennach</span><span class="sxs-lookup"><span data-stu-id="35eab-146">-SortBy</span></span>
<span data-ttu-id="35eab-147">Benachrichtigungs Eigenschaft, die beim Sortieren verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="35eab-147">Alert property to use while sorting</span></span>

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

### <span data-ttu-id="35eab-148">-Sortierreihenfolge</span><span class="sxs-lookup"><span data-stu-id="35eab-148">-SortOrder</span></span>
<span data-ttu-id="35eab-149">Sortierreihenfolge</span><span class="sxs-lookup"><span data-stu-id="35eab-149">Sort Order</span></span>

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

### <span data-ttu-id="35eab-150">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="35eab-150">-State</span></span>
<span data-ttu-id="35eab-151">Nach Warnungsstatus Filtern</span><span class="sxs-lookup"><span data-stu-id="35eab-151">Filter on State of alert</span></span>

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

### <span data-ttu-id="35eab-152">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="35eab-152">-TargetResourceGroup</span></span>
<span data-ttu-id="35eab-153">Filtern nach Ressourcengruppenname der Zielressource für Alert.</span><span class="sxs-lookup"><span data-stu-id="35eab-153">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="35eab-154">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="35eab-154">-TargetResourceId</span></span>
<span data-ttu-id="35eab-155">Filtern Sie nach der Ressourcen-ID der Zielressource der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="35eab-155">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="35eab-156">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="35eab-156">-TargetResourceType</span></span>
<span data-ttu-id="35eab-157">Filtern Sie nach dem Ressourcentyp der Zielressource für Alert.</span><span class="sxs-lookup"><span data-stu-id="35eab-157">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="35eab-158">-Zeitraum</span><span class="sxs-lookup"><span data-stu-id="35eab-158">-TimeRange</span></span>
<span data-ttu-id="35eab-159">Unterstützte Zeitbereichs Werte – 1H, 1D, 7D, 30D (Standard ist 1D)</span><span class="sxs-lookup"><span data-stu-id="35eab-159">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="35eab-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35eab-160">CommonParameters</span></span>
<span data-ttu-id="35eab-161">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35eab-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35eab-162">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35eab-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35eab-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="35eab-163">INPUTS</span></span>

### <span data-ttu-id="35eab-164">Keine</span><span class="sxs-lookup"><span data-stu-id="35eab-164">None</span></span>

## <span data-ttu-id="35eab-165">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="35eab-165">OUTPUTS</span></span>

### <span data-ttu-id="35eab-166">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSAlert</span><span class="sxs-lookup"><span data-stu-id="35eab-166">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="35eab-167">Notizen</span><span class="sxs-lookup"><span data-stu-id="35eab-167">NOTES</span></span>

## <span data-ttu-id="35eab-168">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="35eab-168">RELATED LINKS</span></span>
