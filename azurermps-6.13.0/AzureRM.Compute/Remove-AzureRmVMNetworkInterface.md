---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMNetworkInterface.md
ms.openlocfilehash: 349c4590116c05c28c1fc1220e98e946519cd8f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664102"
---
# <span data-ttu-id="6a81a-101">Remove-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6a81a-101">Remove-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="6a81a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6a81a-102">SYNOPSIS</span></span>
<span data-ttu-id="6a81a-103">Entfernt eine Netzwerkschnittstelle von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="6a81a-103">Removes a network interface from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a81a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a81a-104">SYNTAX</span></span>

```
Remove-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a81a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6a81a-105">DESCRIPTION</span></span>
<span data-ttu-id="6a81a-106">Das Cmdlet **Remove-AzureRmVMNetworkInterface** entfernt eine Netzwerkschnittstelle von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="6a81a-106">The **Remove-AzureRmVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="6a81a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6a81a-107">EXAMPLES</span></span>

## <span data-ttu-id="6a81a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a81a-108">PARAMETERS</span></span>

### <span data-ttu-id="6a81a-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a81a-109">-DefaultProfile</span></span>
<span data-ttu-id="6a81a-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6a81a-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a81a-111">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="6a81a-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="6a81a-112">Gibt ein Array von Netzwerkschnittstellen-IDs an, die von diesem Cmdlet entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="6a81a-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id, NicIds

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a81a-113">-VM</span><span class="sxs-lookup"><span data-stu-id="6a81a-113">-VM</span></span>
<span data-ttu-id="6a81a-114">Gibt den virtuellen Computer an, von dem dieses Cmdlet eine Netzwerkschnittstelle entfernt.</span><span class="sxs-lookup"><span data-stu-id="6a81a-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="6a81a-115">Verwenden Sie das Get-AzureRmVM-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6a81a-115">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a81a-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6a81a-116">-Confirm</span></span>
<span data-ttu-id="6a81a-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6a81a-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a81a-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a81a-118">-WhatIf</span></span>
<span data-ttu-id="6a81a-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6a81a-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6a81a-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6a81a-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a81a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a81a-121">CommonParameters</span></span>
<span data-ttu-id="6a81a-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a81a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a81a-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a81a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a81a-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6a81a-124">INPUTS</span></span>

### <span data-ttu-id="6a81a-125">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6a81a-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="6a81a-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6a81a-126">OUTPUTS</span></span>

### <span data-ttu-id="6a81a-127">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6a81a-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="6a81a-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="6a81a-128">NOTES</span></span>

## <span data-ttu-id="6a81a-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6a81a-129">RELATED LINKS</span></span>

[<span data-ttu-id="6a81a-130">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6a81a-130">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


