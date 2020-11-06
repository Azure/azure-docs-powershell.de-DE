---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMExtension.md
ms.openlocfilehash: da05148a0e27ba553f80fa18b44cb45decf9f1df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476957"
---
# <span data-ttu-id="22de1-101">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="22de1-101">Remove-AzureRmVMExtension</span></span>

## <span data-ttu-id="22de1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="22de1-102">SYNOPSIS</span></span>
<span data-ttu-id="22de1-103">Entfernt eine Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="22de1-103">Removes an extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22de1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="22de1-104">SYNTAX</span></span>

```
Remove-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22de1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22de1-105">DESCRIPTION</span></span>
<span data-ttu-id="22de1-106">Das Cmdlet " **Remove-AzureRmVMExtension** " entfernt eine Erweiterung von den Virtual Machine-Erweiterungen einer virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="22de1-106">The **Remove-AzureRmVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="22de1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="22de1-107">EXAMPLES</span></span>

### <span data-ttu-id="22de1-108">Beispiel 1: Entfernen einer Erweiterung von einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="22de1-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="22de1-109">Dieser Befehl entfernt die Erweiterung mit dem Namen ContosoTest aus dem virtuellen Computer mit dem Namen VirtualMachine22 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="22de1-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="22de1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="22de1-110">PARAMETERS</span></span>

### <span data-ttu-id="22de1-111">-Force</span><span class="sxs-lookup"><span data-stu-id="22de1-111">-Force</span></span>
<span data-ttu-id="22de1-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="22de1-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22de1-113">-Name</span><span class="sxs-lookup"><span data-stu-id="22de1-113">-Name</span></span>
<span data-ttu-id="22de1-114">Gibt den Namen der Erweiterung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="22de1-114">Specifies the name of the extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22de1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22de1-115">-ResourceGroupName</span></span>
<span data-ttu-id="22de1-116">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="22de1-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="22de1-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="22de1-117">-VMName</span></span>
<span data-ttu-id="22de1-118">Gibt den Namen eines virtuellen Computers an, von dem dieses Cmdlet die Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="22de1-118">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="22de1-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="22de1-119">-Confirm</span></span>
<span data-ttu-id="22de1-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="22de1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22de1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22de1-121">-WhatIf</span></span>
<span data-ttu-id="22de1-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="22de1-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="22de1-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="22de1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22de1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22de1-124">CommonParameters</span></span>
<span data-ttu-id="22de1-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22de1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22de1-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22de1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22de1-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="22de1-127">INPUTS</span></span>

### <span data-ttu-id="22de1-128">Keine</span><span class="sxs-lookup"><span data-stu-id="22de1-128">None</span></span>
<span data-ttu-id="22de1-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="22de1-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="22de1-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="22de1-130">OUTPUTS</span></span>

## <span data-ttu-id="22de1-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="22de1-131">NOTES</span></span>

## <span data-ttu-id="22de1-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="22de1-132">RELATED LINKS</span></span>

[<span data-ttu-id="22de1-133">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="22de1-133">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="22de1-134">Satz-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="22de1-134">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


