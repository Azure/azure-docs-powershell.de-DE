---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: b28cb8ac408ff281930eac68bf2b97d288150dd6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155953"
---
# <span data-ttu-id="0dc96-101">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="0dc96-101">Add-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="0dc96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0dc96-102">SYNOPSIS</span></span>
<span data-ttu-id="0dc96-103">Fügt einer Azure Web App eine Access-Restiction-Regel hinzu.</span><span class="sxs-lookup"><span data-stu-id="0dc96-103">Adds an Access Restiction rule to an Azure Web App.</span></span>

## <span data-ttu-id="0dc96-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0dc96-104">SYNTAX</span></span>

### <span data-ttu-id="0dc96-105">IpAddressParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0dc96-105">IpAddressParameterSet (Default)</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -IpAddress <String> [-PassThru] [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dc96-106">ServiceTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc96-106">ServiceTagParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 [-PassThru] -ServiceTag <String> [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dc96-107">SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc96-107">SubnetNameParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetName <String> -VirtualNetworkName <String> [-IgnoreMissingServiceEndpoint] [-PassThru]
 [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dc96-108">SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc96-108">SubnetIdParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetId <String> [-IgnoreMissingServiceEndpoint] [-PassThru] [-HttpHeader <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0dc96-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0dc96-109">DESCRIPTION</span></span>
<span data-ttu-id="0dc96-110">Das **Cmdlet "Add-AzWebAppAccessRestrictionRule"** fügt einer Azure Web App eine Zugriffseinschränkungsregel hinzu.</span><span class="sxs-lookup"><span data-stu-id="0dc96-110">The **Add-AzWebAppAccessRestrictionRule** cmdlet adds an Access Restriction rule to an Azure Web App.</span></span>

## <span data-ttu-id="0dc96-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0dc96-111">EXAMPLES</span></span>

### <span data-ttu-id="0dc96-112">Beispiel 1: Hinzufügen einer Zugriffseinschränkungsregel für "IpAddress" zu einer Web App</span><span class="sxs-lookup"><span data-stu-id="0dc96-112">Example 1: Add IpAddress Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name IpRule -Priority 200 -Action Allow -IpAddress 10.10.0.0/8
```

<span data-ttu-id="0dc96-113">Mit diesem Befehl wird einer Web App mit dem Namen "ContosoSite" eine Zugriffseinschränkungsregel mit der Priorität 200 und dem Ip-Bereich hinzufügt, die zur Ressourcengruppe "Default-Web-WestUS" gehört.</span><span class="sxs-lookup"><span data-stu-id="0dc96-113">This command adds an access restriction rule with priority 200 and ip range to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="0dc96-114">Beispiel 2: Hinzufügen einer Zugriffseinschränkungsregel für den Subnetzdienstendpunkt zu einer Web App</span><span class="sxs-lookup"><span data-stu-id="0dc96-114">Example 2: Add Subnet Service Endpoint Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name SubnetRule -Priority 300 -Action Allow -SubnetName appgw-subnet -VirtualNetworkName corp-vnet
```

<span data-ttu-id="0dc96-115">Mit diesem Befehl wird einer Web App mit dem Namen "ContosoSite", die zur Ressourcengruppe "Default-Web-WestUS" gehört, eine Zugriffseinschränkungsregel mit der Priorität 300 und mit dem Subnetz -Appgw-Subnetz in corp-vnet hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="0dc96-115">This command adds an access restriction rule with priority 300 and with subnet appgw-subnet in corp-vnet to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="0dc96-116">Beispiel 3: Hinzufügen einer #A0 zu einer Web App</span><span class="sxs-lookup"><span data-stu-id="0dc96-116">Example 3: Add ServiceTag Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name ServiceTagRule -Priority 200 -Action Allow -ServiceTag AzureFrontDoor.Backend
```

<span data-ttu-id="0dc96-117">Dieser Befehl fügt einer Web App mit dem Namen "ContosoSite", die zur Ressourcengruppe "Default-Web-WestUS" gehört, eine Zugriffseinschränkungsregel mit der Priorität 200 und ein Diensttag hinzu, das den ip-Bereich von Azure Front Door darstellt.</span><span class="sxs-lookup"><span data-stu-id="0dc96-117">This command adds an access restriction rule with priority 200 and a Service Tag representing the ip scope of Azure Front Door to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="0dc96-118">Beispiel 4: Hinzufügen einer Zugriffseinschränkungsregel für mehrere Adressen zu einer Web App</span><span class="sxs-lookup"><span data-stu-id="0dc96-118">Example 4: Add multi-address Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name MultipleIpRule -Priority 200 -Action Allow -IpAddress "10.10.0.0/8,192.168.0.0/16"
```

<span data-ttu-id="0dc96-119">Dieser Befehl fügt einer Web App mit dem Namen "ContosoSite" eine Zugriffseinschränkungsregel mit der Priorität 200 und zwei IP-Bereichen hinzu, die zur Ressourcengruppe "Default-Web-WestUS" gehört.</span><span class="sxs-lookup"><span data-stu-id="0dc96-119">This command adds an access restriction rule with priority 200 and two ip ranges to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="0dc96-120">Beispiel 5: Hinzufügen einer Zugriffseinschränkungsregel mit dem Http-Header zu einer Web App</span><span class="sxs-lookup"><span data-stu-id="0dc96-120">Example 5: Add Access Restriction rule with http header to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name MultipleIpRule -Priority 400 -Action Allow -ServiceTag AzureFrontDoor.Backend
-HttpHeader @{'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'; 'x-azure-fdid' = '355deb06-47c4-4ba4-9641-c7d7a98b913e'}
```

<span data-ttu-id="0dc96-121">Mit diesem Befehl wird eine Zugriffseinschränkungsregel mit der Priorität 400 für das Diensttag "AzureFrontDhttp.Back-End" hinzugefügt und der Zugriff auf http-Header bestimmter Werte auf eine Web App mit dem Namen "ContosoSite" beschränkt, die zur Ressourcengruppe "Default-Web-WestUS" gehört.</span><span class="sxs-lookup"><span data-stu-id="0dc96-121">This command adds an access restriction rule with priority 400 for Service Tag AzureFrontDoor.Backend and further restricts access only to http headers of certain values to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="0dc96-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0dc96-122">PARAMETERS</span></span>

### <span data-ttu-id="0dc96-123">-Aktion</span><span class="sxs-lookup"><span data-stu-id="0dc96-123">-Action</span></span>
<span data-ttu-id="0dc96-124">"Regel zulassen" oder "Verweigern".</span><span class="sxs-lookup"><span data-stu-id="0dc96-124">Allow or Deny rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: Allow
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc96-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dc96-125">-DefaultProfile</span></span>
<span data-ttu-id="0dc96-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0dc96-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0dc96-127">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0dc96-127">-Description</span></span>
<span data-ttu-id="0dc96-128">Beschreibung der Zugriffsbeschränkung.</span><span class="sxs-lookup"><span data-stu-id="0dc96-128">Access Restriction description.</span></span>

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

### <span data-ttu-id="0dc96-129">-HttpHeader</span><span class="sxs-lookup"><span data-stu-id="0dc96-129">-HttpHeader</span></span>
<span data-ttu-id="0dc96-130">Einschränkungen für http-Header.</span><span class="sxs-lookup"><span data-stu-id="0dc96-130">Http header restrictions.</span></span> <span data-ttu-id="0dc96-131">Beispiel: -HttpHeader @{'x-azure-fdid' = '7acacb02-47ea-4cd4-b568-5e880e72582e'; 'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'}</span><span class="sxs-lookup"><span data-stu-id="0dc96-131">Example: -HttpHeader @{'x-azure-fdid' = '7acacb02-47ea-4cd4-b568-5e880e72582e'; 'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc96-132">-IgnoreMissingServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="0dc96-132">-IgnoreMissingServiceEndpoint</span></span>
<span data-ttu-id="0dc96-133">Geben Sie an, ob die Registrierung des Dienstendpunkts im Subnetz überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="0dc96-133">Specify if Service Endpoint registration at Subnet should be validated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SubnetNameParameterSet, SubnetIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc96-134">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="0dc96-134">-IpAddress</span></span>
<span data-ttu-id="0dc96-135">Ip Address v4 oder v6 CIDR Range.</span><span class="sxs-lookup"><span data-stu-id="0dc96-135">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="0dc96-136">Beispiel: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="0dc96-136">E.g.: 192.168.0.0/24</span></span>

```yaml
Type: System.String
Parameter Sets: IpAddressParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc96-137">-Name</span><span class="sxs-lookup"><span data-stu-id="0dc96-137">-Name</span></span>
<span data-ttu-id="0dc96-138">Regelname</span><span class="sxs-lookup"><span data-stu-id="0dc96-138">Rule Name</span></span>

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

### <span data-ttu-id="0dc96-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0dc96-139">-PassThru</span></span>
<span data-ttu-id="0dc96-140">Geben Sie das Konfigurationsobjekt für Zugriffseinschränkungen zurück.</span><span class="sxs-lookup"><span data-stu-id="0dc96-140">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="0dc96-141">-Priority</span><span class="sxs-lookup"><span data-stu-id="0dc96-141">-Priority</span></span>
<span data-ttu-id="0dc96-142">Priorität der Zugriffseinschränkung.</span><span class="sxs-lookup"><span data-stu-id="0dc96-142">Access Restriction priority.</span></span> <span data-ttu-id="0dc96-143">Beispiel: 500.</span><span class="sxs-lookup"><span data-stu-id="0dc96-143">E.g.: 500.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc96-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dc96-144">-ResourceGroupName</span></span>
<span data-ttu-id="0dc96-145">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="0dc96-145">Resource Group Name</span></span>

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

### <span data-ttu-id="0dc96-146">-ServiceTag</span><span class="sxs-lookup"><span data-stu-id="0dc96-146">-ServiceTag</span></span>
<span data-ttu-id="0dc96-147">Name des Servicetags</span><span class="sxs-lookup"><span data-stu-id="0dc96-147">Name of Service Tag</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceTagParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc96-148">-SlotName</span><span class="sxs-lookup"><span data-stu-id="0dc96-148">-SlotName</span></span>
<span data-ttu-id="0dc96-149">Name des Bereitstellungsplatzes.</span><span class="sxs-lookup"><span data-stu-id="0dc96-149">Deployment Slot name.</span></span>

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

### <span data-ttu-id="0dc96-150">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="0dc96-150">-SubnetId</span></span>
<span data-ttu-id="0dc96-151">ResourceId des Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="0dc96-151">ResourceId of Subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc96-152">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="0dc96-152">-SubnetName</span></span>
<span data-ttu-id="0dc96-153">Name des Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="0dc96-153">Name of Subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc96-154">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="0dc96-154">-TargetScmSite</span></span>
<span data-ttu-id="0dc96-155">Die Regel gilt für die Haupt- oder Scm-Website.</span><span class="sxs-lookup"><span data-stu-id="0dc96-155">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="0dc96-156">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="0dc96-156">-VirtualNetworkName</span></span>
<span data-ttu-id="0dc96-157">Name des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="0dc96-157">Name of Virtual Network.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc96-158">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="0dc96-158">-WebAppName</span></span>
<span data-ttu-id="0dc96-159">Der Name der Web App.</span><span class="sxs-lookup"><span data-stu-id="0dc96-159">The name of the web app.</span></span>

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

### <span data-ttu-id="0dc96-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0dc96-160">-Confirm</span></span>
<span data-ttu-id="0dc96-161">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0dc96-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0dc96-162">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0dc96-162">-WhatIf</span></span>
<span data-ttu-id="0dc96-163">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0dc96-163">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0dc96-164">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0dc96-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0dc96-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dc96-165">CommonParameters</span></span>
<span data-ttu-id="0dc96-166">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dc96-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dc96-167">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0dc96-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dc96-168">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0dc96-168">INPUTS</span></span>

### <span data-ttu-id="0dc96-169">System.String</span><span class="sxs-lookup"><span data-stu-id="0dc96-169">System.String</span></span>

## <span data-ttu-id="0dc96-170">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0dc96-170">OUTPUTS</span></span>

### <span data-ttu-id="0dc96-171">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="0dc96-171">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="0dc96-172">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0dc96-172">NOTES</span></span>

## <span data-ttu-id="0dc96-173">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0dc96-173">RELATED LINKS</span></span>

[<span data-ttu-id="0dc96-174">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="0dc96-174">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="0dc96-175">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="0dc96-175">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="0dc96-176">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="0dc96-176">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
