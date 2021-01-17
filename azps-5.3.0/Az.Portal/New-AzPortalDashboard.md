---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/new-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
ms.openlocfilehash: 80b2289b4f481fff126d9cd5dfc98ca94536cfa0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470096"
---
# <span data-ttu-id="4960e-101">New-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="4960e-101">New-AzPortalDashboard</span></span>

## <span data-ttu-id="4960e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4960e-102">SYNOPSIS</span></span>
<span data-ttu-id="4960e-103">Erstellt oder aktualisiert ein Dashboard.</span><span class="sxs-lookup"><span data-stu-id="4960e-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="4960e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4960e-104">SYNTAX</span></span>

### <span data-ttu-id="4960e-105">CreateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="4960e-105">CreateExpanded (Default)</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4960e-106">Erstellen</span><span class="sxs-lookup"><span data-stu-id="4960e-106">Create</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Dashboard <IDashboard>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4960e-107">CreateByFile</span><span class="sxs-lookup"><span data-stu-id="4960e-107">CreateByFile</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4960e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4960e-108">DESCRIPTION</span></span>
<span data-ttu-id="4960e-109">Erstellt oder aktualisiert ein Dashboard.</span><span class="sxs-lookup"><span data-stu-id="4960e-109">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="4960e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4960e-110">EXAMPLES</span></span>

### <span data-ttu-id="4960e-111">Beispiel 1: Erstellen eines Dashboards mithilfe einer Dashboardvorlagendatei</span><span class="sxs-lookup"><span data-stu-id="4960e-111">Example 1: Create a dashboard using a dashboard template file</span></span>
```powershell
PS C:\> New-AzPortalDashboard -DashboardPath .\resources\dash1.json -ResourceGroupName mydash-rg -DashboardName my-dashboard03

Location Name           Type
-------- ----           ----
eastasia my-dashboard03 Microsoft.Portal/dashboards
```

<span data-ttu-id="4960e-112">Erstellen Sie ein neues Dashboard mithilfe der bereitgestellten Dashboardvorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="4960e-112">Create a new dashboard using the provided dashboard template file.</span></span>

## <span data-ttu-id="4960e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4960e-113">PARAMETERS</span></span>

### <span data-ttu-id="4960e-114">-Dashboard</span><span class="sxs-lookup"><span data-stu-id="4960e-114">-Dashboard</span></span>
<span data-ttu-id="4960e-115">Definition der freigegebenen Dashboardressourcen.</span><span class="sxs-lookup"><span data-stu-id="4960e-115">The shared dashboard resource definition.</span></span>
<span data-ttu-id="4960e-116">Informationen zum Erstellen von Dashboardeigenschaften finden Sie im Abschnitt "NOTIZEN" und erstellen eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="4960e-116">To construct, see NOTES section for DASHBOARD properties and create a hash table.</span></span>

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

### <span data-ttu-id="4960e-117">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="4960e-117">-DashboardPath</span></span>
<span data-ttu-id="4960e-118">Der Pfad zu einer vorhandenen Dashboardvorlage.</span><span class="sxs-lookup"><span data-stu-id="4960e-118">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="4960e-119">Dashboardvorlagen können aus dem Portal heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="4960e-119">Dashboard templates may be downloaded from the portal.</span></span>

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

### <span data-ttu-id="4960e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4960e-120">-DefaultProfile</span></span>
<span data-ttu-id="4960e-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4960e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4960e-122">-Lens</span><span class="sxs-lookup"><span data-stu-id="4960e-122">-Lens</span></span>
<span data-ttu-id="4960e-123">Die Dashboardobjektive.</span><span class="sxs-lookup"><span data-stu-id="4960e-123">The dashboard lenses.</span></span>

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

### <span data-ttu-id="4960e-124">-Location</span><span class="sxs-lookup"><span data-stu-id="4960e-124">-Location</span></span>
<span data-ttu-id="4960e-125">Ressourcenspeicherort</span><span class="sxs-lookup"><span data-stu-id="4960e-125">Resource location</span></span>

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

