---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaccessextension
schema: 2.0.0
ms.openlocfilehash: 5d07d90e7a9902713be3ef4d2acf3a2650e4f1b4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848899"
---
# <span data-ttu-id="e2f25-101">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="e2f25-101">Get-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="e2f25-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e2f25-102">SYNOPSIS</span></span>
<span data-ttu-id="e2f25-103">Ruft Informationen zur VMAccess-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="e2f25-103">Gets information about the VMAccess extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2f25-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2f25-104">SYNTAX</span></span>

```
Get-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2f25-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2f25-105">DESCRIPTION</span></span>
<span data-ttu-id="e2f25-106">Das Cmdlet " **Get-AzureRmVMAccessExtension** " Ruft Informationen zur virtuellen Computererweiterung (Virtual Machine Access, VMAccess) ab.</span><span class="sxs-lookup"><span data-stu-id="e2f25-106">The **Get-AzureRmVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="e2f25-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e2f25-107">EXAMPLES</span></span>

### <span data-ttu-id="e2f25-108">Beispiel 1: Abrufen der VMAccess-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="e2f25-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="e2f25-109">Dieser Befehl ruft die VMAccess-Erweiterung mit dem Namen ContosoTest für den virtuellen Computer mit dem Namen VirtualMachine07 ab.</span><span class="sxs-lookup"><span data-stu-id="e2f25-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="e2f25-110">Beispiel 2: Abrufen der Instanzen Ansicht der VMAccess-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="e2f25-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="e2f25-111">Dieser Befehl ruft die Instanzen Ansicht der VMAccess-Erweiterung mit dem Namen ContosoTest für den virtuellen Computer mit dem Namen VirtualMachine07 ab.</span><span class="sxs-lookup"><span data-stu-id="e2f25-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="e2f25-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2f25-112">PARAMETERS</span></span>

### <span data-ttu-id="e2f25-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2f25-113">-DefaultProfile</span></span>
<span data-ttu-id="e2f25-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e2f25-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2f25-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e2f25-115">-Name</span></span>
<span data-ttu-id="e2f25-116">Gibt den Namen der Erweiterung an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="e2f25-116">Specifies the name of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e2f25-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2f25-117">-ResourceGroupName</span></span>
<span data-ttu-id="e2f25-118">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="e2f25-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="e2f25-119">-Status</span><span class="sxs-lookup"><span data-stu-id="e2f25-119">-Status</span></span>
<span data-ttu-id="e2f25-120">Gibt an, dass dieses Cmdlet nur die Instanzen Ansicht der Erweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="e2f25-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

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

### <span data-ttu-id="e2f25-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="e2f25-121">-VMName</span></span>
<span data-ttu-id="e2f25-122">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="e2f25-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="e2f25-123">Dieses Cmdlet ruft Informationen zu VMAccess für den virtuellen Computer ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="e2f25-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="e2f25-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2f25-124">CommonParameters</span></span>
<span data-ttu-id="e2f25-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2f25-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2f25-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2f25-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2f25-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e2f25-127">INPUTS</span></span>

### <span data-ttu-id="e2f25-128">Keine</span><span class="sxs-lookup"><span data-stu-id="e2f25-128">None</span></span>
<span data-ttu-id="e2f25-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="e2f25-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e2f25-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e2f25-130">OUTPUTS</span></span>

### <span data-ttu-id="e2f25-131">Microsoft. Azure. Commands. Compute. Models. VirtualMachineAccessExtensionContext</span><span class="sxs-lookup"><span data-stu-id="e2f25-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="e2f25-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="e2f25-132">NOTES</span></span>

## <span data-ttu-id="e2f25-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e2f25-133">RELATED LINKS</span></span>

[<span data-ttu-id="e2f25-134">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="e2f25-134">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="e2f25-135">Satz-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="e2f25-135">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="e2f25-136">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="e2f25-136">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)


