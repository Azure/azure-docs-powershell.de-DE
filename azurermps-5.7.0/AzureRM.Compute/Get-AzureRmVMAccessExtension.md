---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
ms.openlocfilehash: 9e7cb85bf29d6982271768af6948db1d3c5b8605
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481333"
---
# <span data-ttu-id="5966d-101">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="5966d-101">Get-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="5966d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5966d-102">SYNOPSIS</span></span>
<span data-ttu-id="5966d-103">Ruft Informationen zur VMAccess-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="5966d-103">Gets information about the VMAccess extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5966d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5966d-104">SYNTAX</span></span>

```
Get-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="5966d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5966d-105">DESCRIPTION</span></span>
<span data-ttu-id="5966d-106">Das Cmdlet " **Get-AzureRmVMAccessExtension** " Ruft Informationen zur virtuellen Computererweiterung (Virtual Machine Access, VMAccess) ab.</span><span class="sxs-lookup"><span data-stu-id="5966d-106">The **Get-AzureRmVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="5966d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5966d-107">EXAMPLES</span></span>

### <span data-ttu-id="5966d-108">Beispiel 1: Abrufen der VMAccess-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="5966d-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="5966d-109">Dieser Befehl ruft die VMAccess-Erweiterung mit dem Namen ContosoTest für den virtuellen Computer mit dem Namen VirtualMachine07 ab.</span><span class="sxs-lookup"><span data-stu-id="5966d-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="5966d-110">Beispiel 2: Abrufen der Instanzen Ansicht der VMAccess-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="5966d-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="5966d-111">Dieser Befehl ruft die Instanzen Ansicht der VMAccess-Erweiterung mit dem Namen ContosoTest für den virtuellen Computer mit dem Namen VirtualMachine07 ab.</span><span class="sxs-lookup"><span data-stu-id="5966d-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="5966d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5966d-112">PARAMETERS</span></span>

### <span data-ttu-id="5966d-113">-Name</span><span class="sxs-lookup"><span data-stu-id="5966d-113">-Name</span></span>
<span data-ttu-id="5966d-114">Gibt den Namen der Erweiterung an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5966d-114">Specifies the name of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5966d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5966d-115">-ResourceGroupName</span></span>
<span data-ttu-id="5966d-116">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="5966d-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="5966d-117">-Status</span><span class="sxs-lookup"><span data-stu-id="5966d-117">-Status</span></span>
<span data-ttu-id="5966d-118">Gibt an, dass dieses Cmdlet nur die Instanzen Ansicht der Erweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="5966d-118">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5966d-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="5966d-119">-VMName</span></span>
<span data-ttu-id="5966d-120">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="5966d-120">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="5966d-121">Dieses Cmdlet ruft Informationen zu VMAccess für den virtuellen Computer ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="5966d-121">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="5966d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5966d-122">CommonParameters</span></span>
<span data-ttu-id="5966d-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5966d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5966d-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5966d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5966d-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5966d-125">INPUTS</span></span>

### <span data-ttu-id="5966d-126">Keine</span><span class="sxs-lookup"><span data-stu-id="5966d-126">None</span></span>
<span data-ttu-id="5966d-127">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="5966d-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5966d-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5966d-128">OUTPUTS</span></span>

## <span data-ttu-id="5966d-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="5966d-129">NOTES</span></span>

## <span data-ttu-id="5966d-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5966d-130">RELATED LINKS</span></span>

[<span data-ttu-id="5966d-131">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="5966d-131">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="5966d-132">Satz-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="5966d-132">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="5966d-133">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="5966d-133">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)


