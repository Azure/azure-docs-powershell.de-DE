---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/get-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
ms.openlocfilehash: aa11a9828c422069823226b2d5df57efc84f8c7b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179389"
---
# <span data-ttu-id="17ff0-101">Get-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="17ff0-101">Get-AzPortalDashboard</span></span>

## <span data-ttu-id="17ff0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="17ff0-102">SYNOPSIS</span></span>
<span data-ttu-id="17ff0-103">Ruft das Dashboard ab.</span><span class="sxs-lookup"><span data-stu-id="17ff0-103">Gets the Dashboard.</span></span>

## <span data-ttu-id="17ff0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="17ff0-104">SYNTAX</span></span>

### <span data-ttu-id="17ff0-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="17ff0-105">List1 (Default)</span></span>
```
Get-AzPortalDashboard [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="17ff0-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="17ff0-106">Get</span></span>
```
Get-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="17ff0-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="17ff0-107">GetViaIdentity</span></span>
```
Get-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="17ff0-108">Liste</span><span class="sxs-lookup"><span data-stu-id="17ff0-108">List</span></span>
```
Get-AzPortalDashboard -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="17ff0-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17ff0-109">DESCRIPTION</span></span>
<span data-ttu-id="17ff0-110">Ruft das Dashboard ab.</span><span class="sxs-lookup"><span data-stu-id="17ff0-110">Gets the Dashboard.</span></span>

## <span data-ttu-id="17ff0-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="17ff0-111">EXAMPLES</span></span>

### <span data-ttu-id="17ff0-112">Beispiel 1: Auflisten aller Dashboards in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="17ff0-112">Example 1: List all dashboards in a subscription</span></span>
```powershell
PS C:> Get-AzPortalDashboard                                                                                                                     
Location Name                                           Type
-------- ----                                           ----
eastasia my-custom-dashboard1                           Microsoft.Portal/dashboards
westus   my-second-custom-dashboard1                    Microsoft.Portal/dashboards

```

<span data-ttu-id="17ff0-113">Auflisten aller Dashboards in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="17ff0-113">List all dashboards in a subscription</span></span>

### <span data-ttu-id="17ff0-114">Beispiel 2: Abrufen von Details für ein einzelnes Portal-Dashboard</span><span class="sxs-lookup"><span data-stu-id="17ff0-114">Example 2: Get details for a single Portal Dashboard</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name mydashboard

Location Name        Type
-------- ----        ----
eastus   mydashboard Microsoft.Portal/dashboards
```

<span data-ttu-id="17ff0-115">Abrufen von Details für ein einzelnes Dashboard</span><span class="sxs-lookup"><span data-stu-id="17ff0-115">Get details for a single dashboard</span></span>

## <span data-ttu-id="17ff0-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="17ff0-116">PARAMETERS</span></span>

### <span data-ttu-id="17ff0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17ff0-117">-DefaultProfile</span></span>
<span data-ttu-id="17ff0-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="17ff0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17ff0-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="17ff0-119">-InputObject</span></span>
<span data-ttu-id="17ff0-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="17ff0-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="17ff0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="17ff0-121">-Name</span></span>
<span data-ttu-id="17ff0-122">Der Name des Dashboards.</span><span class="sxs-lookup"><span data-stu-id="17ff0-122">The name of the dashboard.</span></span>

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

### <span data-ttu-id="17ff0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17ff0-123">-ResourceGroupName</span></span>
<span data-ttu-id="17ff0-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="17ff0-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="17ff0-125">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="17ff0-125">-SubscriptionId</span></span>
<span data-ttu-id="17ff0-126">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="17ff0-126">The Azure subscription ID.</span></span>
<span data-ttu-id="17ff0-127">Hierbei handelt es sich um eine GUID-formatierte Zeichenfolge (z.b. 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="17ff0-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="17ff0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17ff0-128">CommonParameters</span></span>
<span data-ttu-id="17ff0-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17ff0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17ff0-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17ff0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17ff0-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="17ff0-131">INPUTS</span></span>

### <span data-ttu-id="17ff0-132">Microsoft. Azure. PowerShell. Cmdlets. Portal. Models. IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="17ff0-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="17ff0-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="17ff0-133">OUTPUTS</span></span>

### <span data-ttu-id="17ff0-134">Microsoft. Azure. PowerShell. Cmdlets. Portal. Models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="17ff0-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="17ff0-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="17ff0-135">NOTES</span></span>

<span data-ttu-id="17ff0-136">Aliase</span><span class="sxs-lookup"><span data-stu-id="17ff0-136">ALIASES</span></span>

<span data-ttu-id="17ff0-137">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="17ff0-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="17ff0-138">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="17ff0-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="17ff0-139">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="17ff0-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="17ff0-140">Inputobject <IPortalIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="17ff0-140">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="17ff0-141">`[DashboardName <String>]`: Der Name des Dashboards.</span><span class="sxs-lookup"><span data-stu-id="17ff0-141">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="17ff0-142">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="17ff0-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="17ff0-143">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="17ff0-143">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="17ff0-144">`[SubscriptionId <String>]`: Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="17ff0-144">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="17ff0-145">Hierbei handelt es sich um eine GUID-formatierte Zeichenfolge (z.b. 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="17ff0-145">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="17ff0-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="17ff0-146">RELATED LINKS</span></span>

