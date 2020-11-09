---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
ms.openlocfilehash: eedf639ebf5c25ff9153072a337ea659b41a9e92
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297063"
---
# <span data-ttu-id="2be18-101">Get-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="2be18-101">Get-AzWvdUserSession</span></span>

## <span data-ttu-id="2be18-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2be18-102">SYNOPSIS</span></span>
<span data-ttu-id="2be18-103">Besorgen Sie sich eine userSession.</span><span class="sxs-lookup"><span data-stu-id="2be18-103">Get a userSession.</span></span>

## <span data-ttu-id="2be18-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2be18-104">SYNTAX</span></span>

### <span data-ttu-id="2be18-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="2be18-105">List (Default)</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2be18-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="2be18-106">Get</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2be18-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2be18-107">GetViaIdentity</span></span>
```
Get-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="2be18-108">List1</span><span class="sxs-lookup"><span data-stu-id="2be18-108">List1</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2be18-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2be18-109">DESCRIPTION</span></span>
<span data-ttu-id="2be18-110">Besorgen Sie sich eine userSession.</span><span class="sxs-lookup"><span data-stu-id="2be18-110">Get a userSession.</span></span>

## <span data-ttu-id="2be18-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2be18-111">EXAMPLES</span></span>

### <span data-ttu-id="2be18-112">Beispiel 1: Abrufen eines virtuellen Windows-Desktop-UserSession nach Name</span><span class="sxs-lookup"><span data-stu-id="2be18-112">Example 1: Get a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="2be18-113">Dieser Befehl ruft einen virtuellen Windows-Desktop-UserSession in einem Sitzungs Host ab.</span><span class="sxs-lookup"><span data-stu-id="2be18-113">This command gets a Windows Virtual Desktop UserSession in a Session Host.</span></span>

### <span data-ttu-id="2be18-114">Beispiel 2: Auflisten von Windows Virtual Desktop-UserSessions</span><span class="sxs-lookup"><span data-stu-id="2be18-114">Example 2: List Windows Virtual Desktop UserSessions</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="2be18-115">Dieser Befehl listet eine Windows Virtual Desktop-UserSessions in einem Sitzungs Host auf.</span><span class="sxs-lookup"><span data-stu-id="2be18-115">This command lists a Windows Virtual Desktop UserSessions in a Session Host.</span></span>

### <span data-ttu-id="2be18-116">Beispiel 3: Auflisten von Windows Virtual Desktop-UserSessions im Host Pool</span><span class="sxs-lookup"><span data-stu-id="2be18-116">Example 3: List Windows Virtual Desktop UserSessions in host pool</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="2be18-117">Dieser Befehl listet einen virtuellen Windows-Desktop-UserSessions in einem Sitzungshost in einem Host Pool auf.</span><span class="sxs-lookup"><span data-stu-id="2be18-117">This command lists a Windows Virtual Desktop UserSessions in a Session Host in a host pool.</span></span>

## <span data-ttu-id="2be18-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="2be18-118">PARAMETERS</span></span>

### <span data-ttu-id="2be18-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2be18-119">-DefaultProfile</span></span>
<span data-ttu-id="2be18-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2be18-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2be18-121">-Filter</span><span class="sxs-lookup"><span data-stu-id="2be18-121">-Filter</span></span>
<span data-ttu-id="2be18-122">OData-Filterausdruck.</span><span class="sxs-lookup"><span data-stu-id="2be18-122">OData filter expression.</span></span>
<span data-ttu-id="2be18-123">Gültige Eigenschaften für das Filtern sind userPrincipalName und SessionState.</span><span class="sxs-lookup"><span data-stu-id="2be18-123">Valid properties for filtering are userprincipalname and sessionstate.</span></span>

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

### <span data-ttu-id="2be18-124">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="2be18-124">-HostPoolName</span></span>
<span data-ttu-id="2be18-125">Der Name des Host Pools in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2be18-125">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="2be18-126">-ID</span><span class="sxs-lookup"><span data-stu-id="2be18-126">-Id</span></span>
<span data-ttu-id="2be18-127">Der Name der Benutzersitzung innerhalb des angegebenen Sitzungs Hosts</span><span class="sxs-lookup"><span data-stu-id="2be18-127">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="2be18-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2be18-128">-InputObject</span></span>
<span data-ttu-id="2be18-129">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="2be18-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2be18-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2be18-130">-ResourceGroupName</span></span>
<span data-ttu-id="2be18-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2be18-131">The name of the resource group.</span></span>
<span data-ttu-id="2be18-132">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="2be18-132">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2be18-133">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="2be18-133">-SessionHostName</span></span>
<span data-ttu-id="2be18-134">Der Name des Sitzungs Hosts innerhalb des angegebenen Host Pools</span><span class="sxs-lookup"><span data-stu-id="2be18-134">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="2be18-135">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="2be18-135">-SubscriptionId</span></span>
<span data-ttu-id="2be18-136">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="2be18-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2be18-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2be18-137">CommonParameters</span></span>
<span data-ttu-id="2be18-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2be18-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2be18-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2be18-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2be18-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2be18-140">INPUTS</span></span>

### <span data-ttu-id="2be18-141">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="2be18-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="2be18-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2be18-142">OUTPUTS</span></span>

### <span data-ttu-id="2be18-143">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IUserSession</span><span class="sxs-lookup"><span data-stu-id="2be18-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IUserSession</span></span>

## <span data-ttu-id="2be18-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="2be18-144">NOTES</span></span>

<span data-ttu-id="2be18-145">Aliase</span><span class="sxs-lookup"><span data-stu-id="2be18-145">ALIASES</span></span>

<span data-ttu-id="2be18-146">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2be18-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2be18-147">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2be18-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2be18-148">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="2be18-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2be18-149">Inputobject <IDesktopVirtualizationIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="2be18-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2be18-150">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="2be18-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="2be18-151">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="2be18-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="2be18-152">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktop Gruppe</span><span class="sxs-lookup"><span data-stu-id="2be18-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="2be18-153">`[HostPoolName <String>]`: Der Name des Host Pools in der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="2be18-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="2be18-154">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="2be18-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2be18-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2be18-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2be18-156">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="2be18-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="2be18-157">`[SessionHostName <String>]`: Der Name des Sitzungs Hosts innerhalb des angegebenen Host Pools</span><span class="sxs-lookup"><span data-stu-id="2be18-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="2be18-158">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="2be18-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="2be18-159">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungs Hosts</span><span class="sxs-lookup"><span data-stu-id="2be18-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="2be18-160">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="2be18-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="2be18-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2be18-161">RELATED LINKS</span></span>

