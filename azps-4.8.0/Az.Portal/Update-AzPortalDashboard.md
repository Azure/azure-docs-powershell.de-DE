---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/update-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
ms.openlocfilehash: 42c5d90a24e671c47245ace0046c6f5987dbcd94
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174478"
---
# <span data-ttu-id="2eab5-101">Update-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="2eab5-101">Update-AzPortalDashboard</span></span>

## <span data-ttu-id="2eab5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2eab5-102">SYNOPSIS</span></span>
<span data-ttu-id="2eab5-103">Aktualisiert ein vorhandenes Dashboard.</span><span class="sxs-lookup"><span data-stu-id="2eab5-103">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="2eab5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2eab5-104">SYNTAX</span></span>

### <span data-ttu-id="2eab5-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="2eab5-105">UpdateExpanded (Default)</span></span>
```
Update-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2eab5-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2eab5-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPortalDashboard -InputObject <IPortalIdentity> [-Lens <Hashtable>] [-Metadata <Hashtable>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2eab5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2eab5-107">DESCRIPTION</span></span>
<span data-ttu-id="2eab5-108">Aktualisiert ein vorhandenes Dashboard.</span><span class="sxs-lookup"><span data-stu-id="2eab5-108">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="2eab5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2eab5-109">EXAMPLES</span></span>

### <span data-ttu-id="2eab5-110">Beispiel 1: Aktualisieren der Tags eines Dashboards</span><span class="sxs-lookup"><span data-stu-id="2eab5-110">Example 1: Update the Tags of a Dashboard</span></span>
```powershell
PS C:\> Update-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="2eab5-111">Aktualisieren Sie die Tags in einem Dashboard.</span><span class="sxs-lookup"><span data-stu-id="2eab5-111">Update the tags in a dashboard.</span></span>
<span data-ttu-id="2eab5-112">Tags werden als Inline-Hashtable dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2eab5-112">Tags are represented as an inline hashtable.</span></span>

### <span data-ttu-id="2eab5-113">Beispiel 2: Aktualisieren von Dashboard-Tags mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="2eab5-113">Example 2: Update Dashboard tags using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 | Update-AzPortalDashboard -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="2eab5-114">Aktualisieren Sie die Tags in einem Dashboard, das mit Get-AzPortalDashboard wiederholt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2eab5-114">Update the Tags in a Dashboard retried using Get-AzPortalDashboard.</span></span>
<span data-ttu-id="2eab5-115">Dies kann verwendet werden, um die Tags über ein einzelnes Dashboard oder mehrere dashboardfs zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="2eab5-115">This can be used to update the tags over a single dashboard, or multiple dashboardfs.</span></span>

## <span data-ttu-id="2eab5-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="2eab5-116">PARAMETERS</span></span>

### <span data-ttu-id="2eab5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eab5-117">-DefaultProfile</span></span>
<span data-ttu-id="2eab5-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2eab5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2eab5-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2eab5-119">-InputObject</span></span>
<span data-ttu-id="2eab5-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="2eab5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2eab5-121">-Objektiv</span><span class="sxs-lookup"><span data-stu-id="2eab5-121">-Lens</span></span>
<span data-ttu-id="2eab5-122">Die Dashboard-Objektive.</span><span class="sxs-lookup"><span data-stu-id="2eab5-122">The dashboard lenses.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eab5-123">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="2eab5-123">-Metadata</span></span>
<span data-ttu-id="2eab5-124">Die Dashboard-Metadaten.</span><span class="sxs-lookup"><span data-stu-id="2eab5-124">The dashboard metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eab5-125">-Name</span><span class="sxs-lookup"><span data-stu-id="2eab5-125">-Name</span></span>
<span data-ttu-id="2eab5-126">Der Name des Dashboards.</span><span class="sxs-lookup"><span data-stu-id="2eab5-126">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eab5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2eab5-127">-ResourceGroupName</span></span>
<span data-ttu-id="2eab5-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2eab5-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eab5-129">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="2eab5-129">-SubscriptionId</span></span>
<span data-ttu-id="2eab5-130">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="2eab5-130">The Azure subscription ID.</span></span>
<span data-ttu-id="2eab5-131">Hierbei handelt es sich um eine GUID-formatierte Zeichenfolge (z.b. 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="2eab5-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eab5-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="2eab5-132">-Tag</span></span>
<span data-ttu-id="2eab5-133">Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="2eab5-133">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eab5-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2eab5-134">-Confirm</span></span>
<span data-ttu-id="2eab5-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2eab5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2eab5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2eab5-136">-WhatIf</span></span>
<span data-ttu-id="2eab5-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2eab5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2eab5-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2eab5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2eab5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eab5-139">CommonParameters</span></span>
<span data-ttu-id="2eab5-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eab5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eab5-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2eab5-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eab5-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2eab5-142">INPUTS</span></span>

### <span data-ttu-id="2eab5-143">Microsoft. Azure. PowerShell. Cmdlets. Portal. Models. IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="2eab5-143">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="2eab5-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2eab5-144">OUTPUTS</span></span>

### <span data-ttu-id="2eab5-145">Microsoft. Azure. PowerShell. Cmdlets. Portal. Models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="2eab5-145">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="2eab5-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="2eab5-146">NOTES</span></span>

<span data-ttu-id="2eab5-147">Aliase</span><span class="sxs-lookup"><span data-stu-id="2eab5-147">ALIASES</span></span>

<span data-ttu-id="2eab5-148">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2eab5-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2eab5-149">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2eab5-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2eab5-150">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="2eab5-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2eab5-151">Inputobject <IPortalIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="2eab5-151">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2eab5-152">`[DashboardName <String>]`: Der Name des Dashboards.</span><span class="sxs-lookup"><span data-stu-id="2eab5-152">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="2eab5-153">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="2eab5-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2eab5-154">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2eab5-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="2eab5-155">`[SubscriptionId <String>]`: Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="2eab5-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="2eab5-156">Hierbei handelt es sich um eine GUID-formatierte Zeichenfolge (z.b. 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="2eab5-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="2eab5-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2eab5-157">RELATED LINKS</span></span>

