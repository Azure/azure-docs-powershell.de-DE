---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualWan.md
ms.openlocfilehash: 8d514ae4f01709d499c7685958cf13671e9b0c13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504330"
---
# <span data-ttu-id="ad25d-101">New-AzureRmVirtualWan</span><span class="sxs-lookup"><span data-stu-id="ad25d-101">New-AzureRmVirtualWan</span></span>

## <span data-ttu-id="ad25d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ad25d-102">SYNOPSIS</span></span>
<span data-ttu-id="ad25d-103">Erstellt ein Azure-virtuelles WAN.</span><span class="sxs-lookup"><span data-stu-id="ad25d-103">Creates an Azure Virtual WAN.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad25d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad25d-104">SYNTAX</span></span>

```
New-AzureRmVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad25d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad25d-105">DESCRIPTION</span></span>
<span data-ttu-id="ad25d-106">Erstellt eine neue Azure VirtualWAN-Ressource.</span><span class="sxs-lookup"><span data-stu-id="ad25d-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="ad25d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad25d-107">EXAMPLES</span></span>

### <span data-ttu-id="ad25d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ad25d-108">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="ad25d-109">Im obigen Abschnitt wird eine Ressourcengruppe "testRG" in der Region "West US" und ein Azure Virtual WAN mit Branch to Branch-Datenverkehr, der in dieser Ressourcengruppe in Azure zulässig ist, erstellt.</span><span class="sxs-lookup"><span data-stu-id="ad25d-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="ad25d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad25d-110">PARAMETERS</span></span>

### <span data-ttu-id="ad25d-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="ad25d-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="ad25d-112">Branch-to-Branch-Datenverkehr für VirtualWan zulassen</span><span class="sxs-lookup"><span data-stu-id="ad25d-112">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="ad25d-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="ad25d-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="ad25d-114">Erlauben Sie vnet den vnet-Datenverkehr für VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="ad25d-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="ad25d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad25d-115">-AsJob</span></span>
<span data-ttu-id="ad25d-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ad25d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ad25d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad25d-117">-DefaultProfile</span></span>
<span data-ttu-id="ad25d-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ad25d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad25d-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="ad25d-119">-Location</span></span>
<span data-ttu-id="ad25d-120">Der Speicherort der VirtualWAN-Ressource.</span><span class="sxs-lookup"><span data-stu-id="ad25d-120">The location of the VirtualWAN resource.</span></span>

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

### <span data-ttu-id="ad25d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ad25d-121">-Name</span></span>
<span data-ttu-id="ad25d-122">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="ad25d-122">The resource name.</span></span>

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

### <span data-ttu-id="ad25d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad25d-123">-ResourceGroupName</span></span>
<span data-ttu-id="ad25d-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ad25d-124">The resource group name.</span></span>

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

### <span data-ttu-id="ad25d-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="ad25d-125">-Tag</span></span>
<span data-ttu-id="ad25d-126">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="ad25d-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="ad25d-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ad25d-127">-Confirm</span></span>
<span data-ttu-id="ad25d-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ad25d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad25d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad25d-129">-WhatIf</span></span>
<span data-ttu-id="ad25d-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ad25d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad25d-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ad25d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad25d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad25d-132">CommonParameters</span></span>
<span data-ttu-id="ad25d-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad25d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad25d-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad25d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad25d-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ad25d-135">INPUTS</span></span>

### <span data-ttu-id="ad25d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ad25d-136">System.String</span></span>

### <span data-ttu-id="ad25d-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ad25d-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ad25d-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ad25d-138">OUTPUTS</span></span>

### <span data-ttu-id="ad25d-139">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="ad25d-139">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="ad25d-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="ad25d-140">NOTES</span></span>

## <span data-ttu-id="ad25d-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ad25d-141">RELATED LINKS</span></span>
