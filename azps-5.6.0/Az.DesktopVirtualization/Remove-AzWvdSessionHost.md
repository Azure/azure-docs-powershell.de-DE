---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/remove-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
ms.openlocfilehash: ee8334a233c35c2b834bfb89ddf20152d466367f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925616"
---
# <span data-ttu-id="0bfec-101">Remove-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="0bfec-101">Remove-AzWvdSessionHost</span></span>

## <span data-ttu-id="0bfec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bfec-102">SYNOPSIS</span></span>
<span data-ttu-id="0bfec-103">Entfernen Sie einen SessionHost.</span><span class="sxs-lookup"><span data-stu-id="0bfec-103">Remove a SessionHost.</span></span>

## <span data-ttu-id="0bfec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0bfec-104">SYNTAX</span></span>

### <span data-ttu-id="0bfec-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="0bfec-105">Delete (Default)</span></span>
```
Remove-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="0bfec-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0bfec-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0bfec-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0bfec-107">DESCRIPTION</span></span>
<span data-ttu-id="0bfec-108">Entfernen Sie einen SessionHost.</span><span class="sxs-lookup"><span data-stu-id="0bfec-108">Remove a SessionHost.</span></span>

## <span data-ttu-id="0bfec-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0bfec-109">EXAMPLES</span></span>

### <span data-ttu-id="0bfec-110">Beispiel 1: Löschen einer Windows Virtual Desktop SessionHost nach Name</span><span class="sxs-lookup"><span data-stu-id="0bfec-110">Example 1: Delete a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Remove-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName
```

<span data-ttu-id="0bfec-111">Mit diesem Befehl wird ein Windows Virtual Desktop SessionHost in einem Hostpool gelöscht.</span><span class="sxs-lookup"><span data-stu-id="0bfec-111">This command deletes a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="0bfec-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0bfec-112">PARAMETERS</span></span>

### <span data-ttu-id="0bfec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bfec-113">-DefaultProfile</span></span>
<span data-ttu-id="0bfec-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0bfec-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bfec-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="0bfec-115">-Force</span></span>
<span data-ttu-id="0bfec-116">Erzwingen, dass das Löschen von sessionHost auch dann erzwingen wird, wenn userSession vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0bfec-116">Force flag to force sessionHost deletion even when userSession exists.</span></span>

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

### <span data-ttu-id="0bfec-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="0bfec-117">-HostPoolName</span></span>
<span data-ttu-id="0bfec-118">Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="0bfec-118">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bfec-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0bfec-119">-InputObject</span></span>
<span data-ttu-id="0bfec-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="0bfec-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0bfec-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0bfec-121">-Name</span></span>
<span data-ttu-id="0bfec-122">Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="0bfec-122">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bfec-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0bfec-123">-PassThru</span></span>
<span data-ttu-id="0bfec-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0bfec-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0bfec-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bfec-125">-ResourceGroupName</span></span>
<span data-ttu-id="0bfec-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0bfec-126">The name of the resource group.</span></span>
<span data-ttu-id="0bfec-127">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="0bfec-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bfec-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0bfec-128">-SubscriptionId</span></span>
<span data-ttu-id="0bfec-129">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="0bfec-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bfec-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0bfec-130">-Confirm</span></span>
<span data-ttu-id="0bfec-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0bfec-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bfec-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bfec-132">-WhatIf</span></span>
<span data-ttu-id="0bfec-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0bfec-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bfec-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0bfec-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bfec-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bfec-135">CommonParameters</span></span>
<span data-ttu-id="0bfec-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bfec-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bfec-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0bfec-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bfec-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0bfec-138">INPUTS</span></span>

### <span data-ttu-id="0bfec-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="0bfec-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="0bfec-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0bfec-140">OUTPUTS</span></span>

### <span data-ttu-id="0bfec-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0bfec-141">System.Boolean</span></span>

## <span data-ttu-id="0bfec-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0bfec-142">NOTES</span></span>

<span data-ttu-id="0bfec-143">ALIASE</span><span class="sxs-lookup"><span data-stu-id="0bfec-143">ALIASES</span></span>

<span data-ttu-id="0bfec-144">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="0bfec-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0bfec-145">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="0bfec-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0bfec-146">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0bfec-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0bfec-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="0bfec-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0bfec-148">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="0bfec-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="0bfec-149">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="0bfec-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="0bfec-150">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="0bfec-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="0bfec-151">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="0bfec-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="0bfec-152">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="0bfec-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0bfec-153">`[MsixPackageFullName <String>]`: Der versionsspezifische Paketname des MSIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="0bfec-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="0bfec-154">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0bfec-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0bfec-155">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="0bfec-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="0bfec-156">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="0bfec-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="0bfec-157">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="0bfec-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0bfec-158">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungshosts</span><span class="sxs-lookup"><span data-stu-id="0bfec-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="0bfec-159">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="0bfec-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="0bfec-160">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0bfec-160">RELATED LINKS</span></span>

