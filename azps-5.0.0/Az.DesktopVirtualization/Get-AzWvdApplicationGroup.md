---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
ms.openlocfilehash: 1ad8b51a39cdde66728200af28c77f7b094f19c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297100"
---
# <span data-ttu-id="a4191-101">Get-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="a4191-101">Get-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="a4191-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a4191-102">SYNOPSIS</span></span>
<span data-ttu-id="a4191-103">Rufen Sie eine Anwendungsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="a4191-103">Get an application group.</span></span>

## <span data-ttu-id="a4191-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4191-104">SYNTAX</span></span>

### <span data-ttu-id="a4191-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="a4191-105">List1 (Default)</span></span>
```
Get-AzWvdApplicationGroup [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="a4191-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="a4191-106">Get</span></span>
```
Get-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a4191-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a4191-107">GetViaIdentity</span></span>
```
Get-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="a4191-108">Liste</span><span class="sxs-lookup"><span data-stu-id="a4191-108">List</span></span>
```
Get-AzWvdApplicationGroup -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a4191-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a4191-109">DESCRIPTION</span></span>
<span data-ttu-id="a4191-110">Rufen Sie eine Anwendungsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="a4191-110">Get an application group.</span></span>

## <span data-ttu-id="a4191-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a4191-111">EXAMPLES</span></span>

### <span data-ttu-id="a4191-112">Beispiel 1: Abrufen einer Windows-virtuellen Desktop Anwendung mit Namen</span><span class="sxs-lookup"><span data-stu-id="a4191-112">Example 1: Get a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="a4191-113">Dieser Befehl ruft eine Windows Virtual Desktop-Anwendungsgruppe in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="a4191-113">This command gets a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="a4191-114">Beispiel 2: Auflisten von Windows Virtual Desktop-ApplicationGroups</span><span class="sxs-lookup"><span data-stu-id="a4191-114">Example 2: List Windows Virtual Desktop ApplicationGroups</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName

Location   Name                  Type
--------   ----                  ----
eastus     ApplicationGroupName1 Microsoft.DesktopVirtualization/applicationgroups
eastus     ApplicationGroupName2 Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="a4191-115">Dieser Befehl listet einen virtuellen Windows-Desktop ApplicationGroups in einer Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="a4191-115">This command lists a Windows Virtual Desktop ApplicationGroups in a Resource Group.</span></span>

## <span data-ttu-id="a4191-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4191-116">PARAMETERS</span></span>

### <span data-ttu-id="a4191-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4191-117">-DefaultProfile</span></span>
<span data-ttu-id="a4191-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a4191-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4191-119">-Filter</span><span class="sxs-lookup"><span data-stu-id="a4191-119">-Filter</span></span>
<span data-ttu-id="a4191-120">OData-Filterausdruck.</span><span class="sxs-lookup"><span data-stu-id="a4191-120">OData filter expression.</span></span>
<span data-ttu-id="a4191-121">Gültige Eigenschaften für das Filtern sind applicationGroupType.</span><span class="sxs-lookup"><span data-stu-id="a4191-121">Valid properties for filtering are applicationGroupType.</span></span>

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

### <span data-ttu-id="a4191-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a4191-122">-InputObject</span></span>
<span data-ttu-id="a4191-123">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="a4191-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a4191-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a4191-124">-Name</span></span>
<span data-ttu-id="a4191-125">Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="a4191-125">The name of the application group</span></span>

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

### <span data-ttu-id="a4191-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4191-126">-ResourceGroupName</span></span>
<span data-ttu-id="a4191-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a4191-127">The name of the resource group.</span></span>
<span data-ttu-id="a4191-128">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="a4191-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a4191-129">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="a4191-129">-SubscriptionId</span></span>
<span data-ttu-id="a4191-130">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="a4191-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a4191-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4191-131">CommonParameters</span></span>
<span data-ttu-id="a4191-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4191-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4191-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4191-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4191-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a4191-134">INPUTS</span></span>

### <span data-ttu-id="a4191-135">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="a4191-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="a4191-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a4191-136">OUTPUTS</span></span>

### <span data-ttu-id="a4191-137">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="a4191-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplicationGroup</span></span>

## <span data-ttu-id="a4191-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="a4191-138">NOTES</span></span>

<span data-ttu-id="a4191-139">Aliase</span><span class="sxs-lookup"><span data-stu-id="a4191-139">ALIASES</span></span>

<span data-ttu-id="a4191-140">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a4191-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a4191-141">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a4191-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a4191-142">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="a4191-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a4191-143">Inputobject <IDesktopVirtualizationIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="a4191-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a4191-144">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="a4191-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="a4191-145">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="a4191-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="a4191-146">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktop Gruppe</span><span class="sxs-lookup"><span data-stu-id="a4191-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="a4191-147">`[HostPoolName <String>]`: Der Name des Host Pools in der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="a4191-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="a4191-148">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="a4191-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a4191-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a4191-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a4191-150">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="a4191-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="a4191-151">`[SessionHostName <String>]`: Der Name des Sitzungs Hosts innerhalb des angegebenen Host Pools</span><span class="sxs-lookup"><span data-stu-id="a4191-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="a4191-152">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="a4191-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a4191-153">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungs Hosts</span><span class="sxs-lookup"><span data-stu-id="a4191-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="a4191-154">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="a4191-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="a4191-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a4191-155">RELATED LINKS</span></span>

