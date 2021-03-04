---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
ms.openlocfilehash: 1ba4b3141b2254de9e1988fbd2b76f03a06ceb99
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932904"
---
# <span data-ttu-id="6db7b-101">Get-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="6db7b-101">Get-AzWvdHostPool</span></span>

## <span data-ttu-id="6db7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6db7b-102">SYNOPSIS</span></span>
<span data-ttu-id="6db7b-103">Holen Sie sich einen Hostpool.</span><span class="sxs-lookup"><span data-stu-id="6db7b-103">Get a host pool.</span></span>

## <span data-ttu-id="6db7b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6db7b-104">SYNTAX</span></span>

### <span data-ttu-id="6db7b-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="6db7b-105">List1 (Default)</span></span>
```
Get-AzWvdHostPool [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6db7b-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="6db7b-106">Get</span></span>
```
Get-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6db7b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6db7b-107">GetViaIdentity</span></span>
```
Get-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="6db7b-108">Liste</span><span class="sxs-lookup"><span data-stu-id="6db7b-108">List</span></span>
```
Get-AzWvdHostPool -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="6db7b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6db7b-109">DESCRIPTION</span></span>
<span data-ttu-id="6db7b-110">Holen Sie sich einen Hostpool.</span><span class="sxs-lookup"><span data-stu-id="6db7b-110">Get a host pool.</span></span>

## <span data-ttu-id="6db7b-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6db7b-111">EXAMPLES</span></span>

### <span data-ttu-id="6db7b-112">Beispiel 1: Herunterladen eines virtuellen Windows-DesktophostPools nach Name</span><span class="sxs-lookup"><span data-stu-id="6db7b-112">Example 1: Get a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName -Name HostPoolName

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="6db7b-113">Dieser Befehl ruft eine Windows Virtual Desktop HostPool in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="6db7b-113">This command gets a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="6db7b-114">Beispiel 2: Auflisten von virtuellen Windows-DesktophostPools</span><span class="sxs-lookup"><span data-stu-id="6db7b-114">Example 2: List Windows Virtual Desktop HostPools</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName

Location   Name          Type
--------   ----          ----
eastus     HostPoolName1 Microsoft.DesktopVirtualization/hostpools
eastus     HostPoolName2 Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="6db7b-115">Mit diesem Befehl werden windows Virtual Desktop HostPools in einer Ressourcengruppe aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="6db7b-115">This command lists a Windows Virtual Desktop HostPools in a Resource Group.</span></span>

## <span data-ttu-id="6db7b-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6db7b-116">PARAMETERS</span></span>

### <span data-ttu-id="6db7b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6db7b-117">-DefaultProfile</span></span>
<span data-ttu-id="6db7b-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6db7b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6db7b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6db7b-119">-InputObject</span></span>
<span data-ttu-id="6db7b-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="6db7b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6db7b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6db7b-121">-Name</span></span>
<span data-ttu-id="6db7b-122">Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="6db7b-122">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="6db7b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6db7b-123">-ResourceGroupName</span></span>
<span data-ttu-id="6db7b-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6db7b-124">The name of the resource group.</span></span>
<span data-ttu-id="6db7b-125">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="6db7b-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6db7b-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6db7b-126">-SubscriptionId</span></span>
<span data-ttu-id="6db7b-127">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="6db7b-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6db7b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6db7b-128">CommonParameters</span></span>
<span data-ttu-id="6db7b-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6db7b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6db7b-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6db7b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6db7b-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6db7b-131">INPUTS</span></span>

### <span data-ttu-id="6db7b-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="6db7b-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="6db7b-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6db7b-133">OUTPUTS</span></span>

### <span data-ttu-id="6db7b-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span><span class="sxs-lookup"><span data-stu-id="6db7b-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="6db7b-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6db7b-135">NOTES</span></span>

<span data-ttu-id="6db7b-136">ALIASE</span><span class="sxs-lookup"><span data-stu-id="6db7b-136">ALIASES</span></span>

<span data-ttu-id="6db7b-137">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="6db7b-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6db7b-138">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="6db7b-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6db7b-139">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6db7b-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6db7b-140">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="6db7b-140">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6db7b-141">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="6db7b-141">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="6db7b-142">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="6db7b-142">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="6db7b-143">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="6db7b-143">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="6db7b-144">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="6db7b-144">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="6db7b-145">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="6db7b-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6db7b-146">`[MsixPackageFullName <String>]`: Der versionsspezifische Paketname des MSIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="6db7b-146">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="6db7b-147">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6db7b-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6db7b-148">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="6db7b-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="6db7b-149">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="6db7b-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="6db7b-150">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="6db7b-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6db7b-151">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungshosts</span><span class="sxs-lookup"><span data-stu-id="6db7b-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="6db7b-152">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="6db7b-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="6db7b-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6db7b-153">RELATED LINKS</span></span>

