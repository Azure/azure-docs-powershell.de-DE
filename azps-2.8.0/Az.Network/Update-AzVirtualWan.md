---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
ms.openlocfilehash: b5486b5ae88555305c1b0e5672fb2ebc3af07103
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823696"
---
# <span data-ttu-id="cdcaf-101">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="cdcaf-101">Update-AzVirtualWan</span></span>

## <span data-ttu-id="cdcaf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cdcaf-102">SYNOPSIS</span></span>
<span data-ttu-id="cdcaf-103">Aktualisiert ein Azure Virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="cdcaf-103">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="cdcaf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cdcaf-104">SYNTAX</span></span>

### <span data-ttu-id="cdcaf-105">ByVirtualWanName (Standard)</span><span class="sxs-lookup"><span data-stu-id="cdcaf-105">ByVirtualWanName (Default)</span></span>
```
Update-AzVirtualWan -ResourceGroupName <String> -Name <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdcaf-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="cdcaf-106">ByVirtualWanObject</span></span>
```
Update-AzVirtualWan -InputObject <PSVirtualWan> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdcaf-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="cdcaf-107">ByVirtualWanResourceId</span></span>
```
Update-AzVirtualWan -ResourceId <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdcaf-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cdcaf-108">DESCRIPTION</span></span>
<span data-ttu-id="cdcaf-109">Aktualisiert ein Azure Virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="cdcaf-109">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="cdcaf-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cdcaf-110">EXAMPLES</span></span>

### <span data-ttu-id="cdcaf-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cdcaf-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> Update-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -AllowBranchToBranchTraffic $true -AllowVnetToVnetTraffic $false

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="cdcaf-112">Das obige wird eine Ressourcengruppe "testRG" in der Region "West US" und ein Azure Virtual WAN in dieser Ressourcengruppe in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="cdcaf-112">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN in that resource group in Azure.</span></span> <span data-ttu-id="cdcaf-113">VirtualWan wird mit neuen Eigenschaften aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cdcaf-113">VirtualWan is updated with new properties.</span></span>

## <span data-ttu-id="cdcaf-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="cdcaf-114">PARAMETERS</span></span>

### <span data-ttu-id="cdcaf-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="cdcaf-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="cdcaf-116">Branch-to-Branch-Datenverkehr für VirtualWan zulassen</span><span class="sxs-lookup"><span data-stu-id="cdcaf-116">Allow branch to branch traffic for VirtualWan.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdcaf-117">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="cdcaf-117">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="cdcaf-118">Erlauben Sie vnet den vnet-Datenverkehr für VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="cdcaf-118">Allow vnet to vnet traffic for VirtualWan.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdcaf-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cdcaf-119">-AsJob</span></span>
<span data-ttu-id="cdcaf-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="cdcaf-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cdcaf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdcaf-121">-DefaultProfile</span></span>
<span data-ttu-id="cdcaf-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cdcaf-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdcaf-123">-Force</span><span class="sxs-lookup"><span data-stu-id="cdcaf-123">-Force</span></span>
<span data-ttu-id="cdcaf-124">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="cdcaf-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="cdcaf-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cdcaf-125">-InputObject</span></span>
<span data-ttu-id="cdcaf-126">Das zu ändernde virtuelle WAN-Objekt</span><span class="sxs-lookup"><span data-stu-id="cdcaf-126">The virtual wan object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cdcaf-127">-Name</span><span class="sxs-lookup"><span data-stu-id="cdcaf-127">-Name</span></span>
<span data-ttu-id="cdcaf-128">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="cdcaf-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdcaf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdcaf-129">-ResourceGroupName</span></span>
<span data-ttu-id="cdcaf-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cdcaf-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdcaf-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="cdcaf-131">-ResourceId</span></span>
<span data-ttu-id="cdcaf-132">Die Azure-Ressourcen-ID für das virtuelle WAN.</span><span class="sxs-lookup"><span data-stu-id="cdcaf-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdcaf-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="cdcaf-133">-Tag</span></span>
<span data-ttu-id="cdcaf-134">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="cdcaf-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="cdcaf-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cdcaf-135">-Confirm</span></span>
<span data-ttu-id="cdcaf-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cdcaf-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdcaf-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdcaf-137">-WhatIf</span></span>
<span data-ttu-id="cdcaf-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cdcaf-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdcaf-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cdcaf-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdcaf-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdcaf-140">CommonParameters</span></span>
<span data-ttu-id="cdcaf-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdcaf-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdcaf-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdcaf-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdcaf-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cdcaf-143">INPUTS</span></span>

### <span data-ttu-id="cdcaf-144">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="cdcaf-144">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="cdcaf-145">System. String</span><span class="sxs-lookup"><span data-stu-id="cdcaf-145">System.String</span></span>

## <span data-ttu-id="cdcaf-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cdcaf-146">OUTPUTS</span></span>

### <span data-ttu-id="cdcaf-147">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="cdcaf-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="cdcaf-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="cdcaf-148">NOTES</span></span>

## <span data-ttu-id="cdcaf-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cdcaf-149">RELATED LINKS</span></span>

[<span data-ttu-id="cdcaf-150">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="cdcaf-150">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="cdcaf-151">Neu – AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="cdcaf-151">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="cdcaf-152">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="cdcaf-152">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)
