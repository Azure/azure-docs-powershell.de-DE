---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: a7ff5c406cea050f809ef9ffa1e2d9974903fdc2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460388"
---
# <span data-ttu-id="25f4e-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="25f4e-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="25f4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25f4e-102">SYNOPSIS</span></span>
<span data-ttu-id="25f4e-103">Entfernt eine Zugriffseinschränkungsregel aus einer Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="25f4e-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="25f4e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25f4e-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Action <String>] [-SlotName <String>] [-TargetScmSite] [-IpAddress <String>] [-SubnetName <String>]
 [-VirtualNetworkName <String>] [-SubnetId <String>] [-ServiceTag <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25f4e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="25f4e-105">DESCRIPTION</span></span>
<span data-ttu-id="25f4e-106">Das **Cmdlet "Remove-AzWebAppAccessRestrictionRule"** entfernt eine Zugriffseinschränkungsregel aus einer Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="25f4e-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="25f4e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="25f4e-107">EXAMPLES</span></span>

### <span data-ttu-id="25f4e-108">Beispiel 1: Entfernen einer Web App-Zugriffseinschränkungsregel</span><span class="sxs-lookup"><span data-stu-id="25f4e-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="25f4e-109">Mit diesem Befehl wird die Zugriffseinschränkungsregel "IpRule" aus Azure Web App namens "ContosoSite" entfernt, die zur Ressourcengruppe "Default-Web-WestUS" gehört.</span><span class="sxs-lookup"><span data-stu-id="25f4e-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="25f4e-110">Beispiel 2: Entfernen einer Zugriffseinschränkungsregel für ein Diensttag (Web App)</span><span class="sxs-lookup"><span data-stu-id="25f4e-110">Example 2: Remove a Service Tag Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -ServiceTag AzureFrontDoor.Backend
```

<span data-ttu-id="25f4e-111">Mit diesem Befehl wird die Zugriffseinschränkungsregel mit "ServiceTag" gleich "AzureFrontD backend" aus Azure Web App namens "ContosoSite" entfernt, die zur Ressourcengruppe "Default-Web-WestUS" gehört.</span><span class="sxs-lookup"><span data-stu-id="25f4e-111">This command removes the access restriction rule with ServiceTag equals AzureFrontDoor.Backend from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="25f4e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25f4e-112">PARAMETERS</span></span>

### <span data-ttu-id="25f4e-113">-Action</span><span class="sxs-lookup"><span data-stu-id="25f4e-113">-Action</span></span>
<span data-ttu-id="25f4e-114">Regel "Zulassen" oder "Verweigern".</span><span class="sxs-lookup"><span data-stu-id="25f4e-114">Allow or Deny rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25f4e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25f4e-115">-DefaultProfile</span></span>
<span data-ttu-id="25f4e-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="25f4e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25f4e-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="25f4e-117">-IpAddress</span></span>
<span data-ttu-id="25f4e-118">Ip Address v4 oder v6 CIDR Range.</span><span class="sxs-lookup"><span data-stu-id="25f4e-118">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="25f4e-119">Beispiel: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="25f4e-119">E.g.: 192.168.0.0/24</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25f4e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="25f4e-120">-Name</span></span>
<span data-ttu-id="25f4e-121">Name der Zugriffseinschränkungsregel</span><span class="sxs-lookup"><span data-stu-id="25f4e-121">Access Restriction Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25f4e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25f4e-122">-PassThru</span></span>
<span data-ttu-id="25f4e-123">Geben Sie das Konfigurationsobjekt für Zugriffseinschränkungen zurück.</span><span class="sxs-lookup"><span data-stu-id="25f4e-123">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="25f4e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25f4e-124">-ResourceGroupName</span></span>
<span data-ttu-id="25f4e-125">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="25f4e-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25f4e-126">-ServiceTag</span><span class="sxs-lookup"><span data-stu-id="25f4e-126">-ServiceTag</span></span>
<span data-ttu-id="25f4e-127">Name des Servicetags</span><span class="sxs-lookup"><span data-stu-id="25f4e-127">Name of Service Tag</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25f4e-128">-SlotName</span><span class="sxs-lookup"><span data-stu-id="25f4e-128">-SlotName</span></span>
<span data-ttu-id="25f4e-129">Name des Bereitstellungsplatzes.</span><span class="sxs-lookup"><span data-stu-id="25f4e-129">Deployment Slot Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25f4e-130">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="25f4e-130">-SubnetId</span></span>
<span data-ttu-id="25f4e-131">ResourceId des Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="25f4e-131">ResourceId of Subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25f4e-132">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="25f4e-132">-SubnetName</span></span>
<span data-ttu-id="25f4e-133">Name des Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="25f4e-133">Name of Subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25f4e-134">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="25f4e-134">-TargetScmSite</span></span>
<span data-ttu-id="25f4e-135">Die Regel gilt für die Hauptwebsite oder die Scm-Website.</span><span class="sxs-lookup"><span data-stu-id="25f4e-135">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="25f4e-136">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="25f4e-136">-VirtualNetworkName</span></span>
<span data-ttu-id="25f4e-137">Name des virtuellen Netzwerks (muss in derselben Ressourcengruppe wie Web App sein).</span><span class="sxs-lookup"><span data-stu-id="25f4e-137">Name of Virtual Network (must be in same resource group as Web App).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25f4e-138">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="25f4e-138">-WebAppName</span></span>
<span data-ttu-id="25f4e-139">Der Name der Web App.</span><span class="sxs-lookup"><span data-stu-id="25f4e-139">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25f4e-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25f4e-140">-Confirm</span></span>
<span data-ttu-id="25f4e-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="25f4e-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25f4e-142">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="25f4e-142">-WhatIf</span></span>
<span data-ttu-id="25f4e-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="25f4e-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="25f4e-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="25f4e-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25f4e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25f4e-145">CommonParameters</span></span>
<span data-ttu-id="25f4e-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25f4e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25f4e-147">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25f4e-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25f4e-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="25f4e-148">INPUTS</span></span>

### <span data-ttu-id="25f4e-149">System.String</span><span class="sxs-lookup"><span data-stu-id="25f4e-149">System.String</span></span>

## <span data-ttu-id="25f4e-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="25f4e-150">OUTPUTS</span></span>

### <span data-ttu-id="25f4e-151">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="25f4e-151">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="25f4e-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="25f4e-152">NOTES</span></span>

## <span data-ttu-id="25f4e-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="25f4e-153">RELATED LINKS</span></span>

[<span data-ttu-id="25f4e-154">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="25f4e-154">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="25f4e-155">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="25f4e-155">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="25f4e-156">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="25f4e-156">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)