### <span data-ttu-id="4960e-126">-Metadata</span><span class="sxs-lookup"><span data-stu-id="4960e-126">-Metadata</span></span>
<span data-ttu-id="4960e-127">Die Dashboardmetadaten.</span><span class="sxs-lookup"><span data-stu-id="4960e-127">The dashboard metadata.</span></span>

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

### <span data-ttu-id="4960e-128">-Name</span><span class="sxs-lookup"><span data-stu-id="4960e-128">-Name</span></span>
<span data-ttu-id="4960e-129">Der Name des Dashboards.</span><span class="sxs-lookup"><span data-stu-id="4960e-129">The name of the dashboard.</span></span>

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

### <span data-ttu-id="4960e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4960e-130">-ResourceGroupName</span></span>
<span data-ttu-id="4960e-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4960e-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="4960e-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4960e-132">-SubscriptionId</span></span>
<span data-ttu-id="4960e-133">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="4960e-133">The Azure subscription ID.</span></span>
<span data-ttu-id="4960e-134">Dies ist eine GUID-formatierte Zeichenfolge (z. B. 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="4960e-134">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="4960e-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="4960e-135">-Tag</span></span>
<span data-ttu-id="4960e-136">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="4960e-136">Resource tags</span></span>

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

### <span data-ttu-id="4960e-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4960e-137">-Confirm</span></span>
<span data-ttu-id="4960e-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4960e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4960e-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4960e-139">-WhatIf</span></span>
<span data-ttu-id="4960e-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4960e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4960e-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4960e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4960e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4960e-142">CommonParameters</span></span>
<span data-ttu-id="4960e-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4960e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4960e-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4960e-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4960e-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4960e-145">INPUTS</span></span>

### <span data-ttu-id="4960e-146">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="4960e-146">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="4960e-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4960e-147">OUTPUTS</span></span>

### <span data-ttu-id="4960e-148">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="4960e-148">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="4960e-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4960e-149">NOTES</span></span>

<span data-ttu-id="4960e-150">ALIASE</span><span class="sxs-lookup"><span data-stu-id="4960e-150">ALIASES</span></span>

<span data-ttu-id="4960e-151">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="4960e-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4960e-152">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4960e-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4960e-153">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4960e-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4960e-154">DASHBOARD: <IDashboard> Definition der freigegebenen Dashboardressourcen.</span><span class="sxs-lookup"><span data-stu-id="4960e-154">DASHBOARD <IDashboard>: The shared dashboard resource definition.</span></span>
  - <span data-ttu-id="4960e-155">`Location <String>`: Ressourcenstandort</span><span class="sxs-lookup"><span data-stu-id="4960e-155">`Location <String>`: Resource location</span></span>
  - <span data-ttu-id="4960e-156">`[Lens <IDashboardPropertiesLenses>]`: Die Dashboardobjektive.</span><span class="sxs-lookup"><span data-stu-id="4960e-156">`[Lens <IDashboardPropertiesLenses>]`: The dashboard lenses.</span></span>
    - <span data-ttu-id="4960e-157">`[(Any) <IDashboardLens>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="4960e-157">`[(Any) <IDashboardLens>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="4960e-158">`[Metadata <IDashboardPropertiesMetadata>]`: Die Dashboardmetadaten.</span><span class="sxs-lookup"><span data-stu-id="4960e-158">`[Metadata <IDashboardPropertiesMetadata>]`: The dashboard metadata.</span></span>
    - <span data-ttu-id="4960e-159">`[(Any) <Object>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="4960e-159">`[(Any) <Object>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="4960e-160">`[Tag <IDashboardTags>]`: Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="4960e-160">`[Tag <IDashboardTags>]`: Resource tags</span></span>
    - <span data-ttu-id="4960e-161">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="4960e-161">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="4960e-162">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4960e-162">RELATED LINKS</span></span>

