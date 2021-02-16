---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
ms.openlocfilehash: 9ac7885cc81744914599308c20bf3350642fc967
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160801"
---
# <span data-ttu-id="78bfb-101">New-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="78bfb-101">New-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="78bfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78bfb-102">SYNOPSIS</span></span>
<span data-ttu-id="78bfb-103">Erstellen Sie eine Website, die mit einer virtuellen Network Appliance verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="78bfb-103">Create a site connected to a Network Virtual Appliance.</span></span>

## <span data-ttu-id="78bfb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="78bfb-104">SYNTAX</span></span>

### <span data-ttu-id="78bfb-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="78bfb-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78bfb-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78bfb-106">ResourceIdParameterSet</span></span>
```
New-AzVirtualApplianceSite -ResourceId <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78bfb-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="78bfb-107">DESCRIPTION</span></span>
<span data-ttu-id="78bfb-108">Mit New-AzVirtualApplianceSite Befehl wird eine Virtual Appliance-Website erstellt, die mit einer Network Virtual Appliance-Ressource verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="78bfb-108">The New-AzVirtualApplianceSite command creates a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="78bfb-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="78bfb-109">EXAMPLES</span></span>

### <span data-ttu-id="78bfb-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="78bfb-110">Example 1</span></span>
```powershell
PS C:\> $nva = Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva 
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize
PS C:\> $site = New-AzVirtualApplianceSite -ResourceGroupName testrg -Name testsite -NetworkVirtualApplianceId $nva.Id -AddressPrefix 10.0.1.0/24 -O365Policy $o365Policy
```

<span data-ttu-id="78bfb-111">Erstellen Sie eine neue Virtual Appliance-Website in der Ressourcengruppe: testrg.</span><span class="sxs-lookup"><span data-stu-id="78bfb-111">Create a new Virtual Appliance site in the resource group: testrg.</span></span>

## <span data-ttu-id="78bfb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78bfb-112">PARAMETERS</span></span>

### <span data-ttu-id="78bfb-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="78bfb-113">-AddressPrefix</span></span>
<span data-ttu-id="78bfb-114">Das Adresspräfix für die Website.</span><span class="sxs-lookup"><span data-stu-id="78bfb-114">The address prefix for the site.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78bfb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78bfb-115">-AsJob</span></span>
<span data-ttu-id="78bfb-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="78bfb-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="78bfb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78bfb-117">-DefaultProfile</span></span>
<span data-ttu-id="78bfb-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="78bfb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78bfb-119">-Force</span><span class="sxs-lookup"><span data-stu-id="78bfb-119">-Force</span></span>
<span data-ttu-id="78bfb-120">Bestätigen Sie nicht, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="78bfb-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="78bfb-121">-Name</span><span class="sxs-lookup"><span data-stu-id="78bfb-121">-Name</span></span>
<span data-ttu-id="78bfb-122">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="78bfb-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78bfb-123">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="78bfb-123">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="78bfb-124">Das virtuelle Netzwerkgerät, dem diese Website zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="78bfb-124">The Network virtual appliance that this site is attached to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78bfb-125">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="78bfb-125">-O365Policy</span></span>
<span data-ttu-id="78bfb-126">Die Office 365-Halterichtlinie.</span><span class="sxs-lookup"><span data-stu-id="78bfb-126">The Office 365 breakout policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78bfb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78bfb-127">-ResourceGroupName</span></span>
<span data-ttu-id="78bfb-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="78bfb-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78bfb-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78bfb-129">-ResourceId</span></span>
<span data-ttu-id="78bfb-130">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="78bfb-130">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78bfb-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="78bfb-131">-Tag</span></span>
<span data-ttu-id="78bfb-132">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="78bfb-132">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78bfb-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78bfb-133">-Confirm</span></span>
<span data-ttu-id="78bfb-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="78bfb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78bfb-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="78bfb-135">-WhatIf</span></span>
<span data-ttu-id="78bfb-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="78bfb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78bfb-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="78bfb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78bfb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78bfb-138">CommonParameters</span></span>
<span data-ttu-id="78bfb-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78bfb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78bfb-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78bfb-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78bfb-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="78bfb-141">INPUTS</span></span>

### <span data-ttu-id="78bfb-142">System.String</span><span class="sxs-lookup"><span data-stu-id="78bfb-142">System.String</span></span>

### <span data-ttu-id="78bfb-143">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="78bfb-143">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="78bfb-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="78bfb-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="78bfb-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="78bfb-145">OUTPUTS</span></span>

### <span data-ttu-id="78bfb-146">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="78bfb-146">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="78bfb-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="78bfb-147">NOTES</span></span>

## <span data-ttu-id="78bfb-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="78bfb-148">RELATED LINKS</span></span>
