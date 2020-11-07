---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 58029017f4a6a272856f7badd6b09a9ba1f37ac3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651975"
---
# <span data-ttu-id="fb3c4-101">Remove-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb3c4-101">Remove-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="fb3c4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fb3c4-102">SYNOPSIS</span></span>
<span data-ttu-id="fb3c4-103">Entfernt eine Netzwerkschnittstellenkonfiguration aus einem VMSS.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-103">Removes a network interface configuration from a VMSS.</span></span>

## <span data-ttu-id="fb3c4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb3c4-104">SYNTAX</span></span>

### <span data-ttu-id="fb3c4-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb3c4-105">NameParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb3c4-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb3c4-106">IdParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb3c4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb3c4-107">DESCRIPTION</span></span>
<span data-ttu-id="fb3c4-108">Das Cmdlet **Remove-AzVmssNetworkInterfaceConfiguration** entfernt eine Netzwerkschnittstellenkonfiguration von einem virtuellen Computer-Skalierungs Satz (VMSS).</span><span class="sxs-lookup"><span data-stu-id="fb3c4-108">The **Remove-AzVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="fb3c4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fb3c4-109">EXAMPLES</span></span>

### <span data-ttu-id="fb3c4-110">Beispiel 1: Entfernen einer Schnittstellenkonfiguration</span><span class="sxs-lookup"><span data-stu-id="fb3c4-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="fb3c4-111">Der erste Befehl ruft einen VMSS mithilfe des Get-AzVmss-Cmdlets ab und speichert ihn dann in der $VMSS-Variablen.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-111">The first command gets a VMSS by using the Get-AzVmss cmdlet, and then stores it in the $VMSS variable.</span></span>
<span data-ttu-id="fb3c4-112">Der zweite Befehl entfernt die Netzwerkschnittstellenkonfiguration mit dem Namen ContosoVmssInterface02 aus der Gruppe in $VMSS.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="fb3c4-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb3c4-113">PARAMETERS</span></span>

### <span data-ttu-id="fb3c4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb3c4-114">-DefaultProfile</span></span>
<span data-ttu-id="fb3c4-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb3c4-116">-ID</span><span class="sxs-lookup"><span data-stu-id="fb3c4-116">-Id</span></span>
<span data-ttu-id="fb3c4-117">Gibt die ID der Netzwerkschnittstellenkonfiguration an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fb3c4-118">-Name</span><span class="sxs-lookup"><span data-stu-id="fb3c4-118">-Name</span></span>
<span data-ttu-id="fb3c4-119">Gibt den Namen der Netzwerkschnittstellenkonfiguration an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fb3c4-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fb3c4-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="fb3c4-121">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-121">Specifies the VMSS object.</span></span>

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

### <span data-ttu-id="fb3c4-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fb3c4-122">-Confirm</span></span>
<span data-ttu-id="fb3c4-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb3c4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb3c4-124">-WhatIf</span></span>
<span data-ttu-id="fb3c4-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb3c4-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb3c4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb3c4-127">CommonParameters</span></span>
<span data-ttu-id="fb3c4-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb3c4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb3c4-129">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb3c4-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb3c4-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fb3c4-130">INPUTS</span></span>

### <span data-ttu-id="fb3c4-131">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fb3c4-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="fb3c4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fb3c4-132">System.String</span></span>

## <span data-ttu-id="fb3c4-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fb3c4-133">OUTPUTS</span></span>

### <span data-ttu-id="fb3c4-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fb3c4-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="fb3c4-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="fb3c4-135">NOTES</span></span>

## <span data-ttu-id="fb3c4-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fb3c4-136">RELATED LINKS</span></span>

[<span data-ttu-id="fb3c4-137">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb3c4-137">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="fb3c4-138">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fb3c4-138">Get-AzVmss</span></span>](./Get-AzVmss.md)


