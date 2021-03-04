---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/disconnect-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
ms.openlocfilehash: 61e1eb1f5ae3846ce2f0cf7ad82d17d613d27e0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925715"
---
# <span data-ttu-id="5b33e-101">Disconnect-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="5b33e-101">Disconnect-AzWvdUserSession</span></span>

## <span data-ttu-id="5b33e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b33e-102">SYNOPSIS</span></span>
<span data-ttu-id="5b33e-103">Trennen sie eine userSession.</span><span class="sxs-lookup"><span data-stu-id="5b33e-103">Disconnect a userSession.</span></span>

## <span data-ttu-id="5b33e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5b33e-104">SYNTAX</span></span>

### <span data-ttu-id="5b33e-105">Trennen (Standard)</span><span class="sxs-lookup"><span data-stu-id="5b33e-105">Disconnect (Default)</span></span>
```
Disconnect-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5b33e-106">DisconnectViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5b33e-106">DisconnectViaIdentity</span></span>
```
Disconnect-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5b33e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5b33e-107">DESCRIPTION</span></span>
<span data-ttu-id="5b33e-108">Trennen sie eine userSession.</span><span class="sxs-lookup"><span data-stu-id="5b33e-108">Disconnect a userSession.</span></span>

## <span data-ttu-id="5b33e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5b33e-109">EXAMPLES</span></span>

### <span data-ttu-id="5b33e-110">Beispiel 1: Trennen einer Windows Virtual Desktop UserSession nach Name</span><span class="sxs-lookup"><span data-stu-id="5b33e-110">Example 1: Disconnect a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Disconnect-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="5b33e-111">Mit diesem Befehl wird eine Windows Virtual Desktop UserSession in einem Sitzungshost getrennt.</span><span class="sxs-lookup"><span data-stu-id="5b33e-111">This command disconnects a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="5b33e-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5b33e-112">PARAMETERS</span></span>

### <span data-ttu-id="5b33e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b33e-113">-DefaultProfile</span></span>
<span data-ttu-id="5b33e-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5b33e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b33e-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="5b33e-115">-HostPoolName</span></span>
<span data-ttu-id="5b33e-116">Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="5b33e-116">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b33e-117">-ID</span><span class="sxs-lookup"><span data-stu-id="5b33e-117">-Id</span></span>
<span data-ttu-id="5b33e-118">Der Name der Benutzersitzung innerhalb des angegebenen Sitzungshosts</span><span class="sxs-lookup"><span data-stu-id="5b33e-118">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b33e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b33e-119">-InputObject</span></span>
<span data-ttu-id="5b33e-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="5b33e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DisconnectViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b33e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b33e-121">-PassThru</span></span>
<span data-ttu-id="5b33e-122">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5b33e-122">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b33e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b33e-123">-ResourceGroupName</span></span>
<span data-ttu-id="5b33e-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5b33e-124">The name of the resource group.</span></span>
<span data-ttu-id="5b33e-125">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="5b33e-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b33e-126">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="5b33e-126">-SessionHostName</span></span>
<span data-ttu-id="5b33e-127">Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="5b33e-127">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b33e-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5b33e-128">-SubscriptionId</span></span>
<span data-ttu-id="5b33e-129">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="5b33e-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b33e-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5b33e-130">-Confirm</span></span>
<span data-ttu-id="5b33e-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5b33e-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b33e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b33e-132">-WhatIf</span></span>
<span data-ttu-id="5b33e-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5b33e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b33e-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5b33e-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b33e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b33e-135">CommonParameters</span></span>
<span data-ttu-id="5b33e-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b33e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b33e-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b33e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b33e-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5b33e-138">INPUTS</span></span>

### <span data-ttu-id="5b33e-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="5b33e-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="5b33e-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5b33e-140">OUTPUTS</span></span>

### <span data-ttu-id="5b33e-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5b33e-141">System.Boolean</span></span>

## <span data-ttu-id="5b33e-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5b33e-142">NOTES</span></span>

<span data-ttu-id="5b33e-143">ALIASE</span><span class="sxs-lookup"><span data-stu-id="5b33e-143">ALIASES</span></span>

<span data-ttu-id="5b33e-144">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="5b33e-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5b33e-145">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="5b33e-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5b33e-146">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5b33e-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5b33e-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="5b33e-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5b33e-148">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="5b33e-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="5b33e-149">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="5b33e-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="5b33e-150">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="5b33e-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="5b33e-151">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="5b33e-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="5b33e-152">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="5b33e-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5b33e-153">`[MsixPackageFullName <String>]`: Der versionsspezifische Paketname des MSIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="5b33e-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="5b33e-154">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5b33e-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5b33e-155">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="5b33e-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="5b33e-156">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="5b33e-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="5b33e-157">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="5b33e-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5b33e-158">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungshosts</span><span class="sxs-lookup"><span data-stu-id="5b33e-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="5b33e-159">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="5b33e-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="5b33e-160">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5b33e-160">RELATED LINKS</span></span>

