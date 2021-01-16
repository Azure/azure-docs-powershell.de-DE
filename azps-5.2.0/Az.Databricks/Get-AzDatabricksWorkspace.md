---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
ms.openlocfilehash: 7f2bb3f1d378afec5b0774aec2977b507654b931
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368806"
---
# <span data-ttu-id="e96ed-101">Get-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="e96ed-101">Get-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="e96ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e96ed-102">SYNOPSIS</span></span>
<span data-ttu-id="e96ed-103">Ruft den Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="e96ed-103">Gets the workspace.</span></span>

## <span data-ttu-id="e96ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e96ed-104">SYNTAX</span></span>

### <span data-ttu-id="e96ed-105">Liste1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="e96ed-105">List1 (Default)</span></span>
```
Get-AzDatabricksWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e96ed-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="e96ed-106">Get</span></span>
```
Get-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e96ed-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e96ed-107">GetViaIdentity</span></span>
```
Get-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e96ed-108">Liste</span><span class="sxs-lookup"><span data-stu-id="e96ed-108">List</span></span>
```
Get-AzDatabricksWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e96ed-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e96ed-109">DESCRIPTION</span></span>
<span data-ttu-id="e96ed-110">Ruft den Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="e96ed-110">Gets the workspace.</span></span>

## <span data-ttu-id="e96ed-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e96ed-111">EXAMPLES</span></span>

### <span data-ttu-id="e96ed-112">Beispiel 1: Erstellen eines Arbeitsbereichs "Databinnen" mit Namen</span><span class="sxs-lookup"><span data-stu-id="e96ed-112">Example 1: Get a Databricks workspace with name</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="e96ed-113">Dieser Befehl ruft einen Arbeitsbereich "Databungs" in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="e96ed-113">This command gets a Databricks workspace in a resource group.</span></span>

### <span data-ttu-id="e96ed-114">Beispiel 2: Auflisten aller Datenarbeitsräume in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="e96ed-114">Example 2: List all Databricks workspaces in a subscription</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="e96ed-115">Mit diesem Befehl werden alle Databungsarbeitsbereich in einem Abonnement aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e96ed-115">This command lists all Databricks workspaces in a subscription.</span></span>

### <span data-ttu-id="e96ed-116">Beispiel 3: Auflisten aller Arbeitsbereiche in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="e96ed-116">Example 3: List all Databricks workspaces in a resource group</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -ResourceGroupName testgroup

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="e96ed-117">Mit diesem Befehl werden alle Databungsarbeitsbereich in einer Ressourcengruppe aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e96ed-117">This command lists all Databricks workspaces in a resource group.</span></span>

## <span data-ttu-id="e96ed-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e96ed-118">PARAMETERS</span></span>

### <span data-ttu-id="e96ed-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e96ed-119">-DefaultProfile</span></span>
<span data-ttu-id="e96ed-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e96ed-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e96ed-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e96ed-121">-InputObject</span></span>
<span data-ttu-id="e96ed-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e96ed-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e96ed-123">-Name</span><span class="sxs-lookup"><span data-stu-id="e96ed-123">-Name</span></span>
<span data-ttu-id="e96ed-124">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="e96ed-124">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e96ed-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e96ed-125">-ResourceGroupName</span></span>
<span data-ttu-id="e96ed-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e96ed-126">The name of the resource group.</span></span>
<span data-ttu-id="e96ed-127">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="e96ed-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e96ed-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e96ed-128">-SubscriptionId</span></span>
<span data-ttu-id="e96ed-129">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="e96ed-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e96ed-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e96ed-130">CommonParameters</span></span>
<span data-ttu-id="e96ed-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e96ed-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e96ed-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e96ed-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e96ed-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e96ed-133">INPUTS</span></span>

### <span data-ttu-id="e96ed-134">Microsoft.Azure.PowerShell.Cmdlets.Databpersonenbezogenes.Models.IDatabseriesIdentity</span><span class="sxs-lookup"><span data-stu-id="e96ed-134">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="e96ed-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e96ed-135">OUTPUTS</span></span>

### <span data-ttu-id="e96ed-136">Microsoft.Azure.PowerShell.Cmdlets.Databpersonenbezogenes.Models.Api20180401.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="e96ed-136">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="e96ed-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e96ed-137">NOTES</span></span>

<span data-ttu-id="e96ed-138">ALIASE</span><span class="sxs-lookup"><span data-stu-id="e96ed-138">ALIASES</span></span>

<span data-ttu-id="e96ed-139">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="e96ed-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e96ed-140">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e96ed-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e96ed-141">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e96ed-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e96ed-142">INPUTOBJECT <IDatabricksIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="e96ed-142">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e96ed-143">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="e96ed-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e96ed-144">`[PeeringName <String>]`: Der Name des vNet-Arbeitsbereichs-Peerings.</span><span class="sxs-lookup"><span data-stu-id="e96ed-144">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="e96ed-145">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e96ed-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e96ed-146">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="e96ed-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="e96ed-147">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="e96ed-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e96ed-148">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="e96ed-148">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="e96ed-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e96ed-149">RELATED LINKS</span></span>

