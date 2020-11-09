---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
ms.openlocfilehash: e9ed9350b8ffdd93dd83843ee083c90bac786edd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301534"
---
# <span data-ttu-id="04abc-101">Get-AzVMSize</span><span class="sxs-lookup"><span data-stu-id="04abc-101">Get-AzVMSize</span></span>

## <span data-ttu-id="04abc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="04abc-102">SYNOPSIS</span></span>
<span data-ttu-id="04abc-103">Ruft Verfügbare Größen für virtuelle Maschinen ab.</span><span class="sxs-lookup"><span data-stu-id="04abc-103">Gets available virtual machine sizes.</span></span>

## <span data-ttu-id="04abc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="04abc-104">SYNTAX</span></span>

### <span data-ttu-id="04abc-105">ListVirtualMachineSizeParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="04abc-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04abc-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="04abc-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04abc-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="04abc-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="04abc-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="04abc-108">DESCRIPTION</span></span>
<span data-ttu-id="04abc-109">Das Cmdlet " **Get-AzVMSize** " ruft Verfügbare Größen für virtuelle Maschinen ab.</span><span class="sxs-lookup"><span data-stu-id="04abc-109">The **Get-AzVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="04abc-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="04abc-110">EXAMPLES</span></span>

### <span data-ttu-id="04abc-111">Beispiel 1: Abrufen von Größen für virtuelle Maschinen für einen Standort</span><span class="sxs-lookup"><span data-stu-id="04abc-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzVMSize -Location "Central US"
```

<span data-ttu-id="04abc-112">Dieser Befehl ruft die verfügbaren Größen für virtuelle Computer an der angegebenen Position ab.</span><span class="sxs-lookup"><span data-stu-id="04abc-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="04abc-113">Beispiel 2: Abrufen von Größen für einen Verfügbarkeits Satz</span><span class="sxs-lookup"><span data-stu-id="04abc-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="04abc-114">Dieser Befehl ruft Verfügbare Größen für virtuelle Computer ab, die Sie im Verfügbarkeits Satz mit dem Namen AvailabilitySet17 bereitstellen können.</span><span class="sxs-lookup"><span data-stu-id="04abc-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="04abc-115">Beispiel 3: Abrufen von Größen für einen vorhandenen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="04abc-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="04abc-116">Dieser Befehl ruft Verfügbare Größen für den vorhandenen virtuellen Computer mit dem Namen VirtualMachine12 ab.</span><span class="sxs-lookup"><span data-stu-id="04abc-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="04abc-117">Sie können die Größe dieses virtuellen Computers auf die Größen ändern, die dieser Befehl erhält.</span><span class="sxs-lookup"><span data-stu-id="04abc-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="04abc-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="04abc-118">PARAMETERS</span></span>

### <span data-ttu-id="04abc-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="04abc-119">-AvailabilitySetName</span></span>
<span data-ttu-id="04abc-120">Gibt den Namen der verfügbarkeitsgruppe an, für die dieses Cmdlet die verfügbaren Größen für virtuelle Maschinen erhält.</span><span class="sxs-lookup"><span data-stu-id="04abc-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="04abc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04abc-121">-DefaultProfile</span></span>
<span data-ttu-id="04abc-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="04abc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04abc-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="04abc-123">-Location</span></span>
<span data-ttu-id="04abc-124">Gibt den Speicherort an, für den dieses Cmdlet die verfügbaren Größen für virtuelle Maschinen erhält.</span><span class="sxs-lookup"><span data-stu-id="04abc-124">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="04abc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04abc-125">-ResourceGroupName</span></span>
<span data-ttu-id="04abc-126">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="04abc-126">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="04abc-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="04abc-127">-VMName</span></span>
<span data-ttu-id="04abc-128">Gibt den Namen des virtuellen Computers an, an dem dieses Cmdlet die verfügbaren Größen für virtuelle Maschinen zur Größenänderung erhält.</span><span class="sxs-lookup"><span data-stu-id="04abc-128">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

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

### <span data-ttu-id="04abc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04abc-129">CommonParameters</span></span>
<span data-ttu-id="04abc-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04abc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04abc-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04abc-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04abc-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="04abc-132">INPUTS</span></span>

### <span data-ttu-id="04abc-133">System. String</span><span class="sxs-lookup"><span data-stu-id="04abc-133">System.String</span></span>

## <span data-ttu-id="04abc-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="04abc-134">OUTPUTS</span></span>

### <span data-ttu-id="04abc-135">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="04abc-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span></span>

## <span data-ttu-id="04abc-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="04abc-136">NOTES</span></span>

## <span data-ttu-id="04abc-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="04abc-137">RELATED LINKS</span></span>

[<span data-ttu-id="04abc-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="04abc-138">Get-AzVM</span></span>](./Get-AzVM.md)


