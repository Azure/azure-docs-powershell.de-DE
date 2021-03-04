---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/remove-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplication.md
ms.openlocfilehash: 0d8f3f3fa1f89c2045b10e07a5f7b11358222234
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925640"
---
# <span data-ttu-id="a50e4-101">Remove-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="a50e4-101">Remove-AzWvdApplication</span></span>

## <span data-ttu-id="a50e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a50e4-102">SYNOPSIS</span></span>
<span data-ttu-id="a50e4-103">Entfernen Sie eine Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a50e4-103">Remove an application.</span></span>

## <span data-ttu-id="a50e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a50e4-104">SYNTAX</span></span>

### <span data-ttu-id="a50e4-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="a50e4-105">Delete (Default)</span></span>
```
Remove-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a50e4-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a50e4-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a50e4-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a50e4-107">DESCRIPTION</span></span>
<span data-ttu-id="a50e4-108">Entfernen Sie eine Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a50e4-108">Remove an application.</span></span>

## <span data-ttu-id="a50e4-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a50e4-109">EXAMPLES</span></span>

### <span data-ttu-id="a50e4-110">Beispiel 1: Löschen einer virtuellen Windows-Desktopanwendung nach Name</span><span class="sxs-lookup"><span data-stu-id="a50e4-110">Example 1: Delete a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Remove-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName
```

<span data-ttu-id="a50e4-111">Mit diesem Befehl wird eine virtuelle Windows-Desktopanwendung in einer applicaton-Gruppe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a50e4-111">This command deletes a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="a50e4-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a50e4-112">PARAMETERS</span></span>

### <span data-ttu-id="a50e4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a50e4-113">-DefaultProfile</span></span>
<span data-ttu-id="a50e4-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a50e4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a50e4-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="a50e4-115">-GroupName</span></span>
<span data-ttu-id="a50e4-116">Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="a50e4-116">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a50e4-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a50e4-117">-InputObject</span></span>
<span data-ttu-id="a50e4-118">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="a50e4-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a50e4-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a50e4-119">-Name</span></span>
<span data-ttu-id="a50e4-120">Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="a50e4-120">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a50e4-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a50e4-121">-PassThru</span></span>
<span data-ttu-id="a50e4-122">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a50e4-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a50e4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a50e4-123">-ResourceGroupName</span></span>
<span data-ttu-id="a50e4-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a50e4-124">The name of the resource group.</span></span>
<span data-ttu-id="a50e4-125">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="a50e4-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a50e4-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a50e4-126">-SubscriptionId</span></span>
<span data-ttu-id="a50e4-127">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="a50e4-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a50e4-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a50e4-128">-Confirm</span></span>
<span data-ttu-id="a50e4-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a50e4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a50e4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a50e4-130">-WhatIf</span></span>
<span data-ttu-id="a50e4-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a50e4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a50e4-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a50e4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a50e4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a50e4-133">CommonParameters</span></span>
<span data-ttu-id="a50e4-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a50e4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a50e4-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a50e4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a50e4-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a50e4-136">INPUTS</span></span>

### <span data-ttu-id="a50e4-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="a50e4-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="a50e4-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a50e4-138">OUTPUTS</span></span>

### <span data-ttu-id="a50e4-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a50e4-139">System.Boolean</span></span>

## <span data-ttu-id="a50e4-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a50e4-140">NOTES</span></span>

<span data-ttu-id="a50e4-141">ALIASE</span><span class="sxs-lookup"><span data-stu-id="a50e4-141">ALIASES</span></span>

<span data-ttu-id="a50e4-142">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="a50e4-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a50e4-143">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="a50e4-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a50e4-144">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a50e4-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a50e4-145">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="a50e4-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a50e4-146">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="a50e4-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="a50e4-147">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="a50e4-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="a50e4-148">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="a50e4-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="a50e4-149">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="a50e4-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="a50e4-150">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="a50e4-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a50e4-151">`[MsixPackageFullName <String>]`: Der versionsspezifische Paketname des MSIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="a50e4-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="a50e4-152">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a50e4-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a50e4-153">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="a50e4-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="a50e4-154">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="a50e4-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="a50e4-155">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="a50e4-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a50e4-156">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungshosts</span><span class="sxs-lookup"><span data-stu-id="a50e4-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="a50e4-157">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="a50e4-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="a50e4-158">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a50e4-158">RELATED LINKS</span></span>

