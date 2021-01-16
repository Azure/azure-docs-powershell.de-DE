---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
ms.openlocfilehash: 559cff58ac8d6c3f3d8f116b6147d6f4c2a4378d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293224"
---
# <span data-ttu-id="43b01-101">Get-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="43b01-101">Get-AzWvdMsixPackage</span></span>

## <span data-ttu-id="43b01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43b01-102">SYNOPSIS</span></span>
<span data-ttu-id="43b01-103">Holen Sie sich ein msixpackage.</span><span class="sxs-lookup"><span data-stu-id="43b01-103">Get a msixpackage.</span></span>

## <span data-ttu-id="43b01-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43b01-104">SYNTAX</span></span>

### <span data-ttu-id="43b01-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="43b01-105">List (Default)</span></span>
```
Get-AzWvdMsixPackage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="43b01-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="43b01-106">Get</span></span>
```
Get-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="43b01-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="43b01-107">GetViaIdentity</span></span>
```
Get-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="43b01-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43b01-108">DESCRIPTION</span></span>
<span data-ttu-id="43b01-109">Holen Sie sich ein msixpackage.</span><span class="sxs-lookup"><span data-stu-id="43b01-109">Get a msixpackage.</span></span>

## <span data-ttu-id="43b01-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="43b01-110">EXAMPLES</span></span>

### <span data-ttu-id="43b01-111">Beispiel 1: Erhalten eines "MSIX Package by Name"</span><span class="sxs-lookup"><span data-stu-id="43b01-111">Example 1: Get a MSIX Package by Name</span></span>
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName                     Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="43b01-112">Dieser Befehl ruft ein "MSIX Package" in einem HostPool ab.</span><span class="sxs-lookup"><span data-stu-id="43b01-112">This command gets a MSIX Package in a HostPool.</span></span>

### <span data-ttu-id="43b01-113">Beispiel 2: Auflisten von MSIX-Paketen</span><span class="sxs-lookup"><span data-stu-id="43b01-113">Example 2: List MSIX Packages</span></span> 
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName1                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName2                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName3                    Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="43b01-114">Mit diesem Befehl werden die MSIX-Pakete in einem HostPool aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="43b01-114">This command Lists MSIX Packages in a HostPool.</span></span>

## <span data-ttu-id="43b01-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43b01-115">PARAMETERS</span></span>

### <span data-ttu-id="43b01-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43b01-116">-DefaultProfile</span></span>
<span data-ttu-id="43b01-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="43b01-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43b01-118">-FullName</span><span class="sxs-lookup"><span data-stu-id="43b01-118">-FullName</span></span>
<span data-ttu-id="43b01-119">Der versionspezifische Paketname des vollständigen Pakets des MSIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="43b01-119">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43b01-120">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="43b01-120">-HostPoolName</span></span>
<span data-ttu-id="43b01-121">Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="43b01-121">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="43b01-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43b01-122">-InputObject</span></span>
<span data-ttu-id="43b01-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="43b01-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="43b01-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43b01-124">-ResourceGroupName</span></span>
<span data-ttu-id="43b01-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="43b01-125">The name of the resource group.</span></span>
<span data-ttu-id="43b01-126">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="43b01-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="43b01-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="43b01-127">-SubscriptionId</span></span>
<span data-ttu-id="43b01-128">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="43b01-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="43b01-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43b01-129">CommonParameters</span></span>
<span data-ttu-id="43b01-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43b01-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43b01-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43b01-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43b01-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="43b01-132">INPUTS</span></span>

### <span data-ttu-id="43b01-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="43b01-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="43b01-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="43b01-134">OUTPUTS</span></span>

### <span data-ttu-id="43b01-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="43b01-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackage</span></span>

## <span data-ttu-id="43b01-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="43b01-136">NOTES</span></span>

<span data-ttu-id="43b01-137">ALIASE</span><span class="sxs-lookup"><span data-stu-id="43b01-137">ALIASES</span></span>

<span data-ttu-id="43b01-138">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="43b01-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="43b01-139">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="43b01-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="43b01-140">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="43b01-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="43b01-141">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="43b01-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="43b01-142">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="43b01-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="43b01-143">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="43b01-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="43b01-144">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="43b01-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="43b01-145">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="43b01-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="43b01-146">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="43b01-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="43b01-147">`[MsixPackageFullName <String>]`: Der versionsspezifische Paketname des vollständigen Pakets des MsIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="43b01-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="43b01-148">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="43b01-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="43b01-149">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="43b01-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="43b01-150">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="43b01-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="43b01-151">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="43b01-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="43b01-152">`[UserSessionId <String>]`: Der Name der Benutzersitzung im angegebenen Sitzungshost</span><span class="sxs-lookup"><span data-stu-id="43b01-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="43b01-153">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="43b01-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="43b01-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="43b01-154">RELATED LINKS</span></span>

