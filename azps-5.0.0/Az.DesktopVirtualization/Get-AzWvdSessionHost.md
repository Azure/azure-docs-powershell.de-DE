---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
ms.openlocfilehash: 94f4c5ad9c401c429c9ef2f2f1c146f83a407196
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297058"
---
# <span data-ttu-id="f1e8e-101">Get-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="f1e8e-101">Get-AzWvdSessionHost</span></span>

## <span data-ttu-id="f1e8e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f1e8e-102">SYNOPSIS</span></span>
<span data-ttu-id="f1e8e-103">Rufen Sie einen Sitzungshost ab.</span><span class="sxs-lookup"><span data-stu-id="f1e8e-103">Get a session host.</span></span>

## <span data-ttu-id="f1e8e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1e8e-104">SYNTAX</span></span>

### <span data-ttu-id="f1e8e-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="f1e8e-105">List (Default)</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f1e8e-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="f1e8e-106">Get</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f1e8e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f1e8e-107">GetViaIdentity</span></span>
```
Get-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f1e8e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1e8e-108">DESCRIPTION</span></span>
<span data-ttu-id="f1e8e-109">Rufen Sie einen Sitzungshost ab.</span><span class="sxs-lookup"><span data-stu-id="f1e8e-109">Get a session host.</span></span>

## <span data-ttu-id="f1e8e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1e8e-110">EXAMPLES</span></span>

### <span data-ttu-id="f1e8e-111">Beispiel 1: Abrufen eines virtuellen Windows-Desktop-SessionHost nach Name</span><span class="sxs-lookup"><span data-stu-id="f1e8e-111">Example 1: Get a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="f1e8e-112">Dieser Befehl ruft einen virtuellen Windows-Desktop-SessionHost in einem Host Pool ab.</span><span class="sxs-lookup"><span data-stu-id="f1e8e-112">This command gets a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

### <span data-ttu-id="f1e8e-113">Beispiel 2: Auflisten von Windows Virtual Desktop-SessionHosts</span><span class="sxs-lookup"><span data-stu-id="f1e8e-113">Example 2: List Windows Virtual Desktop SessionHosts</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName1 Microsoft.DesktopVirtualization/hostpools/sessionhosts
HostPoolName/SessionHostName2 Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="f1e8e-114">Dieser Befehl listet einen virtuellen Windows-Desktop SessionHosts in einem Host Pool auf.</span><span class="sxs-lookup"><span data-stu-id="f1e8e-114">This command lists a Windows Virtual Desktop SessionHosts in a Host Pool.</span></span>

## <span data-ttu-id="f1e8e-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1e8e-115">PARAMETERS</span></span>

### <span data-ttu-id="f1e8e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1e8e-116">-DefaultProfile</span></span>
<span data-ttu-id="f1e8e-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f1e8e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1e8e-118">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="f1e8e-118">-HostPoolName</span></span>
<span data-ttu-id="f1e8e-119">Der Name des Host Pools in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f1e8e-119">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="f1e8e-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f1e8e-120">-InputObject</span></span>
<span data-ttu-id="f1e8e-121">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="f1e8e-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f1e8e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f1e8e-122">-Name</span></span>
<span data-ttu-id="f1e8e-123">Der Name des Sitzungs Hosts innerhalb des angegebenen Host Pools</span><span class="sxs-lookup"><span data-stu-id="f1e8e-123">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1e8e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1e8e-124">-ResourceGroupName</span></span>
<span data-ttu-id="f1e8e-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f1e8e-125">The name of the resource group.</span></span>
<span data-ttu-id="f1e8e-126">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="f1e8e-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f1e8e-127">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="f1e8e-127">-SubscriptionId</span></span>
<span data-ttu-id="f1e8e-128">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="f1e8e-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f1e8e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1e8e-129">CommonParameters</span></span>
<span data-ttu-id="f1e8e-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1e8e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1e8e-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1e8e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1e8e-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f1e8e-132">INPUTS</span></span>

### <span data-ttu-id="f1e8e-133">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="f1e8e-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="f1e8e-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f1e8e-134">OUTPUTS</span></span>

### <span data-ttu-id="f1e8e-135">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. ISessionHost</span><span class="sxs-lookup"><span data-stu-id="f1e8e-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.ISessionHost</span></span>

## <span data-ttu-id="f1e8e-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="f1e8e-136">NOTES</span></span>

<span data-ttu-id="f1e8e-137">Aliase</span><span class="sxs-lookup"><span data-stu-id="f1e8e-137">ALIASES</span></span>

<span data-ttu-id="f1e8e-138">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f1e8e-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f1e8e-139">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f1e8e-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f1e8e-140">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="f1e8e-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f1e8e-141">Inputobject <IDesktopVirtualizationIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="f1e8e-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f1e8e-142">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="f1e8e-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="f1e8e-143">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="f1e8e-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="f1e8e-144">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktop Gruppe</span><span class="sxs-lookup"><span data-stu-id="f1e8e-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="f1e8e-145">`[HostPoolName <String>]`: Der Name des Host Pools in der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f1e8e-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="f1e8e-146">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="f1e8e-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f1e8e-147">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f1e8e-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f1e8e-148">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="f1e8e-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="f1e8e-149">`[SessionHostName <String>]`: Der Name des Sitzungs Hosts innerhalb des angegebenen Host Pools</span><span class="sxs-lookup"><span data-stu-id="f1e8e-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="f1e8e-150">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="f1e8e-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f1e8e-151">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungs Hosts</span><span class="sxs-lookup"><span data-stu-id="f1e8e-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="f1e8e-152">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="f1e8e-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="f1e8e-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f1e8e-153">RELATED LINKS</span></span>

