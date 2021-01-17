---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/expand-azwvdmsiximage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
ms.openlocfilehash: 417acf03af2bf73d57759841bacc3ed532e8f043
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303227"
---
# <span data-ttu-id="8767b-101">Expand-AzWvdMsixImage</span><span class="sxs-lookup"><span data-stu-id="8767b-101">Expand-AzWvdMsixImage</span></span>

## <span data-ttu-id="8767b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8767b-102">SYNOPSIS</span></span>
<span data-ttu-id="8767b-103">Mit dem Bildpfad werden die MSIX-Pakete in einem Bild erweitert und aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="8767b-103">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="8767b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8767b-104">SYNTAX</span></span>

### <span data-ttu-id="8767b-105">ExpandExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="8767b-105">ExpandExpanded (Default)</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Uri <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8767b-106">Erweitern</span><span class="sxs-lookup"><span data-stu-id="8767b-106">Expand</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> -MsixImageUri <IMsixImageUri>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8767b-107">ExpandViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8767b-107">ExpandViaIdentity</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> -MsixImageUri <IMsixImageUri>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8767b-108">ExpandViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8767b-108">ExpandViaIdentityExpanded</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> [-Uri <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8767b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8767b-109">DESCRIPTION</span></span>
<span data-ttu-id="8767b-110">Mit dem Bildpfad werden die MSIX-Pakete in einem Bild erweitert und aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="8767b-110">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="8767b-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8767b-111">EXAMPLES</span></span>

### <span data-ttu-id="8767b-112">Beispiel 1: Erweitert den angegebenen Bildpfad und ruft Paketmetadaten aus der AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="8767b-112">Example 1: Expands specified Image Path and retrieves Package metadata found in AppxManifest.xml</span></span>
```powershell
PS C:\> Expand-AzWvdMsixImage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
          -Uri ImagePathURI

Name                          Type
----                          ----
HostPoolName/extractmsiximage Microsoft.DesktopVirtualization/hostpools/extractmsiximage
```

<span data-ttu-id="8767b-113">Dieser Befehl gibt Metadaten von MSIX Package zurück, die im angegebenen Bildpfad gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="8767b-113">This command returns Metadata of MSIX Package found in the given Image Path.</span></span>

## <span data-ttu-id="8767b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8767b-114">PARAMETERS</span></span>

### <span data-ttu-id="8767b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8767b-115">-DefaultProfile</span></span>
<span data-ttu-id="8767b-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8767b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8767b-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="8767b-117">-HostPoolName</span></span>
<span data-ttu-id="8767b-118">Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="8767b-118">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Expand, ExpandExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8767b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8767b-119">-InputObject</span></span>
<span data-ttu-id="8767b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="8767b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: ExpandViaIdentity, ExpandViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8767b-121">-MsixImageUri</span><span class="sxs-lookup"><span data-stu-id="8767b-121">-MsixImageUri</span></span>
<span data-ttu-id="8767b-122">Stellt einen URI dar, der sich auf "MSIX Image To construct" bezieht. Informationen finden Sie im Abschnitt "NOTES" für #A0 und erstellen eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="8767b-122">Represents URI referring to MSIX Image To construct, see NOTES section for MSIXIMAGEURI properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixImageUri
Parameter Sets: Expand, ExpandViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8767b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8767b-123">-ResourceGroupName</span></span>
<span data-ttu-id="8767b-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8767b-124">The name of the resource group.</span></span>
<span data-ttu-id="8767b-125">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="8767b-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand, ExpandExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8767b-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8767b-126">-SubscriptionId</span></span>
<span data-ttu-id="8767b-127">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="8767b-127">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand, ExpandExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8767b-128">-URI</span><span class="sxs-lookup"><span data-stu-id="8767b-128">-Uri</span></span>
<span data-ttu-id="8767b-129">URI zu Bild</span><span class="sxs-lookup"><span data-stu-id="8767b-129">URI to Image</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandExpanded, ExpandViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8767b-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8767b-130">-Confirm</span></span>
<span data-ttu-id="8767b-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8767b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8767b-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8767b-132">-WhatIf</span></span>
<span data-ttu-id="8767b-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8767b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8767b-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8767b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8767b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8767b-135">CommonParameters</span></span>
<span data-ttu-id="8767b-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8767b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8767b-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8767b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8767b-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8767b-138">INPUTS</span></span>

### <span data-ttu-id="8767b-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixImageUri</span><span class="sxs-lookup"><span data-stu-id="8767b-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixImageUri</span></span>

### <span data-ttu-id="8767b-140">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="8767b-140">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="8767b-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8767b-141">OUTPUTS</span></span>

### <span data-ttu-id="8767b-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IExpandMsixImage</span><span class="sxs-lookup"><span data-stu-id="8767b-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IExpandMsixImage</span></span>

## <span data-ttu-id="8767b-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8767b-143">NOTES</span></span>

<span data-ttu-id="8767b-144">ALIASE</span><span class="sxs-lookup"><span data-stu-id="8767b-144">ALIASES</span></span>

<span data-ttu-id="8767b-145">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="8767b-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8767b-146">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8767b-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8767b-147">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8767b-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8767b-148">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="8767b-148">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8767b-149">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="8767b-149">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="8767b-150">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="8767b-150">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="8767b-151">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="8767b-151">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="8767b-152">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="8767b-152">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="8767b-153">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="8767b-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8767b-154">`[MsixPackageFullName <String>]`: Der versionsspezifische Paketname des vollständigen Pakets des MsIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="8767b-154">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="8767b-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8767b-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8767b-156">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="8767b-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="8767b-157">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="8767b-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="8767b-158">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="8767b-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8767b-159">`[UserSessionId <String>]`: Der Name der Benutzersitzung im angegebenen Sitzungshost</span><span class="sxs-lookup"><span data-stu-id="8767b-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="8767b-160">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="8767b-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

<span data-ttu-id="8767b-161">MSIXIMAGEURI <IMsixImageUri> : Stellt einen URI dar, der auf das MSIX Image verweist.</span><span class="sxs-lookup"><span data-stu-id="8767b-161">MSIXIMAGEURI <IMsixImageUri>: Represents URI referring to MSIX Image</span></span>
  - <span data-ttu-id="8767b-162">`[Uri <String>]`: URI zu Bild</span><span class="sxs-lookup"><span data-stu-id="8767b-162">`[Uri <String>]`: URI to Image</span></span>

## <span data-ttu-id="8767b-163">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8767b-163">RELATED LINKS</span></span>

