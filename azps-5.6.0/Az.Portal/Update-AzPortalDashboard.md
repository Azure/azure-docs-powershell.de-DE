---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/powershell/module/az.portal/update-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Update-AzPortalDashboard.md
ms.openlocfilehash: 97d5519d1b643a04fb1f6375030f178f9ccfbfe1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937416"
---
# <span data-ttu-id="29f22-101">Update-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="29f22-101">Update-AzPortalDashboard</span></span>

## <span data-ttu-id="29f22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29f22-102">SYNOPSIS</span></span>
<span data-ttu-id="29f22-103">Aktualisiert ein vorhandenes Dashboard.</span><span class="sxs-lookup"><span data-stu-id="29f22-103">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="29f22-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29f22-104">SYNTAX</span></span>

### <span data-ttu-id="29f22-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="29f22-105">UpdateExpanded (Default)</span></span>
```
Update-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Lens <Hashtable>] [-Metadata <Hashtable>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="29f22-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="29f22-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPortalDashboard -InputObject <IPortalIdentity> [-Lens <Hashtable>] [-Metadata <Hashtable>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="29f22-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29f22-107">DESCRIPTION</span></span>
<span data-ttu-id="29f22-108">Aktualisiert ein vorhandenes Dashboard.</span><span class="sxs-lookup"><span data-stu-id="29f22-108">Updates an existing Dashboard.</span></span>

## <span data-ttu-id="29f22-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="29f22-109">EXAMPLES</span></span>

### <span data-ttu-id="29f22-110">Beispiel 1: Aktualisieren der Tags eines Dashboards</span><span class="sxs-lookup"><span data-stu-id="29f22-110">Example 1: Update the Tags of a Dashboard</span></span>
```powershell
PS C:\> Update-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="29f22-111">Aktualisieren Sie die Tags in einem Dashboard.</span><span class="sxs-lookup"><span data-stu-id="29f22-111">Update the tags in a dashboard.</span></span>
<span data-ttu-id="29f22-112">Tags werden als Inlinehashtable dargestellt.</span><span class="sxs-lookup"><span data-stu-id="29f22-112">Tags are represented as an inline hashtable.</span></span>

### <span data-ttu-id="29f22-113">Beispiel 2: Aktualisieren von Dashboardtags mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="29f22-113">Example 2: Update Dashboard tags using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name dashbase03 | Update-AzPortalDashboard -Tag @{'hidden-title'="My Dashboard Title"; NewTag="NewValue"}

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="29f22-114">Aktualisieren Sie die Tags in einem Dashboard, das mit Get-AzPortalDashboard erneut wiederholt wurde.</span><span class="sxs-lookup"><span data-stu-id="29f22-114">Update the Tags in a Dashboard retried using Get-AzPortalDashboard.</span></span>
<span data-ttu-id="29f22-115">Dies kann verwendet werden, um die Tags über ein einzelnes Dashboard oder mehrere Dashboards zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="29f22-115">This can be used to update the tags over a single dashboard, or multiple dashboardfs.</span></span>

## <span data-ttu-id="29f22-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="29f22-116">PARAMETERS</span></span>

### <span data-ttu-id="29f22-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29f22-117">-DefaultProfile</span></span>
<span data-ttu-id="29f22-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="29f22-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29f22-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29f22-119">-InputObject</span></span>
<span data-ttu-id="29f22-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="29f22-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="29f22-121">-Lens</span><span class="sxs-lookup"><span data-stu-id="29f22-121">-Lens</span></span>
<span data-ttu-id="29f22-122">Die Dashboardlinsen.</span><span class="sxs-lookup"><span data-stu-id="29f22-122">The dashboard lenses.</span></span>

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

### <span data-ttu-id="29f22-123">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="29f22-123">-Metadata</span></span>
<span data-ttu-id="29f22-124">Die Dashboardmetadaten.</span><span class="sxs-lookup"><span data-stu-id="29f22-124">The dashboard metadata.</span></span>

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

### <span data-ttu-id="29f22-125">-Name</span><span class="sxs-lookup"><span data-stu-id="29f22-125">-Name</span></span>
<span data-ttu-id="29f22-126">Der Name des Dashboards.</span><span class="sxs-lookup"><span data-stu-id="29f22-126">The name of the dashboard.</span></span>

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

### <span data-ttu-id="29f22-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29f22-127">-ResourceGroupName</span></span>
<span data-ttu-id="29f22-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="29f22-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="29f22-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="29f22-129">-SubscriptionId</span></span>
<span data-ttu-id="29f22-130">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="29f22-130">The Azure subscription ID.</span></span>
<span data-ttu-id="29f22-131">Dies ist eine GUID-formatierte Zeichenfolge (z. B. 000000000-0000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="29f22-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="29f22-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="29f22-132">-Tag</span></span>
<span data-ttu-id="29f22-133">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="29f22-133">Resource tags</span></span>

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

### <span data-ttu-id="29f22-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="29f22-134">-Confirm</span></span>
<span data-ttu-id="29f22-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="29f22-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29f22-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29f22-136">-WhatIf</span></span>
<span data-ttu-id="29f22-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="29f22-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29f22-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="29f22-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29f22-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29f22-139">CommonParameters</span></span>
<span data-ttu-id="29f22-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29f22-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29f22-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29f22-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29f22-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="29f22-142">INPUTS</span></span>

### <span data-ttu-id="29f22-143">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="29f22-143">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="29f22-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="29f22-144">OUTPUTS</span></span>

### <span data-ttu-id="29f22-145">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="29f22-145">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="29f22-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="29f22-146">NOTES</span></span>

<span data-ttu-id="29f22-147">ALIASE</span><span class="sxs-lookup"><span data-stu-id="29f22-147">ALIASES</span></span>

<span data-ttu-id="29f22-148">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="29f22-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="29f22-149">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="29f22-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="29f22-150">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="29f22-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="29f22-151">INPUTOBJECT <IPortalIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="29f22-151">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="29f22-152">`[DashboardName <String>]`: Der Name des Dashboards.</span><span class="sxs-lookup"><span data-stu-id="29f22-152">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="29f22-153">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="29f22-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="29f22-154">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="29f22-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="29f22-155">`[SubscriptionId <String>]`: Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="29f22-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="29f22-156">Dies ist eine GUID-formatierte Zeichenfolge (z. B. 000000000-0000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="29f22-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="29f22-157">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="29f22-157">RELATED LINKS</span></span>

