---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
ms.openlocfilehash: 72075a00cab24d9e7ac82814b2f1e644d90d74c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297087"
---
# <span data-ttu-id="e49a3-101">Get-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="e49a3-101">Get-AzWvdDesktop</span></span>

## <span data-ttu-id="e49a3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e49a3-102">SYNOPSIS</span></span>
<span data-ttu-id="e49a3-103">Besorgen Sie sich einen Desktop.</span><span class="sxs-lookup"><span data-stu-id="e49a3-103">Get a desktop.</span></span>

## <span data-ttu-id="e49a3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e49a3-104">SYNTAX</span></span>

### <span data-ttu-id="e49a3-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="e49a3-105">List (Default)</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e49a3-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="e49a3-106">Get</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e49a3-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e49a3-107">GetViaIdentity</span></span>
```
Get-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e49a3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e49a3-108">DESCRIPTION</span></span>
<span data-ttu-id="e49a3-109">Besorgen Sie sich einen Desktop.</span><span class="sxs-lookup"><span data-stu-id="e49a3-109">Get a desktop.</span></span>

## <span data-ttu-id="e49a3-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e49a3-110">EXAMPLES</span></span>

### <span data-ttu-id="e49a3-111">Beispiel 1: Abrufen eines virtuellen Windows-Desktop Desktops anhand des Namens</span><span class="sxs-lookup"><span data-stu-id="e49a3-111">Example 1: Get a Windows Virtual Desktop Desktop by name</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name DesktopName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="e49a3-112">Dieser Befehl ruft einen virtuellen Windows-Desktop Desktop in einer Applicaton-Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="e49a3-112">This command gets a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

### <span data-ttu-id="e49a3-113">Beispiel 2: Auflisten von Windows-virtuellen Desktop Desktops</span><span class="sxs-lookup"><span data-stu-id="e49a3-113">Example 2: List Windows Virtual Desktop Desktops</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="e49a3-114">Dieser Befehl listsWindows virtuelle Desktop Desktops in einer Applicaton-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="e49a3-114">This command listsWindows Virtual Desktop Desktops in an applicaton Group.</span></span>

## <span data-ttu-id="e49a3-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="e49a3-115">PARAMETERS</span></span>

### <span data-ttu-id="e49a3-116">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="e49a3-116">-ApplicationGroupName</span></span>
<span data-ttu-id="e49a3-117">Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="e49a3-117">The name of the application group</span></span>

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

### <span data-ttu-id="e49a3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e49a3-118">-DefaultProfile</span></span>
<span data-ttu-id="e49a3-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e49a3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e49a3-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e49a3-120">-InputObject</span></span>
<span data-ttu-id="e49a3-121">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="e49a3-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e49a3-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e49a3-122">-Name</span></span>
<span data-ttu-id="e49a3-123">Der Name des Desktops in der angegebenen Desktop Gruppe</span><span class="sxs-lookup"><span data-stu-id="e49a3-123">The name of the desktop within the specified desktop group</span></span>

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

### <span data-ttu-id="e49a3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e49a3-124">-ResourceGroupName</span></span>
<span data-ttu-id="e49a3-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e49a3-125">The name of the resource group.</span></span>
<span data-ttu-id="e49a3-126">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="e49a3-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e49a3-127">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="e49a3-127">-SubscriptionId</span></span>
<span data-ttu-id="e49a3-128">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="e49a3-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e49a3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e49a3-129">CommonParameters</span></span>
<span data-ttu-id="e49a3-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e49a3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e49a3-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e49a3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e49a3-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e49a3-132">INPUTS</span></span>

### <span data-ttu-id="e49a3-133">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="e49a3-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="e49a3-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e49a3-134">OUTPUTS</span></span>

### <span data-ttu-id="e49a3-135">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IDesktop</span><span class="sxs-lookup"><span data-stu-id="e49a3-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IDesktop</span></span>

### <span data-ttu-id="e49a3-136">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IDesktopList</span><span class="sxs-lookup"><span data-stu-id="e49a3-136">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IDesktopList</span></span>

## <span data-ttu-id="e49a3-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="e49a3-137">NOTES</span></span>

<span data-ttu-id="e49a3-138">Aliase</span><span class="sxs-lookup"><span data-stu-id="e49a3-138">ALIASES</span></span>

<span data-ttu-id="e49a3-139">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e49a3-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e49a3-140">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e49a3-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e49a3-141">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="e49a3-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e49a3-142">Inputobject <IDesktopVirtualizationIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="e49a3-142">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e49a3-143">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="e49a3-143">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="e49a3-144">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="e49a3-144">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="e49a3-145">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktop Gruppe</span><span class="sxs-lookup"><span data-stu-id="e49a3-145">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="e49a3-146">`[HostPoolName <String>]`: Der Name des Host Pools in der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="e49a3-146">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="e49a3-147">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="e49a3-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e49a3-148">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e49a3-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e49a3-149">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="e49a3-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="e49a3-150">`[SessionHostName <String>]`: Der Name des Sitzungs Hosts innerhalb des angegebenen Host Pools</span><span class="sxs-lookup"><span data-stu-id="e49a3-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="e49a3-151">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="e49a3-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e49a3-152">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungs Hosts</span><span class="sxs-lookup"><span data-stu-id="e49a3-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="e49a3-153">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="e49a3-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="e49a3-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e49a3-154">RELATED LINKS</span></span>

