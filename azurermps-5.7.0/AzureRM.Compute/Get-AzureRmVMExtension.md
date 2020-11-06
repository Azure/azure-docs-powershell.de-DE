---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtension.md
ms.openlocfilehash: 82ab2f02d47b17342f71b09eebe826fc48c07b81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478629"
---
# <span data-ttu-id="2aeef-101">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="2aeef-101">Get-AzureRmVMExtension</span></span>

## <span data-ttu-id="2aeef-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2aeef-102">SYNOPSIS</span></span>
<span data-ttu-id="2aeef-103">Ruft Eigenschaften der auf einem virtuellen Computer installierten Virtual Machine-Erweiterungen ab.</span><span class="sxs-lookup"><span data-stu-id="2aeef-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2aeef-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2aeef-104">SYNTAX</span></span>

```
Get-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="2aeef-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2aeef-105">DESCRIPTION</span></span>
<span data-ttu-id="2aeef-106">Das Cmdlet " **Get-AzureRmVMExtension** " Ruft Eigenschaften der auf einem virtuellen Computer installierten Virtual Machine-Erweiterungen ab.</span><span class="sxs-lookup"><span data-stu-id="2aeef-106">The **Get-AzureRmVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="2aeef-107">Geben Sie den Namen einer Erweiterung an, für die Eigenschaften abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2aeef-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="2aeef-108">Um nur die Instanzen Ansicht einer Erweiterung abzurufen, geben Sie den Parameter Status an.</span><span class="sxs-lookup"><span data-stu-id="2aeef-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="2aeef-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2aeef-109">EXAMPLES</span></span>

### <span data-ttu-id="2aeef-110">Beispiel 1: Abrufen von Eigenschaften einer Erweiterung</span><span class="sxs-lookup"><span data-stu-id="2aeef-110">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"
```

<span data-ttu-id="2aeef-111">Dieser Befehl ruft Eigenschaften für die Erweiterung mit dem Namen CustomScriptExtension auf dem virtuellen Computer mit dem Namen VirtualMachine22 in der Ressourcengruppe ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="2aeef-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="2aeef-112">Beispiel 2: Abrufen der Instanzen Ansicht einer Erweiterung</span><span class="sxs-lookup"><span data-stu-id="2aeef-112">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status
```

<span data-ttu-id="2aeef-113">Dieser Befehl ruft die Instanzen Ansicht für die Erweiterung mit dem Namen CustomScriptExtension auf dem virtuellen Computer mit dem Namen VirtualMachine22 in der Ressourcengruppe ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="2aeef-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="2aeef-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2aeef-114">PARAMETERS</span></span>

### <span data-ttu-id="2aeef-115">-Name</span><span class="sxs-lookup"><span data-stu-id="2aeef-115">-Name</span></span>
<span data-ttu-id="2aeef-116">Gibt den Namen einer Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="2aeef-116">Specifies the name of an extension.</span></span>
<span data-ttu-id="2aeef-117">Dieses Cmdlet ruft Eigenschaften für die Erweiterung ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="2aeef-117">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

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

### <span data-ttu-id="2aeef-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2aeef-118">-ResourceGroupName</span></span>
<span data-ttu-id="2aeef-119">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2aeef-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2aeef-120">-Status</span><span class="sxs-lookup"><span data-stu-id="2aeef-120">-Status</span></span>
<span data-ttu-id="2aeef-121">Gibt an, dass dieses Cmdlet nur die Instanzen Ansicht einer Erweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="2aeef-121">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="2aeef-122">-VMName</span><span class="sxs-lookup"><span data-stu-id="2aeef-122">-VMName</span></span>
<span data-ttu-id="2aeef-123">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="2aeef-123">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="2aeef-124">Dieses Cmdlet ruft Eigenschaften einer Erweiterung vom virtuellen Computer ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="2aeef-124">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="2aeef-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aeef-125">CommonParameters</span></span>
<span data-ttu-id="2aeef-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aeef-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aeef-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2aeef-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aeef-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2aeef-128">INPUTS</span></span>

### <span data-ttu-id="2aeef-129">Keine</span><span class="sxs-lookup"><span data-stu-id="2aeef-129">None</span></span>
<span data-ttu-id="2aeef-130">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="2aeef-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2aeef-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2aeef-131">OUTPUTS</span></span>

## <span data-ttu-id="2aeef-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="2aeef-132">NOTES</span></span>

## <span data-ttu-id="2aeef-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2aeef-133">RELATED LINKS</span></span>

[<span data-ttu-id="2aeef-134">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="2aeef-134">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)

[<span data-ttu-id="2aeef-135">Satz-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="2aeef-135">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


