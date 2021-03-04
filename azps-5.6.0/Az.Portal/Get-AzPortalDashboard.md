---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/powershell/module/az.portal/get-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
ms.openlocfilehash: fc888161df56e3edbf1a51014c7173542e395ad3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937464"
---
# <span data-ttu-id="14a31-101">Get-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="14a31-101">Get-AzPortalDashboard</span></span>

## <span data-ttu-id="14a31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14a31-102">SYNOPSIS</span></span>
<span data-ttu-id="14a31-103">Ruft das Dashboard ab.</span><span class="sxs-lookup"><span data-stu-id="14a31-103">Gets the Dashboard.</span></span>

## <span data-ttu-id="14a31-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14a31-104">SYNTAX</span></span>

### <span data-ttu-id="14a31-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="14a31-105">List1 (Default)</span></span>
```
Get-AzPortalDashboard [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="14a31-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="14a31-106">Get</span></span>
```
Get-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="14a31-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="14a31-107">GetViaIdentity</span></span>
```
Get-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="14a31-108">Liste</span><span class="sxs-lookup"><span data-stu-id="14a31-108">List</span></span>
```
Get-AzPortalDashboard -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="14a31-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="14a31-109">DESCRIPTION</span></span>
<span data-ttu-id="14a31-110">Ruft das Dashboard ab.</span><span class="sxs-lookup"><span data-stu-id="14a31-110">Gets the Dashboard.</span></span>

## <span data-ttu-id="14a31-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="14a31-111">EXAMPLES</span></span>

### <span data-ttu-id="14a31-112">Beispiel 1: Auflisten aller Dashboards in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="14a31-112">Example 1: List all dashboards in a subscription</span></span>
```powershell
PS C:> Get-AzPortalDashboard                                                                                                                     
Location Name                                           Type
-------- ----                                           ----
eastasia my-custom-dashboard1                           Microsoft.Portal/dashboards
westus   my-second-custom-dashboard1                    Microsoft.Portal/dashboards

```

<span data-ttu-id="14a31-113">Auflisten aller Dashboards in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="14a31-113">List all dashboards in a subscription</span></span>

### <span data-ttu-id="14a31-114">Beispiel 2: Anzeigen von Details für ein einzelnes Portaldashboard</span><span class="sxs-lookup"><span data-stu-id="14a31-114">Example 2: Get details for a single Portal Dashboard</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name mydashboard

Location Name        Type
-------- ----        ----
eastus   mydashboard Microsoft.Portal/dashboards
```

<span data-ttu-id="14a31-115">Details für ein einzelnes Dashboard erhalten</span><span class="sxs-lookup"><span data-stu-id="14a31-115">Get details for a single dashboard</span></span>

## <span data-ttu-id="14a31-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="14a31-116">PARAMETERS</span></span>

### <span data-ttu-id="14a31-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14a31-117">-DefaultProfile</span></span>
<span data-ttu-id="14a31-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="14a31-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14a31-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14a31-119">-InputObject</span></span>
<span data-ttu-id="14a31-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="14a31-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="14a31-121">-Name</span><span class="sxs-lookup"><span data-stu-id="14a31-121">-Name</span></span>
<span data-ttu-id="14a31-122">Der Name des Dashboards.</span><span class="sxs-lookup"><span data-stu-id="14a31-122">The name of the dashboard.</span></span>

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

### <span data-ttu-id="14a31-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14a31-123">-ResourceGroupName</span></span>
<span data-ttu-id="14a31-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="14a31-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="14a31-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="14a31-125">-SubscriptionId</span></span>
<span data-ttu-id="14a31-126">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="14a31-126">The Azure subscription ID.</span></span>
<span data-ttu-id="14a31-127">Dies ist eine GUID-formatierte Zeichenfolge (z. B. 000000000-0000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="14a31-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="14a31-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14a31-128">CommonParameters</span></span>
<span data-ttu-id="14a31-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14a31-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14a31-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14a31-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14a31-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="14a31-131">INPUTS</span></span>

### <span data-ttu-id="14a31-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="14a31-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="14a31-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="14a31-133">OUTPUTS</span></span>

### <span data-ttu-id="14a31-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="14a31-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="14a31-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="14a31-135">NOTES</span></span>

<span data-ttu-id="14a31-136">ALIASE</span><span class="sxs-lookup"><span data-stu-id="14a31-136">ALIASES</span></span>

<span data-ttu-id="14a31-137">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="14a31-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="14a31-138">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="14a31-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="14a31-139">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="14a31-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="14a31-140">INPUTOBJECT <IPortalIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="14a31-140">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="14a31-141">`[DashboardName <String>]`: Der Name des Dashboards.</span><span class="sxs-lookup"><span data-stu-id="14a31-141">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="14a31-142">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="14a31-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="14a31-143">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="14a31-143">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="14a31-144">`[SubscriptionId <String>]`: Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="14a31-144">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="14a31-145">Dies ist eine GUID-formatierte Zeichenfolge (z. B. 000000000-0000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="14a31-145">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="14a31-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="14a31-146">RELATED LINKS</span></span>

