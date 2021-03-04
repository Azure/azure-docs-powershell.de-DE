---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/get-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
ms.openlocfilehash: ec44b1ace55a36ebaa56c8b0242db485581c5e10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925848"
---
# <span data-ttu-id="2b661-101">Get-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="2b661-101">Get-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="2b661-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b661-102">SYNOPSIS</span></span>
<span data-ttu-id="2b661-103">Ruft den Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="2b661-103">Gets the workspace.</span></span>

## <span data-ttu-id="2b661-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2b661-104">SYNTAX</span></span>

### <span data-ttu-id="2b661-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="2b661-105">List1 (Default)</span></span>
```
Get-AzDatabricksWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2b661-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="2b661-106">Get</span></span>
```
Get-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2b661-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2b661-107">GetViaIdentity</span></span>
```
Get-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2b661-108">Liste</span><span class="sxs-lookup"><span data-stu-id="2b661-108">List</span></span>
```
Get-AzDatabricksWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2b661-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2b661-109">DESCRIPTION</span></span>
<span data-ttu-id="2b661-110">Ruft den Arbeitsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="2b661-110">Gets the workspace.</span></span>

## <span data-ttu-id="2b661-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2b661-111">EXAMPLES</span></span>

### <span data-ttu-id="2b661-112">Beispiel 1: Erstellen eines Databricks-Arbeitsbereichs mit Namen</span><span class="sxs-lookup"><span data-stu-id="2b661-112">Example 1: Get a Databricks workspace with name</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="2b661-113">Dieser Befehl ruft einen Databricks-Arbeitsbereich in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="2b661-113">This command gets a Databricks workspace in a resource group.</span></span>

### <span data-ttu-id="2b661-114">Beispiel 2: Auflisten aller Databricks-Arbeitsbereiche in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="2b661-114">Example 2: List all Databricks workspaces in a subscription</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="2b661-115">Mit diesem Befehl werden alle Databricks-Arbeitsbereiche in einem Abonnement aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2b661-115">This command lists all Databricks workspaces in a subscription.</span></span>

### <span data-ttu-id="2b661-116">Beispiel 3: Auflisten aller Databricks-Arbeitsbereiche in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="2b661-116">Example 3: List all Databricks workspaces in a resource group</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -ResourceGroupName testgroup

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="2b661-117">Mit diesem Befehl werden alle Databricks-Arbeitsbereiche in einer Ressourcengruppe aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2b661-117">This command lists all Databricks workspaces in a resource group.</span></span>

## <span data-ttu-id="2b661-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2b661-118">PARAMETERS</span></span>

### <span data-ttu-id="2b661-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b661-119">-DefaultProfile</span></span>
<span data-ttu-id="2b661-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2b661-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b661-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b661-121">-InputObject</span></span>
<span data-ttu-id="2b661-122">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="2b661-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2b661-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2b661-123">-Name</span></span>
<span data-ttu-id="2b661-124">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="2b661-124">The name of the workspace.</span></span>

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

### <span data-ttu-id="2b661-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b661-125">-ResourceGroupName</span></span>
<span data-ttu-id="2b661-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2b661-126">The name of the resource group.</span></span>
<span data-ttu-id="2b661-127">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="2b661-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2b661-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2b661-128">-SubscriptionId</span></span>
<span data-ttu-id="2b661-129">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="2b661-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2b661-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b661-130">CommonParameters</span></span>
<span data-ttu-id="2b661-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b661-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b661-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b661-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b661-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2b661-133">INPUTS</span></span>

### <span data-ttu-id="2b661-134">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="2b661-134">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="2b661-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2b661-135">OUTPUTS</span></span>

### <span data-ttu-id="2b661-136">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="2b661-136">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="2b661-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2b661-137">NOTES</span></span>

<span data-ttu-id="2b661-138">ALIASE</span><span class="sxs-lookup"><span data-stu-id="2b661-138">ALIASES</span></span>

<span data-ttu-id="2b661-139">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="2b661-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2b661-140">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="2b661-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2b661-141">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2b661-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2b661-142">INPUTOBJECT <IDatabricksIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="2b661-142">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2b661-143">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="2b661-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2b661-144">`[PeeringName <String>]`: Der Name des Arbeitsbereichs vNet-Peering.</span><span class="sxs-lookup"><span data-stu-id="2b661-144">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="2b661-145">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2b661-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2b661-146">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="2b661-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="2b661-147">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="2b661-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="2b661-148">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="2b661-148">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="2b661-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2b661-149">RELATED LINKS</span></span>

