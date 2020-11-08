---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: 0abad2b3d38a5f614222a8eda7e3c27b9fda9556
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167157"
---
# <span data-ttu-id="a5d1f-101">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="a5d1f-101">Add-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="a5d1f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a5d1f-102">SYNOPSIS</span></span>
<span data-ttu-id="a5d1f-103">Fügt eine Access-Restiction-Regel zu einer Azure Web App hinzu.</span><span class="sxs-lookup"><span data-stu-id="a5d1f-103">Adds an Access Restiction rule to an Azure Web App.</span></span>

## <span data-ttu-id="a5d1f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5d1f-104">SYNTAX</span></span>

### <span data-ttu-id="a5d1f-105">IpAddressParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a5d1f-105">IpAddressParameterSet (Default)</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -IpAddress <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5d1f-106">SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5d1f-106">SubnetNameParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetName <String> -VirtualNetworkName <String> [-IgnoreMissingServiceEndpoint] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5d1f-107">SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5d1f-107">SubnetIdParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetId <String> [-IgnoreMissingServiceEndpoint] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5d1f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5d1f-108">DESCRIPTION</span></span>
<span data-ttu-id="a5d1f-109">Mit dem Cmdlet **Add-AzWebAppAccessRestrictionRule** wird eine Zugriffs Einschränkungs Regel zu einer Azure Web App hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a5d1f-109">The **Add-AzWebAppAccessRestrictionRule** cmdlet adds an Access Restriction rule to an Azure Web App.</span></span>

## <span data-ttu-id="a5d1f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5d1f-110">EXAMPLES</span></span>

### <span data-ttu-id="a5d1f-111">Beispiel 1: Hinzufügen einer IP-Zugriffs Beschränkungsregel zu einer Web-App</span><span class="sxs-lookup"><span data-stu-id="a5d1f-111">Example 1: Add IpAddress Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name IpRule -Priority 200 -Action Allow -IpAddress 10.10.0.0/8
```

<span data-ttu-id="a5d1f-112">Mit diesem Befehl wird eine Zugriffs Einschränkungs Regel mit der Priorität 200 und dem IP-Bereich zu einer Web-App mit dem Namen ContosoSite hinzugefügt, die zur Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="a5d1f-112">This command adds an access restriction rule with priority 200 and ip range to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="a5d1f-113">Beispiel 2: Hinzufügen einer Einschränkungs Regel für den Subnetzdienst-Endpunkt zu einer Web-App</span><span class="sxs-lookup"><span data-stu-id="a5d1f-113">Example 2: Add Subnet Service Endpoint Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name SubnetRule -Priority 300 -Action Allow -SubnetName appgw-subnet -VirtualNetworkName corp-vnet
```

<span data-ttu-id="a5d1f-114">Dieser Befehl fügt eine Zugriffs Einschränkungs Regel mit der Priorität 300 und dem Subnetz appgw-Subnetz in Corp-vnet zu einer Web-App mit dem Namen ContosoSite hinzu, die zu der Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="a5d1f-114">This command adds an access restriction rule with priority 300 and with subnet appgw-subnet in corp-vnet to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="a5d1f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5d1f-115">PARAMETERS</span></span>

### <span data-ttu-id="a5d1f-116">– Aktion</span><span class="sxs-lookup"><span data-stu-id="a5d1f-116">-Action</span></span>
<span data-ttu-id="a5d1f-117">Regel zulassen oder ablehnen.</span><span class="sxs-lookup"><span data-stu-id="a5d1f-117">Allow or Deny rule.</span></span>

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

### <span data-ttu-id="a5d1f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5d1f-118">-DefaultProfile</span></span>
<span data-ttu-id="a5d1f-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a5d1f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5d1f-120">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5d1f-120">-Description</span></span>
<span data-ttu-id="a5d1f-121">Beschreibung der Zugriffseinschränkung</span><span class="sxs-lookup"><span data-stu-id="a5d1f-121">Access Restriction description.</span></span>

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

### <span data-ttu-id="a5d1f-122">-IgnoreMissingServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="a5d1f-122">-IgnoreMissingServiceEndpoint</span></span>
<span data-ttu-id="a5d1f-123">Geben Sie an, ob die Dienstendpunkt Registrierung im Subnetz überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="a5d1f-123">Specify if Service Endpoint registration at Subnet should be validated.</span></span>

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

