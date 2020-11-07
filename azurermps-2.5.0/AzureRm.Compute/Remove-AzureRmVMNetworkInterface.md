---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 0c7900d50074e185d26f4fafccd9b63756749fd8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849739"
---
# <span data-ttu-id="1fef3-101">Remove-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="1fef3-101">Remove-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="1fef3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1fef3-102">SYNOPSIS</span></span>
<span data-ttu-id="1fef3-103">Entfernt eine Netzwerkschnittstelle von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="1fef3-103">Removes a network interface from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fef3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1fef3-104">SYNTAX</span></span>

```
Remove-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fef3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1fef3-105">DESCRIPTION</span></span>
<span data-ttu-id="1fef3-106">Das Cmdlet **Remove-AzureRmVMNetworkInterface** entfernt eine Netzwerkschnittstelle von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="1fef3-106">The **Remove-AzureRmVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="1fef3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1fef3-107">EXAMPLES</span></span>

### <span data-ttu-id="1fef3-108">1:</span><span class="sxs-lookup"><span data-stu-id="1fef3-108">1:</span></span>
```

```

## <span data-ttu-id="1fef3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1fef3-109">PARAMETERS</span></span>

### <span data-ttu-id="1fef3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fef3-110">-DefaultProfile</span></span>
<span data-ttu-id="1fef3-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1fef3-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fef3-112">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="1fef3-112">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="1fef3-113">Gibt ein Array von Netzwerkschnittstellen-IDs an, die von diesem Cmdlet entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="1fef3-113">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1fef3-114">-VM</span><span class="sxs-lookup"><span data-stu-id="1fef3-114">-VM</span></span>
<span data-ttu-id="1fef3-115">Gibt den virtuellen Computer an, von dem dieses Cmdlet eine Netzwerkschnittstelle entfernt.</span><span class="sxs-lookup"><span data-stu-id="1fef3-115">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="1fef3-116">Verwenden Sie das Get-AzureRmVM-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1fef3-116">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="1fef3-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1fef3-117">-Confirm</span></span>
<span data-ttu-id="1fef3-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1fef3-118">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="1fef3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fef3-119">-WhatIf</span></span>
<span data-ttu-id="1fef3-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1fef3-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1fef3-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1fef3-121">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="1fef3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fef3-122">CommonParameters</span></span>
<span data-ttu-id="1fef3-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fef3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fef3-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fef3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fef3-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1fef3-125">INPUTS</span></span>

### <span data-ttu-id="1fef3-126">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1fef3-126">PSVirtualMachine</span></span>
<span data-ttu-id="1fef3-127">Der Parameter "VM" akzeptiert den Wert vom Typ "PSVirtualMachine" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="1fef3-127">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="1fef3-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1fef3-128">OUTPUTS</span></span>

### <span data-ttu-id="1fef3-129">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1fef3-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="1fef3-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="1fef3-130">NOTES</span></span>

## <span data-ttu-id="1fef3-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1fef3-131">RELATED LINKS</span></span>

[<span data-ttu-id="1fef3-132">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1fef3-132">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


