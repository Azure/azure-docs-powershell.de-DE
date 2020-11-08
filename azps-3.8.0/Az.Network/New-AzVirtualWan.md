---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
ms.openlocfilehash: 75b729437599f66be567229a1899028e628079fc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003426"
---
# <span data-ttu-id="bf9ab-101">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="bf9ab-101">New-AzVirtualWan</span></span>

## <span data-ttu-id="bf9ab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bf9ab-102">SYNOPSIS</span></span>
<span data-ttu-id="bf9ab-103">Erstellt ein Azure-virtuelles WAN.</span><span class="sxs-lookup"><span data-stu-id="bf9ab-103">Creates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="bf9ab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf9ab-104">SYNTAX</span></span>

```
New-AzVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-VirtualWANType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf9ab-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf9ab-105">DESCRIPTION</span></span>
<span data-ttu-id="bf9ab-106">Erstellt eine neue Azure VirtualWAN-Ressource.</span><span class="sxs-lookup"><span data-stu-id="bf9ab-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="bf9ab-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bf9ab-107">EXAMPLES</span></span>

### <span data-ttu-id="bf9ab-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bf9ab-108">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
VirtualWANType             : Standard
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="bf9ab-109">Im obigen Abschnitt wird eine Ressourcengruppe "testRG" in der Region "West US" und ein Azure Virtual WAN mit Branch to Branch-Datenverkehr, der in dieser Ressourcengruppe in Azure zulässig ist, erstellt.</span><span class="sxs-lookup"><span data-stu-id="bf9ab-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="bf9ab-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf9ab-110">PARAMETERS</span></span>

### <span data-ttu-id="bf9ab-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="bf9ab-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="bf9ab-112">Branch-to-Branch-Datenverkehr für VirtualWan zulassen</span><span class="sxs-lookup"><span data-stu-id="bf9ab-112">Allow branch to branch traffic for VirtualWan.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9ab-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="bf9ab-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="bf9ab-114">Erlauben Sie vnet den vnet-Datenverkehr für VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="bf9ab-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9ab-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf9ab-115">-AsJob</span></span>
<span data-ttu-id="bf9ab-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="bf9ab-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9ab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf9ab-117">-DefaultProfile</span></span>
<span data-ttu-id="bf9ab-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bf9ab-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9ab-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="bf9ab-119">-Location</span></span>
<span data-ttu-id="bf9ab-120">Der Speicherort der VirtualWAN-Ressource.</span><span class="sxs-lookup"><span data-stu-id="bf9ab-120">The location of the VirtualWAN resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9ab-121">-Name</span><span class="sxs-lookup"><span data-stu-id="bf9ab-121">-Name</span></span>
<span data-ttu-id="bf9ab-122">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="bf9ab-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9ab-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf9ab-123">-ResourceGroupName</span></span>
<span data-ttu-id="bf9ab-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bf9ab-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9ab-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="bf9ab-125">-Tag</span></span>
<span data-ttu-id="bf9ab-126">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="bf9ab-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9ab-127">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="bf9ab-127">-VirtualWANType</span></span>
<span data-ttu-id="bf9ab-128">Der Typ des virtuellen WAN.</span><span class="sxs-lookup"><span data-stu-id="bf9ab-128">The type of the Virtual Wan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9ab-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bf9ab-129">-Confirm</span></span>
<span data-ttu-id="bf9ab-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bf9ab-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9ab-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf9ab-131">-WhatIf</span></span>
<span data-ttu-id="bf9ab-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bf9ab-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf9ab-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bf9ab-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9ab-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf9ab-134">CommonParameters</span></span>
<span data-ttu-id="bf9ab-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf9ab-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf9ab-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf9ab-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf9ab-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bf9ab-137">INPUTS</span></span>

### <span data-ttu-id="bf9ab-138">Keine</span><span class="sxs-lookup"><span data-stu-id="bf9ab-138">None</span></span>

## <span data-ttu-id="bf9ab-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bf9ab-139">OUTPUTS</span></span>

### <span data-ttu-id="bf9ab-140">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="bf9ab-140">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="bf9ab-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="bf9ab-141">NOTES</span></span>

## <span data-ttu-id="bf9ab-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bf9ab-142">RELATED LINKS</span></span>

[<span data-ttu-id="bf9ab-143">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="bf9ab-143">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="bf9ab-144">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="bf9ab-144">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="bf9ab-145">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="bf9ab-145">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
