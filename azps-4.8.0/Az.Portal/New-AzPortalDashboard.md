---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/new-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/New-AzPortalDashboard.md
ms.openlocfilehash: 80b2289b4f481fff126d9cd5dfc98ca94536cfa0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174486"
---
# <span data-ttu-id="0b2d1-101">New-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="0b2d1-101">New-AzPortalDashboard</span></span>

## <span data-ttu-id="0b2d1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0b2d1-102">SYNOPSIS</span></span>
<span data-ttu-id="0b2d1-103">Erstellt oder aktualisiert ein Dashboard.</span><span class="sxs-lookup"><span data-stu-id="0b2d1-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="0b2d1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b2d1-104">SYNTAX</span></span>

### <span data-ttu-id="0b2d1-105">Createexpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="0b2d1-105">CreateExpanded (Default)</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0b2d1-106">Erstellen</span><span class="sxs-lookup"><span data-stu-id="0b2d1-106">Create</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -Dashboard <IDashboard>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0b2d1-107">CreateByFile</span><span class="sxs-lookup"><span data-stu-id="0b2d1-107">CreateByFile</span></span>
```
New-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0b2d1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b2d1-108">DESCRIPTION</span></span>
<span data-ttu-id="0b2d1-109">Erstellt oder aktualisiert ein Dashboard.</span><span class="sxs-lookup"><span data-stu-id="0b2d1-109">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="0b2d1-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0b2d1-110">EXAMPLES</span></span>

### <span data-ttu-id="0b2d1-111">Beispiel 1: Erstellen eines Dashboards mithilfe einer Dashboard-Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="0b2d1-111">Example 1: Create a dashboard using a dashboard template file</span></span>
```powershell
PS C:\> New-AzPortalDashboard -DashboardPath .\resources\dash1.json -ResourceGroupName mydash-rg -DashboardName my-dashboard03

