---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssExtension.md
ms.openlocfilehash: 8044be4e6d9c353dd50420fe73066a8f47d53855
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844327"
---
# <span data-ttu-id="deda4-101">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="deda4-101">Remove-AzVmssExtension</span></span>

## <span data-ttu-id="deda4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="deda4-102">SYNOPSIS</span></span>
<span data-ttu-id="deda4-103">Entfernt eine Erweiterung aus der VMSS.</span><span class="sxs-lookup"><span data-stu-id="deda4-103">Removes an extension from the VMSS.</span></span>

## <span data-ttu-id="deda4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="deda4-104">SYNTAX</span></span>

### <span data-ttu-id="deda4-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="deda4-105">NameParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="deda4-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="deda4-106">IdParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="deda4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="deda4-107">DESCRIPTION</span></span>
<span data-ttu-id="deda4-108">Das Cmdlet **Remove-AzVmssExtension** entfernt eine Erweiterung aus dem Skalierungs Satz virtueller Computer (VMSS).</span><span class="sxs-lookup"><span data-stu-id="deda4-108">The **Remove-AzVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="deda4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="deda4-109">EXAMPLES</span></span>

### <span data-ttu-id="deda4-110">Beispiel 1: Entfernen der Erweiterung vom VMSS</span><span class="sxs-lookup"><span data-stu-id="deda4-110">Example 1: Remove extension from the VMSS</span></span>
```
PS C:\> Remove-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

## <span data-ttu-id="deda4-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="deda4-111">PARAMETERS</span></span>

### <span data-ttu-id="deda4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deda4-112">-DefaultProfile</span></span>
<span data-ttu-id="deda4-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="deda4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="deda4-114">-ID</span><span class="sxs-lookup"><span data-stu-id="deda4-114">-Id</span></span>
<span data-ttu-id="deda4-115">Gibt die ID der Erweiterung an, die dieses Cmdlet aus der VMSS entfernt.</span><span class="sxs-lookup"><span data-stu-id="deda4-115">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="deda4-116">-Name</span><span class="sxs-lookup"><span data-stu-id="deda4-116">-Name</span></span>
<span data-ttu-id="deda4-117">Gibt den Namen der Erweiterung an, die dieses Cmdlet aus der VMSS entfernt.</span><span class="sxs-lookup"><span data-stu-id="deda4-117">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="deda4-118">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="deda4-118">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="deda4-119">Gibt den VMSS an, aus dem die Erweiterung entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="deda4-119">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="deda4-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="deda4-120">-Confirm</span></span>
<span data-ttu-id="deda4-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="deda4-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="deda4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="deda4-122">-WhatIf</span></span>
<span data-ttu-id="deda4-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="deda4-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="deda4-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="deda4-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="deda4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deda4-125">CommonParameters</span></span>
<span data-ttu-id="deda4-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="deda4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deda4-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="deda4-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deda4-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="deda4-128">INPUTS</span></span>

### <span data-ttu-id="deda4-129">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="deda4-129">VirtualMachineScaleSet</span></span>
<span data-ttu-id="deda4-130">Der Parameter "VirtualMachineScaleSet" akzeptiert den Wert vom Typ "VirtualMachineScaleSet" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="deda4-130">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="deda4-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="deda4-131">OUTPUTS</span></span>

### <span data-ttu-id="deda4-132">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="deda4-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="deda4-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="deda4-133">NOTES</span></span>

## <span data-ttu-id="deda4-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="deda4-134">RELATED LINKS</span></span>

[<span data-ttu-id="deda4-135">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="deda4-135">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)
