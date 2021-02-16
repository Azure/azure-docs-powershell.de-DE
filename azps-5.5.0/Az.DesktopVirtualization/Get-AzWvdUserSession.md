---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
ms.openlocfilehash: 8dde4305003b97bd186a4601106a93e6f471edf4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148001"
---
# <span data-ttu-id="10c0a-101">Get-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="10c0a-101">Get-AzWvdUserSession</span></span>

## <span data-ttu-id="10c0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10c0a-102">SYNOPSIS</span></span>
<span data-ttu-id="10c0a-103">"Get a userSession" aus.</span><span class="sxs-lookup"><span data-stu-id="10c0a-103">Get a userSession.</span></span>

## <span data-ttu-id="10c0a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="10c0a-104">SYNTAX</span></span>

### <span data-ttu-id="10c0a-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="10c0a-105">List (Default)</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="10c0a-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="10c0a-106">Get</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="10c0a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="10c0a-107">GetViaIdentity</span></span>
```
Get-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="10c0a-108">Liste1</span><span class="sxs-lookup"><span data-stu-id="10c0a-108">List1</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="10c0a-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10c0a-109">DESCRIPTION</span></span>
<span data-ttu-id="10c0a-110">"Get a userSession" aus.</span><span class="sxs-lookup"><span data-stu-id="10c0a-110">Get a userSession.</span></span>

## <span data-ttu-id="10c0a-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="10c0a-111">EXAMPLES</span></span>

### <span data-ttu-id="10c0a-112">Beispiel 1: Erhalten einer Windows Virtual Desktop UserSession nach Name</span><span class="sxs-lookup"><span data-stu-id="10c0a-112">Example 1: Get a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="10c0a-113">Dieser Befehl ruft eine Windows Virtual Desktop UserSession in einem Sitzungshost ab.</span><span class="sxs-lookup"><span data-stu-id="10c0a-113">This command gets a Windows Virtual Desktop UserSession in a Session Host.</span></span>

### <span data-ttu-id="10c0a-114">Beispiel 2: Auflisten von Windows Virtual Desktop UserSessions</span><span class="sxs-lookup"><span data-stu-id="10c0a-114">Example 2: List Windows Virtual Desktop UserSessions</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="10c0a-115">Dieser Befehl listet Windows Virtual Desktop UserSessions in einem Sitzungshost auf.</span><span class="sxs-lookup"><span data-stu-id="10c0a-115">This command lists a Windows Virtual Desktop UserSessions in a Session Host.</span></span>

### <span data-ttu-id="10c0a-116">Beispiel 3: Auflisten von Windows Virtual Desktop UserSessions im Hostpool</span><span class="sxs-lookup"><span data-stu-id="10c0a-116">Example 3: List Windows Virtual Desktop UserSessions in host pool</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="10c0a-117">Dieser Befehl listet windows Virtual Desktop UserSessions in einem Sitzungshost in einem Hostpool auf.</span><span class="sxs-lookup"><span data-stu-id="10c0a-117">This command lists a Windows Virtual Desktop UserSessions in a Session Host in a host pool.</span></span>

## <span data-ttu-id="10c0a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10c0a-118">PARAMETERS</span></span>

### <span data-ttu-id="10c0a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10c0a-119">-DefaultProfile</span></span>
<span data-ttu-id="10c0a-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="10c0a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10c0a-121">-Filter</span><span class="sxs-lookup"><span data-stu-id="10c0a-121">-Filter</span></span>
<span data-ttu-id="10c0a-122">OData-Filterausdruck.</span><span class="sxs-lookup"><span data-stu-id="10c0a-122">OData filter expression.</span></span>
<span data-ttu-id="10c0a-123">Gültige Eigenschaften für die Filterung sind "userprincipalname" und "sessionstate".</span><span class="sxs-lookup"><span data-stu-id="10c0a-123">Valid properties for filtering are userprincipalname and sessionstate.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10c0a-124">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="10c0a-124">-HostPoolName</span></span>
<span data-ttu-id="10c0a-125">Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="10c0a-125">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10c0a-126">-ID</span><span class="sxs-lookup"><span data-stu-id="10c0a-126">-Id</span></span>
<span data-ttu-id="10c0a-127">Der Name der Benutzersitzung im angegebenen Sitzungshost</span><span class="sxs-lookup"><span data-stu-id="10c0a-127">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10c0a-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10c0a-128">-InputObject</span></span>
<span data-ttu-id="10c0a-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="10c0a-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="10c0a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10c0a-130">-ResourceGroupName</span></span>
<span data-ttu-id="10c0a-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="10c0a-131">The name of the resource group.</span></span>
<span data-ttu-id="10c0a-132">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="10c0a-132">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10c0a-133">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="10c0a-133">-SessionHostName</span></span>
<span data-ttu-id="10c0a-134">Der Name des Sitzungshosts innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="10c0a-134">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10c0a-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="10c0a-135">-SubscriptionId</span></span>
<span data-ttu-id="10c0a-136">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="10c0a-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="10c0a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10c0a-137">CommonParameters</span></span>
<span data-ttu-id="10c0a-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10c0a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10c0a-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10c0a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10c0a-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="10c0a-140">INPUTS</span></span>

### <span data-ttu-id="10c0a-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="10c0a-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="10c0a-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="10c0a-142">OUTPUTS</span></span>

### <span data-ttu-id="10c0a-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IUserSession</span><span class="sxs-lookup"><span data-stu-id="10c0a-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IUserSession</span></span>

## <span data-ttu-id="10c0a-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="10c0a-144">NOTES</span></span>

<span data-ttu-id="10c0a-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="10c0a-145">ALIASES</span></span>

<span data-ttu-id="10c0a-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="10c0a-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="10c0a-147">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="10c0a-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="10c0a-148">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="10c0a-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="10c0a-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="10c0a-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="10c0a-150">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="10c0a-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="10c0a-151">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="10c0a-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="10c0a-152">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="10c0a-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="10c0a-153">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="10c0a-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="10c0a-154">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="10c0a-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="10c0a-155">`[MsixPackageFullName <String>]`: Der versionspezifische Paketname des vollständigen Pakets des MSIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="10c0a-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="10c0a-156">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="10c0a-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="10c0a-157">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="10c0a-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="10c0a-158">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="10c0a-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="10c0a-159">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="10c0a-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="10c0a-160">`[UserSessionId <String>]`: Der Name der Benutzersitzung im angegebenen Sitzungshost</span><span class="sxs-lookup"><span data-stu-id="10c0a-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="10c0a-161">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="10c0a-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="10c0a-162">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="10c0a-162">RELATED LINKS</span></span>

