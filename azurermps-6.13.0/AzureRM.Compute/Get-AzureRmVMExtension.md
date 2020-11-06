---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMExtension.md
ms.openlocfilehash: 4aaee403007561797614b2534e29c5918dad3643
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501161"
---
# <span data-ttu-id="fb562-101">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="fb562-101">Get-AzureRmVMExtension</span></span>

## <span data-ttu-id="fb562-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fb562-102">SYNOPSIS</span></span>
<span data-ttu-id="fb562-103">Ruft Eigenschaften der auf einem virtuellen Computer installierten Virtual Machine-Erweiterungen ab.</span><span class="sxs-lookup"><span data-stu-id="fb562-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb562-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb562-104">SYNTAX</span></span>

```
Get-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb562-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb562-105">DESCRIPTION</span></span>
<span data-ttu-id="fb562-106">Das Cmdlet " **Get-AzureRmVMExtension** " Ruft Eigenschaften der auf einem virtuellen Computer installierten Virtual Machine-Erweiterungen ab.</span><span class="sxs-lookup"><span data-stu-id="fb562-106">The **Get-AzureRmVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="fb562-107">Geben Sie den Namen einer Erweiterung an, für die Eigenschaften abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fb562-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="fb562-108">Um nur die Instanzen Ansicht einer Erweiterung abzurufen, geben Sie den Parameter Status an.</span><span class="sxs-lookup"><span data-stu-id="fb562-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="fb562-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fb562-109">EXAMPLES</span></span>

### <span data-ttu-id="fb562-110">Beispiel 1: Abrufen von Eigenschaften einer Erweiterung</span><span class="sxs-lookup"><span data-stu-id="fb562-110">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"
```

<span data-ttu-id="fb562-111">Dieser Befehl ruft Eigenschaften für die Erweiterung mit dem Namen CustomScriptExtension auf dem virtuellen Computer mit dem Namen VirtualMachine22 in der Ressourcengruppe ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="fb562-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="fb562-112">Beispiel 2: Abrufen der Instanzen Ansicht einer Erweiterung</span><span class="sxs-lookup"><span data-stu-id="fb562-112">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status
```

<span data-ttu-id="fb562-113">Dieser Befehl ruft die Instanzen Ansicht für die Erweiterung mit dem Namen CustomScriptExtension auf dem virtuellen Computer mit dem Namen VirtualMachine22 in der Ressourcengruppe ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="fb562-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="fb562-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb562-114">PARAMETERS</span></span>

### <span data-ttu-id="fb562-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb562-115">-DefaultProfile</span></span>
<span data-ttu-id="fb562-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fb562-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb562-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fb562-117">-Name</span></span>
<span data-ttu-id="fb562-118">Gibt den Namen einer Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="fb562-118">Specifies the name of an extension.</span></span>
<span data-ttu-id="fb562-119">Dieses Cmdlet ruft Eigenschaften für die Erweiterung ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="fb562-119">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb562-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb562-120">-ResourceGroupName</span></span>
<span data-ttu-id="fb562-121">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="fb562-121">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb562-122">-Status</span><span class="sxs-lookup"><span data-stu-id="fb562-122">-Status</span></span>
<span data-ttu-id="fb562-123">Gibt an, dass dieses Cmdlet nur die Instanzen Ansicht einer Erweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="fb562-123">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb562-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="fb562-124">-VMName</span></span>
<span data-ttu-id="fb562-125">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="fb562-125">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="fb562-126">Dieses Cmdlet ruft Eigenschaften einer Erweiterung vom virtuellen Computer ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="fb562-126">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb562-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb562-127">CommonParameters</span></span>
<span data-ttu-id="fb562-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb562-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb562-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb562-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb562-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fb562-130">INPUTS</span></span>

### <span data-ttu-id="fb562-131">System. String</span><span class="sxs-lookup"><span data-stu-id="fb562-131">System.String</span></span>

### <span data-ttu-id="fb562-132">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="fb562-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fb562-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fb562-133">OUTPUTS</span></span>

### <span data-ttu-id="fb562-134">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="fb562-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="fb562-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="fb562-135">NOTES</span></span>

## <span data-ttu-id="fb562-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fb562-136">RELATED LINKS</span></span>

[<span data-ttu-id="fb562-137">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="fb562-137">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)

[<span data-ttu-id="fb562-138">Satz-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="fb562-138">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


