---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdWorkspace.md
ms.openlocfilehash: 3fa80fc69679346e3462a96340f4af9fc6a251d5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387286"
---
# <span data-ttu-id="a2eb0-101">Get-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="a2eb0-101">Get-AzWvdWorkspace</span></span>

## <span data-ttu-id="a2eb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2eb0-102">SYNOPSIS</span></span>
<span data-ttu-id="a2eb0-103">Erstellen sie einen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="a2eb0-103">Get a workspace.</span></span>

## <span data-ttu-id="a2eb0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a2eb0-104">SYNTAX</span></span>

### <span data-ttu-id="a2eb0-105">Liste1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="a2eb0-105">List1 (Default)</span></span>
```
Get-AzWvdWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a2eb0-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="a2eb0-106">Get</span></span>
```
Get-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a2eb0-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a2eb0-107">GetViaIdentity</span></span>
```
Get-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="a2eb0-108">Liste</span><span class="sxs-lookup"><span data-stu-id="a2eb0-108">List</span></span>
```
Get-AzWvdWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a2eb0-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a2eb0-109">DESCRIPTION</span></span>
<span data-ttu-id="a2eb0-110">Erstellen sie einen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="a2eb0-110">Get a workspace.</span></span>

## <span data-ttu-id="a2eb0-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a2eb0-111">EXAMPLES</span></span>

### <span data-ttu-id="a2eb0-112">Beispiel 1: Erstellen eines virtuellen Desktoparbeitsbereichs für Windows nach Name</span><span class="sxs-lookup"><span data-stu-id="a2eb0-112">Example 1: Get a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> Get-AzWvdWorkspace -ResourceGroupName ResourceGroupName -Name WorkspaceName

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="a2eb0-113">Dieser Befehl ruft einen virtuellen Windows-Desktoparbeitsbereich in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="a2eb0-113">This command gets a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="a2eb0-114">Beispiel 2: Auflisten virtueller Desktoparbeitsräume von Windows</span><span class="sxs-lookup"><span data-stu-id="a2eb0-114">Example 2: List Windows Virtual Desktop Workspaces</span></span>
```powershell
PS C:\> Get-AzWvdWorkspace -ResourceGroupName ResourceGroupName

Location   Name           Type
--------   ----           ----
eastus     WorkspaceName1 Microsoft.DesktopVirtualization/workspaces
eastus     WorkspaceName2 Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="a2eb0-115">Dieser Befehl listet einen virtuellen Windows-Desktoparbeitsbereich in einer Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="a2eb0-115">This command lists a Windows Virtual Desktop Workspaces in a Resource Group.</span></span>

## <span data-ttu-id="a2eb0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2eb0-116">PARAMETERS</span></span>

### <span data-ttu-id="a2eb0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2eb0-117">-DefaultProfile</span></span>
<span data-ttu-id="a2eb0-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a2eb0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2eb0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2eb0-119">-InputObject</span></span>
<span data-ttu-id="a2eb0-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="a2eb0-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2eb0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a2eb0-121">-Name</span></span>
<span data-ttu-id="a2eb0-122">Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="a2eb0-122">The name of the workspace</span></span>

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

### <span data-ttu-id="a2eb0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2eb0-123">-ResourceGroupName</span></span>
<span data-ttu-id="a2eb0-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a2eb0-124">The name of the resource group.</span></span>
<span data-ttu-id="a2eb0-125">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="a2eb0-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a2eb0-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a2eb0-126">-SubscriptionId</span></span>
<span data-ttu-id="a2eb0-127">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="a2eb0-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a2eb0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2eb0-128">CommonParameters</span></span>
<span data-ttu-id="a2eb0-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2eb0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2eb0-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2eb0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2eb0-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a2eb0-131">INPUTS</span></span>

### <span data-ttu-id="a2eb0-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="a2eb0-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="a2eb0-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a2eb0-133">OUTPUTS</span></span>

### <span data-ttu-id="a2eb0-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="a2eb0-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span></span>

## <span data-ttu-id="a2eb0-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a2eb0-135">NOTES</span></span>

<span data-ttu-id="a2eb0-136">ALIASE</span><span class="sxs-lookup"><span data-stu-id="a2eb0-136">ALIASES</span></span>

<span data-ttu-id="a2eb0-137">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="a2eb0-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a2eb0-138">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a2eb0-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a2eb0-139">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a2eb0-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a2eb0-140">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="a2eb0-140">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a2eb0-141">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="a2eb0-141">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="a2eb0-142">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="a2eb0-142">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="a2eb0-143">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="a2eb0-143">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="a2eb0-144">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="a2eb0-144">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="a2eb0-145">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="a2eb0-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a2eb0-146">`[MsixPackageFullName <String>]`: Der versionspezifische Paketname des vollständigen Pakets des MSIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="a2eb0-146">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="a2eb0-147">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a2eb0-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a2eb0-148">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="a2eb0-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="a2eb0-149">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="a2eb0-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="a2eb0-150">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="a2eb0-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a2eb0-151">`[UserSessionId <String>]`: Der Name der Benutzersitzung im angegebenen Sitzungshost</span><span class="sxs-lookup"><span data-stu-id="a2eb0-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="a2eb0-152">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="a2eb0-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="a2eb0-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a2eb0-153">RELATED LINKS</span></span>

