---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
ms.openlocfilehash: e75a9db71a4b20ed87d4e9564597af758af16304
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297105"
---
# <span data-ttu-id="628d5-101">Get-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="628d5-101">Get-AzWvdApplication</span></span>

## <span data-ttu-id="628d5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="628d5-102">SYNOPSIS</span></span>
<span data-ttu-id="628d5-103">Besorgen Sie sich eine Anwendung.</span><span class="sxs-lookup"><span data-stu-id="628d5-103">Get an application.</span></span>

## <span data-ttu-id="628d5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="628d5-104">SYNTAX</span></span>

### <span data-ttu-id="628d5-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="628d5-105">List (Default)</span></span>
```
Get-AzWvdApplication -GroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="628d5-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="628d5-106">Get</span></span>
```
Get-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="628d5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="628d5-107">GetViaIdentity</span></span>
```
Get-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="628d5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="628d5-108">DESCRIPTION</span></span>
<span data-ttu-id="628d5-109">Besorgen Sie sich eine Anwendung.</span><span class="sxs-lookup"><span data-stu-id="628d5-109">Get an application.</span></span>

## <span data-ttu-id="628d5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="628d5-110">EXAMPLES</span></span>

### <span data-ttu-id="628d5-111">Beispiel 1: Abrufen einer Windows-virtuellen Desktop Anwendung nach Namen</span><span class="sxs-lookup"><span data-stu-id="628d5-111">Example 1: Get a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="628d5-112">Dieser Befehl ruft eine virtuelle Windows-Desktop Anwendung in einer Applicaton-Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="628d5-112">This command gets a Windows Virtual Desktop Application in an applicaton Group.</span></span>

### <span data-ttu-id="628d5-113">Beispiel 2: Auflisten von Windows-virtuellen Desktop Anwendungen</span><span class="sxs-lookup"><span data-stu-id="628d5-113">Example 2: List Windows Virtual Desktop Applications</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName1 Microsoft.DesktopVirtualization/applicationgroups/applications
ApplicationGroupName/ApplicationName2 Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="628d5-114">Dieser Befehl listet die virtuellen Windows-Desktop Anwendungen in einer Applicaton-Gruppe auf.</span><span class="sxs-lookup"><span data-stu-id="628d5-114">This command Lists Windows Virtual Desktop Applications in an applicaton Group.</span></span>

## <span data-ttu-id="628d5-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="628d5-115">PARAMETERS</span></span>

### <span data-ttu-id="628d5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="628d5-116">-DefaultProfile</span></span>
<span data-ttu-id="628d5-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="628d5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="628d5-118">-GroupName</span><span class="sxs-lookup"><span data-stu-id="628d5-118">-GroupName</span></span>
<span data-ttu-id="628d5-119">Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="628d5-119">The name of the application group</span></span>

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

### <span data-ttu-id="628d5-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="628d5-120">-InputObject</span></span>
<span data-ttu-id="628d5-121">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="628d5-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="628d5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="628d5-122">-Name</span></span>
<span data-ttu-id="628d5-123">Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="628d5-123">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="628d5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="628d5-124">-ResourceGroupName</span></span>
<span data-ttu-id="628d5-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="628d5-125">The name of the resource group.</span></span>
<span data-ttu-id="628d5-126">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="628d5-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="628d5-127">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="628d5-127">-SubscriptionId</span></span>
<span data-ttu-id="628d5-128">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="628d5-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="628d5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="628d5-129">CommonParameters</span></span>
<span data-ttu-id="628d5-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="628d5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="628d5-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="628d5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="628d5-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="628d5-132">INPUTS</span></span>

### <span data-ttu-id="628d5-133">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="628d5-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="628d5-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="628d5-134">OUTPUTS</span></span>

### <span data-ttu-id="628d5-135">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IApplication</span><span class="sxs-lookup"><span data-stu-id="628d5-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplication</span></span>

## <span data-ttu-id="628d5-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="628d5-136">NOTES</span></span>

<span data-ttu-id="628d5-137">Aliase</span><span class="sxs-lookup"><span data-stu-id="628d5-137">ALIASES</span></span>

<span data-ttu-id="628d5-138">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="628d5-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="628d5-139">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="628d5-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="628d5-140">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="628d5-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="628d5-141">Inputobject <IDesktopVirtualizationIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="628d5-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="628d5-142">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="628d5-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="628d5-143">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="628d5-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="628d5-144">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktop Gruppe</span><span class="sxs-lookup"><span data-stu-id="628d5-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="628d5-145">`[HostPoolName <String>]`: Der Name des Host Pools in der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="628d5-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="628d5-146">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="628d5-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="628d5-147">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="628d5-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="628d5-148">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="628d5-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="628d5-149">`[SessionHostName <String>]`: Der Name des Sitzungs Hosts innerhalb des angegebenen Host Pools</span><span class="sxs-lookup"><span data-stu-id="628d5-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="628d5-150">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="628d5-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="628d5-151">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungs Hosts</span><span class="sxs-lookup"><span data-stu-id="628d5-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="628d5-152">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="628d5-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="628d5-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="628d5-153">RELATED LINKS</span></span>

