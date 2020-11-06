---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
ms.openlocfilehash: 89ab4ea57f5f03fbc26d33e1a9087371f215d4ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476954"
---
# <span data-ttu-id="fa33d-101">Remove-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="fa33d-101">Remove-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="fa33d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fa33d-102">SYNOPSIS</span></span>
<span data-ttu-id="fa33d-103">Entfernt eine Netzwerkschnittstelle von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="fa33d-103">Removes a network interface from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa33d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa33d-104">SYNTAX</span></span>

```
Remove-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa33d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa33d-105">DESCRIPTION</span></span>
<span data-ttu-id="fa33d-106">Das Cmdlet **Remove-AzureRmVMNetworkInterface** entfernt eine Netzwerkschnittstelle von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="fa33d-106">The **Remove-AzureRmVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="fa33d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fa33d-107">EXAMPLES</span></span>

## <span data-ttu-id="fa33d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa33d-108">PARAMETERS</span></span>

### <span data-ttu-id="fa33d-109">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="fa33d-109">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="fa33d-110">Gibt ein Array von Netzwerkschnittstellen-IDs an, die von diesem Cmdlet entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="fa33d-110">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fa33d-111">-VM</span><span class="sxs-lookup"><span data-stu-id="fa33d-111">-VM</span></span>
<span data-ttu-id="fa33d-112">Gibt den virtuellen Computer an, von dem dieses Cmdlet eine Netzwerkschnittstelle entfernt.</span><span class="sxs-lookup"><span data-stu-id="fa33d-112">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="fa33d-113">Verwenden Sie das Get-AzureRmVM-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fa33d-113">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="fa33d-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fa33d-114">-Confirm</span></span>
<span data-ttu-id="fa33d-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fa33d-115">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="fa33d-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa33d-116">-WhatIf</span></span>
<span data-ttu-id="fa33d-117">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fa33d-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fa33d-118">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fa33d-118">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="fa33d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa33d-119">CommonParameters</span></span>
<span data-ttu-id="fa33d-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa33d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa33d-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa33d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa33d-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fa33d-122">INPUTS</span></span>

### <span data-ttu-id="fa33d-123">Keine</span><span class="sxs-lookup"><span data-stu-id="fa33d-123">None</span></span>
<span data-ttu-id="fa33d-124">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="fa33d-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fa33d-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fa33d-125">OUTPUTS</span></span>

## <span data-ttu-id="fa33d-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="fa33d-126">NOTES</span></span>

## <span data-ttu-id="fa33d-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fa33d-127">RELATED LINKS</span></span>

[<span data-ttu-id="fa33d-128">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="fa33d-128">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


