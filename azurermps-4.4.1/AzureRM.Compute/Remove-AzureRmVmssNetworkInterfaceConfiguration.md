---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 85f593c1d66b02f9982cecc4606603fbef1385d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662274"
---
# <span data-ttu-id="56e08-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="56e08-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="56e08-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="56e08-102">SYNOPSIS</span></span>
<span data-ttu-id="56e08-103">Entfernt eine Netzwerkschnittstellenkonfiguration aus einem VMSS.</span><span class="sxs-lookup"><span data-stu-id="56e08-103">Removes a network interface configuration from a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56e08-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="56e08-104">SYNTAX</span></span>

### <span data-ttu-id="56e08-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="56e08-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56e08-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="56e08-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56e08-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56e08-107">DESCRIPTION</span></span>
<span data-ttu-id="56e08-108">Das Cmdlet **Remove-AzureRmVmssNetworkInterfaceConfiguration** entfernt eine Netzwerkschnittstellenkonfiguration von einem virtuellen Computer-Skalierungs Satz (VMSS).</span><span class="sxs-lookup"><span data-stu-id="56e08-108">The **Remove-AzureRmVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="56e08-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="56e08-109">EXAMPLES</span></span>

### <span data-ttu-id="56e08-110">Beispiel 1: Entfernen einer Schnittstellenkonfiguration</span><span class="sxs-lookup"><span data-stu-id="56e08-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzureRmVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="56e08-111">Der erste Befehl ruft einen VMSS mithilfe des Get-AzureRmVmss-Cmdlets ab und speichert ihn dann in der $VMSS-Variablen.</span><span class="sxs-lookup"><span data-stu-id="56e08-111">The first command gets a VMSS by using the Get-AzureRmVmss cmdlet, and then stores it in the $VMSS variable.</span></span>

<span data-ttu-id="56e08-112">Der zweite Befehl entfernt die Netzwerkschnittstellenkonfiguration mit dem Namen ContosoVmssInterface02 aus der Gruppe in $VMSS.</span><span class="sxs-lookup"><span data-stu-id="56e08-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="56e08-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="56e08-113">PARAMETERS</span></span>

### <span data-ttu-id="56e08-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56e08-114">-DefaultProfile</span></span>
<span data-ttu-id="56e08-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="56e08-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56e08-116">-ID</span><span class="sxs-lookup"><span data-stu-id="56e08-116">-Id</span></span>
<span data-ttu-id="56e08-117">Gibt die ID der Netzwerkschnittstellenkonfiguration an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="56e08-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="56e08-118">-Name</span><span class="sxs-lookup"><span data-stu-id="56e08-118">-Name</span></span>
<span data-ttu-id="56e08-119">Gibt den Namen der Netzwerkschnittstellenkonfiguration an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="56e08-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="56e08-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="56e08-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="56e08-121">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="56e08-121">Specifies the VMSS object.</span></span>

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

### <span data-ttu-id="56e08-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="56e08-122">-Confirm</span></span>
<span data-ttu-id="56e08-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="56e08-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56e08-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56e08-124">-WhatIf</span></span>
<span data-ttu-id="56e08-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="56e08-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56e08-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="56e08-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56e08-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56e08-127">CommonParameters</span></span>
<span data-ttu-id="56e08-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56e08-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56e08-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56e08-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56e08-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="56e08-130">INPUTS</span></span>

## <span data-ttu-id="56e08-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="56e08-131">OUTPUTS</span></span>

## <span data-ttu-id="56e08-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="56e08-132">NOTES</span></span>

## <span data-ttu-id="56e08-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="56e08-133">RELATED LINKS</span></span>

[<span data-ttu-id="56e08-134">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="56e08-134">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="56e08-135">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="56e08-135">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


