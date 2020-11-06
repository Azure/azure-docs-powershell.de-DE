---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDscExtension.md
ms.openlocfilehash: b3e9f8703b2130426d98a4a59fe25eb2f3f8fbdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476962"
---
# <span data-ttu-id="be2a7-101">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="be2a7-101">Remove-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="be2a7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="be2a7-102">SYNOPSIS</span></span>
<span data-ttu-id="be2a7-103">Entfernt einen DSC-Erweiterungshandler von einem virtuellen Computer in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="be2a7-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be2a7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="be2a7-104">SYNTAX</span></span>

```
Remove-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be2a7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="be2a7-105">DESCRIPTION</span></span>
<span data-ttu-id="be2a7-106">Mit dem Cmdlet **Remove-AzureRmVMDscExtension** wird der Erweiterungshandler für die gewünschte Zustands Konfiguration (DSC) von einem virtuellen Computer in einer Ressourcengruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="be2a7-106">The **Remove-AzureRmVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="be2a7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="be2a7-107">EXAMPLES</span></span>

### <span data-ttu-id="be2a7-108">Beispiel 1: Entfernen einer DSC-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="be2a7-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzureRmVMDscExtension -ResouceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="be2a7-109">Dieser Befehl entfernt die Erweiterung mit dem Namen DSC auf dem virtuellen Computer mit dem Namen VM07.</span><span class="sxs-lookup"><span data-stu-id="be2a7-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="be2a7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="be2a7-110">PARAMETERS</span></span>

### <span data-ttu-id="be2a7-111">-Name</span><span class="sxs-lookup"><span data-stu-id="be2a7-111">-Name</span></span>
<span data-ttu-id="be2a7-112">Gibt den Namen der DSC-Erweiterung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="be2a7-112">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="be2a7-113">Mit dem Set-AzureRmVMDscExtension-Cmdlet wird dieser Name auf Microsoft. PowerShell. DSC festgelegt, bei dem es sich um den Standardwert handelt, der von **Remove-AzureRmVMDscExtension** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="be2a7-113">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzureRmVMDscExtension**.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be2a7-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be2a7-114">-ResourceGroupName</span></span>
<span data-ttu-id="be2a7-115">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="be2a7-115">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="be2a7-116">-VMName</span><span class="sxs-lookup"><span data-stu-id="be2a7-116">-VMName</span></span>
<span data-ttu-id="be2a7-117">Gibt den Namen eines virtuellen Computers an, von dem dieses Cmdlet die DSC-Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="be2a7-117">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

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

### <span data-ttu-id="be2a7-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="be2a7-118">-Confirm</span></span>
<span data-ttu-id="be2a7-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="be2a7-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be2a7-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be2a7-120">-WhatIf</span></span>
<span data-ttu-id="be2a7-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="be2a7-121">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="be2a7-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="be2a7-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be2a7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be2a7-123">CommonParameters</span></span>
<span data-ttu-id="be2a7-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be2a7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be2a7-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be2a7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be2a7-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="be2a7-126">INPUTS</span></span>

### <span data-ttu-id="be2a7-127">Keine</span><span class="sxs-lookup"><span data-stu-id="be2a7-127">None</span></span>
<span data-ttu-id="be2a7-128">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="be2a7-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="be2a7-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="be2a7-129">OUTPUTS</span></span>

## <span data-ttu-id="be2a7-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="be2a7-130">NOTES</span></span>

## <span data-ttu-id="be2a7-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="be2a7-131">RELATED LINKS</span></span>

[<span data-ttu-id="be2a7-132">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="be2a7-132">Get-AzureRmVMDscExtension</span></span>](./Get-AzureRmVMDscExtension.md)

[<span data-ttu-id="be2a7-133">Satz-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="be2a7-133">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


