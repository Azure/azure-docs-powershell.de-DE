---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/repair-azvmssservicefabricupdatedomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
ms.openlocfilehash: 3bec7d92716f31a3aac3c204548ad01f534fa405
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661471"
---
# <span data-ttu-id="d4c23-101">Repair-AzVmssServiceFabricUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="d4c23-101">Repair-AzVmssServiceFabricUpdateDomain</span></span>

## <span data-ttu-id="d4c23-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d4c23-102">SYNOPSIS</span></span>
<span data-ttu-id="d4c23-103">Manueller Platt Form Update-Domänen Schritt zum Aktualisieren virtueller Computer in einem Skalierungs Satz für virtuelle Maschinen in einem Dienst Fabric</span><span class="sxs-lookup"><span data-stu-id="d4c23-103">Manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="d4c23-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4c23-104">SYNTAX</span></span>

### <span data-ttu-id="d4c23-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="d4c23-105">DefaultParameter (Default)</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-PlatformUpdateDomain] <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4c23-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="d4c23-106">ResourceIdParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4c23-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="d4c23-107">ObjectParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4c23-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4c23-108">DESCRIPTION</span></span>
<span data-ttu-id="d4c23-109">Erzwingen der manuellen Aktualisierung von Platt Form Update-Domänen zum Aktualisieren virtueller Computer in einem Skalierungs Satz für virtuelle Maschinen in einem Dienst Fabric</span><span class="sxs-lookup"><span data-stu-id="d4c23-109">Force manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="d4c23-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4c23-110">EXAMPLES</span></span>

### <span data-ttu-id="d4c23-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d4c23-111">Example 1</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceGroupName $rgname -VMScaleSetName $vmssName -PlatformUpdateDomain 0
```

<span data-ttu-id="d4c23-112">Mit diesem Befehl wird das Service Fabric-Update auf UD 0 für den Skalierungs Satz der virtuellen Maschine erzwungen, der durch Ressourcengruppenname und Skalierungs Satz Name angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d4c23-112">This command forces service fabric update walk on UD 0 for the virtual machine scale set specified by resource group name and scale set name.</span></span>

### <span data-ttu-id="d4c23-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d4c23-113">Example 2</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $rgname -VMScaleSetName $vmssName
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -VirtualMachineScaleSet $vmss -PlatformUpdateDomain 1
```

<span data-ttu-id="d4c23-114">Mit diesem Befehl wird das Service Fabric-Update auf UD 1 für den Skalierungs Satz der virtuellen Maschine erzwungen, der durch das VM-Skalierungs Satz Objekt angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d4c23-114">This command forces service fabric update walk on UD 1 for the virtual machine scale set specified by VM scale set object.</span></span>

### <span data-ttu-id="d4c23-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d4c23-115">Example 3</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceId $resoureId  -PlatformUpdateDomain 2;
```

<span data-ttu-id="d4c23-116">Dieser Befehl erzwingt, dass das Service Fabric-Update auf UD 2 für den Skalierungs Satz der virtuellen Maschine durchgeführt wird, der durch Ressourcen-ID angegeben wird</span><span class="sxs-lookup"><span data-stu-id="d4c23-116">This command forces service fabric update walk on UD 2 for the virtual machine scale set specified by resource id.</span></span>

## <span data-ttu-id="d4c23-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4c23-117">PARAMETERS</span></span>

### <span data-ttu-id="d4c23-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4c23-118">-AsJob</span></span>
<span data-ttu-id="d4c23-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d4c23-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4c23-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4c23-120">-DefaultProfile</span></span>
<span data-ttu-id="d4c23-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d4c23-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4c23-122">-PlatformUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="d4c23-122">-PlatformUpdateDomain</span></span>
<span data-ttu-id="d4c23-123">Die Plattform-Update-Domäne, für die ein manueller Wiederherstellungsschritt angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="d4c23-123">The platform update domain for which a manual recovery walk is requested.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4c23-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4c23-124">-ResourceGroupName</span></span>
<span data-ttu-id="d4c23-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d4c23-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4c23-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d4c23-126">-ResourceId</span></span>
<span data-ttu-id="d4c23-127">Die Ressourcen-ID für den Skalierungs Satz der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="d4c23-127">The resource id for the virtual machine scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4c23-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d4c23-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d4c23-129">Skalierungs Satz Objekt für lokalen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="d4c23-129">Local virtual machine scale set object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4c23-130">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d4c23-130">-VMScaleSetName</span></span>
<span data-ttu-id="d4c23-131">Der Name des Skalierungs Satzes für virtuelle Maschinen</span><span class="sxs-lookup"><span data-stu-id="d4c23-131">The name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4c23-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d4c23-132">-Confirm</span></span>
<span data-ttu-id="d4c23-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4c23-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4c23-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4c23-134">-WhatIf</span></span>
<span data-ttu-id="d4c23-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4c23-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4c23-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4c23-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4c23-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4c23-137">CommonParameters</span></span>
<span data-ttu-id="d4c23-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4c23-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4c23-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4c23-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4c23-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d4c23-140">INPUTS</span></span>

### <span data-ttu-id="d4c23-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d4c23-141">System.String</span></span>

### <span data-ttu-id="d4c23-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d4c23-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="d4c23-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d4c23-143">OUTPUTS</span></span>

### <span data-ttu-id="d4c23-144">Microsoft. Azure. Commands. Compute. Automation. Models. PSRecoveryWalkResponse</span><span class="sxs-lookup"><span data-stu-id="d4c23-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSRecoveryWalkResponse</span></span>

## <span data-ttu-id="d4c23-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="d4c23-145">NOTES</span></span>

## <span data-ttu-id="d4c23-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d4c23-146">RELATED LINKS</span></span>
