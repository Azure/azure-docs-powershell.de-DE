---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
ms.openlocfilehash: 1e7727933f01f1b2fa3196e3c195c25dda5c247b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923624"
---
# <span data-ttu-id="ad3c8-101">Get-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="ad3c8-101">Get-AzWvdSessionHost</span></span>

## <span data-ttu-id="ad3c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad3c8-102">SYNOPSIS</span></span>
<span data-ttu-id="ad3c8-103">Holen Sie sich einen Sitzungshost.</span><span class="sxs-lookup"><span data-stu-id="ad3c8-103">Get a session host.</span></span>

## <span data-ttu-id="ad3c8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ad3c8-104">SYNTAX</span></span>

### <span data-ttu-id="ad3c8-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="ad3c8-105">List (Default)</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ad3c8-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="ad3c8-106">Get</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ad3c8-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ad3c8-107">GetViaIdentity</span></span>
```
Get-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad3c8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ad3c8-108">DESCRIPTION</span></span>
<span data-ttu-id="ad3c8-109">Holen Sie sich einen Sitzungshost.</span><span class="sxs-lookup"><span data-stu-id="ad3c8-109">Get a session host.</span></span>

## <span data-ttu-id="ad3c8-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ad3c8-110">EXAMPLES</span></span>

### <span data-ttu-id="ad3c8-111">Beispiel 1: Herunterladen eines virtuellen Windows-Desktopsitzungshosts nach Name</span><span class="sxs-lookup"><span data-stu-id="ad3c8-111">Example 1: Get a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="ad3c8-112">Dieser Befehl ruft einen virtuellen Windows-Desktopsitzungshost in einem Hostpool ab.</span><span class="sxs-lookup"><span data-stu-id="ad3c8-112">This command gets a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

### <span data-ttu-id="ad3c8-113">Beispiel 2: Auflisten von virtuellen Windows-Desktopsitzungshosts</span><span class="sxs-lookup"><span data-stu-id="ad3c8-113">Example 2: List Windows Virtual Desktop SessionHosts</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName1 Microsoft.DesktopVirtualization/hostpools/sessionhosts
HostPoolName/SessionHostName2 Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="ad3c8-114">Mit diesem Befehl werden windows Virtual Desktop SessionHosts in einem Hostpool aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="ad3c8-114">This command lists a Windows Virtual Desktop SessionHosts in a Host Pool.</span></span>

## <span data-ttu-id="ad3c8-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ad3c8-115">PARAMETERS</span></span>

### <span data-ttu-id="ad3c8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad3c8-116">-DefaultProfile</span></span>
<span data-ttu-id="ad3c8-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ad3c8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad3c8-118">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="ad3c8-118">-HostPoolName</span></span>
<span data-ttu-id="ad3c8-119">Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="ad3c8-119">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="ad3c8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad3c8-120">-InputObject</span></span>
<span data-ttu-id="ad3c8-121">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="ad3c8-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ad3c8-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ad3c8-122">-Name</span></span>
<span data-ttu-id="ad3c8-123">Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="ad3c8-123">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="ad3c8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad3c8-124">-ResourceGroupName</span></span>
<span data-ttu-id="ad3c8-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ad3c8-125">The name of the resource group.</span></span>
<span data-ttu-id="ad3c8-126">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="ad3c8-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ad3c8-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ad3c8-127">-SubscriptionId</span></span>
<span data-ttu-id="ad3c8-128">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="ad3c8-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ad3c8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad3c8-129">CommonParameters</span></span>
<span data-ttu-id="ad3c8-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad3c8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad3c8-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad3c8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad3c8-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ad3c8-132">INPUTS</span></span>

### <span data-ttu-id="ad3c8-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="ad3c8-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="ad3c8-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ad3c8-134">OUTPUTS</span></span>

### <span data-ttu-id="ad3c8-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.ISessionHost</span><span class="sxs-lookup"><span data-stu-id="ad3c8-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.ISessionHost</span></span>

## <span data-ttu-id="ad3c8-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ad3c8-136">NOTES</span></span>

<span data-ttu-id="ad3c8-137">ALIASE</span><span class="sxs-lookup"><span data-stu-id="ad3c8-137">ALIASES</span></span>

<span data-ttu-id="ad3c8-138">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="ad3c8-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ad3c8-139">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="ad3c8-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ad3c8-140">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ad3c8-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ad3c8-141">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="ad3c8-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ad3c8-142">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="ad3c8-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="ad3c8-143">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="ad3c8-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="ad3c8-144">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="ad3c8-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="ad3c8-145">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="ad3c8-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="ad3c8-146">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="ad3c8-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ad3c8-147">`[MsixPackageFullName <String>]`: Der versionsspezifische Paketname des MSIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="ad3c8-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="ad3c8-148">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ad3c8-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ad3c8-149">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="ad3c8-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="ad3c8-150">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="ad3c8-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="ad3c8-151">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="ad3c8-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ad3c8-152">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungshosts</span><span class="sxs-lookup"><span data-stu-id="ad3c8-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="ad3c8-153">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="ad3c8-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="ad3c8-154">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ad3c8-154">RELATED LINKS</span></span>

