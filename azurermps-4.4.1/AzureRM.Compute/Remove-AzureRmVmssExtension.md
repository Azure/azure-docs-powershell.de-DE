---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
ms.openlocfilehash: f99df428f99ec0e75eb4b1b220dde657be6f7458
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477278"
---
# <span data-ttu-id="6cd52-101">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="6cd52-101">Remove-AzureRmVmssExtension</span></span>

## <span data-ttu-id="6cd52-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6cd52-102">SYNOPSIS</span></span>
<span data-ttu-id="6cd52-103">Entfernt eine Erweiterung aus der VMSS.</span><span class="sxs-lookup"><span data-stu-id="6cd52-103">Removes an extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cd52-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6cd52-104">SYNTAX</span></span>

### <span data-ttu-id="6cd52-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cd52-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cd52-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cd52-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cd52-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6cd52-107">DESCRIPTION</span></span>
<span data-ttu-id="6cd52-108">Das Cmdlet **Remove-AzureRmVmssExtension** entfernt eine Erweiterung aus dem Skalierungs Satz virtueller Computer (VMSS).</span><span class="sxs-lookup"><span data-stu-id="6cd52-108">The **Remove-AzureRmVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="6cd52-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6cd52-109">EXAMPLES</span></span>

## <span data-ttu-id="6cd52-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6cd52-110">PARAMETERS</span></span>

### <span data-ttu-id="6cd52-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cd52-111">-DefaultProfile</span></span>
<span data-ttu-id="6cd52-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6cd52-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cd52-113">-ID</span><span class="sxs-lookup"><span data-stu-id="6cd52-113">-Id</span></span>
<span data-ttu-id="6cd52-114">Gibt die ID der Erweiterung an, die dieses Cmdlet aus der VMSS entfernt.</span><span class="sxs-lookup"><span data-stu-id="6cd52-114">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="6cd52-115">-Name</span><span class="sxs-lookup"><span data-stu-id="6cd52-115">-Name</span></span>
<span data-ttu-id="6cd52-116">Gibt den Namen der Erweiterung an, die dieses Cmdlet aus der VMSS entfernt.</span><span class="sxs-lookup"><span data-stu-id="6cd52-116">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="6cd52-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6cd52-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="6cd52-118">Gibt den VMSS an, aus dem die Erweiterung entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6cd52-118">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="6cd52-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6cd52-119">-Confirm</span></span>
<span data-ttu-id="6cd52-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6cd52-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cd52-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cd52-121">-WhatIf</span></span>
<span data-ttu-id="6cd52-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6cd52-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6cd52-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6cd52-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cd52-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cd52-124">CommonParameters</span></span>
<span data-ttu-id="6cd52-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cd52-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cd52-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cd52-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cd52-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6cd52-127">INPUTS</span></span>

## <span data-ttu-id="6cd52-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6cd52-128">OUTPUTS</span></span>

### <span data-ttu-id="6cd52-129">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="6cd52-129">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="6cd52-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="6cd52-130">NOTES</span></span>

## <span data-ttu-id="6cd52-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6cd52-131">RELATED LINKS</span></span>

[<span data-ttu-id="6cd52-132">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="6cd52-132">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)
