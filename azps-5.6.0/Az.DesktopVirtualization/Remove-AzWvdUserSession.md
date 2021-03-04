---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/remove-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
ms.openlocfilehash: a15dc7c72f2f7ef321f05f51d5b90c936f0406e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932875"
---
# <span data-ttu-id="40478-101">Remove-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="40478-101">Remove-AzWvdUserSession</span></span>

## <span data-ttu-id="40478-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40478-102">SYNOPSIS</span></span>
<span data-ttu-id="40478-103">Entfernen sie eine userSession.</span><span class="sxs-lookup"><span data-stu-id="40478-103">Remove a userSession.</span></span>

## <span data-ttu-id="40478-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40478-104">SYNTAX</span></span>

### <span data-ttu-id="40478-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="40478-105">Delete (Default)</span></span>
```
Remove-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="40478-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="40478-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="40478-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40478-107">DESCRIPTION</span></span>
<span data-ttu-id="40478-108">Entfernen sie eine userSession.</span><span class="sxs-lookup"><span data-stu-id="40478-108">Remove a userSession.</span></span>

## <span data-ttu-id="40478-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="40478-109">EXAMPLES</span></span>

### <span data-ttu-id="40478-110">Beispiel 1: Löschen einer Windows Virtual Desktop UserSession nach Name</span><span class="sxs-lookup"><span data-stu-id="40478-110">Example 1: Delete a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Remove-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="40478-111">Mit diesem Befehl wird eine Windows Virtual Desktop UserSession in einem Sitzungshost gelöscht.</span><span class="sxs-lookup"><span data-stu-id="40478-111">This command deletes a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="40478-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="40478-112">PARAMETERS</span></span>

### <span data-ttu-id="40478-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40478-113">-DefaultProfile</span></span>
<span data-ttu-id="40478-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40478-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40478-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="40478-115">-Force</span></span>
<span data-ttu-id="40478-116">Erzwingen sie, dass sich das Flag von userSession abmeldet.</span><span class="sxs-lookup"><span data-stu-id="40478-116">Force flag to login off userSession.</span></span>

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

### <span data-ttu-id="40478-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="40478-117">-HostPoolName</span></span>
<span data-ttu-id="40478-118">Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="40478-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="40478-119">-ID</span><span class="sxs-lookup"><span data-stu-id="40478-119">-Id</span></span>
<span data-ttu-id="40478-120">Der Name der Benutzersitzung innerhalb des angegebenen Sitzungshosts</span><span class="sxs-lookup"><span data-stu-id="40478-120">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40478-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40478-121">-InputObject</span></span>
<span data-ttu-id="40478-122">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="40478-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="40478-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40478-123">-PassThru</span></span>
<span data-ttu-id="40478-124">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="40478-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="40478-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40478-125">-ResourceGroupName</span></span>
<span data-ttu-id="40478-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="40478-126">The name of the resource group.</span></span>
<span data-ttu-id="40478-127">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="40478-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="40478-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="40478-128">-SessionHostName</span></span>
<span data-ttu-id="40478-129">Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="40478-129">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="40478-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="40478-130">-SubscriptionId</span></span>
<span data-ttu-id="40478-131">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="40478-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="40478-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="40478-132">-Confirm</span></span>
<span data-ttu-id="40478-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="40478-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40478-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40478-134">-WhatIf</span></span>
<span data-ttu-id="40478-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="40478-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40478-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="40478-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40478-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40478-137">CommonParameters</span></span>
<span data-ttu-id="40478-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40478-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40478-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40478-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40478-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="40478-140">INPUTS</span></span>

### <span data-ttu-id="40478-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="40478-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="40478-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="40478-142">OUTPUTS</span></span>

### <span data-ttu-id="40478-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="40478-143">System.Boolean</span></span>

## <span data-ttu-id="40478-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="40478-144">NOTES</span></span>

<span data-ttu-id="40478-145">ALIASE</span><span class="sxs-lookup"><span data-stu-id="40478-145">ALIASES</span></span>

<span data-ttu-id="40478-146">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="40478-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="40478-147">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="40478-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="40478-148">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="40478-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="40478-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="40478-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="40478-150">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="40478-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="40478-151">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="40478-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="40478-152">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="40478-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="40478-153">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="40478-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="40478-154">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="40478-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="40478-155">`[MsixPackageFullName <String>]`: Der versionsspezifische Paketname des MSIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="40478-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="40478-156">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="40478-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="40478-157">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="40478-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="40478-158">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="40478-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="40478-159">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="40478-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="40478-160">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungshosts</span><span class="sxs-lookup"><span data-stu-id="40478-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="40478-161">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="40478-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="40478-162">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="40478-162">RELATED LINKS</span></span>

