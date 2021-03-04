---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
ms.openlocfilehash: e5cef84d4ae45e4ce55b1f377ab16edc2449c72c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923640"
---
# <span data-ttu-id="96902-101">Get-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="96902-101">Get-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="96902-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96902-102">SYNOPSIS</span></span>
<span data-ttu-id="96902-103">Eine Anwendungsgruppe erhalten.</span><span class="sxs-lookup"><span data-stu-id="96902-103">Get an application group.</span></span>

## <span data-ttu-id="96902-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="96902-104">SYNTAX</span></span>

### <span data-ttu-id="96902-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="96902-105">List1 (Default)</span></span>
```
Get-AzWvdApplicationGroup [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="96902-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="96902-106">Get</span></span>
```
Get-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="96902-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="96902-107">GetViaIdentity</span></span>
```
Get-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="96902-108">Liste</span><span class="sxs-lookup"><span data-stu-id="96902-108">List</span></span>
```
Get-AzWvdApplicationGroup -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="96902-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="96902-109">DESCRIPTION</span></span>
<span data-ttu-id="96902-110">Eine Anwendungsgruppe erhalten.</span><span class="sxs-lookup"><span data-stu-id="96902-110">Get an application group.</span></span>

## <span data-ttu-id="96902-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="96902-111">EXAMPLES</span></span>

### <span data-ttu-id="96902-112">Beispiel 1: Herunterladen einer Windows Virtual Desktop ApplicationGroup nach Name</span><span class="sxs-lookup"><span data-stu-id="96902-112">Example 1: Get a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="96902-113">Dieser Befehl ruft eine Windows Virtual Desktop ApplicationGroup in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="96902-113">This command gets a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="96902-114">Beispiel 2: Auflisten von virtuellen Windows-Desktopanwendungsgruppen</span><span class="sxs-lookup"><span data-stu-id="96902-114">Example 2: List Windows Virtual Desktop ApplicationGroups</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName

Location   Name                  Type
--------   ----                  ----
eastus     ApplicationGroupName1 Microsoft.DesktopVirtualization/applicationgroups
eastus     ApplicationGroupName2 Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="96902-115">Dieser Befehl listet eine Windows Virtual Desktop ApplicationGroups in einer Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="96902-115">This command lists a Windows Virtual Desktop ApplicationGroups in a Resource Group.</span></span>

## <span data-ttu-id="96902-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="96902-116">PARAMETERS</span></span>

### <span data-ttu-id="96902-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96902-117">-DefaultProfile</span></span>
<span data-ttu-id="96902-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="96902-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96902-119">-Filter</span><span class="sxs-lookup"><span data-stu-id="96902-119">-Filter</span></span>
<span data-ttu-id="96902-120">OData-Filterausdruck.</span><span class="sxs-lookup"><span data-stu-id="96902-120">OData filter expression.</span></span>
<span data-ttu-id="96902-121">Gültige Eigenschaften zum Filtern sind applicationGroupType.</span><span class="sxs-lookup"><span data-stu-id="96902-121">Valid properties for filtering are applicationGroupType.</span></span>

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

### <span data-ttu-id="96902-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96902-122">-InputObject</span></span>
<span data-ttu-id="96902-123">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="96902-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="96902-124">-Name</span><span class="sxs-lookup"><span data-stu-id="96902-124">-Name</span></span>
<span data-ttu-id="96902-125">Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="96902-125">The name of the application group</span></span>

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

### <span data-ttu-id="96902-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96902-126">-ResourceGroupName</span></span>
<span data-ttu-id="96902-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="96902-127">The name of the resource group.</span></span>
<span data-ttu-id="96902-128">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="96902-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="96902-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="96902-129">-SubscriptionId</span></span>
<span data-ttu-id="96902-130">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="96902-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="96902-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96902-131">CommonParameters</span></span>
<span data-ttu-id="96902-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96902-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96902-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96902-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96902-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="96902-134">INPUTS</span></span>

### <span data-ttu-id="96902-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="96902-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="96902-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="96902-136">OUTPUTS</span></span>

### <span data-ttu-id="96902-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="96902-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span></span>

## <span data-ttu-id="96902-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="96902-138">NOTES</span></span>

<span data-ttu-id="96902-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="96902-139">ALIASES</span></span>

<span data-ttu-id="96902-140">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="96902-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="96902-141">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="96902-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="96902-142">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="96902-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="96902-143">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="96902-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="96902-144">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="96902-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="96902-145">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="96902-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="96902-146">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="96902-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="96902-147">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="96902-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="96902-148">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="96902-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="96902-149">`[MsixPackageFullName <String>]`: Der versionsspezifische Paketname des MSIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="96902-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="96902-150">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="96902-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="96902-151">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="96902-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="96902-152">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="96902-152">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="96902-153">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="96902-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="96902-154">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungshosts</span><span class="sxs-lookup"><span data-stu-id="96902-154">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="96902-155">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="96902-155">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="96902-156">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="96902-156">RELATED LINKS</span></span>

