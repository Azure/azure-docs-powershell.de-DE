---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: b28cb8ac408ff281930eac68bf2b97d288150dd6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934584"
---
# <span data-ttu-id="6e3a0-101">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="6e3a0-101">Add-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="6e3a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e3a0-102">SYNOPSIS</span></span>
<span data-ttu-id="6e3a0-103">Fügt einer Azure Web App eine Access-Restiction-Regel hinzu.</span><span class="sxs-lookup"><span data-stu-id="6e3a0-103">Adds an Access Restiction rule to an Azure Web App.</span></span>

## <span data-ttu-id="6e3a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6e3a0-104">SYNTAX</span></span>

### <span data-ttu-id="6e3a0-105">IpAddressParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6e3a0-105">IpAddressParameterSet (Default)</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -IpAddress <String> [-PassThru] [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e3a0-106">ServiceTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e3a0-106">ServiceTagParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 [-PassThru] -ServiceTag <String> [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e3a0-107">SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e3a0-107">SubnetNameParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetName <String> -VirtualNetworkName <String> [-IgnoreMissingServiceEndpoint] [-PassThru]
 [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e3a0-108">SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e3a0-108">SubnetIdParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetId <String> [-IgnoreMissingServiceEndpoint] [-PassThru] [-HttpHeader <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e3a0-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6e3a0-109">DESCRIPTION</span></span>
<span data-ttu-id="6e3a0-110">Das **Cmdlet Add-AzWebAppAccessRestrictionRule** fügt einer Azure Web App eine Zugriffseinschränkungsregel hinzu.</span><span class="sxs-lookup"><span data-stu-id="6e3a0-110">The **Add-AzWebAppAccessRestrictionRule** cmdlet adds an Access Restriction rule to an Azure Web App.</span></span>

## <span data-ttu-id="6e3a0-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6e3a0-111">EXAMPLES</span></span>

### <span data-ttu-id="6e3a0-112">Beispiel 1: Hinzufügen einer IpAddress-Zugriffseinschränkungsregel zu einer Web App</span><span class="sxs-lookup"><span data-stu-id="6e3a0-112">Example 1: Add IpAddress Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name IpRule -Priority 200 -Action Allow -IpAddress 10.10.0.0/8
```

<span data-ttu-id="6e3a0-113">Mit diesem Befehl wird einer Web App mit dem Namen ContosoSite, die zur Ressourcengruppe Default-Web-WestUS gehört, eine Zugriffseinschränkungsregel mit Priorität 200 und ip-Bereich hinzu.</span><span class="sxs-lookup"><span data-stu-id="6e3a0-113">This command adds an access restriction rule with priority 200 and ip range to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="6e3a0-114">Beispiel 2: Hinzufügen einer Einschränkungsregel für den Endpunktzugriff für Subnetzdienste zu einer Web App</span><span class="sxs-lookup"><span data-stu-id="6e3a0-114">Example 2: Add Subnet Service Endpoint Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name SubnetRule -Priority 300 -Action Allow -SubnetName appgw-subnet -VirtualNetworkName corp-vnet
```

<span data-ttu-id="6e3a0-115">Dieser Befehl fügt einer Web App mit dem Namen ContosoSite, die zur Ressourcengruppe Default-Web-WestUS gehört, eine Zugriffseinschränkungsregel mit Der Priorität 300 und dem Subnetz-Appgw-Subnetz in corp-vnet hinzu.</span><span class="sxs-lookup"><span data-stu-id="6e3a0-115">This command adds an access restriction rule with priority 300 and with subnet appgw-subnet in corp-vnet to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="6e3a0-116">Beispiel 3: Hinzufügen einer ServiceTag-Zugriffseinschränkungsregel zu einer Web App</span><span class="sxs-lookup"><span data-stu-id="6e3a0-116">Example 3: Add ServiceTag Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name ServiceTagRule -Priority 200 -Action Allow -ServiceTag AzureFrontDoor.Backend
```

<span data-ttu-id="6e3a0-117">Dieser Befehl fügt einer Web App mit dem Namen ContosoSite, die zur Ressourcengruppe Default-Web-WestUS gehört, eine Zugriffseinschränkungsregel mit Priorität 200 und ein Diensttag hinzu, das den IP-Bereich von Azure Front Door darstellt.</span><span class="sxs-lookup"><span data-stu-id="6e3a0-117">This command adds an access restriction rule with priority 200 and a Service Tag representing the ip scope of Azure Front Door to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="6e3a0-118">Beispiel 4: Hinzufügen einer Zugriffseinschränkungsregel mit mehreren Adressen zu einer Web App</span><span class="sxs-lookup"><span data-stu-id="6e3a0-118">Example 4: Add multi-address Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name MultipleIpRule -Priority 200 -Action Allow -IpAddress "10.10.0.0/8,192.168.0.0/16"
```

<span data-ttu-id="6e3a0-119">Dieser Befehl fügt einer Web App mit dem Namen ContosoSite, die zur Ressourcengruppe Default-Web-WestUS gehört, eine Zugriffseinschränkungsregel mit Priorität 200 und zwei IP-Bereichen hinzu.</span><span class="sxs-lookup"><span data-stu-id="6e3a0-119">This command adds an access restriction rule with priority 200 and two ip ranges to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="6e3a0-120">Beispiel 5: Hinzufügen einer Zugriffseinschränkungsregel mit http-Header zu einer Web App</span><span class="sxs-lookup"><span data-stu-id="6e3a0-120">Example 5: Add Access Restriction rule with http header to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name MultipleIpRule -Priority 400 -Action Allow -ServiceTag AzureFrontDoor.Backend
-HttpHeader @{'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'; 'x-azure-fdid' = '355deb06-47c4-4ba4-9641-c7d7a98b913e'}
```

<span data-ttu-id="6e3a0-121">Dieser Befehl fügt eine Zugriffseinschränkungsregel mit der Priorität 400 für Diensttag AzureFrontDoor.Back-End hinzu und schränkt den Zugriff nur auf http-Header bestimmter Werte zu einer Web App namens ContosoSite ein, die zur Ressourcengruppe Default-Web-WestUS gehört.</span><span class="sxs-lookup"><span data-stu-id="6e3a0-121">This command adds an access restriction rule with priority 400 for Service Tag AzureFrontDoor.Backend and further restricts access only to http headers of certain values to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="6e3a0-122">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6e3a0-122">PARAMETERS</span></span>

### <span data-ttu-id="6e3a0-123">-Aktion</span><span class="sxs-lookup"><span data-stu-id="6e3a0-123">-Action</span></span>
<span data-ttu-id="6e3a0-124">Regel zulassen oder verweigern</span><span class="sxs-lookup"><span data-stu-id="6e3a0-124">Allow or Deny rule.</span></span>

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

### <span data-ttu-id="6e3a0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e3a0-125">-DefaultProfile</span></span>
<span data-ttu-id="6e3a0-126">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6e3a0-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e3a0-127">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e3a0-127">-Description</span></span>
<span data-ttu-id="6e3a0-128">Beschreibung der Zugriffseinschränkung.</span><span class="sxs-lookup"><span data-stu-id="6e3a0-128">Access Restriction description.</span></span>

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

### <span data-ttu-id="6e3a0-129">-HttpHeader</span><span class="sxs-lookup"><span data-stu-id="6e3a0-129">-HttpHeader</span></span>
<span data-ttu-id="6e3a0-130">Http-Headereinschränkungen.</span><span class="sxs-lookup"><span data-stu-id="6e3a0-130">Http header restrictions.</span></span> <span data-ttu-id="6e3a0-131">Beispiel: -HttpHeader @{'x-azure-fdid' = '7acacb02-47ea-4cd4-b568-5e880e72582e'; 'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'}</span><span class="sxs-lookup"><span data-stu-id="6e3a0-131">Example: -HttpHeader @{'x-azure-fdid' = '7acacb02-47ea-4cd4-b568-5e880e72582e'; 'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'}</span></span>

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

### <span data-ttu-id="6e3a0-132">-IgnoreMissingServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="6e3a0-132">-IgnoreMissingServiceEndpoint</span></span>
<span data-ttu-id="6e3a0-133">Geben Sie an, ob die Dienstendpunktregistrierung im Subnetz überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="6e3a0-133">Specify if Service Endpoint registration at Subnet should be validated.</span></span>

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

### <span data-ttu-id="6e3a0-134">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="6e3a0-134">-IpAddress</span></span>
<span data-ttu-id="6e3a0-135">Ip-Adresse v4 oder v6 CIDR-Bereich.</span><span class="sxs-lookup"><span data-stu-id="6e3a0-135">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="6e3a0-136">Beispiel: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="6e3a0-136">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="6e3a0-137">-Name</span><span class="sxs-lookup"><span data-stu-id="6e3a0-137">-Name</span></span>
<span data-ttu-id="6e3a0-138">Regelname</span><span class="sxs-lookup"><span data-stu-id="6e3a0-138">Rule Name</span></span>

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

### <span data-ttu-id="6e3a0-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e3a0-139">-PassThru</span></span>
<span data-ttu-id="6e3a0-140">Geben Sie das Konfigurationsobjekt für Zugriffseinschränkungen zurück.</span><span class="sxs-lookup"><span data-stu-id="6e3a0-140">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="6e3a0-141">-Priorität</span><span class="sxs-lookup"><span data-stu-id="6e3a0-141">-Priority</span></span>
<span data-ttu-id="6e3a0-142">Zugriffseinschränkungspriorität.</span><span class="sxs-lookup"><span data-stu-id="6e3a0-142">Access Restriction priority.</span></span> <span data-ttu-id="6e3a0-143">Beispiel: 500.</span><span class="sxs-lookup"><span data-stu-id="6e3a0-143">E.g.: 500.</span></span>

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

### <span data-ttu-id="6e3a0-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e3a0-144">-ResourceGroupName</span></span>
<span data-ttu-id="6e3a0-145">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="6e3a0-145">Resource Group Name</span></span>

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

### <span data-ttu-id="6e3a0-146">-ServiceTag</span><span class="sxs-lookup"><span data-stu-id="6e3a0-146">-ServiceTag</span></span>
<span data-ttu-id="6e3a0-147">Name des Servicetags</span><span class="sxs-lookup"><span data-stu-id="6e3a0-147">Name of Service Tag</span></span>

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

### <span data-ttu-id="6e3a0-148">-SlotName</span><span class="sxs-lookup"><span data-stu-id="6e3a0-148">-SlotName</span></span>
<span data-ttu-id="6e3a0-149">Name des Bereitstellungsplatzes.</span><span class="sxs-lookup"><span data-stu-id="6e3a0-149">Deployment Slot name.</span></span>

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

### <span data-ttu-id="6e3a0-150">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="6e3a0-150">-SubnetId</span></span>
<span data-ttu-id="6e3a0-151">ResourceId des Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="6e3a0-151">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="6e3a0-152">-Subnetzname</span><span class="sxs-lookup"><span data-stu-id="6e3a0-152">-SubnetName</span></span>
<span data-ttu-id="6e3a0-153">Name des Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="6e3a0-153">Name of Subnet.</span></span>

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

### <span data-ttu-id="6e3a0-154">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="6e3a0-154">-TargetScmSite</span></span>
<span data-ttu-id="6e3a0-155">Regel richtet sich an die Hauptwebsite oder Scm-Website.</span><span class="sxs-lookup"><span data-stu-id="6e3a0-155">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="6e3a0-156">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="6e3a0-156">-VirtualNetworkName</span></span>
<span data-ttu-id="6e3a0-157">Name des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="6e3a0-157">Name of Virtual Network.</span></span>

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

### <span data-ttu-id="6e3a0-158">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="6e3a0-158">-WebAppName</span></span>
<span data-ttu-id="6e3a0-159">Der Name der Web App.</span><span class="sxs-lookup"><span data-stu-id="6e3a0-159">The name of the web app.</span></span>

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

### <span data-ttu-id="6e3a0-160">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6e3a0-160">-Confirm</span></span>
<span data-ttu-id="6e3a0-161">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6e3a0-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e3a0-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e3a0-162">-WhatIf</span></span>
<span data-ttu-id="6e3a0-163">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6e3a0-163">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6e3a0-164">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6e3a0-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e3a0-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e3a0-165">CommonParameters</span></span>
<span data-ttu-id="6e3a0-166">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e3a0-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e3a0-167">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e3a0-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e3a0-168">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6e3a0-168">INPUTS</span></span>

### <span data-ttu-id="6e3a0-169">System.String</span><span class="sxs-lookup"><span data-stu-id="6e3a0-169">System.String</span></span>

## <span data-ttu-id="6e3a0-170">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6e3a0-170">OUTPUTS</span></span>

### <span data-ttu-id="6e3a0-171">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="6e3a0-171">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="6e3a0-172">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6e3a0-172">NOTES</span></span>

## <span data-ttu-id="6e3a0-173">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6e3a0-173">RELATED LINKS</span></span>

[<span data-ttu-id="6e3a0-174">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="6e3a0-174">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="6e3a0-175">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="6e3a0-175">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="6e3a0-176">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="6e3a0-176">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
