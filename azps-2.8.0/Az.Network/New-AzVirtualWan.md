---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
ms.openlocfilehash: 17ace5a209a34fc65d79efaac0bfb477e00b2472
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822984"
---
# <span data-ttu-id="b285d-101">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="b285d-101">New-AzVirtualWan</span></span>

## <span data-ttu-id="b285d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b285d-102">SYNOPSIS</span></span>
<span data-ttu-id="b285d-103">Erstellt ein Azure-virtuelles WAN.</span><span class="sxs-lookup"><span data-stu-id="b285d-103">Creates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="b285d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b285d-104">SYNTAX</span></span>

```
New-AzVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b285d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b285d-105">DESCRIPTION</span></span>
<span data-ttu-id="b285d-106">Erstellt eine neue Azure VirtualWAN-Ressource.</span><span class="sxs-lookup"><span data-stu-id="b285d-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="b285d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b285d-107">EXAMPLES</span></span>

### <span data-ttu-id="b285d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b285d-108">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="b285d-109">Im obigen Abschnitt wird eine Ressourcengruppe "testRG" in der Region "West US" und ein Azure Virtual WAN mit Branch to Branch-Datenverkehr, der in dieser Ressourcengruppe in Azure zulässig ist, erstellt.</span><span class="sxs-lookup"><span data-stu-id="b285d-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="b285d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b285d-110">PARAMETERS</span></span>

### <span data-ttu-id="b285d-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="b285d-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="b285d-112">Branch-to-Branch-Datenverkehr für VirtualWan zulassen</span><span class="sxs-lookup"><span data-stu-id="b285d-112">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="b285d-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="b285d-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="b285d-114">Erlauben Sie vnet den vnet-Datenverkehr für VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="b285d-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="b285d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b285d-115">-AsJob</span></span>
<span data-ttu-id="b285d-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b285d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b285d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b285d-117">-DefaultProfile</span></span>
<span data-ttu-id="b285d-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b285d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b285d-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="b285d-119">-Location</span></span>
<span data-ttu-id="b285d-120">Der Speicherort der VirtualWAN-Ressource.</span><span class="sxs-lookup"><span data-stu-id="b285d-120">The location of the VirtualWAN resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b285d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b285d-121">-Name</span></span>
<span data-ttu-id="b285d-122">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="b285d-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b285d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b285d-123">-ResourceGroupName</span></span>
<span data-ttu-id="b285d-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b285d-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b285d-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="b285d-125">-Tag</span></span>
<span data-ttu-id="b285d-126">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="b285d-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b285d-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b285d-127">-Confirm</span></span>
<span data-ttu-id="b285d-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b285d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b285d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b285d-129">-WhatIf</span></span>
<span data-ttu-id="b285d-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b285d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b285d-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b285d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b285d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b285d-132">CommonParameters</span></span>
<span data-ttu-id="b285d-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b285d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b285d-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b285d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b285d-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b285d-135">INPUTS</span></span>

### <span data-ttu-id="b285d-136">Keine</span><span class="sxs-lookup"><span data-stu-id="b285d-136">None</span></span>

## <span data-ttu-id="b285d-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b285d-137">OUTPUTS</span></span>

### <span data-ttu-id="b285d-138">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="b285d-138">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="b285d-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="b285d-139">NOTES</span></span>

## <span data-ttu-id="b285d-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b285d-140">RELATED LINKS</span></span>

[<span data-ttu-id="b285d-141">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="b285d-141">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="b285d-142">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="b285d-142">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="b285d-143">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="b285d-143">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
