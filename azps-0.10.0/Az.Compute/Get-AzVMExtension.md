---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtension.md
ms.openlocfilehash: a8ac31efd77d5b8ff5c07920bb14b44f80ac0955
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844600"
---
# <span data-ttu-id="a25cb-101">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="a25cb-101">Get-AzVMExtension</span></span>

## <span data-ttu-id="a25cb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a25cb-102">SYNOPSIS</span></span>
<span data-ttu-id="a25cb-103">Ruft Eigenschaften der auf einem virtuellen Computer installierten Virtual Machine-Erweiterungen ab.</span><span class="sxs-lookup"><span data-stu-id="a25cb-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

## <span data-ttu-id="a25cb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a25cb-104">SYNTAX</span></span>

```
Get-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a25cb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a25cb-105">DESCRIPTION</span></span>
<span data-ttu-id="a25cb-106">Das Cmdlet " **Get-AzVMExtension** " Ruft Eigenschaften der auf einem virtuellen Computer installierten Virtual Machine-Erweiterungen ab.</span><span class="sxs-lookup"><span data-stu-id="a25cb-106">The **Get-AzVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="a25cb-107">Geben Sie den Namen einer Erweiterung an, für die Eigenschaften abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a25cb-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="a25cb-108">Um nur die Instanzen Ansicht einer Erweiterung abzurufen, geben Sie den Parameter Status an.</span><span class="sxs-lookup"><span data-stu-id="a25cb-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="a25cb-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a25cb-109">EXAMPLES</span></span>

### <span data-ttu-id="a25cb-110">Beispiel 1: Abrufen von Eigenschaften einer Erweiterung</span><span class="sxs-lookup"><span data-stu-id="a25cb-110">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"
```

<span data-ttu-id="a25cb-111">Dieser Befehl ruft Eigenschaften für die Erweiterung mit dem Namen CustomScriptExtension auf dem virtuellen Computer mit dem Namen VirtualMachine22 in der Ressourcengruppe ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="a25cb-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="a25cb-112">Beispiel 2: Abrufen der Instanzen Ansicht einer Erweiterung</span><span class="sxs-lookup"><span data-stu-id="a25cb-112">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status
```

<span data-ttu-id="a25cb-113">Dieser Befehl ruft die Instanzen Ansicht für die Erweiterung mit dem Namen CustomScriptExtension auf dem virtuellen Computer mit dem Namen VirtualMachine22 in der Ressourcengruppe ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="a25cb-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="a25cb-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a25cb-114">PARAMETERS</span></span>

### <span data-ttu-id="a25cb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a25cb-115">-DefaultProfile</span></span>
<span data-ttu-id="a25cb-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a25cb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a25cb-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a25cb-117">-Name</span></span>
<span data-ttu-id="a25cb-118">Gibt den Namen einer Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="a25cb-118">Specifies the name of an extension.</span></span>
<span data-ttu-id="a25cb-119">Dieses Cmdlet ruft Eigenschaften für die Erweiterung ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a25cb-119">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

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

### <span data-ttu-id="a25cb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a25cb-120">-ResourceGroupName</span></span>
<span data-ttu-id="a25cb-121">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="a25cb-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a25cb-122">-Status</span><span class="sxs-lookup"><span data-stu-id="a25cb-122">-Status</span></span>
<span data-ttu-id="a25cb-123">Gibt an, dass dieses Cmdlet nur die Instanzen Ansicht einer Erweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="a25cb-123">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="a25cb-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="a25cb-124">-VMName</span></span>
<span data-ttu-id="a25cb-125">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="a25cb-125">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="a25cb-126">Dieses Cmdlet ruft Eigenschaften einer Erweiterung vom virtuellen Computer ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a25cb-126">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="a25cb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a25cb-127">CommonParameters</span></span>
<span data-ttu-id="a25cb-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a25cb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a25cb-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a25cb-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a25cb-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a25cb-130">INPUTS</span></span>

### <span data-ttu-id="a25cb-131">Keine</span><span class="sxs-lookup"><span data-stu-id="a25cb-131">None</span></span>
<span data-ttu-id="a25cb-132">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="a25cb-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a25cb-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a25cb-133">OUTPUTS</span></span>

### <span data-ttu-id="a25cb-134">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="a25cb-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="a25cb-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="a25cb-135">NOTES</span></span>

## <span data-ttu-id="a25cb-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a25cb-136">RELATED LINKS</span></span>

[<span data-ttu-id="a25cb-137">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="a25cb-137">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)

[<span data-ttu-id="a25cb-138">Satz-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="a25cb-138">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


