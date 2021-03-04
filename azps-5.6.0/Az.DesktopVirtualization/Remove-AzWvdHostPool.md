---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/remove-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdHostPool.md
ms.openlocfilehash: 42902280d93797613197f7da3263418e0fc8672e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925632"
---
# <span data-ttu-id="d7850-101">Remove-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="d7850-101">Remove-AzWvdHostPool</span></span>

## <span data-ttu-id="d7850-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7850-102">SYNOPSIS</span></span>
<span data-ttu-id="d7850-103">Entfernen Sie einen Hostpool.</span><span class="sxs-lookup"><span data-stu-id="d7850-103">Remove a host pool.</span></span>

## <span data-ttu-id="d7850-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7850-104">SYNTAX</span></span>

### <span data-ttu-id="d7850-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="d7850-105">Delete (Default)</span></span>
```
Remove-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d7850-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d7850-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d7850-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d7850-107">DESCRIPTION</span></span>
<span data-ttu-id="d7850-108">Entfernen Sie einen Hostpool.</span><span class="sxs-lookup"><span data-stu-id="d7850-108">Remove a host pool.</span></span>

## <span data-ttu-id="d7850-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d7850-109">EXAMPLES</span></span>

### <span data-ttu-id="d7850-110">Beispiel 1: Löschen eines virtuellen Windows-DesktophostPools nach Name</span><span class="sxs-lookup"><span data-stu-id="d7850-110">Example 1: Delete a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Remove-AzWvdHostPool -ResourceGroupName ResourceGroupName -Name HostPoolName
```

<span data-ttu-id="d7850-111">Mit diesem Befehl wird ein virtueller Windows-DesktophostPool in einer Ressourcengruppe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="d7850-111">This command deletes a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="d7850-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d7850-112">PARAMETERS</span></span>

### <span data-ttu-id="d7850-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7850-113">-DefaultProfile</span></span>
<span data-ttu-id="d7850-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d7850-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7850-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="d7850-115">-Force</span></span>
<span data-ttu-id="d7850-116">Erzwingen des Flag zum Löschen von sessionHost.</span><span class="sxs-lookup"><span data-stu-id="d7850-116">Force flag to delete sessionHost.</span></span>

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

### <span data-ttu-id="d7850-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7850-117">-InputObject</span></span>
<span data-ttu-id="d7850-118">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d7850-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d7850-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d7850-119">-Name</span></span>
<span data-ttu-id="d7850-120">Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="d7850-120">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7850-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7850-121">-PassThru</span></span>
<span data-ttu-id="d7850-122">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d7850-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d7850-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7850-123">-ResourceGroupName</span></span>
<span data-ttu-id="d7850-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d7850-124">The name of the resource group.</span></span>
<span data-ttu-id="d7850-125">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="d7850-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d7850-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d7850-126">-SubscriptionId</span></span>
<span data-ttu-id="d7850-127">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="d7850-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d7850-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d7850-128">-Confirm</span></span>
<span data-ttu-id="d7850-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d7850-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7850-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7850-130">-WhatIf</span></span>
<span data-ttu-id="d7850-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d7850-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7850-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d7850-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7850-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7850-133">CommonParameters</span></span>
<span data-ttu-id="d7850-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7850-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7850-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7850-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7850-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d7850-136">INPUTS</span></span>

### <span data-ttu-id="d7850-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="d7850-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="d7850-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d7850-138">OUTPUTS</span></span>

### <span data-ttu-id="d7850-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d7850-139">System.Boolean</span></span>

## <span data-ttu-id="d7850-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d7850-140">NOTES</span></span>

<span data-ttu-id="d7850-141">ALIASE</span><span class="sxs-lookup"><span data-stu-id="d7850-141">ALIASES</span></span>

<span data-ttu-id="d7850-142">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="d7850-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d7850-143">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="d7850-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d7850-144">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d7850-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d7850-145">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="d7850-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d7850-146">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="d7850-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="d7850-147">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="d7850-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="d7850-148">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="d7850-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="d7850-149">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="d7850-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="d7850-150">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="d7850-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d7850-151">`[MsixPackageFullName <String>]`: Der versionsspezifische Paketname des MSIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="d7850-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="d7850-152">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d7850-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d7850-153">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="d7850-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="d7850-154">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="d7850-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="d7850-155">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="d7850-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d7850-156">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungshosts</span><span class="sxs-lookup"><span data-stu-id="d7850-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="d7850-157">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="d7850-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="d7850-158">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d7850-158">RELATED LINKS</span></span>

