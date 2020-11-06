---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 8f2d061fa67ed8e588ae162fbf7bd0a094ae6b1c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483061"
---
# <span data-ttu-id="7c725-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c725-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="7c725-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7c725-102">SYNOPSIS</span></span>
<span data-ttu-id="7c725-103">Entfernt eine Netzwerkschnittstellenkonfiguration aus einem VMSS.</span><span class="sxs-lookup"><span data-stu-id="7c725-103">Removes a network interface configuration from a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c725-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c725-104">SYNTAX</span></span>

### <span data-ttu-id="7c725-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c725-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-Name] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c725-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c725-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-Id] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c725-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7c725-107">DESCRIPTION</span></span>
<span data-ttu-id="7c725-108">Das Cmdlet **Remove-AzureRmVmssNetworkInterfaceConfiguration** entfernt eine Netzwerkschnittstellenkonfiguration von einem virtuellen Computer-Skalierungs Satz (VMSS).</span><span class="sxs-lookup"><span data-stu-id="7c725-108">The **Remove-AzureRmVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="7c725-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7c725-109">EXAMPLES</span></span>

### <span data-ttu-id="7c725-110">Beispiel 1: Entfernen einer Schnittstellenkonfiguration</span><span class="sxs-lookup"><span data-stu-id="7c725-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzureRmVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="7c725-111">Der erste Befehl ruft einen VMSS mithilfe des Get-AzureRmVmss-Cmdlets ab und speichert ihn dann in der $VMSS-Variablen.</span><span class="sxs-lookup"><span data-stu-id="7c725-111">The first command gets a VMSS by using the Get-AzureRmVmss cmdlet, and then stores it in the $VMSS variable.</span></span>

<span data-ttu-id="7c725-112">Der zweite Befehl entfernt die Netzwerkschnittstellenkonfiguration mit dem Namen ContosoVmssInterface02 aus der Gruppe in $VMSS.</span><span class="sxs-lookup"><span data-stu-id="7c725-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="7c725-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c725-113">PARAMETERS</span></span>

### <span data-ttu-id="7c725-114">-ID</span><span class="sxs-lookup"><span data-stu-id="7c725-114">-Id</span></span>
<span data-ttu-id="7c725-115">Gibt die ID der Netzwerkschnittstellenkonfiguration an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="7c725-115">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c725-116">-Name</span><span class="sxs-lookup"><span data-stu-id="7c725-116">-Name</span></span>
<span data-ttu-id="7c725-117">Gibt den Namen der Netzwerkschnittstellenkonfiguration an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="7c725-117">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c725-118">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7c725-118">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="7c725-119">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="7c725-119">Specifies the VMSS object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c725-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7c725-120">-Confirm</span></span>
<span data-ttu-id="7c725-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7c725-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c725-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c725-122">-WhatIf</span></span>
<span data-ttu-id="7c725-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c725-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c725-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7c725-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c725-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c725-125">CommonParameters</span></span>
<span data-ttu-id="7c725-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c725-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c725-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c725-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c725-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7c725-128">INPUTS</span></span>

### <span data-ttu-id="7c725-129">Keine</span><span class="sxs-lookup"><span data-stu-id="7c725-129">None</span></span>
<span data-ttu-id="7c725-130">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="7c725-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7c725-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7c725-131">OUTPUTS</span></span>

## <span data-ttu-id="7c725-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="7c725-132">NOTES</span></span>

## <span data-ttu-id="7c725-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7c725-133">RELATED LINKS</span></span>

[<span data-ttu-id="7c725-134">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c725-134">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="7c725-135">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="7c725-135">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


