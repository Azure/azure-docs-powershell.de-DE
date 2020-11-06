---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVirtualWan.md
ms.openlocfilehash: 3f62cf755ac06efe9ed5f04a6657a36cfe612abe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480266"
---
# <span data-ttu-id="0e97b-101">Update-AzureRmVirtualWan</span><span class="sxs-lookup"><span data-stu-id="0e97b-101">Update-AzureRmVirtualWan</span></span>

## <span data-ttu-id="0e97b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0e97b-102">SYNOPSIS</span></span>
<span data-ttu-id="0e97b-103">Aktualisiert ein Azure Virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="0e97b-103">Updates an Azure Virtual WAN.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e97b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e97b-104">SYNTAX</span></span>

### <span data-ttu-id="0e97b-105">ByVirtualWanName (Standard)</span><span class="sxs-lookup"><span data-stu-id="0e97b-105">ByVirtualWanName (Default)</span></span>
```
Update-AzureRmVirtualWan -ResourceGroupName <String> -Name <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e97b-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="0e97b-106">ByVirtualWanObject</span></span>
```
Update-AzureRmVirtualWan -InputObject <PSVirtualWan> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e97b-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="0e97b-107">ByVirtualWanResourceId</span></span>
```
Update-AzureRmVirtualWan -ResourceId <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e97b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e97b-108">DESCRIPTION</span></span>
<span data-ttu-id="0e97b-109">Aktualisiert ein Azure Virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="0e97b-109">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="0e97b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0e97b-110">EXAMPLES</span></span>

### <span data-ttu-id="0e97b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0e97b-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> Update-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -AllowBranchToBranchTraffic $true -AllowVnetToVnetTraffic $false

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="0e97b-112">Das obige wird eine Ressourcengruppe "testRG" in der Region "West US" und ein Azure Virtual WAN in dieser Ressourcengruppe in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="0e97b-112">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN in that resource group in Azure.</span></span> <span data-ttu-id="0e97b-113">VirtualWan wird mit neuen Eigenschaften aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0e97b-113">VirtualWan is updated with new properties.</span></span>

## <span data-ttu-id="0e97b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e97b-114">PARAMETERS</span></span>

### <span data-ttu-id="0e97b-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="0e97b-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="0e97b-116">Branch-to-Branch-Datenverkehr für VirtualWan zulassen</span><span class="sxs-lookup"><span data-stu-id="0e97b-116">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="0e97b-117">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="0e97b-117">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="0e97b-118">Erlauben Sie vnet den vnet-Datenverkehr für VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="0e97b-118">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="0e97b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e97b-119">-AsJob</span></span>
<span data-ttu-id="0e97b-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0e97b-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0e97b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e97b-121">-DefaultProfile</span></span>
<span data-ttu-id="0e97b-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0e97b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e97b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="0e97b-123">-Force</span></span>
<span data-ttu-id="0e97b-124">Keine Bestätigung anfordern, wenn Sie eine Ressource overriten möchten</span><span class="sxs-lookup"><span data-stu-id="0e97b-124">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="0e97b-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0e97b-125">-InputObject</span></span>
<span data-ttu-id="0e97b-126">Das zu ändernde virtuelle WAN-Objekt</span><span class="sxs-lookup"><span data-stu-id="0e97b-126">The virtual wan object to be modified</span></span>

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

### <span data-ttu-id="0e97b-127">-Name</span><span class="sxs-lookup"><span data-stu-id="0e97b-127">-Name</span></span>
<span data-ttu-id="0e97b-128">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="0e97b-128">The resource name.</span></span>

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

### <span data-ttu-id="0e97b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e97b-129">-ResourceGroupName</span></span>
<span data-ttu-id="0e97b-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0e97b-130">The resource group name.</span></span>

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

### <span data-ttu-id="0e97b-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0e97b-131">-ResourceId</span></span>
<span data-ttu-id="0e97b-132">Die Azure-Ressourcen-ID für das virtuelle WAN.</span><span class="sxs-lookup"><span data-stu-id="0e97b-132">The Azure resource ID for the virtual wan.</span></span>

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

### <span data-ttu-id="0e97b-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="0e97b-133">-Tag</span></span>
<span data-ttu-id="0e97b-134">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="0e97b-134">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="0e97b-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0e97b-135">-Confirm</span></span>
<span data-ttu-id="0e97b-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0e97b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e97b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e97b-137">-WhatIf</span></span>
<span data-ttu-id="0e97b-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0e97b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e97b-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0e97b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e97b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e97b-140">CommonParameters</span></span>
<span data-ttu-id="0e97b-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e97b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e97b-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e97b-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e97b-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0e97b-143">INPUTS</span></span>

### <span data-ttu-id="0e97b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="0e97b-144">System.String</span></span>

### <span data-ttu-id="0e97b-145">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="0e97b-145">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="0e97b-146">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0e97b-146">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0e97b-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0e97b-147">OUTPUTS</span></span>

### <span data-ttu-id="0e97b-148">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="0e97b-148">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="0e97b-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="0e97b-149">NOTES</span></span>

## <span data-ttu-id="0e97b-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0e97b-150">RELATED LINKS</span></span>
