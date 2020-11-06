---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmss.md
ms.openlocfilehash: 9837098586212cfa777c01fcb76a0db05f39eaf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497705"
---
# <span data-ttu-id="2d4ee-101">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2d4ee-101">Remove-AzureRmVmss</span></span>

## <span data-ttu-id="2d4ee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2d4ee-102">SYNOPSIS</span></span>
<span data-ttu-id="2d4ee-103">Entfernt das VMSS oder einen virtuellen Computer, der sich innerhalb des VMSS befindet.</span><span class="sxs-lookup"><span data-stu-id="2d4ee-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d4ee-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d4ee-104">SYNTAX</span></span>

```
Remove-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d4ee-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2d4ee-105">DESCRIPTION</span></span>
<span data-ttu-id="2d4ee-106">Das Cmdlet **Remove-AzureRmVmss** entfernt den virtuellen Computer-Skalierungs Satz (VMSS) aus Azure.</span><span class="sxs-lookup"><span data-stu-id="2d4ee-106">The **Remove-AzureRmVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="2d4ee-107">Dieses Cmdlet kann auch verwendet werden, um einen bestimmten virtuellen Computer innerhalb des VMSS zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="2d4ee-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="2d4ee-108">Sie können den *InstanceId* -Parameter verwenden, um einen bestimmten virtuellen Computer innerhalb des VMSS zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="2d4ee-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="2d4ee-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2d4ee-109">EXAMPLES</span></span>

### <span data-ttu-id="2d4ee-110">Beispiel 1: Entfernen eines VMSS</span><span class="sxs-lookup"><span data-stu-id="2d4ee-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="2d4ee-111">Mit diesem Befehl wird der VMSS mit dem Namen VMScaleSet001 entfernt, der zur Ressourcengruppe mit dem Namen Group001 gehört.</span><span class="sxs-lookup"><span data-stu-id="2d4ee-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="2d4ee-112">Beispiel 2: Entfernen eines virtuellen Computers in einem VMSS</span><span class="sxs-lookup"><span data-stu-id="2d4ee-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="2d4ee-113">Dieser Befehl entfernt den virtuellen Computer mit Instanz-ID 3 aus dem VMSS mit dem Namen VMScaleSet002, der zur Ressourcengruppe mit dem Namen Group002 gehört.</span><span class="sxs-lookup"><span data-stu-id="2d4ee-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="2d4ee-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d4ee-114">PARAMETERS</span></span>

### <span data-ttu-id="2d4ee-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2d4ee-115">-Force</span></span>
<span data-ttu-id="2d4ee-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="2d4ee-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d4ee-117">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="2d4ee-117">-InstanceId</span></span>
<span data-ttu-id="2d4ee-118">Gibt als Zeichenfolgenarray die ID der Instanzen an, die gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="2d4ee-118">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="2d4ee-119">Zum Beispiel: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="2d4ee-119">For instance: `-InstanceId "0", "3"`</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d4ee-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d4ee-120">-ResourceGroupName</span></span>
<span data-ttu-id="2d4ee-121">Gibt den Namen der Ressourcengruppe an, zu der der VMSS gehört.</span><span class="sxs-lookup"><span data-stu-id="2d4ee-121">Specifies the name of the resource group that the VMSS belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d4ee-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="2d4ee-122">-VMScaleSetName</span></span>
<span data-ttu-id="2d4ee-123">Art der Name des VMSS, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="2d4ee-123">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="2d4ee-124">Wenn Sie den *InstanceId* -Parameter angeben, entfernt das Cmdlet den angegebenen virtuellen Computer aus dem VMSS, der durch diesen Parameter benannt wird.</span><span class="sxs-lookup"><span data-stu-id="2d4ee-124">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d4ee-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2d4ee-125">-Confirm</span></span>
<span data-ttu-id="2d4ee-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2d4ee-126">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="2d4ee-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d4ee-127">-WhatIf</span></span>
<span data-ttu-id="2d4ee-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d4ee-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d4ee-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d4ee-129">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="2d4ee-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d4ee-130">CommonParameters</span></span>
<span data-ttu-id="2d4ee-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d4ee-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d4ee-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d4ee-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d4ee-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2d4ee-133">INPUTS</span></span>

### <span data-ttu-id="2d4ee-134">Keine</span><span class="sxs-lookup"><span data-stu-id="2d4ee-134">None</span></span>
<span data-ttu-id="2d4ee-135">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="2d4ee-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2d4ee-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2d4ee-136">OUTPUTS</span></span>

## <span data-ttu-id="2d4ee-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="2d4ee-137">NOTES</span></span>

## <span data-ttu-id="2d4ee-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2d4ee-138">RELATED LINKS</span></span>

[<span data-ttu-id="2d4ee-139">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2d4ee-139">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="2d4ee-140">Neu – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2d4ee-140">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="2d4ee-141">Neustart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2d4ee-141">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="2d4ee-142">Satz-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2d4ee-142">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="2d4ee-143">Anfang-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2d4ee-143">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="2d4ee-144">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2d4ee-144">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="2d4ee-145">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2d4ee-145">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