Location Name           Type
-------- ----           ----
eastasia my-dashboard03 Microsoft.Portal/dashboards
```

<span data-ttu-id="0b2d1-112">Erstellen Sie ein neues Dashboard mit der bereitgestellten Dashboard-Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="0b2d1-112">Create a new dashboard using the provided dashboard template file.</span></span>

## <span data-ttu-id="0b2d1-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b2d1-113">PARAMETERS</span></span>

### <span data-ttu-id="0b2d1-114">-Dashboard</span><span class="sxs-lookup"><span data-stu-id="0b2d1-114">-Dashboard</span></span>
<span data-ttu-id="0b2d1-115">Die Ressourcendefinition für freigegebene Dashboards.</span><span class="sxs-lookup"><span data-stu-id="0b2d1-115">The shared dashboard resource definition.</span></span>
<span data-ttu-id="0b2d1-116">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Dashboard-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="0b2d1-116">To construct, see NOTES section for DASHBOARD properties and create a hash table.</span></span>

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

### <span data-ttu-id="0b2d1-117">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="0b2d1-117">-DashboardPath</span></span>
<span data-ttu-id="0b2d1-118">Der Pfad zu einer vorhandenen Dashboard-Vorlage.</span><span class="sxs-lookup"><span data-stu-id="0b2d1-118">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="0b2d1-119">Dashboard-Vorlagen können aus dem Portal heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="0b2d1-119">Dashboard templates may be downloaded from the portal.</span></span>

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

### <span data-ttu-id="0b2d1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b2d1-120">-DefaultProfile</span></span>
<span data-ttu-id="0b2d1-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0b2d1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b2d1-122">-Objektiv</span><span class="sxs-lookup"><span data-stu-id="0b2d1-122">-Lens</span></span>
<span data-ttu-id="0b2d1-123">Die Dashboard-Objektive.</span><span class="sxs-lookup"><span data-stu-id="0b2d1-123">The dashboard lenses.</span></span>

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

### <span data-ttu-id="0b2d1-124">-Standort</span><span class="sxs-lookup"><span data-stu-id="0b2d1-124">-Location</span></span>
<span data-ttu-id="0b2d1-125">Ressourcen Standort</span><span class="sxs-lookup"><span data-stu-id="0b2d1-125">Resource location</span></span>

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

### <span data-ttu-id="0b2d1-126">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="0b2d1-126">-Metadata</span></span>
<span data-ttu-id="0b2d1-127">Die Dashboard-Metadaten.</span><span class="sxs-lookup"><span data-stu-id="0b2d1-127">The dashboard metadata.</span></span>

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

### <span data-ttu-id="0b2d1-128">-Name</span><span class="sxs-lookup"><span data-stu-id="0b2d1-128">-Name</span></span>
<span data-ttu-id="0b2d1-129">Der Name des Dashboards.</span><span class="sxs-lookup"><span data-stu-id="0b2d1-129">The name of the dashboard.</span></span>

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

### <span data-ttu-id="0b2d1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b2d1-130">-ResourceGroupName</span></span>
<span data-ttu-id="0b2d1-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0b2d1-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="0b2d1-132">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="0b2d1-132">-SubscriptionId</span></span>
<span data-ttu-id="0b2d1-133">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="0b2d1-133">The Azure subscription ID.</span></span>
<span data-ttu-id="0b2d1-134">Hierbei handelt es sich um eine GUID-formatierte Zeichenfolge (z.b. 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="0b2d1-134">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="0b2d1-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="0b2d1-135">-Tag</span></span>
<span data-ttu-id="0b2d1-136">Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="0b2d1-136">Resource tags</span></span>

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

### <span data-ttu-id="0b2d1-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0b2d1-137">-Confirm</span></span>
<span data-ttu-id="0b2d1-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0b2d1-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b2d1-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b2d1-139">-WhatIf</span></span>
<span data-ttu-id="0b2d1-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b2d1-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b2d1-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0b2d1-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b2d1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b2d1-142">CommonParameters</span></span>
<span data-ttu-id="0b2d1-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b2d1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b2d1-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b2d1-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b2d1-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0b2d1-145">INPUTS</span></span>

### <span data-ttu-id="0b2d1-146">Microsoft. Azure. PowerShell. Cmdlets. Portal. Models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="0b2d1-146">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="0b2d1-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0b2d1-147">OUTPUTS</span></span>

### <span data-ttu-id="0b2d1-148">Microsoft. Azure. PowerShell. Cmdlets. Portal. Models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="0b2d1-148">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="0b2d1-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="0b2d1-149">NOTES</span></span>

<span data-ttu-id="0b2d1-150">Aliase</span><span class="sxs-lookup"><span data-stu-id="0b2d1-150">ALIASES</span></span>

<span data-ttu-id="0b2d1-151">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0b2d1-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0b2d1-152">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0b2d1-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0b2d1-153">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="0b2d1-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0b2d1-154">Dashboard <IDashboard> : die Ressourcendefinition für freigegebene Dashboards.</span><span class="sxs-lookup"><span data-stu-id="0b2d1-154">DASHBOARD <IDashboard>: The shared dashboard resource definition.</span></span>
  - <span data-ttu-id="0b2d1-155">`Location <String>`: Ressourcen Standort</span><span class="sxs-lookup"><span data-stu-id="0b2d1-155">`Location <String>`: Resource location</span></span>
  - <span data-ttu-id="0b2d1-156">`[Lens <IDashboardPropertiesLenses>]`: Die Dashboard-Objektive.</span><span class="sxs-lookup"><span data-stu-id="0b2d1-156">`[Lens <IDashboardPropertiesLenses>]`: The dashboard lenses.</span></span>
    - <span data-ttu-id="0b2d1-157">`[(Any) <IDashboardLens>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0b2d1-157">`[(Any) <IDashboardLens>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="0b2d1-158">`[Metadata <IDashboardPropertiesMetadata>]`: Die Dashboard-Metadaten.</span><span class="sxs-lookup"><span data-stu-id="0b2d1-158">`[Metadata <IDashboardPropertiesMetadata>]`: The dashboard metadata.</span></span>
    - <span data-ttu-id="0b2d1-159">`[(Any) <Object>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0b2d1-159">`[(Any) <Object>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="0b2d1-160">`[Tag <IDashboardTags>]`: Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="0b2d1-160">`[Tag <IDashboardTags>]`: Resource tags</span></span>
    - <span data-ttu-id="0b2d1-161">`[(Any) <String>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0b2d1-161">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

## <span data-ttu-id="0b2d1-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0b2d1-162">RELATED LINKS</span></span>

