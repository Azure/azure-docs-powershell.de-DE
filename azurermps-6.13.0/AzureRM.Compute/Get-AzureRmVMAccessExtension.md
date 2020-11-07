---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
ms.openlocfilehash: 889bd206566b9c722aa187f9e32a76c1711af337
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662522"
---
# <span data-ttu-id="d2dec-101">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d2dec-101">Get-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="d2dec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d2dec-102">SYNOPSIS</span></span>
<span data-ttu-id="d2dec-103">Ruft Informationen zur VMAccess-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="d2dec-103">Gets information about the VMAccess extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2dec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2dec-104">SYNTAX</span></span>

```
Get-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2dec-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d2dec-105">DESCRIPTION</span></span>
<span data-ttu-id="d2dec-106">Das Cmdlet " **Get-AzureRmVMAccessExtension** " Ruft Informationen zur virtuellen Computererweiterung (Virtual Machine Access, VMAccess) ab.</span><span class="sxs-lookup"><span data-stu-id="d2dec-106">The **Get-AzureRmVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="d2dec-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d2dec-107">EXAMPLES</span></span>

### <span data-ttu-id="d2dec-108">Beispiel 1: Abrufen der VMAccess-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="d2dec-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="d2dec-109">Dieser Befehl ruft die VMAccess-Erweiterung mit dem Namen ContosoTest für den virtuellen Computer mit dem Namen VirtualMachine07 ab.</span><span class="sxs-lookup"><span data-stu-id="d2dec-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="d2dec-110">Beispiel 2: Abrufen der Instanzen Ansicht der VMAccess-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="d2dec-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="d2dec-111">Dieser Befehl ruft die Instanzen Ansicht der VMAccess-Erweiterung mit dem Namen ContosoTest für den virtuellen Computer mit dem Namen VirtualMachine07 ab.</span><span class="sxs-lookup"><span data-stu-id="d2dec-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="d2dec-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2dec-112">PARAMETERS</span></span>

### <span data-ttu-id="d2dec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2dec-113">-DefaultProfile</span></span>
<span data-ttu-id="d2dec-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d2dec-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2dec-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d2dec-115">-Name</span></span>
<span data-ttu-id="d2dec-116">Gibt den Namen der Erweiterung an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="d2dec-116">Specifies the name of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d2dec-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2dec-117">-ResourceGroupName</span></span>
<span data-ttu-id="d2dec-118">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="d2dec-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d2dec-119">-Status</span><span class="sxs-lookup"><span data-stu-id="d2dec-119">-Status</span></span>
<span data-ttu-id="d2dec-120">Gibt an, dass dieses Cmdlet nur die Instanzen Ansicht der Erweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="d2dec-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

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

### <span data-ttu-id="d2dec-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="d2dec-121">-VMName</span></span>
<span data-ttu-id="d2dec-122">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="d2dec-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="d2dec-123">Dieses Cmdlet ruft Informationen zu VMAccess für den virtuellen Computer ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d2dec-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="d2dec-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2dec-124">CommonParameters</span></span>
<span data-ttu-id="d2dec-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2dec-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2dec-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2dec-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2dec-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d2dec-127">INPUTS</span></span>

### <span data-ttu-id="d2dec-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d2dec-128">System.String</span></span>

### <span data-ttu-id="d2dec-129">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="d2dec-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d2dec-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d2dec-130">OUTPUTS</span></span>

### <span data-ttu-id="d2dec-131">Microsoft. Azure. Commands. Compute. Models. VirtualMachineAccessExtensionContext</span><span class="sxs-lookup"><span data-stu-id="d2dec-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="d2dec-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="d2dec-132">NOTES</span></span>

## <span data-ttu-id="d2dec-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d2dec-133">RELATED LINKS</span></span>

[<span data-ttu-id="d2dec-134">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d2dec-134">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="d2dec-135">Satz-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d2dec-135">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="d2dec-136">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="d2dec-136">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)


