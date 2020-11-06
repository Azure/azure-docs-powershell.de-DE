---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMChefExtension.md
ms.openlocfilehash: dc2e22acf8efd18a565c1ede7ff22aeb21679a47
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483086"
---
# <span data-ttu-id="927c3-101">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="927c3-101">Remove-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="927c3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="927c3-102">SYNOPSIS</span></span>
<span data-ttu-id="927c3-103">Entfernt die Erweiterung des Chefkochs von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="927c3-103">Removes the Chef extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="927c3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="927c3-104">SYNTAX</span></span>

### <span data-ttu-id="927c3-105">Linux</span><span class="sxs-lookup"><span data-stu-id="927c3-105">Linux</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="927c3-106">Windows</span><span class="sxs-lookup"><span data-stu-id="927c3-106">Windows</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="927c3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="927c3-107">DESCRIPTION</span></span>
<span data-ttu-id="927c3-108">Das Cmdlet **Remove-AzureVMChefExtension** entfernt die Erweiterung des Chefkochs von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="927c3-108">The **Remove-AzureVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="927c3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="927c3-109">EXAMPLES</span></span>

### <span data-ttu-id="927c3-110">Beispiel 1: Entfernen einer Chefkoch-Erweiterung von einem Windows-virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="927c3-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="927c3-111">Mit diesem Befehl wird eine Erweiterung des Chefkochs von einem Windows-basierten virtuellen Computer mit dem Namen "WindowsVM001" entfernt, der zur Ressourcengruppe mit dem Namen ResourceGroup001 gehört.</span><span class="sxs-lookup"><span data-stu-id="927c3-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="927c3-112">Beispiel 2: Entfernen einer Erweiterung des Chefkochs von einem virtuellen Linux-Computer</span><span class="sxs-lookup"><span data-stu-id="927c3-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="927c3-113">Mit diesem Befehl wird eine Erweiterung des Chefkochs von einem Linux-basierten virtuellen Computer mit dem Namen "LinuxVM001" entfernt, der zur Ressourcengruppe mit dem Namen ResourceGroup002 gehört.</span><span class="sxs-lookup"><span data-stu-id="927c3-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="927c3-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="927c3-114">PARAMETERS</span></span>

### <span data-ttu-id="927c3-115">-Linux</span><span class="sxs-lookup"><span data-stu-id="927c3-115">-Linux</span></span>
<span data-ttu-id="927c3-116">Gibt an, dass dieses Cmdlet auf einen virtuellen Linux-Computer ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="927c3-116">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="927c3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="927c3-117">-Name</span></span>
<span data-ttu-id="927c3-118">Gibt den Namen der Erweiterung des Chefkochs an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="927c3-118">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="927c3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="927c3-119">-ResourceGroupName</span></span>
<span data-ttu-id="927c3-120">Gibt den Namen der Ressourcengruppe an, die den virtuellen Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="927c3-120">Specifies the name of the resource group that contains the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="927c3-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="927c3-121">-VMName</span></span>
<span data-ttu-id="927c3-122">Gibt den Namen eines virtuellen Computers an, für den dieses Cmdlet die Erweiterung "Chef" entfernt.</span><span class="sxs-lookup"><span data-stu-id="927c3-122">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="927c3-123">-Windows</span><span class="sxs-lookup"><span data-stu-id="927c3-123">-Windows</span></span>
<span data-ttu-id="927c3-124">Gibt an, dass dieses Cmdlet auf einen virtuellen Windows-Computer ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="927c3-124">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="927c3-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="927c3-125">-Confirm</span></span>
<span data-ttu-id="927c3-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="927c3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="927c3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="927c3-127">-WhatIf</span></span>
<span data-ttu-id="927c3-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="927c3-128">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="927c3-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="927c3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="927c3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="927c3-130">CommonParameters</span></span>
<span data-ttu-id="927c3-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="927c3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="927c3-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="927c3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="927c3-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="927c3-133">INPUTS</span></span>

### <span data-ttu-id="927c3-134">Keine</span><span class="sxs-lookup"><span data-stu-id="927c3-134">None</span></span>
<span data-ttu-id="927c3-135">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="927c3-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="927c3-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="927c3-136">OUTPUTS</span></span>

## <span data-ttu-id="927c3-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="927c3-137">NOTES</span></span>

## <span data-ttu-id="927c3-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="927c3-138">RELATED LINKS</span></span>

[<span data-ttu-id="927c3-139">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="927c3-139">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="927c3-140">Satz-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="927c3-140">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)
