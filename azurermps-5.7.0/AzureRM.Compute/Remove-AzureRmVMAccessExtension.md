---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
ms.openlocfilehash: 16095113dcc0604bfb7b739b1227db337a0cf6f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483089"
---
# <span data-ttu-id="7b29f-101">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="7b29f-101">Remove-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="7b29f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7b29f-102">SYNOPSIS</span></span>
<span data-ttu-id="7b29f-103">Entfernt die VMAccess-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="7b29f-103">Removes the VMAccess extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b29f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b29f-104">SYNTAX</span></span>

```
Remove-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b29f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b29f-105">DESCRIPTION</span></span>
<span data-ttu-id="7b29f-106">Das Cmdlet **Remove-AzureRmVMAccessExtension** entfernt die Virtual Machine Access-Erweiterung (Virtual Machine Access, VMAccess) von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="7b29f-106">The **Remove-AzureRmVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="7b29f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7b29f-107">EXAMPLES</span></span>

## <span data-ttu-id="7b29f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b29f-108">PARAMETERS</span></span>

### <span data-ttu-id="7b29f-109">-Force</span><span class="sxs-lookup"><span data-stu-id="7b29f-109">-Force</span></span>
<span data-ttu-id="7b29f-110">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="7b29f-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7b29f-111">-Name</span><span class="sxs-lookup"><span data-stu-id="7b29f-111">-Name</span></span>
<span data-ttu-id="7b29f-112">Gibt den Namen der Erweiterung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="7b29f-112">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7b29f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b29f-113">-ResourceGroupName</span></span>
<span data-ttu-id="7b29f-114">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="7b29f-114">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7b29f-115">-VMName</span><span class="sxs-lookup"><span data-stu-id="7b29f-115">-VMName</span></span>
<span data-ttu-id="7b29f-116">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="7b29f-116">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="7b29f-117">Dieses Cmdlet entfernt VMAccess für den virtuellen Computer, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="7b29f-117">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="7b29f-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7b29f-118">-Confirm</span></span>
<span data-ttu-id="7b29f-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7b29f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b29f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b29f-120">-WhatIf</span></span>
<span data-ttu-id="7b29f-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7b29f-121">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="7b29f-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7b29f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b29f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b29f-123">CommonParameters</span></span>
<span data-ttu-id="7b29f-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b29f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b29f-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b29f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b29f-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7b29f-126">INPUTS</span></span>

### <span data-ttu-id="7b29f-127">Keine</span><span class="sxs-lookup"><span data-stu-id="7b29f-127">None</span></span>
<span data-ttu-id="7b29f-128">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="7b29f-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7b29f-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7b29f-129">OUTPUTS</span></span>

## <span data-ttu-id="7b29f-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="7b29f-130">NOTES</span></span>

## <span data-ttu-id="7b29f-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7b29f-131">RELATED LINKS</span></span>

[<span data-ttu-id="7b29f-132">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="7b29f-132">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="7b29f-133">Satz-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="7b29f-133">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="7b29f-134">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="7b29f-134">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)
