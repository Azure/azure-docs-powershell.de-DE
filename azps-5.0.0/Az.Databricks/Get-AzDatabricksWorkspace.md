---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
ms.openlocfilehash: 7f2bb3f1d378afec5b0774aec2977b507654b931
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297340"
---
# <span data-ttu-id="7ce46-101">Get-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="7ce46-101">Get-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="7ce46-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7ce46-102">SYNOPSIS</span></span>
<span data-ttu-id="7ce46-103">Ruft den Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="7ce46-103">Gets the workspace.</span></span>

## <span data-ttu-id="7ce46-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ce46-104">SYNTAX</span></span>

### <span data-ttu-id="7ce46-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="7ce46-105">List1 (Default)</span></span>
```
Get-AzDatabricksWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7ce46-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="7ce46-106">Get</span></span>
```
Get-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7ce46-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7ce46-107">GetViaIdentity</span></span>
```
Get-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7ce46-108">Liste</span><span class="sxs-lookup"><span data-stu-id="7ce46-108">List</span></span>
```
Get-AzDatabricksWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7ce46-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7ce46-109">DESCRIPTION</span></span>
<span data-ttu-id="7ce46-110">Ruft den Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="7ce46-110">Gets the workspace.</span></span>

## <span data-ttu-id="7ce46-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7ce46-111">EXAMPLES</span></span>

### <span data-ttu-id="7ce46-112">Beispiel 1: Abrufen eines databricks-Arbeitsbereichs mit dem Namen</span><span class="sxs-lookup"><span data-stu-id="7ce46-112">Example 1: Get a Databricks workspace with name</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="7ce46-113">Dieser Befehl ruft einen Arbeitsbereich "databricks" in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="7ce46-113">This command gets a Databricks workspace in a resource group.</span></span>

### <span data-ttu-id="7ce46-114">Beispiel 2: Auflisten aller databricks-Arbeitsbereiche in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="7ce46-114">Example 2: List all Databricks workspaces in a subscription</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="7ce46-115">Dieser Befehl listet alle databricks-Arbeitsbereiche in einem Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="7ce46-115">This command lists all Databricks workspaces in a subscription.</span></span>

### <span data-ttu-id="7ce46-116">Beispiel 3: Auflisten aller databricks-Arbeitsbereiche in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="7ce46-116">Example 3: List all Databricks workspaces in a resource group</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -ResourceGroupName testgroup

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="7ce46-117">Dieser Befehl listet alle databricks-Arbeitsbereiche in einer Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="7ce46-117">This command lists all Databricks workspaces in a resource group.</span></span>

## <span data-ttu-id="7ce46-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ce46-118">PARAMETERS</span></span>

### <span data-ttu-id="7ce46-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ce46-119">-DefaultProfile</span></span>
<span data-ttu-id="7ce46-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7ce46-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ce46-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7ce46-121">-InputObject</span></span>
<span data-ttu-id="7ce46-122">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="7ce46-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7ce46-123">-Name</span><span class="sxs-lookup"><span data-stu-id="7ce46-123">-Name</span></span>
<span data-ttu-id="7ce46-124">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="7ce46-124">The name of the workspace.</span></span>

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

### <span data-ttu-id="7ce46-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ce46-125">-ResourceGroupName</span></span>
<span data-ttu-id="7ce46-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7ce46-126">The name of the resource group.</span></span>
<span data-ttu-id="7ce46-127">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="7ce46-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7ce46-128">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="7ce46-128">-SubscriptionId</span></span>
<span data-ttu-id="7ce46-129">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="7ce46-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="7ce46-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ce46-130">CommonParameters</span></span>
<span data-ttu-id="7ce46-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ce46-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ce46-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ce46-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ce46-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7ce46-133">INPUTS</span></span>

### <span data-ttu-id="7ce46-134">Microsoft. Azure. PowerShell. Cmdlets. databricks. Models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="7ce46-134">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="7ce46-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7ce46-135">OUTPUTS</span></span>

### <span data-ttu-id="7ce46-136">Microsoft. Azure. PowerShell. Cmdlets. databricks. Models. Api20180401. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="7ce46-136">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="7ce46-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="7ce46-137">NOTES</span></span>

<span data-ttu-id="7ce46-138">Aliase</span><span class="sxs-lookup"><span data-stu-id="7ce46-138">ALIASES</span></span>

<span data-ttu-id="7ce46-139">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7ce46-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7ce46-140">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7ce46-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7ce46-141">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="7ce46-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7ce46-142">Inputobject <IDatabricksIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="7ce46-142">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7ce46-143">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="7ce46-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7ce46-144">`[PeeringName <String>]`: Der Name des Arbeitsbereichs vNet Peering.</span><span class="sxs-lookup"><span data-stu-id="7ce46-144">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="7ce46-145">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7ce46-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7ce46-146">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="7ce46-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="7ce46-147">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="7ce46-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="7ce46-148">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="7ce46-148">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="7ce46-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7ce46-149">RELATED LINKS</span></span>

