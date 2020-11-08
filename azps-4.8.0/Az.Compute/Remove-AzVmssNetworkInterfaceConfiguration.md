---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 1b8f9b7843cccf2475e17e1c5d8866972b5b9ee4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009308"
---
# <span data-ttu-id="734dd-101">Remove-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="734dd-101">Remove-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="734dd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="734dd-102">SYNOPSIS</span></span>
<span data-ttu-id="734dd-103">Entfernt eine Netzwerkschnittstellenkonfiguration aus einem VMSS.</span><span class="sxs-lookup"><span data-stu-id="734dd-103">Removes a network interface configuration from a VMSS.</span></span>

## <span data-ttu-id="734dd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="734dd-104">SYNTAX</span></span>

### <span data-ttu-id="734dd-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="734dd-105">NameParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="734dd-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="734dd-106">IdParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="734dd-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="734dd-107">DESCRIPTION</span></span>
<span data-ttu-id="734dd-108">Das Cmdlet **Remove-AzVmssNetworkInterfaceConfiguration** entfernt eine Netzwerkschnittstellenkonfiguration von einem virtuellen Computer-Skalierungs Satz (VMSS).</span><span class="sxs-lookup"><span data-stu-id="734dd-108">The **Remove-AzVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="734dd-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="734dd-109">EXAMPLES</span></span>

### <span data-ttu-id="734dd-110">Beispiel 1: Entfernen einer Schnittstellenkonfiguration</span><span class="sxs-lookup"><span data-stu-id="734dd-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="734dd-111">Der erste Befehl ruft einen VMSS mithilfe des Get-AzVmss-Cmdlets ab und speichert ihn dann in der $VMSS-Variablen.</span><span class="sxs-lookup"><span data-stu-id="734dd-111">The first command gets a VMSS by using the Get-AzVmss cmdlet, and then stores it in the $VMSS variable.</span></span>
<span data-ttu-id="734dd-112">Der zweite Befehl entfernt die Netzwerkschnittstellenkonfiguration mit dem Namen ContosoVmssInterface02 aus der Gruppe in $VMSS.</span><span class="sxs-lookup"><span data-stu-id="734dd-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="734dd-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="734dd-113">PARAMETERS</span></span>

### <span data-ttu-id="734dd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="734dd-114">-DefaultProfile</span></span>
<span data-ttu-id="734dd-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="734dd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="734dd-116">-ID</span><span class="sxs-lookup"><span data-stu-id="734dd-116">-Id</span></span>
<span data-ttu-id="734dd-117">Gibt die ID der Netzwerkschnittstellenkonfiguration an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="734dd-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="734dd-118">-Name</span><span class="sxs-lookup"><span data-stu-id="734dd-118">-Name</span></span>
<span data-ttu-id="734dd-119">Gibt den Namen der Netzwerkschnittstellenkonfiguration an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="734dd-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="734dd-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="734dd-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="734dd-121">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="734dd-121">Specifies the VMSS object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="734dd-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="734dd-122">-Confirm</span></span>
<span data-ttu-id="734dd-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="734dd-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="734dd-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="734dd-124">-WhatIf</span></span>
<span data-ttu-id="734dd-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="734dd-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="734dd-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="734dd-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="734dd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="734dd-127">CommonParameters</span></span>
<span data-ttu-id="734dd-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="734dd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="734dd-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="734dd-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="734dd-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="734dd-130">INPUTS</span></span>

### <span data-ttu-id="734dd-131">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="734dd-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="734dd-132">System. String</span><span class="sxs-lookup"><span data-stu-id="734dd-132">System.String</span></span>

## <span data-ttu-id="734dd-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="734dd-133">OUTPUTS</span></span>

### <span data-ttu-id="734dd-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="734dd-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="734dd-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="734dd-135">NOTES</span></span>

## <span data-ttu-id="734dd-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="734dd-136">RELATED LINKS</span></span>

[<span data-ttu-id="734dd-137">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="734dd-137">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="734dd-138">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="734dd-138">Get-AzVmss</span></span>](./Get-AzVmss.md)


