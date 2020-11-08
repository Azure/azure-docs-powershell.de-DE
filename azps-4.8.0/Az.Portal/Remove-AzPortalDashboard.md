---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/remove-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Remove-AzPortalDashboard.md
ms.openlocfilehash: f0ef681f09caf43ac2f2100d1a30af19b1b3c364
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174485"
---
# <span data-ttu-id="8e4fe-101">Remove-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="8e4fe-101">Remove-AzPortalDashboard</span></span>

## <span data-ttu-id="8e4fe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8e4fe-102">SYNOPSIS</span></span>
<span data-ttu-id="8e4fe-103">Löscht das Dashboard.</span><span class="sxs-lookup"><span data-stu-id="8e4fe-103">Deletes the Dashboard.</span></span>

## <span data-ttu-id="8e4fe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e4fe-104">SYNTAX</span></span>

### <span data-ttu-id="8e4fe-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="8e4fe-105">Delete (Default)</span></span>
```
Remove-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8e4fe-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8e4fe-106">DeleteViaIdentity</span></span>
```
Remove-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8e4fe-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e4fe-107">DESCRIPTION</span></span>
<span data-ttu-id="8e4fe-108">Löscht das Dashboard.</span><span class="sxs-lookup"><span data-stu-id="8e4fe-108">Deletes the Dashboard.</span></span>

## <span data-ttu-id="8e4fe-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8e4fe-109">EXAMPLES</span></span>

### <span data-ttu-id="8e4fe-110">Beispiel 1: Entfernen eines Dashboards</span><span class="sxs-lookup"><span data-stu-id="8e4fe-110">Example 1: Remove a Dashboard</span></span>
```powershell
PS C:\td\> Remove-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02
```

<span data-ttu-id="8e4fe-111">Entfernen Sie einen Dashbaord mit dem Namen der Ressourcengruppe und dem Dashboardnamen.</span><span class="sxs-lookup"><span data-stu-id="8e4fe-111">Remove a Dashbaord using resource group name and dashboard name.</span></span>

### <span data-ttu-id="8e4fe-112">Beispiel 2: Entfernen eines Dashboards mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="8e4fe-112">Example 2: Remove a Dashboard using the pipeline</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -DashboardName dashbase02 | Remove-AzPortalDashboard
```

<span data-ttu-id="8e4fe-113">Entfernen Sie das von einem Get-AzDashboard-Anruf zurückgegebene Dashboard.</span><span class="sxs-lookup"><span data-stu-id="8e4fe-113">Remove the dashboard returned from a Get-AzDashboard call.</span></span>

## <span data-ttu-id="8e4fe-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e4fe-114">PARAMETERS</span></span>

### <span data-ttu-id="8e4fe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e4fe-115">-DefaultProfile</span></span>
<span data-ttu-id="8e4fe-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e4fe-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e4fe-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8e4fe-117">-InputObject</span></span>
<span data-ttu-id="8e4fe-118">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="8e4fe-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e4fe-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8e4fe-119">-Name</span></span>
<span data-ttu-id="8e4fe-120">Der Name des Dashboards.</span><span class="sxs-lookup"><span data-stu-id="8e4fe-120">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e4fe-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e4fe-121">-PassThru</span></span>
<span data-ttu-id="8e4fe-122">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="8e4fe-122">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e4fe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e4fe-123">-ResourceGroupName</span></span>
<span data-ttu-id="8e4fe-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8e4fe-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e4fe-125">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="8e4fe-125">-SubscriptionId</span></span>
<span data-ttu-id="8e4fe-126">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="8e4fe-126">The Azure subscription ID.</span></span>
<span data-ttu-id="8e4fe-127">Hierbei handelt es sich um eine GUID-formatierte Zeichenfolge (z.b. 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="8e4fe-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e4fe-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8e4fe-128">-Confirm</span></span>
<span data-ttu-id="8e4fe-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8e4fe-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e4fe-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e4fe-130">-WhatIf</span></span>
<span data-ttu-id="8e4fe-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8e4fe-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e4fe-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8e4fe-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e4fe-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e4fe-133">CommonParameters</span></span>
<span data-ttu-id="8e4fe-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e4fe-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e4fe-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e4fe-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e4fe-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8e4fe-136">INPUTS</span></span>

### <span data-ttu-id="8e4fe-137">Microsoft. Azure. PowerShell. Cmdlets. Portal. Models. IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="8e4fe-137">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="8e4fe-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8e4fe-138">OUTPUTS</span></span>

### <span data-ttu-id="8e4fe-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8e4fe-139">System.Boolean</span></span>

## <span data-ttu-id="8e4fe-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="8e4fe-140">NOTES</span></span>

<span data-ttu-id="8e4fe-141">Aliase</span><span class="sxs-lookup"><span data-stu-id="8e4fe-141">ALIASES</span></span>

<span data-ttu-id="8e4fe-142">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8e4fe-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8e4fe-143">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8e4fe-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8e4fe-144">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="8e4fe-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8e4fe-145">Inputobject <IPortalIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="8e4fe-145">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8e4fe-146">`[DashboardName <String>]`: Der Name des Dashboards.</span><span class="sxs-lookup"><span data-stu-id="8e4fe-146">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="8e4fe-147">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="8e4fe-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8e4fe-148">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8e4fe-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="8e4fe-149">`[SubscriptionId <String>]`: Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="8e4fe-149">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="8e4fe-150">Hierbei handelt es sich um eine GUID-formatierte Zeichenfolge (z.b. 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="8e4fe-150">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="8e4fe-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8e4fe-151">RELATED LINKS</span></span>