### <span data-ttu-id="a5d1f-124">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="a5d1f-124">-IpAddress</span></span>
<span data-ttu-id="a5d1f-125">IP-Adresse v4 oder V6 CIDR-Bereich.</span><span class="sxs-lookup"><span data-stu-id="a5d1f-125">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="a5d1f-126">Z. b.: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="a5d1f-126">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="a5d1f-127">-Name</span><span class="sxs-lookup"><span data-stu-id="a5d1f-127">-Name</span></span>
<span data-ttu-id="a5d1f-128">Regelname</span><span class="sxs-lookup"><span data-stu-id="a5d1f-128">Rule Name</span></span>

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

### <span data-ttu-id="a5d1f-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5d1f-129">-PassThru</span></span>
<span data-ttu-id="a5d1f-130">Gibt das Config-Objekt für die Zugriffsbeschränkung zurück.</span><span class="sxs-lookup"><span data-stu-id="a5d1f-130">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="a5d1f-131">-Priorität</span><span class="sxs-lookup"><span data-stu-id="a5d1f-131">-Priority</span></span>
<span data-ttu-id="a5d1f-132">Zugriffs Beschränkungs Priorität.</span><span class="sxs-lookup"><span data-stu-id="a5d1f-132">Access Restriction priority.</span></span> <span data-ttu-id="a5d1f-133">Beispiel: 500.</span><span class="sxs-lookup"><span data-stu-id="a5d1f-133">E.g.: 500.</span></span>

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

### <span data-ttu-id="a5d1f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5d1f-134">-ResourceGroupName</span></span>
<span data-ttu-id="a5d1f-135">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="a5d1f-135">Resource Group Name</span></span>

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

### <span data-ttu-id="a5d1f-136">-Slotname</span><span class="sxs-lookup"><span data-stu-id="a5d1f-136">-SlotName</span></span>
<span data-ttu-id="a5d1f-137">Name des Bereitstellungs Steckplatzes.</span><span class="sxs-lookup"><span data-stu-id="a5d1f-137">Deployment Slot name.</span></span>

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

### <span data-ttu-id="a5d1f-138">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="a5d1f-138">-SubnetId</span></span>
<span data-ttu-id="a5d1f-139">Die Quell-Nr des Subnets.</span><span class="sxs-lookup"><span data-stu-id="a5d1f-139">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="a5d1f-140">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="a5d1f-140">-SubnetName</span></span>
<span data-ttu-id="a5d1f-141">Name des Subnets.</span><span class="sxs-lookup"><span data-stu-id="a5d1f-141">Name of Subnet.</span></span>

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

### <span data-ttu-id="a5d1f-142">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="a5d1f-142">-TargetScmSite</span></span>
<span data-ttu-id="a5d1f-143">Regel richtet sich an die Hauptwebsite oder die SCM-Website.</span><span class="sxs-lookup"><span data-stu-id="a5d1f-143">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="a5d1f-144">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="a5d1f-144">-VirtualNetworkName</span></span>
<span data-ttu-id="a5d1f-145">Name des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="a5d1f-145">Name of Virtual Network.</span></span>

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

### <span data-ttu-id="a5d1f-146">-Webbasierter</span><span class="sxs-lookup"><span data-stu-id="a5d1f-146">-WebAppName</span></span>
<span data-ttu-id="a5d1f-147">Der Name der Web-App.</span><span class="sxs-lookup"><span data-stu-id="a5d1f-147">The name of the web app.</span></span>

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

### <span data-ttu-id="a5d1f-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a5d1f-148">-Confirm</span></span>
<span data-ttu-id="a5d1f-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a5d1f-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5d1f-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5d1f-150">-WhatIf</span></span>
<span data-ttu-id="a5d1f-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a5d1f-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5d1f-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a5d1f-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5d1f-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5d1f-153">CommonParameters</span></span>
<span data-ttu-id="a5d1f-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5d1f-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5d1f-155">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5d1f-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5d1f-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a5d1f-156">INPUTS</span></span>

### <span data-ttu-id="a5d1f-157">System. String</span><span class="sxs-lookup"><span data-stu-id="a5d1f-157">System.String</span></span>

## <span data-ttu-id="a5d1f-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a5d1f-158">OUTPUTS</span></span>

### <span data-ttu-id="a5d1f-159">Microsoft. Azure. Commands. webapps. Models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="a5d1f-159">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="a5d1f-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="a5d1f-160">NOTES</span></span>

## <span data-ttu-id="a5d1f-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a5d1f-161">RELATED LINKS</span></span>

[<span data-ttu-id="a5d1f-162">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="a5d1f-162">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="a5d1f-163">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="a5d1f-163">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="a5d1f-164">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="a5d1f-164">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
