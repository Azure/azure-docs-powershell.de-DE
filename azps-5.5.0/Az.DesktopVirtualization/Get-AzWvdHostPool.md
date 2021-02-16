---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
ms.openlocfilehash: 480c1d5517aa79ff7b3a0fa5dfa24f2ae6f4ae45
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167748"
---
# <span data-ttu-id="e546d-101">Get-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="e546d-101">Get-AzWvdHostPool</span></span>

## <span data-ttu-id="e546d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e546d-102">SYNOPSIS</span></span>
<span data-ttu-id="e546d-103">Holen Sie sich einen Hostpool.</span><span class="sxs-lookup"><span data-stu-id="e546d-103">Get a host pool.</span></span>

## <span data-ttu-id="e546d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e546d-104">SYNTAX</span></span>

### <span data-ttu-id="e546d-105">Liste1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="e546d-105">List1 (Default)</span></span>
```
Get-AzWvdHostPool [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e546d-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="e546d-106">Get</span></span>
```
Get-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e546d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e546d-107">GetViaIdentity</span></span>
```
Get-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e546d-108">Liste</span><span class="sxs-lookup"><span data-stu-id="e546d-108">List</span></span>
```
Get-AzWvdHostPool -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e546d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e546d-109">DESCRIPTION</span></span>
<span data-ttu-id="e546d-110">Holen Sie sich einen Hostpool.</span><span class="sxs-lookup"><span data-stu-id="e546d-110">Get a host pool.</span></span>

## <span data-ttu-id="e546d-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e546d-111">EXAMPLES</span></span>

### <span data-ttu-id="e546d-112">Beispiel 1: Erhalten eines Virtuellen Desktophostpools für Windows nach Name</span><span class="sxs-lookup"><span data-stu-id="e546d-112">Example 1: Get a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName -Name HostPoolName

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="e546d-113">Dieser Befehl ruft einen Windows Virtual Desktop HostPool in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="e546d-113">This command gets a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="e546d-114">Beispiel 2: Auflisten von HostPools für virtuelle Windows-Desktops</span><span class="sxs-lookup"><span data-stu-id="e546d-114">Example 2: List Windows Virtual Desktop HostPools</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName

Location   Name          Type
--------   ----          ----
eastus     HostPoolName1 Microsoft.DesktopVirtualization/hostpools
eastus     HostPoolName2 Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="e546d-115">Dieser Befehl listet eine Windows Virtual Desktop HostPools in einer Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="e546d-115">This command lists a Windows Virtual Desktop HostPools in a Resource Group.</span></span>

## <span data-ttu-id="e546d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e546d-116">PARAMETERS</span></span>

### <span data-ttu-id="e546d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e546d-117">-DefaultProfile</span></span>
<span data-ttu-id="e546d-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e546d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e546d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e546d-119">-InputObject</span></span>
<span data-ttu-id="e546d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e546d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e546d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e546d-121">-Name</span></span>
<span data-ttu-id="e546d-122">Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="e546d-122">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e546d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e546d-123">-ResourceGroupName</span></span>
<span data-ttu-id="e546d-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e546d-124">The name of the resource group.</span></span>
<span data-ttu-id="e546d-125">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="e546d-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e546d-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e546d-126">-SubscriptionId</span></span>
<span data-ttu-id="e546d-127">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="e546d-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e546d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e546d-128">CommonParameters</span></span>
<span data-ttu-id="e546d-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e546d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e546d-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e546d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e546d-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e546d-131">INPUTS</span></span>

### <span data-ttu-id="e546d-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="e546d-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="e546d-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e546d-133">OUTPUTS</span></span>

### <span data-ttu-id="e546d-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span><span class="sxs-lookup"><span data-stu-id="e546d-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="e546d-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e546d-135">NOTES</span></span>

<span data-ttu-id="e546d-136">ALIASE</span><span class="sxs-lookup"><span data-stu-id="e546d-136">ALIASES</span></span>

<span data-ttu-id="e546d-137">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="e546d-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e546d-138">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e546d-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e546d-139">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e546d-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e546d-140">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="e546d-140">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e546d-141">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="e546d-141">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="e546d-142">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="e546d-142">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="e546d-143">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="e546d-143">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="e546d-144">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="e546d-144">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="e546d-145">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="e546d-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e546d-146">`[MsixPackageFullName <String>]`: Der versionspezifische Paketname des vollständigen Pakets des MSIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="e546d-146">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="e546d-147">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e546d-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e546d-148">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="e546d-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="e546d-149">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="e546d-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="e546d-150">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="e546d-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e546d-151">`[UserSessionId <String>]`: Der Name der Benutzersitzung im angegebenen Sitzungshost</span><span class="sxs-lookup"><span data-stu-id="e546d-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="e546d-152">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="e546d-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="e546d-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e546d-153">RELATED LINKS</span></span>

