---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/powershell/module/az.monitoringsolutions/remove-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/Remove-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: f3a41317663c5b1009a45bfe711cdf3410a784c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934872"
---
# <span data-ttu-id="2181b-101">Remove-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="2181b-101">Remove-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="2181b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2181b-102">SYNOPSIS</span></span>
<span data-ttu-id="2181b-103">Löscht die Projektmappe im Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2181b-103">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="2181b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2181b-104">SYNTAX</span></span>

### <span data-ttu-id="2181b-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="2181b-105">Delete (Default)</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2181b-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2181b-106">DeleteViaIdentity</span></span>
```
Remove-AzMonitorLogAnalyticsSolution -InputObject <IMonitoringSolutionsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2181b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2181b-107">DESCRIPTION</span></span>
<span data-ttu-id="2181b-108">Löscht die Projektmappe im Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2181b-108">Deletes the solution in the subscription.</span></span>

## <span data-ttu-id="2181b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2181b-109">EXAMPLES</span></span>

### <span data-ttu-id="2181b-110">Beispiel 1: Entfernen einer Lösung für die Überwachungsprotokollanalyse nach Name</span><span class="sxs-lookup"><span data-stu-id="2181b-110">Example 1: Remove a monitor log analytics solution by name</span></span>
```powershell
PS C:\> Remove-AzMonitorLogAnalyticsSolution  -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-2vob7n)'

```

<span data-ttu-id="2181b-111">Mit diesem Befehl wird eine Lösung für die Überwachungsprotokollanalyse nach Name entfernt.</span><span class="sxs-lookup"><span data-stu-id="2181b-111">This command removes a monitor log analytics solution by name.</span></span>

### <span data-ttu-id="2181b-112">Beispiel 2: Entfernen einer Lösung für die Überwachungsprotokollanalyse nach Objekt</span><span class="sxs-lookup"><span data-stu-id="2181b-112">Example 2: Remove a monitor log analytics solution by object</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-pevful)'
PS C:\> Remove-AzMonitorLogAnalyticsSolution -InputObject $monitor

```

<span data-ttu-id="2181b-113">Mit diesem Befehl wird eine Lösung für die Überwachungsprotokollanalyse nach Objekt entfernt.</span><span class="sxs-lookup"><span data-stu-id="2181b-113">This command removes a monitor log analytics solution by object.</span></span>

### <span data-ttu-id="2181b-114">Beispiel 3: Entfernen einer Lösung für die Überwachungsprotokollanalyse per Pipeline</span><span class="sxs-lookup"><span data-stu-id="2181b-114">Example 3: Remove a monitor log analytics solution by pipeline</span></span>
```powershell
PS C:\> $monitor = Get-AzMonitorLogAnalyticsSolution -ResourceGroupName azureps-manual-test -Name 'Containers(monitoringworkspace-asdehu)' | Remove-AzMonitorLogAnalyticsSolution

```

<span data-ttu-id="2181b-115">Mit diesem Befehl wird eine Lösung für die Überwachungsprotokollanalyse per Pipeline entfernt.</span><span class="sxs-lookup"><span data-stu-id="2181b-115">This command removes a monitor log analytics solution by pipeline.</span></span>

## <span data-ttu-id="2181b-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2181b-116">PARAMETERS</span></span>

### <span data-ttu-id="2181b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2181b-117">-DefaultProfile</span></span>
<span data-ttu-id="2181b-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2181b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2181b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2181b-119">-InputObject</span></span>
<span data-ttu-id="2181b-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="2181b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2181b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2181b-121">-Name</span></span>
<span data-ttu-id="2181b-122">Benutzername der Projektmappe.</span><span class="sxs-lookup"><span data-stu-id="2181b-122">User Solution Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2181b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2181b-123">-PassThru</span></span>
<span data-ttu-id="2181b-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2181b-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2181b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2181b-125">-ResourceGroupName</span></span>
<span data-ttu-id="2181b-126">Der Name der zu erhaltende Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2181b-126">The name of the resource group to get.</span></span>
<span data-ttu-id="2181b-127">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="2181b-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2181b-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2181b-128">-SubscriptionId</span></span>
<span data-ttu-id="2181b-129">Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="2181b-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2181b-130">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="2181b-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2181b-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2181b-131">-Confirm</span></span>
<span data-ttu-id="2181b-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2181b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2181b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2181b-133">-WhatIf</span></span>
<span data-ttu-id="2181b-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2181b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2181b-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2181b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2181b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2181b-136">CommonParameters</span></span>
<span data-ttu-id="2181b-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2181b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2181b-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2181b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2181b-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2181b-139">INPUTS</span></span>

### <span data-ttu-id="2181b-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span><span class="sxs-lookup"><span data-stu-id="2181b-140">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.IMonitoringSolutionsIdentity</span></span>

## <span data-ttu-id="2181b-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2181b-141">OUTPUTS</span></span>

### <span data-ttu-id="2181b-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2181b-142">System.Boolean</span></span>

## <span data-ttu-id="2181b-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2181b-143">NOTES</span></span>

<span data-ttu-id="2181b-144">ALIASE</span><span class="sxs-lookup"><span data-stu-id="2181b-144">ALIASES</span></span>

<span data-ttu-id="2181b-145">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="2181b-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2181b-146">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="2181b-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2181b-147">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2181b-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2181b-148">INPUTOBJECT <IMonitoringSolutionsIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="2181b-148">INPUTOBJECT <IMonitoringSolutionsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2181b-149">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="2181b-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2181b-150">`[ManagementAssociationName <String>]`: Name der Benutzerverwaltungsassoziation.</span><span class="sxs-lookup"><span data-stu-id="2181b-150">`[ManagementAssociationName <String>]`: User ManagementAssociation Name.</span></span>
  - <span data-ttu-id="2181b-151">`[ManagementConfigurationName <String>]`: Name der Benutzerverwaltungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="2181b-151">`[ManagementConfigurationName <String>]`: User Management Configuration Name.</span></span>
  - <span data-ttu-id="2181b-152">`[ProviderName <String>]`: Anbietername für die übergeordnete Ressource.</span><span class="sxs-lookup"><span data-stu-id="2181b-152">`[ProviderName <String>]`: Provider name for the parent resource.</span></span>
  - <span data-ttu-id="2181b-153">`[ResourceGroupName <String>]`: Der Name der zu erhaltende Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2181b-153">`[ResourceGroupName <String>]`: The name of the resource group to get.</span></span> <span data-ttu-id="2181b-154">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="2181b-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="2181b-155">`[ResourceName <String>]`: Übergeordneter Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="2181b-155">`[ResourceName <String>]`: Parent resource name.</span></span>
  - <span data-ttu-id="2181b-156">`[ResourceType <String>]`: Ressourcentyp für die übergeordnete Ressource</span><span class="sxs-lookup"><span data-stu-id="2181b-156">`[ResourceType <String>]`: Resource type for the parent resource</span></span>
  - <span data-ttu-id="2181b-157">`[SolutionName <String>]`: Name der Benutzerlösung.</span><span class="sxs-lookup"><span data-stu-id="2181b-157">`[SolutionName <String>]`: User Solution Name.</span></span>
  - <span data-ttu-id="2181b-158">`[SubscriptionId <String>]`: Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="2181b-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2181b-159">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="2181b-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2181b-160">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2181b-160">RELATED LINKS</span></span>

