---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
ms.openlocfilehash: 4d63726f67cb43f34e58c8e560a08adefce5fcbd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459832"
---
# <span data-ttu-id="55a45-101">Update-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="55a45-101">Update-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="55a45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55a45-102">SYNOPSIS</span></span>
<span data-ttu-id="55a45-103">Ändern oder ändern Sie eine Virtual Appliance-Website, die mit einer Network Virtual Appliance-Ressource verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="55a45-103">Change or Modify a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="55a45-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55a45-104">SYNTAX</span></span>

```
Update-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -NetworkVirtualApplianceId <String>
 [-AddresssPrefix <String>] [-O365Policy <PSOffice365PolicyProperties>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55a45-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55a45-105">DESCRIPTION</span></span>
<span data-ttu-id="55a45-106">Mit Update-AzVirtualApplianceSite Befehl wird eine Websiteressource des virtuellen Geräts geändert.</span><span class="sxs-lookup"><span data-stu-id="55a45-106">The Update-AzVirtualApplianceSite command modifies a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="55a45-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="55a45-107">EXAMPLES</span></span>

### <span data-ttu-id="55a45-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="55a45-108">Example 1</span></span>
```powershell
PS C:\> $nva=Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
PS C:\> Update-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -AddresssPrefix 10.0.4.0/24 -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="55a45-109">Ändern Sie das Adresspräfix für eine Virtual Appliance-Websiteressource.</span><span class="sxs-lookup"><span data-stu-id="55a45-109">Modify the address prefix for a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="55a45-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55a45-110">PARAMETERS</span></span>

### <span data-ttu-id="55a45-111">-AddresssPrefix</span><span class="sxs-lookup"><span data-stu-id="55a45-111">-AddresssPrefix</span></span>
<span data-ttu-id="55a45-112">Das Adresspräfix für die Website.</span><span class="sxs-lookup"><span data-stu-id="55a45-112">The address prefix for the site.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55a45-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55a45-113">-AsJob</span></span>
<span data-ttu-id="55a45-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="55a45-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="55a45-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55a45-115">-DefaultProfile</span></span>
<span data-ttu-id="55a45-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="55a45-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55a45-117">-Force</span><span class="sxs-lookup"><span data-stu-id="55a45-117">-Force</span></span>
<span data-ttu-id="55a45-118">Bestätigen Sie sie nicht, wenn Sie eine Ressource überschreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="55a45-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="55a45-119">-Name</span><span class="sxs-lookup"><span data-stu-id="55a45-119">-Name</span></span>
<span data-ttu-id="55a45-120">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="55a45-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55a45-121">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="55a45-121">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="55a45-122">Virtuelles Netzwerkgerät, an das diese Website angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="55a45-122">Network virtual appliance that this site is attached to.</span></span>

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

### <span data-ttu-id="55a45-123">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="55a45-123">-O365Policy</span></span>
<span data-ttu-id="55a45-124">Office 365-Breakoutrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="55a45-124">Office 365 breakout policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55a45-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55a45-125">-ResourceGroupName</span></span>
<span data-ttu-id="55a45-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="55a45-126">The resource group name.</span></span>

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

### <span data-ttu-id="55a45-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="55a45-127">-Tag</span></span>
<span data-ttu-id="55a45-128">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="55a45-128">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="55a45-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55a45-129">-Confirm</span></span>
<span data-ttu-id="55a45-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="55a45-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55a45-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="55a45-131">-WhatIf</span></span>
<span data-ttu-id="55a45-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="55a45-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55a45-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="55a45-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55a45-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55a45-134">CommonParameters</span></span>
<span data-ttu-id="55a45-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55a45-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55a45-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55a45-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55a45-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="55a45-137">INPUTS</span></span>

### <span data-ttu-id="55a45-138">System.String</span><span class="sxs-lookup"><span data-stu-id="55a45-138">System.String</span></span>

### <span data-ttu-id="55a45-139">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="55a45-139">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="55a45-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="55a45-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="55a45-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="55a45-141">OUTPUTS</span></span>

### <span data-ttu-id="55a45-142">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="55a45-142">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="55a45-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="55a45-143">NOTES</span></span>

## <span data-ttu-id="55a45-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="55a45-144">RELATED LINKS</span></span>
