---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssnetworkinterfaceconfiguration
schema: 2.0.0
ms.openlocfilehash: 46058901188b99eb30d088e2ea784fdc0df8d782
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850451"
---
# <span data-ttu-id="c605f-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="c605f-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="c605f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c605f-102">SYNOPSIS</span></span>
<span data-ttu-id="c605f-103">Entfernt eine Netzwerkschnittstellenkonfiguration aus einem VMSS.</span><span class="sxs-lookup"><span data-stu-id="c605f-103">Removes a network interface configuration from a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c605f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c605f-104">SYNTAX</span></span>

### <span data-ttu-id="c605f-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c605f-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c605f-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c605f-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c605f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c605f-107">DESCRIPTION</span></span>
<span data-ttu-id="c605f-108">Das Cmdlet **Remove-AzureRmVmssNetworkInterfaceConfiguration** entfernt eine Netzwerkschnittstellenkonfiguration von einem virtuellen Computer-Skalierungs Satz (VMSS).</span><span class="sxs-lookup"><span data-stu-id="c605f-108">The **Remove-AzureRmVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="c605f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c605f-109">EXAMPLES</span></span>

### <span data-ttu-id="c605f-110">Beispiel 1: Entfernen einer Schnittstellenkonfiguration</span><span class="sxs-lookup"><span data-stu-id="c605f-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzureRmVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="c605f-111">Der erste Befehl ruft einen VMSS mithilfe des Get-AzureRmVmss-Cmdlets ab und speichert ihn dann in der $VMSS-Variablen.</span><span class="sxs-lookup"><span data-stu-id="c605f-111">The first command gets a VMSS by using the Get-AzureRmVmss cmdlet, and then stores it in the $VMSS variable.</span></span>

<span data-ttu-id="c605f-112">Der zweite Befehl entfernt die Netzwerkschnittstellenkonfiguration mit dem Namen ContosoVmssInterface02 aus der Gruppe in $VMSS.</span><span class="sxs-lookup"><span data-stu-id="c605f-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="c605f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c605f-113">PARAMETERS</span></span>

### <span data-ttu-id="c605f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c605f-114">-DefaultProfile</span></span>
<span data-ttu-id="c605f-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c605f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c605f-116">-ID</span><span class="sxs-lookup"><span data-stu-id="c605f-116">-Id</span></span>
<span data-ttu-id="c605f-117">Gibt die ID der Netzwerkschnittstellenkonfiguration an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c605f-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c605f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c605f-118">-Name</span></span>
<span data-ttu-id="c605f-119">Gibt den Namen der Netzwerkschnittstellenkonfiguration an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c605f-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c605f-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c605f-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="c605f-121">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="c605f-121">Specifies the VMSS object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c605f-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c605f-122">-Confirm</span></span>
<span data-ttu-id="c605f-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c605f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c605f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c605f-124">-WhatIf</span></span>
<span data-ttu-id="c605f-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c605f-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c605f-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c605f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c605f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c605f-127">CommonParameters</span></span>
<span data-ttu-id="c605f-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c605f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c605f-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c605f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c605f-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c605f-130">INPUTS</span></span>

### <span data-ttu-id="c605f-131">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c605f-131">VirtualMachineScaleSet</span></span>
<span data-ttu-id="c605f-132">Der Parameter "VirtualMachineScaleSet" akzeptiert den Wert vom Typ "VirtualMachineScaleSet" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c605f-132">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="c605f-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c605f-133">OUTPUTS</span></span>

### <span data-ttu-id="c605f-134">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c605f-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="c605f-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="c605f-135">NOTES</span></span>

## <span data-ttu-id="c605f-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c605f-136">RELATED LINKS</span></span>

[<span data-ttu-id="c605f-137">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="c605f-137">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="c605f-138">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c605f-138">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


