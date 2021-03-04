---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/powershell/module/az.portal/new-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
ms.openlocfilehash: 05627146c0b9984ea5222f70f85f801b374e1321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937443"
---
# <span data-ttu-id="ba893-101">New-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="ba893-101">New-AzPortalDashboard</span></span>

## <span data-ttu-id="ba893-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba893-102">SYNOPSIS</span></span>
<span data-ttu-id="ba893-103">Erstellt oder aktualisiert ein Dashboard.</span><span class="sxs-lookup"><span data-stu-id="ba893-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="ba893-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba893-104">SYNTAX</span></span>

### <span data-ttu-id="ba893-105">CreateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="ba893-105">CreateExpanded (Default)</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ba893-106">Erstellen</span><span class="sxs-lookup"><span data-stu-id="ba893-106">Create</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Dashboard <IDashboard>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ba893-107">CreateByFile</span><span class="sxs-lookup"><span data-stu-id="ba893-107">CreateByFile</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ba893-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ba893-108">DESCRIPTION</span></span>
<span data-ttu-id="ba893-109">Erstellt oder aktualisiert ein Dashboard.</span><span class="sxs-lookup"><span data-stu-id="ba893-109">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="ba893-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ba893-110">EXAMPLES</span></span>

### <span data-ttu-id="ba893-111">Beispiel 1: Erstellen eines Dashboards mit einer Dashboardvorlagendatei</span><span class="sxs-lookup"><span data-stu-id="ba893-111">Example 1: Create a dashboard using a dashboard template file</span></span>
```powershell
PS C:\> New-AzPortalDashboard -DashboardPath .\resources\dash1.json -ResourceGroupName mydash-rg -DashboardName my-dashboard03

Location Name           Type
-------- ----           ----
eastasia my-dashboard03 Microsoft.Portal/dashboards
```

<span data-ttu-id="ba893-112">Erstellen Sie ein neues Dashboard mit der bereitgestellten Dashboardvorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="ba893-112">Create a new dashboard using the provided dashboard template file.</span></span>

## <span data-ttu-id="ba893-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ba893-113">PARAMETERS</span></span>

### <span data-ttu-id="ba893-114">-Dashboard</span><span class="sxs-lookup"><span data-stu-id="ba893-114">-Dashboard</span></span>
<span data-ttu-id="ba893-115">Die Definition der freigegebenen Dashboardressourcen.</span><span class="sxs-lookup"><span data-stu-id="ba893-115">The shared dashboard resource definition.</span></span>
<span data-ttu-id="ba893-116">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu #A0 und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="ba893-116">To construct, see NOTES section for DASHBOARD properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba893-117">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="ba893-117">-DashboardPath</span></span>
<span data-ttu-id="ba893-118">Der Pfad zu einer vorhandenen Dashboardvorlage.</span><span class="sxs-lookup"><span data-stu-id="ba893-118">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="ba893-119">Dashboardvorlagen können aus dem Portal heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="ba893-119">Dashboard templates may be downloaded from the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba893-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba893-120">-DefaultProfile</span></span>
<span data-ttu-id="ba893-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ba893-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba893-122">-Lens</span><span class="sxs-lookup"><span data-stu-id="ba893-122">-Lens</span></span>
<span data-ttu-id="ba893-123">Die Dashboardlinsen.</span><span class="sxs-lookup"><span data-stu-id="ba893-123">The dashboard lenses.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba893-124">-Location</span><span class="sxs-lookup"><span data-stu-id="ba893-124">-Location</span></span>
<span data-ttu-id="ba893-125">Ressourcenspeicherort</span><span class="sxs-lookup"><span data-stu-id="ba893-125">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba893-126">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="ba893-126">-Metadata</span></span>
<span data-ttu-id="ba893-127">Die Dashboardmetadaten.</span><span class="sxs-lookup"><span data-stu-id="ba893-127">The dashboard metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba893-128">-Name</span><span class="sxs-lookup"><span data-stu-id="ba893-128">-Name</span></span>
<span data-ttu-id="ba893-129">Der Name des Dashboards.</span><span class="sxs-lookup"><span data-stu-id="ba893-129">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba893-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba893-130">-ResourceGroupName</span></span>
<span data-ttu-id="ba893-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ba893-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba893-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ba893-132">-SubscriptionId</span></span>
<span data-ttu-id="ba893-133">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="ba893-133">The Azure subscription ID.</span></span>
<span data-ttu-id="ba893-134">Dies ist eine GUID-formatierte Zeichenfolge (z. B. 000000000-0000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="ba893-134">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba893-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="ba893-135">-Tag</span></span>
<span data-ttu-id="ba893-136">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="ba893-136">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba893-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ba893-137">-Confirm</span></span>
<span data-ttu-id="ba893-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ba893-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba893-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba893-139">-WhatIf</span></span>
<span data-ttu-id="ba893-140">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ba893-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba893-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ba893-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba893-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba893-142">CommonParameters</span></span>
<span data-ttu-id="ba893-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba893-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba893-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba893-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba893-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ba893-145">INPUTS</span></span>

### <span data-ttu-id="ba893-146">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="ba893-146">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="ba893-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ba893-147">OUTPUTS</span></span>

### <span data-ttu-id="ba893-148">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="ba893-148">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="ba893-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ba893-149">NOTES</span></span>

<span data-ttu-id="ba893-150">ALIASE</span><span class="sxs-lookup"><span data-stu-id="ba893-150">ALIASES</span></span>

<span data-ttu-id="ba893-151">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="ba893-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ba893-152">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="ba893-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ba893-153">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ba893-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ba893-154">DASHBOARD: <IDashboard> Die Definition der freigegebenen Dashboardressourcen.</span><span class="sxs-lookup"><span data-stu-id="ba893-154">DASHBOARD <IDashboard>: The shared dashboard resource definition.</span></span>
  - <span data-ttu-id="ba893-155">`Location <String>`: Ressourcenspeicherort</span><span class="sxs-lookup"><span data-stu-id="ba893-155">`Location <String>`: Resource location</span></span>
  - <span data-ttu-id="ba893-156">`[Lens <IDashboardPropertiesLenses>]`: Die Dashboardlinsen.</span><span class="sxs-lookup"><span data-stu-id="ba893-156">`[Lens <IDashboardPropertiesLenses>]`: The dashboard lenses.</span></span>
    - <span data-ttu-id="ba893-157">`[(Any) <IDashboardLens>]`: Dies gibt an, dass diesem Objekt eine beliebige Eigenschaft hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ba893-157">`[(Any) <IDashboardLens>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="ba893-158">`[Metadata <IDashboardPropertiesMetadata>]`: Die Dashboardmetadaten.</span><span class="sxs-lookup"><span data-stu-id="ba893-158">`[Metadata <IDashboardPropertiesMetadata>]`: The dashboard metadata.</span></span>
    - <span data-ttu-id="ba893-159">`[(Any) <Object>]`: Dies gibt an, dass diesem Objekt eine beliebige Eigenschaft hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ba893-159">`[(Any) <Object>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="ba893-160">`[Tag <IDashboardTags>]`: Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="ba893-160">`[Tag <IDashboardTags>]`: Resource tags</span></span>
    - <span data-ttu-id="ba893-161">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt eine beliebige Eigenschaft hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ba893-161">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="ba893-162">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ba893-162">RELATED LINKS</span></span>

