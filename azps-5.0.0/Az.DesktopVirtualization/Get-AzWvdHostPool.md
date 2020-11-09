---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
ms.openlocfilehash: e04d13b96f36b96b2ae1c22f6f6e5b3c50b338f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297082"
---
# <span data-ttu-id="43250-101">Get-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="43250-101">Get-AzWvdHostPool</span></span>

## <span data-ttu-id="43250-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="43250-102">SYNOPSIS</span></span>
<span data-ttu-id="43250-103">Besorgen Sie sich einen Host-Pool.</span><span class="sxs-lookup"><span data-stu-id="43250-103">Get a host pool.</span></span>

## <span data-ttu-id="43250-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="43250-104">SYNTAX</span></span>

### <span data-ttu-id="43250-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="43250-105">List1 (Default)</span></span>
```
Get-AzWvdHostPool [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="43250-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="43250-106">Get</span></span>
```
Get-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="43250-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="43250-107">GetViaIdentity</span></span>
```
Get-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="43250-108">Liste</span><span class="sxs-lookup"><span data-stu-id="43250-108">List</span></span>
```
Get-AzWvdHostPool -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="43250-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43250-109">DESCRIPTION</span></span>
<span data-ttu-id="43250-110">Besorgen Sie sich einen Host-Pool.</span><span class="sxs-lookup"><span data-stu-id="43250-110">Get a host pool.</span></span>

## <span data-ttu-id="43250-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="43250-111">EXAMPLES</span></span>

### <span data-ttu-id="43250-112">Beispiel 1: Abrufen eines virtuellen Windows-Desktop-HostPool nach Name</span><span class="sxs-lookup"><span data-stu-id="43250-112">Example 1: Get a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName -Name HostPoolName

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="43250-113">Dieser Befehl ruft einen virtuellen Windows-Desktop-HostPool in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="43250-113">This command gets a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="43250-114">Beispiel 2: Auflisten von Windows Virtual Desktop-HostPools</span><span class="sxs-lookup"><span data-stu-id="43250-114">Example 2: List Windows Virtual Desktop HostPools</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName

Location   Name          Type
--------   ----          ----
eastus     HostPoolName1 Microsoft.DesktopVirtualization/hostpools
eastus     HostPoolName2 Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="43250-115">Dieser Befehl listet einen virtuellen Windows-Desktop HostPools in einer Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="43250-115">This command lists a Windows Virtual Desktop HostPools in a Resource Group.</span></span>

## <span data-ttu-id="43250-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="43250-116">PARAMETERS</span></span>

### <span data-ttu-id="43250-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43250-117">-DefaultProfile</span></span>
<span data-ttu-id="43250-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="43250-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43250-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="43250-119">-InputObject</span></span>
<span data-ttu-id="43250-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="43250-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="43250-121">-Name</span><span class="sxs-lookup"><span data-stu-id="43250-121">-Name</span></span>
<span data-ttu-id="43250-122">Der Name des Host Pools in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="43250-122">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="43250-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43250-123">-ResourceGroupName</span></span>
<span data-ttu-id="43250-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="43250-124">The name of the resource group.</span></span>
<span data-ttu-id="43250-125">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="43250-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="43250-126">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="43250-126">-SubscriptionId</span></span>
<span data-ttu-id="43250-127">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="43250-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="43250-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43250-128">CommonParameters</span></span>
<span data-ttu-id="43250-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43250-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43250-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43250-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43250-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="43250-131">INPUTS</span></span>

### <span data-ttu-id="43250-132">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="43250-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="43250-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="43250-133">OUTPUTS</span></span>

### <span data-ttu-id="43250-134">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IHostPool</span><span class="sxs-lookup"><span data-stu-id="43250-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IHostPool</span></span>

## <span data-ttu-id="43250-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="43250-135">NOTES</span></span>

<span data-ttu-id="43250-136">Aliase</span><span class="sxs-lookup"><span data-stu-id="43250-136">ALIASES</span></span>

<span data-ttu-id="43250-137">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="43250-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="43250-138">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="43250-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="43250-139">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="43250-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="43250-140">Inputobject <IDesktopVirtualizationIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="43250-140">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="43250-141">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="43250-141">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="43250-142">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="43250-142">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="43250-143">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktop Gruppe</span><span class="sxs-lookup"><span data-stu-id="43250-143">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="43250-144">`[HostPoolName <String>]`: Der Name des Host Pools in der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="43250-144">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="43250-145">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="43250-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="43250-146">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="43250-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="43250-147">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="43250-147">The name is case insensitive.</span></span>
  - <span data-ttu-id="43250-148">`[SessionHostName <String>]`: Der Name des Sitzungs Hosts innerhalb des angegebenen Host Pools</span><span class="sxs-lookup"><span data-stu-id="43250-148">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="43250-149">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="43250-149">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="43250-150">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungs Hosts</span><span class="sxs-lookup"><span data-stu-id="43250-150">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="43250-151">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="43250-151">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="43250-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="43250-152">RELATED LINKS</span></span>

