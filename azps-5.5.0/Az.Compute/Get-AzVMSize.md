---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
ms.openlocfilehash: e9ed9350b8ffdd93dd83843ee083c90bac786edd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166513"
---
# <span data-ttu-id="8aa29-101">Get-AzVMSize</span><span class="sxs-lookup"><span data-stu-id="8aa29-101">Get-AzVMSize</span></span>

## <span data-ttu-id="8aa29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8aa29-102">SYNOPSIS</span></span>
<span data-ttu-id="8aa29-103">Ruft verfügbare Größen virtueller Computer ab.</span><span class="sxs-lookup"><span data-stu-id="8aa29-103">Gets available virtual machine sizes.</span></span>

## <span data-ttu-id="8aa29-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8aa29-104">SYNTAX</span></span>

### <span data-ttu-id="8aa29-105">ListVirtualMachineSizeParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8aa29-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8aa29-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8aa29-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8aa29-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="8aa29-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8aa29-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8aa29-108">DESCRIPTION</span></span>
<span data-ttu-id="8aa29-109">Das **Get-AzVMSize-Cmdlet** wird für virtuelle Computergrößen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8aa29-109">The **Get-AzVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="8aa29-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8aa29-110">EXAMPLES</span></span>

### <span data-ttu-id="8aa29-111">Beispiel 1: Erhalten der Größe virtueller Computer für einen Speicherort</span><span class="sxs-lookup"><span data-stu-id="8aa29-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzVMSize -Location "Central US"
```

<span data-ttu-id="8aa29-112">Dieser Befehl ruft die verfügbaren Größen für virtuelle Computer am angegebenen Speicherort ab.</span><span class="sxs-lookup"><span data-stu-id="8aa29-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="8aa29-113">Beispiel 2: Erhalten von Größen für einen Verfügbarkeitssatz</span><span class="sxs-lookup"><span data-stu-id="8aa29-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="8aa29-114">Dieser Befehl ruft verfügbare Größen für virtuelle Computer ab, die Sie im Verfügbarkeitssatz namens "AvailabilitySet17" bereitstellen können.</span><span class="sxs-lookup"><span data-stu-id="8aa29-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="8aa29-115">Beispiel 3: Erhalten von Größen für einen vorhandenen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="8aa29-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="8aa29-116">Dieser Befehl ruft verfügbare Größen für den vorhandenen virtuellen Computer "VirtualMachine12" ab.</span><span class="sxs-lookup"><span data-stu-id="8aa29-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="8aa29-117">Sie können die Größe dieses virtuellen Computers auf die Größe ändern, die dieser Befehl erhält.</span><span class="sxs-lookup"><span data-stu-id="8aa29-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="8aa29-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8aa29-118">PARAMETERS</span></span>

### <span data-ttu-id="8aa29-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="8aa29-119">-AvailabilitySetName</span></span>
<span data-ttu-id="8aa29-120">Gibt den Namen des Verfügbarkeitssets an, für den dieses Cmdlet die verfügbaren Größen virtueller Computer erhält.</span><span class="sxs-lookup"><span data-stu-id="8aa29-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForAvailabilitySet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8aa29-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aa29-121">-DefaultProfile</span></span>
<span data-ttu-id="8aa29-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8aa29-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8aa29-123">-Location</span><span class="sxs-lookup"><span data-stu-id="8aa29-123">-Location</span></span>
<span data-ttu-id="8aa29-124">Gibt den Speicherort an, für den dieses Cmdlet die verfügbaren Größen virtueller Computer erhält.</span><span class="sxs-lookup"><span data-stu-id="8aa29-124">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVirtualMachineSizeParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8aa29-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8aa29-125">-ResourceGroupName</span></span>
<span data-ttu-id="8aa29-126">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="8aa29-126">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForAvailabilitySet, ListAvailableSizesForVirtualMachine
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8aa29-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="8aa29-127">-VMName</span></span>
<span data-ttu-id="8aa29-128">Gibt den Namen des virtuellen Computers an, der von diesem Cmdlet die verfügbaren Größen für virtuelle Computer für Größenänderung erhält.</span><span class="sxs-lookup"><span data-stu-id="8aa29-128">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForVirtualMachine
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8aa29-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aa29-129">CommonParameters</span></span>
<span data-ttu-id="8aa29-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8aa29-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aa29-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8aa29-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aa29-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8aa29-132">INPUTS</span></span>

### <span data-ttu-id="8aa29-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8aa29-133">System.String</span></span>

## <span data-ttu-id="8aa29-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8aa29-134">OUTPUTS</span></span>

### <span data-ttu-id="8aa29-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="8aa29-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span></span>

## <span data-ttu-id="8aa29-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8aa29-136">NOTES</span></span>

## <span data-ttu-id="8aa29-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8aa29-137">RELATED LINKS</span></span>

[<span data-ttu-id="8aa29-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="8aa29-138">Get-AzVM</span></span>](./Get-AzVM.md)


