---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/get-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
ms.openlocfilehash: aa11a9828c422069823226b2d5df57efc84f8c7b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298867"
---
# <span data-ttu-id="e613c-101">Get-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="e613c-101">Get-AzPortalDashboard</span></span>

## <span data-ttu-id="e613c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e613c-102">SYNOPSIS</span></span>
<span data-ttu-id="e613c-103">Ruft das Dashboard ab.</span><span class="sxs-lookup"><span data-stu-id="e613c-103">Gets the Dashboard.</span></span>

## <span data-ttu-id="e613c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e613c-104">SYNTAX</span></span>

### <span data-ttu-id="e613c-105">Liste1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="e613c-105">List1 (Default)</span></span>
```
Get-AzPortalDashboard [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e613c-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="e613c-106">Get</span></span>
```
Get-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e613c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e613c-107">GetViaIdentity</span></span>
```
Get-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e613c-108">Liste</span><span class="sxs-lookup"><span data-stu-id="e613c-108">List</span></span>
```
Get-AzPortalDashboard -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e613c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e613c-109">DESCRIPTION</span></span>
<span data-ttu-id="e613c-110">Ruft das Dashboard ab.</span><span class="sxs-lookup"><span data-stu-id="e613c-110">Gets the Dashboard.</span></span>

## <span data-ttu-id="e613c-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e613c-111">EXAMPLES</span></span>

### <span data-ttu-id="e613c-112">Beispiel 1: Auflisten aller Dashboards in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="e613c-112">Example 1: List all dashboards in a subscription</span></span>
```powershell
PS C:> Get-AzPortalDashboard                                                                                                                     
Location Name                                           Type
-------- ----                                           ----
eastasia my-custom-dashboard1                           Microsoft.Portal/dashboards
westus   my-second-custom-dashboard1                    Microsoft.Portal/dashboards

```

<span data-ttu-id="e613c-113">Auflisten aller Dashboards in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="e613c-113">List all dashboards in a subscription</span></span>

### <span data-ttu-id="e613c-114">Beispiel 2: Anzeigen von Details für ein einzelnes Portaldashboard</span><span class="sxs-lookup"><span data-stu-id="e613c-114">Example 2: Get details for a single Portal Dashboard</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name mydashboard

Location Name        Type
-------- ----        ----
eastus   mydashboard Microsoft.Portal/dashboards
```

<span data-ttu-id="e613c-115">Anzeigen von Details für ein einzelnes Dashboard</span><span class="sxs-lookup"><span data-stu-id="e613c-115">Get details for a single dashboard</span></span>

## <span data-ttu-id="e613c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e613c-116">PARAMETERS</span></span>

### <span data-ttu-id="e613c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e613c-117">-DefaultProfile</span></span>
<span data-ttu-id="e613c-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e613c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e613c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e613c-119">-InputObject</span></span>
<span data-ttu-id="e613c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e613c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e613c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e613c-121">-Name</span></span>
<span data-ttu-id="e613c-122">Der Name des Dashboards.</span><span class="sxs-lookup"><span data-stu-id="e613c-122">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e613c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e613c-123">-ResourceGroupName</span></span>
<span data-ttu-id="e613c-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e613c-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e613c-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e613c-125">-SubscriptionId</span></span>
<span data-ttu-id="e613c-126">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="e613c-126">The Azure subscription ID.</span></span>
<span data-ttu-id="e613c-127">Dies ist eine GUID-formatierte Zeichenfolge (z. B. 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="e613c-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e613c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e613c-128">CommonParameters</span></span>
<span data-ttu-id="e613c-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e613c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e613c-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e613c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e613c-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e613c-131">INPUTS</span></span>

### <span data-ttu-id="e613c-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="e613c-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="e613c-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e613c-133">OUTPUTS</span></span>

### <span data-ttu-id="e613c-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="e613c-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="e613c-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e613c-135">NOTES</span></span>

<span data-ttu-id="e613c-136">ALIASE</span><span class="sxs-lookup"><span data-stu-id="e613c-136">ALIASES</span></span>

<span data-ttu-id="e613c-137">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="e613c-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e613c-138">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e613c-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e613c-139">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e613c-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e613c-140">INPUTOBJECT <IPortalIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="e613c-140">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e613c-141">`[DashboardName <String>]`: Der Name des Dashboards.</span><span class="sxs-lookup"><span data-stu-id="e613c-141">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="e613c-142">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="e613c-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e613c-143">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e613c-143">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="e613c-144">`[SubscriptionId <String>]`: Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="e613c-144">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="e613c-145">Dies ist eine GUID-formatierte Zeichenfolge (z. B. 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="e613c-145">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="e613c-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e613c-146">RELATED LINKS</span></span>

