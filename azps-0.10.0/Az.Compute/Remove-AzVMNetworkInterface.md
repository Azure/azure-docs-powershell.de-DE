---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
ms.openlocfilehash: 548d576ff959dd96a6978675ca5a35c18c97e0a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844363"
---
# <span data-ttu-id="15337-101">Remove-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="15337-101">Remove-AzVMNetworkInterface</span></span>

## <span data-ttu-id="15337-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="15337-102">SYNOPSIS</span></span>
<span data-ttu-id="15337-103">Entfernt eine Netzwerkschnittstelle von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="15337-103">Removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="15337-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="15337-104">SYNTAX</span></span>

```
Remove-AzVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15337-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="15337-105">DESCRIPTION</span></span>
<span data-ttu-id="15337-106">Das Cmdlet **Remove-AzVMNetworkInterface** entfernt eine Netzwerkschnittstelle von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="15337-106">The **Remove-AzVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="15337-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="15337-107">EXAMPLES</span></span>

### <span data-ttu-id="15337-108">1:</span><span class="sxs-lookup"><span data-stu-id="15337-108">1:</span></span>
```

```

## <span data-ttu-id="15337-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="15337-109">PARAMETERS</span></span>

### <span data-ttu-id="15337-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15337-110">-DefaultProfile</span></span>
<span data-ttu-id="15337-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="15337-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15337-112">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="15337-112">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="15337-113">Gibt ein Array von Netzwerkschnittstellen-IDs an, die von diesem Cmdlet entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="15337-113">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Id, NicIds

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15337-114">-VM</span><span class="sxs-lookup"><span data-stu-id="15337-114">-VM</span></span>
<span data-ttu-id="15337-115">Gibt den virtuellen Computer an, von dem dieses Cmdlet eine Netzwerkschnittstelle entfernt.</span><span class="sxs-lookup"><span data-stu-id="15337-115">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="15337-116">Verwenden Sie das Get-AzVM-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="15337-116">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15337-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="15337-117">-Confirm</span></span>
<span data-ttu-id="15337-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="15337-118">Prompts you for confirmation before running the cmdlet.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15337-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15337-119">-WhatIf</span></span>
<span data-ttu-id="15337-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15337-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15337-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="15337-121">The cmdlet is not run.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15337-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15337-122">CommonParameters</span></span>
<span data-ttu-id="15337-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15337-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15337-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15337-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15337-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="15337-125">INPUTS</span></span>

### <span data-ttu-id="15337-126">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="15337-126">PSVirtualMachine</span></span>
<span data-ttu-id="15337-127">Der Parameter "VM" akzeptiert den Wert vom Typ "PSVirtualMachine" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="15337-127">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="15337-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="15337-128">OUTPUTS</span></span>

### <span data-ttu-id="15337-129">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="15337-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="15337-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="15337-130">NOTES</span></span>

## <span data-ttu-id="15337-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="15337-131">RELATED LINKS</span></span>

[<span data-ttu-id="15337-132">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="15337-132">Get-AzVM</span></span>](./Get-AzVM.md)


