---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
ms.openlocfilehash: 0bc1c5eef68abc46d43132a86afe3ab6f86b002d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298915"
---
# <span data-ttu-id="0b1dc-101">Get-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="0b1dc-101">Get-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="0b1dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b1dc-102">SYNOPSIS</span></span>
<span data-ttu-id="0b1dc-103">Eine Anwendungsgruppe erhalten.</span><span class="sxs-lookup"><span data-stu-id="0b1dc-103">Get an application group.</span></span>

## <span data-ttu-id="0b1dc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b1dc-104">SYNTAX</span></span>

### <span data-ttu-id="0b1dc-105">Liste1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="0b1dc-105">List1 (Default)</span></span>
```
Get-AzWvdApplicationGroup [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b1dc-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="0b1dc-106">Get</span></span>
```
Get-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0b1dc-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0b1dc-107">GetViaIdentity</span></span>
```
Get-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b1dc-108">Liste</span><span class="sxs-lookup"><span data-stu-id="0b1dc-108">List</span></span>
```
Get-AzWvdApplicationGroup -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0b1dc-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b1dc-109">DESCRIPTION</span></span>
<span data-ttu-id="0b1dc-110">Eine Anwendungsgruppe erhalten.</span><span class="sxs-lookup"><span data-stu-id="0b1dc-110">Get an application group.</span></span>

## <span data-ttu-id="0b1dc-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0b1dc-111">EXAMPLES</span></span>

### <span data-ttu-id="0b1dc-112">Beispiel 1: Erhalten einer Windows Virtual Desktop ApplicationGroup nach Name</span><span class="sxs-lookup"><span data-stu-id="0b1dc-112">Example 1: Get a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="0b1dc-113">Dieser Befehl ruft eine Windows Virtual Desktop ApplicationGroup in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="0b1dc-113">This command gets a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="0b1dc-114">Beispiel 2: Auflisten der Virtuellen Desktopanwendungsgruppe von Windows</span><span class="sxs-lookup"><span data-stu-id="0b1dc-114">Example 2: List Windows Virtual Desktop ApplicationGroups</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName

Location   Name                  Type
--------   ----                  ----
eastus     ApplicationGroupName1 Microsoft.DesktopVirtualization/applicationgroups
eastus     ApplicationGroupName2 Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="0b1dc-115">Dieser Befehl listet eine Windows Virtual Desktop ApplicationGroups in einer Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="0b1dc-115">This command lists a Windows Virtual Desktop ApplicationGroups in a Resource Group.</span></span>

## <span data-ttu-id="0b1dc-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b1dc-116">PARAMETERS</span></span>

### <span data-ttu-id="0b1dc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b1dc-117">-DefaultProfile</span></span>
<span data-ttu-id="0b1dc-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0b1dc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b1dc-119">-Filter</span><span class="sxs-lookup"><span data-stu-id="0b1dc-119">-Filter</span></span>
<span data-ttu-id="0b1dc-120">OData-Filterausdruck.</span><span class="sxs-lookup"><span data-stu-id="0b1dc-120">OData filter expression.</span></span>
<span data-ttu-id="0b1dc-121">Gültige Eigenschaften zum Filtern sind applicationGroupType.</span><span class="sxs-lookup"><span data-stu-id="0b1dc-121">Valid properties for filtering are applicationGroupType.</span></span>

```yaml
Type: System.String
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b1dc-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b1dc-122">-InputObject</span></span>
<span data-ttu-id="0b1dc-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="0b1dc-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0b1dc-124">-Name</span><span class="sxs-lookup"><span data-stu-id="0b1dc-124">-Name</span></span>
<span data-ttu-id="0b1dc-125">Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="0b1dc-125">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b1dc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b1dc-126">-ResourceGroupName</span></span>
<span data-ttu-id="0b1dc-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0b1dc-127">The name of the resource group.</span></span>
<span data-ttu-id="0b1dc-128">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="0b1dc-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0b1dc-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0b1dc-129">-SubscriptionId</span></span>
<span data-ttu-id="0b1dc-130">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="0b1dc-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0b1dc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b1dc-131">CommonParameters</span></span>
<span data-ttu-id="0b1dc-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b1dc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b1dc-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b1dc-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b1dc-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0b1dc-134">INPUTS</span></span>

### <span data-ttu-id="0b1dc-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="0b1dc-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="0b1dc-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0b1dc-136">OUTPUTS</span></span>

### <span data-ttu-id="0b1dc-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="0b1dc-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IApplicationGroup</span></span>

## <span data-ttu-id="0b1dc-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0b1dc-138">NOTES</span></span>

<span data-ttu-id="0b1dc-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="0b1dc-139">ALIASES</span></span>

<span data-ttu-id="0b1dc-140">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="0b1dc-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0b1dc-141">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0b1dc-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0b1dc-142">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0b1dc-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0b1dc-143">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="0b1dc-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0b1dc-144">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="0b1dc-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="0b1dc-145">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="0b1dc-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="0b1dc-146">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="0b1dc-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="0b1dc-147">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="0b1dc-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="0b1dc-148">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="0b1dc-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0b1dc-149">`[MsixPackageFullName <String>]`: Der versionspezifische Paketname des vollständigen Pakets des MSIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="0b1dc-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="0b1dc-150">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0b1dc-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0b1dc-151">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="0b1dc-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="0b1dc-152">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="0b1dc-152">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="0b1dc-153">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="0b1dc-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0b1dc-154">`[UserSessionId <String>]`: Der Name der Benutzersitzung im angegebenen Sitzungshost</span><span class="sxs-lookup"><span data-stu-id="0b1dc-154">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="0b1dc-155">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="0b1dc-155">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="0b1dc-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0b1dc-156">RELATED LINKS</span></span>

