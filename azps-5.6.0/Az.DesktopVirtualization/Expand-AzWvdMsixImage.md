---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/expand-azwvdmsiximage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
ms.openlocfilehash: f4767b87e7230727a2cf9c83af0c2aa5d03b908a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925712"
---
# <span data-ttu-id="a113d-101">Expand-AzWvdMsixImage</span><span class="sxs-lookup"><span data-stu-id="a113d-101">Expand-AzWvdMsixImage</span></span>

## <span data-ttu-id="a113d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a113d-102">SYNOPSIS</span></span>
<span data-ttu-id="a113d-103">Erweitert und listet MSIX-Pakete in einem Bild auf, da der Bildpfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="a113d-103">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="a113d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a113d-104">SYNTAX</span></span>

### <span data-ttu-id="a113d-105">ExpandExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="a113d-105">ExpandExpanded (Default)</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Uri <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a113d-106">Erweitern</span><span class="sxs-lookup"><span data-stu-id="a113d-106">Expand</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> -MsixImageUri <IMsixImageUri>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a113d-107">ExpandViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a113d-107">ExpandViaIdentity</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> -MsixImageUri <IMsixImageUri>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a113d-108">ExpandViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a113d-108">ExpandViaIdentityExpanded</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> [-Uri <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a113d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a113d-109">DESCRIPTION</span></span>
<span data-ttu-id="a113d-110">Erweitert und listet MSIX-Pakete in einem Bild auf, da der Bildpfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="a113d-110">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="a113d-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a113d-111">EXAMPLES</span></span>

### <span data-ttu-id="a113d-112">Beispiel 1: Erweitert den angegebenen Bildpfad und ruft Paketmetadaten ab, die in AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="a113d-112">Example 1: Expands specified Image Path and retrieves Package metadata found in AppxManifest.xml</span></span>
```powershell
PS C:\> Expand-AzWvdMsixImage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
          -Uri ImagePathURI

Name                          Type
----                          ----
HostPoolName/extractmsiximage Microsoft.DesktopVirtualization/hostpools/extractmsiximage
```

<span data-ttu-id="a113d-113">Dieser Befehl gibt Metadaten des MSIX-Pakets zurück, die im angegebenen Bildpfad gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="a113d-113">This command returns Metadata of MSIX Package found in the given Image Path.</span></span>

## <span data-ttu-id="a113d-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a113d-114">PARAMETERS</span></span>

### <span data-ttu-id="a113d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a113d-115">-DefaultProfile</span></span>
<span data-ttu-id="a113d-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a113d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a113d-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="a113d-117">-HostPoolName</span></span>
<span data-ttu-id="a113d-118">Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="a113d-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="a113d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a113d-119">-InputObject</span></span>
<span data-ttu-id="a113d-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="a113d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a113d-121">-MsixImageUri</span><span class="sxs-lookup"><span data-stu-id="a113d-121">-MsixImageUri</span></span>
<span data-ttu-id="a113d-122">Stellt URI dar, der sich auf MSIX Image To construct bezieht, siehe Abschnitt NOTIZEN zu MSIXIMAGEURI-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="a113d-122">Represents URI referring to MSIX Image To construct, see NOTES section for MSIXIMAGEURI properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri
Parameter Sets: Expand, ExpandViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a113d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a113d-123">-ResourceGroupName</span></span>
<span data-ttu-id="a113d-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a113d-124">The name of the resource group.</span></span>
<span data-ttu-id="a113d-125">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="a113d-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a113d-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a113d-126">-SubscriptionId</span></span>
<span data-ttu-id="a113d-127">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="a113d-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a113d-128">-URI</span><span class="sxs-lookup"><span data-stu-id="a113d-128">-Uri</span></span>
<span data-ttu-id="a113d-129">URI zu Bild</span><span class="sxs-lookup"><span data-stu-id="a113d-129">URI to Image</span></span>

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

### <span data-ttu-id="a113d-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a113d-130">-Confirm</span></span>
<span data-ttu-id="a113d-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a113d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a113d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a113d-132">-WhatIf</span></span>
<span data-ttu-id="a113d-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a113d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a113d-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a113d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a113d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a113d-135">CommonParameters</span></span>
<span data-ttu-id="a113d-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a113d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a113d-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a113d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a113d-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a113d-138">INPUTS</span></span>

### <span data-ttu-id="a113d-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri</span><span class="sxs-lookup"><span data-stu-id="a113d-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri</span></span>

### <span data-ttu-id="a113d-140">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="a113d-140">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="a113d-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a113d-141">OUTPUTS</span></span>

### <span data-ttu-id="a113d-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IExpandMsixImage</span><span class="sxs-lookup"><span data-stu-id="a113d-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IExpandMsixImage</span></span>

## <span data-ttu-id="a113d-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a113d-143">NOTES</span></span>

<span data-ttu-id="a113d-144">ALIASE</span><span class="sxs-lookup"><span data-stu-id="a113d-144">ALIASES</span></span>

<span data-ttu-id="a113d-145">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="a113d-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a113d-146">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="a113d-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a113d-147">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a113d-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a113d-148">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="a113d-148">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a113d-149">`[ApplicationGroupName <String>]`: Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="a113d-149">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="a113d-150">`[ApplicationName <String>]`: Der Name der Anwendung innerhalb der angegebenen Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="a113d-150">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="a113d-151">`[DesktopName <String>]`: Der Name des Desktops in der angegebenen Desktopgruppe</span><span class="sxs-lookup"><span data-stu-id="a113d-151">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="a113d-152">`[HostPoolName <String>]`: Der Name des Hostpools innerhalb der angegebenen Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="a113d-152">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="a113d-153">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="a113d-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a113d-154">`[MsixPackageFullName <String>]`: Der versionsspezifische Paketname des MSIX-Pakets innerhalb des angegebenen Hostpools</span><span class="sxs-lookup"><span data-stu-id="a113d-154">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="a113d-155">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a113d-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a113d-156">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="a113d-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="a113d-157">`[SessionHostName <String>]`: Der Name des Sitzungshosts im angegebenen Hostpool</span><span class="sxs-lookup"><span data-stu-id="a113d-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="a113d-158">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="a113d-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a113d-159">`[UserSessionId <String>]`: Der Name der Benutzersitzung innerhalb des angegebenen Sitzungshosts</span><span class="sxs-lookup"><span data-stu-id="a113d-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="a113d-160">`[WorkspaceName <String>]`: Der Name des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="a113d-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

<span data-ttu-id="a113d-161">MSIXIMAGEURI <IMsixImageUri> : Stellt einen URI dar, der sich auf MSIX Image bezieht</span><span class="sxs-lookup"><span data-stu-id="a113d-161">MSIXIMAGEURI <IMsixImageUri>: Represents URI referring to MSIX Image</span></span>
  - <span data-ttu-id="a113d-162">`[Uri <String>]`: URI zu Bild</span><span class="sxs-lookup"><span data-stu-id="a113d-162">`[Uri <String>]`: URI to Image</span></span>

## <span data-ttu-id="a113d-163">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a113d-163">RELATED LINKS</span></span>

