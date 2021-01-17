---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
ms.openlocfilehash: de52995d5cda17e332c137966f58b349d64c01f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467915"
---
# <span data-ttu-id="58c17-101">Get-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="58c17-101">Get-AzWvdDesktop</span></span>

## <span data-ttu-id="58c17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58c17-102">SYNOPSIS</span></span>
<span data-ttu-id="58c17-103">"Desktop herunterladen" aus.</span><span class="sxs-lookup"><span data-stu-id="58c17-103">Get a desktop.</span></span>

## <span data-ttu-id="58c17-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58c17-104">SYNTAX</span></span>

### <span data-ttu-id="58c17-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="58c17-105">List (Default)</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="58c17-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="58c17-106">Get</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="58c17-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="58c17-107">GetViaIdentity</span></span>
```
Get-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="58c17-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="58c17-108">DESCRIPTION</span></span>
<span data-ttu-id="58c17-109">"Desktop herunterladen" aus.</span><span class="sxs-lookup"><span data-stu-id="58c17-109">Get a desktop.</span></span>

## <span data-ttu-id="58c17-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="58c17-110">EXAMPLES</span></span>

### <span data-ttu-id="58c17-111">Beispiel 1: Erhalten eines virtuellen Desktopdesktops für Windows nach Name</span><span class="sxs-lookup"><span data-stu-id="58c17-111">Example 1: Get a Windows Virtual Desktop Desktop by name</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name DesktopName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="58c17-112">Dieser Befehl ruft einen virtuellen Windows-Desktop-Desktop in einer Anwendungsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="58c17-112">This command gets a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

### <span data-ttu-id="58c17-113">Beispiel 2: Auflisten der virtuellen Desktopdesktops von Windows</span><span class="sxs-lookup"><span data-stu-id="58c17-113">Example 2: List Windows Virtual Desktop Desktops</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="58c17-114">In diesem Befehl werden die virtuellen Desktopdesktops in einer Anwendungsgruppe aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="58c17-114">This command listsWindows Virtual Desktop Desktops in an applicaton Group.</span></span>

## <span data-ttu-id="58c17-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58c17-115">PARAMETERS</span></span>

### <span data-ttu-id="58c17-116">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="58c17-116">-ApplicationGroupName</span></span>
<span data-ttu-id="58c17-117">Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="58c17-117">The name of the application group</span></span>

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

### <span data-ttu-id="58c17-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58c17-118">-DefaultProfile</span></span>
<span data-ttu-id="58c17-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58c17-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58c17-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58c17-120">-InputObject</span></span>
<span data-ttu-id="58c17-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="58c17-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="58c17-122">-Name</span><span class="sxs-lookup"><span data-stu-id="58c17-122">-Name</span></span>
<span data-ttu-id="58c17-123">Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="58c17-123">The name of the desktop within the specified desktop group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DesktopName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58c17-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58c17-124">-ResourceGroupName</span></span>
<span data-ttu-id="58c17-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="58c17-125">The name of the resource group.</span></span>
<span data-ttu-id="58c17-126">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="58c17-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="58c17-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="58c17-127">-SubscriptionId</span></span>
<span data-ttu-id="58c17-128">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="58c17-128">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58c17-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58c17-129">CommonParameters</span></span>
<span data-ttu-id="58c17-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58c17-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58c17-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58c17-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58c17-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="58c17-132">INPUTS</span></span>

### <span data-ttu-id="58c17-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="58c17-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="58c17-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="58c17-134">OUTPUTS</span></span>

### <span data-ttu-id="58c17-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span><span class="sxs-lookup"><span data-stu-id="58c17-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span></span>

### <span data-ttu-id="58c17-136">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktopList</span><span class="sxs-lookup"><span data-stu-id="58c17-136">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktopList</span></span>

## <span data-ttu-id="58c17-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="58c17-137">NOTES</span></span>

<span data-ttu-id="58c17-138">ALIASE</span><span class="sxs-lookup"><span data-stu-id="58c17-138">ALIASES</span></span>

<span data-ttu-id="58c17-139">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="58c17-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="58c17-140">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="58c17-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="58c17-141">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="58c17-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="58c17-142">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="58c17-142">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="58c17-143">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="58c17-143">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="58c17-144">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="58c17-144">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="58c17-145">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="58c17-145">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="58c17-146">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="58c17-146">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="58c17-147">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="58c17-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="58c17-148">`[MsixPackageFullName <String>]`: Der versionspezifische Paketname des vollständigen Pakets des MSIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="58c17-148">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="58c17-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="58c17-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="58c17-150">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="58c17-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="58c17-151">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="58c17-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="58c17-152">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="58c17-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="58c17-153">`[UserSessionId <String>]`: Der Name der Benutzersitzung im angegebenen Sitzungshost</span><span class="sxs-lookup"><span data-stu-id="58c17-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="58c17-154">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="58c17-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="58c17-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="58c17-155">RELATED LINKS</span></span>

