---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
ms.openlocfilehash: 52b090f433d3d605c870025d696b2572e6938330
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502186"
---
# <span data-ttu-id="ce630-101">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="ce630-101">Remove-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="ce630-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ce630-102">SYNOPSIS</span></span>
<span data-ttu-id="ce630-103">Entfernt eine Diagnose Erweiterung aus der VMSS.</span><span class="sxs-lookup"><span data-stu-id="ce630-103">Removes a diagnostics extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce630-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce630-104">SYNTAX</span></span>

```
Remove-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce630-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce630-105">DESCRIPTION</span></span>
<span data-ttu-id="ce630-106">Mit dem Cmdlet **Remove-AzureRmVmssDiagnosticsExtension** wird eine Diagnose Erweiterung aus dem Skalierungs Satz virtueller Computer (VMSS) entfernt.</span><span class="sxs-lookup"><span data-stu-id="ce630-106">The **Remove-AzureRmVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="ce630-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ce630-107">EXAMPLES</span></span>

### <span data-ttu-id="ce630-108">Beispiel 1: Entfernen einer Diagnose Erweiterung vom VMSS</span><span class="sxs-lookup"><span data-stu-id="ce630-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="ce630-109">Dieser Befehl entfernt die Diagnose Erweiterung aus dem VMSS.</span><span class="sxs-lookup"><span data-stu-id="ce630-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="ce630-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce630-110">PARAMETERS</span></span>

### <span data-ttu-id="ce630-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce630-111">-DefaultProfile</span></span>
<span data-ttu-id="ce630-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ce630-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce630-113">-Name</span><span class="sxs-lookup"><span data-stu-id="ce630-113">-Name</span></span>
<span data-ttu-id="ce630-114">Gibt den Namen der Erweiterung an, die dieses Cmdlet aus der VMSS entfernt.</span><span class="sxs-lookup"><span data-stu-id="ce630-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce630-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ce630-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="ce630-116">Gibt den VMSS an, aus dem die Erweiterung entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ce630-116">Specifies the VMSS from which to remove the extension.</span></span>

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

### <span data-ttu-id="ce630-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ce630-117">-Confirm</span></span>
<span data-ttu-id="ce630-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ce630-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce630-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce630-119">-WhatIf</span></span>
<span data-ttu-id="ce630-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ce630-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce630-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ce630-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce630-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce630-122">CommonParameters</span></span>
<span data-ttu-id="ce630-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce630-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce630-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce630-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce630-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ce630-125">INPUTS</span></span>

### <span data-ttu-id="ce630-126">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ce630-126">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

### <span data-ttu-id="ce630-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ce630-127">System.String</span></span>

## <span data-ttu-id="ce630-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ce630-128">OUTPUTS</span></span>

### <span data-ttu-id="ce630-129">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ce630-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="ce630-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="ce630-130">NOTES</span></span>

## <span data-ttu-id="ce630-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ce630-131">RELATED LINKS</span></span>

[<span data-ttu-id="ce630-132">Add-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="ce630-132">Add-AzureRmVmssDiagnosticsExtension</span></span>](./Add-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="ce630-133">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="ce630-133">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="ce630-134">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="ce630-134">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)


