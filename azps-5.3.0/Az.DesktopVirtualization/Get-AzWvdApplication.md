---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
ms.openlocfilehash: 67a49250607e1c7d70f1799aa26bd866924b5edc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467916"
---
# <span data-ttu-id="894e3-101">Get-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="894e3-101">Get-AzWvdApplication</span></span>

## <span data-ttu-id="894e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="894e3-102">SYNOPSIS</span></span>
<span data-ttu-id="894e3-103">Holen Sie sich eine Anwendung.</span><span class="sxs-lookup"><span data-stu-id="894e3-103">Get an application.</span></span>

## <span data-ttu-id="894e3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="894e3-104">SYNTAX</span></span>

### <span data-ttu-id="894e3-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="894e3-105">List (Default)</span></span>
```
Get-AzWvdApplication -GroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="894e3-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="894e3-106">Get</span></span>
```
Get-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="894e3-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="894e3-107">GetViaIdentity</span></span>
```
Get-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="894e3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="894e3-108">DESCRIPTION</span></span>
<span data-ttu-id="894e3-109">Holen Sie sich eine Anwendung.</span><span class="sxs-lookup"><span data-stu-id="894e3-109">Get an application.</span></span>

## <span data-ttu-id="894e3-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="894e3-110">EXAMPLES</span></span>

### <span data-ttu-id="894e3-111">Beispiel 1: Erhalten einer virtuellen Windows-Desktopanwendung nach Name</span><span class="sxs-lookup"><span data-stu-id="894e3-111">Example 1: Get a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="894e3-112">Dieser Befehl ruft eine virtuelle Windows-Desktopanwendung in einer Anwendungsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="894e3-112">This command gets a Windows Virtual Desktop Application in an applicaton Group.</span></span>

### <span data-ttu-id="894e3-113">Beispiel 2: Auflisten virtueller Desktopanwendungen von Windows</span><span class="sxs-lookup"><span data-stu-id="894e3-113">Example 2: List Windows Virtual Desktop Applications</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName1 Microsoft.DesktopVirtualization/applicationgroups/applications
ApplicationGroupName/ApplicationName2 Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="894e3-114">Mit diesem Befehl werden die virtuellen Desktopanwendungen von Windows in einer Anwendungsgruppe aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="894e3-114">This command Lists Windows Virtual Desktop Applications in an applicaton Group.</span></span>

## <span data-ttu-id="894e3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="894e3-115">PARAMETERS</span></span>

### <span data-ttu-id="894e3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="894e3-116">-DefaultProfile</span></span>
<span data-ttu-id="894e3-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="894e3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="894e3-118">-GroupName</span><span class="sxs-lookup"><span data-stu-id="894e3-118">-GroupName</span></span>
<span data-ttu-id="894e3-119">Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="894e3-119">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="894e3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="894e3-120">-InputObject</span></span>
<span data-ttu-id="894e3-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="894e3-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="894e3-122">-Name</span><span class="sxs-lookup"><span data-stu-id="894e3-122">-Name</span></span>
<span data-ttu-id="894e3-123">Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="894e3-123">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="894e3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="894e3-124">-ResourceGroupName</span></span>
<span data-ttu-id="894e3-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="894e3-125">The name of the resource group.</span></span>
<span data-ttu-id="894e3-126">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="894e3-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="894e3-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="894e3-127">-SubscriptionId</span></span>
<span data-ttu-id="894e3-128">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="894e3-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="894e3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="894e3-129">CommonParameters</span></span>
<span data-ttu-id="894e3-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="894e3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="894e3-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="894e3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="894e3-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="894e3-132">INPUTS</span></span>

### <span data-ttu-id="894e3-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="894e3-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="894e3-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="894e3-134">OUTPUTS</span></span>

### <span data-ttu-id="894e3-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span><span class="sxs-lookup"><span data-stu-id="894e3-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="894e3-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="894e3-136">NOTES</span></span>

<span data-ttu-id="894e3-137">ALIASE</span><span class="sxs-lookup"><span data-stu-id="894e3-137">ALIASES</span></span>

<span data-ttu-id="894e3-138">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="894e3-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="894e3-139">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="894e3-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="894e3-140">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="894e3-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="894e3-141">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="894e3-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="894e3-142">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="894e3-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="894e3-143">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="894e3-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="894e3-144">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="894e3-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="894e3-145">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="894e3-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="894e3-146">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="894e3-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="894e3-147">`[MsixPackageFullName <String>]`: Der versionspezifische Paketname des vollständigen Pakets des MSIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="894e3-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="894e3-148">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="894e3-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="894e3-149">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="894e3-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="894e3-150">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="894e3-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="894e3-151">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="894e3-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="894e3-152">`[UserSessionId <String>]`: Der Name der Benutzersitzung im angegebenen Sitzungshost</span><span class="sxs-lookup"><span data-stu-id="894e3-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="894e3-153">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="894e3-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="894e3-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="894e3-154">RELATED LINKS</span></span>

