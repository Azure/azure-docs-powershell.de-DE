---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: ad0bdc95ea3d582a2f8b6b6b1f8bc772c795352c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995427"
---
# <span data-ttu-id="4709b-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="4709b-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="4709b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4709b-102">SYNOPSIS</span></span>
<span data-ttu-id="4709b-103">Entfernt eine Zugriffs Einschränkungs Regel aus einer Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="4709b-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="4709b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4709b-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Action <String>] [-TargetScmSite] [-SlotName <String>] [-IpAddress <String>] [-SubnetName <String>]
 [-VirtualNetworkName <String>] [-SubnetId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4709b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4709b-105">DESCRIPTION</span></span>
<span data-ttu-id="4709b-106">Das Cmdlet " **Remove-AzWebAppAccessRestrictionRule** " entfernt eine Zugriffs Einschränkungs Regel aus einer Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="4709b-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="4709b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4709b-107">EXAMPLES</span></span>

### <span data-ttu-id="4709b-108">Beispiel 1: Entfernen einer Einschränkungs Regel für eine Web App-Zugriffsbeschränkung</span><span class="sxs-lookup"><span data-stu-id="4709b-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="4709b-109">Mit diesem Befehl wird die IpRule-Zugriffs Einschränkungs Regel aus Azure Web App mit dem Namen ContosoSite entfernt, die zu der Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="4709b-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="4709b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4709b-110">PARAMETERS</span></span>

### <span data-ttu-id="4709b-111">– Aktion</span><span class="sxs-lookup"><span data-stu-id="4709b-111">-Action</span></span>
<span data-ttu-id="4709b-112">Regel zulassen oder ablehnen.</span><span class="sxs-lookup"><span data-stu-id="4709b-112">Allow or Deny rule.</span></span>

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

### <span data-ttu-id="4709b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4709b-113">-DefaultProfile</span></span>
<span data-ttu-id="4709b-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4709b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4709b-115">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="4709b-115">-IpAddress</span></span>
<span data-ttu-id="4709b-116">IP-Adresse v4 oder V6 CIDR-Bereich.</span><span class="sxs-lookup"><span data-stu-id="4709b-116">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="4709b-117">Z. b.: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="4709b-117">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="4709b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4709b-118">-Name</span></span>
<span data-ttu-id="4709b-119">Name der Zugriffs Beschränkungsregel</span><span class="sxs-lookup"><span data-stu-id="4709b-119">Access Restriction Rule Name</span></span>

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

### <span data-ttu-id="4709b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4709b-120">-PassThru</span></span>
<span data-ttu-id="4709b-121">Gibt das Config-Objekt für die Zugriffsbeschränkung zurück.</span><span class="sxs-lookup"><span data-stu-id="4709b-121">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="4709b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4709b-122">-ResourceGroupName</span></span>
<span data-ttu-id="4709b-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="4709b-123">Resource Group Name</span></span>

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

### <span data-ttu-id="4709b-124">-Slotname</span><span class="sxs-lookup"><span data-stu-id="4709b-124">-SlotName</span></span>
<span data-ttu-id="4709b-125">Name des Bereitstellungs Steckplatzes.</span><span class="sxs-lookup"><span data-stu-id="4709b-125">Deployment Slot Name.</span></span>

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

### <span data-ttu-id="4709b-126">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="4709b-126">-SubnetId</span></span>
<span data-ttu-id="4709b-127">Die Quell-Nr des Subnets.</span><span class="sxs-lookup"><span data-stu-id="4709b-127">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="4709b-128">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="4709b-128">-SubnetName</span></span>
<span data-ttu-id="4709b-129">Name des Subnets.</span><span class="sxs-lookup"><span data-stu-id="4709b-129">Name of Subnet.</span></span>

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

### <span data-ttu-id="4709b-130">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="4709b-130">-TargetScmSite</span></span>
<span data-ttu-id="4709b-131">Regel richtet sich an die Hauptwebsite oder die SCM-Website.</span><span class="sxs-lookup"><span data-stu-id="4709b-131">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="4709b-132">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="4709b-132">-VirtualNetworkName</span></span>
<span data-ttu-id="4709b-133">Name des virtuellen Netzwerks (muss sich in derselben Ressourcengruppe wie Web App befinden).</span><span class="sxs-lookup"><span data-stu-id="4709b-133">Name of Virtual Network (must be in same resource group as Web App).</span></span>

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

### <span data-ttu-id="4709b-134">-Webbasierter</span><span class="sxs-lookup"><span data-stu-id="4709b-134">-WebAppName</span></span>
<span data-ttu-id="4709b-135">Der Name der Web-App.</span><span class="sxs-lookup"><span data-stu-id="4709b-135">The name of the web app.</span></span>

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

### <span data-ttu-id="4709b-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4709b-136">-Confirm</span></span>
<span data-ttu-id="4709b-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4709b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4709b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4709b-138">-WhatIf</span></span>
<span data-ttu-id="4709b-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4709b-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4709b-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4709b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4709b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4709b-141">CommonParameters</span></span>
<span data-ttu-id="4709b-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4709b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4709b-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4709b-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4709b-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4709b-144">INPUTS</span></span>

### <span data-ttu-id="4709b-145">System. String</span><span class="sxs-lookup"><span data-stu-id="4709b-145">System.String</span></span>

## <span data-ttu-id="4709b-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4709b-146">OUTPUTS</span></span>

### <span data-ttu-id="4709b-147">Microsoft. Azure. Commands. webapps. Models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="4709b-147">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="4709b-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="4709b-148">NOTES</span></span>

## <span data-ttu-id="4709b-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4709b-149">RELATED LINKS</span></span>

[<span data-ttu-id="4709b-150">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="4709b-150">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="4709b-151">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="4709b-151">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="4709b-152">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="4709b-152">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)
