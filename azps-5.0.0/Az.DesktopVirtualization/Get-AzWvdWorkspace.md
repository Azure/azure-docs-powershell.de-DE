---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdWorkspace.md
ms.openlocfilehash: 4596900f336c10fe6c91bd62b7a14bde50efeef8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297051"
---
# <span data-ttu-id="6828d-101">Get-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="6828d-101">Get-AzWvdWorkspace</span></span>

## <span data-ttu-id="6828d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6828d-102">SYNOPSIS</span></span>
<span data-ttu-id="6828d-103">Abrufen eines Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="6828d-103">Get a workspace.</span></span>

## <span data-ttu-id="6828d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6828d-104">SYNTAX</span></span>

### <span data-ttu-id="6828d-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="6828d-105">List1 (Default)</span></span>
```
Get-AzWvdWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6828d-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="6828d-106">Get</span></span>
```
Get-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6828d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6828d-107">GetViaIdentity</span></span>
```
Get-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="6828d-108">Liste</span><span class="sxs-lookup"><span data-stu-id="6828d-108">List</span></span>
```
Get-AzWvdWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="6828d-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6828d-109">DESCRIPTION</span></span>
<span data-ttu-id="6828d-110">Abrufen eines Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="6828d-110">Get a workspace.</span></span>

## <span data-ttu-id="6828d-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6828d-111">EXAMPLES</span></span>

### <span data-ttu-id="6828d-112">Beispiel 1: Abrufen eines virtuellen Windows-Desktop-Worksapce nach Name</span><span class="sxs-lookup"><span data-stu-id="6828d-112">Example 1: Get a Windows Virtual Desktop Worksapce by name</span></span>
```powershell
PS C:\> Get-AzWvdWorksapce -ResourceGroupName ResourceGroupName -Name WorkspaceName

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="6828d-113">Dieser Befehl ruft einen virtuellen Windows-Desktop Arbeitsbereich in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="6828d-113">This command gets a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="6828d-114">Beispiel 2: Auflisten von Windows-virtuellen Desktop Arbeitsbereichen</span><span class="sxs-lookup"><span data-stu-id="6828d-114">Example 2: List Windows Virtual Desktop Workspaces</span></span>
```powershell
PS C:\> Get-AzWvdWorksapce -ResourceGroupName ResourceGroupName

Location   Name           Type
--------   ----           ----
eastus     WorkspaceName1 Microsoft.DesktopVirtualization/workspaces
eastus     WorkspaceName2 Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="6828d-115">Dieser Befehl listet einen virtuellen Windows-Desktop Arbeitsbereich in einer Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="6828d-115">This command lists a Windows Virtual Desktop Workspaces in a Resource Group.</span></span>

## <span data-ttu-id="6828d-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="6828d-116">PARAMETERS</span></span>

### <span data-ttu-id="6828d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6828d-117">-DefaultProfile</span></span>
<span data-ttu-id="6828d-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6828d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6828d-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6828d-119">-InputObject</span></span>
<span data-ttu-id="6828d-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="6828d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6828d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6828d-121">-Name</span></span>
<span data-ttu-id="6828d-122">Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="6828d-122">The name of the workspace</span></span>

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

### <span data-ttu-id="6828d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6828d-123">-ResourceGroupName</span></span>
<span data-ttu-id="6828d-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6828d-124">The name of the resource group.</span></span>
<span data-ttu-id="6828d-125">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="6828d-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6828d-126">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="6828d-126">-SubscriptionId</span></span>
<span data-ttu-id="6828d-127">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="6828d-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6828d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6828d-128">CommonParameters</span></span>
<span data-ttu-id="6828d-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6828d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6828d-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6828d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6828d-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6828d-131">INPUTS</span></span>

### <span data-ttu-id="6828d-132">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="6828d-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="6828d-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6828d-133">OUTPUTS</span></span>

### <span data-ttu-id="6828d-134">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="6828d-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="6828d-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="6828d-135">NOTES</span></span>

<span data-ttu-id="6828d-136">Aliase</span><span class="sxs-lookup"><span data-stu-id="6828d-136">ALIASES</span></span>

<span data-ttu-id="6828d-137">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6828d-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6828d-138">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6828d-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6828d-139">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="6828d-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6828d-140">Inputobject <IDesktopVirtualizationIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="6828d-140">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6828d-141">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="6828d-141">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="6828d-142">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="6828d-142">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="6828d-143">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktop Gruppe</span><span class="sxs-lookup"><span data-stu-id="6828d-143">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="6828d-144">`[HostPoolName <String>]`: Der Name des Host Pools in der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="6828d-144">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="6828d-145">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="6828d-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6828d-146">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6828d-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6828d-147">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="6828d-147">The name is case insensitive.</span></span>
  - <span data-ttu-id="6828d-148">`[SessionHostName <String>]`: Der Name des Sitzungs Hosts innerhalb des angegebenen Host Pools</span><span class="sxs-lookup"><span data-stu-id="6828d-148">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="6828d-149">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="6828d-149">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6828d-150">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungs Hosts</span><span class="sxs-lookup"><span data-stu-id="6828d-150">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="6828d-151">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="6828d-151">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="6828d-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6828d-152">RELATED LINKS</span></span>

