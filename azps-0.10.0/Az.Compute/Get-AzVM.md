---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVM.md
ms.openlocfilehash: 2f33b0dbee4f584553eac1047471adef08e3523b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844635"
---
# <span data-ttu-id="d9b1a-101">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="d9b1a-101">Get-AzVM</span></span>

## <span data-ttu-id="d9b1a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d9b1a-102">SYNOPSIS</span></span>
<span data-ttu-id="d9b1a-103">Ruft die Eigenschaften eines virtuellen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="d9b1a-103">Gets the properties of a virtual machine.</span></span>

## <span data-ttu-id="d9b1a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9b1a-104">SYNTAX</span></span>

### <span data-ttu-id="d9b1a-105">ListAllVirtualMachinesParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d9b1a-105">ListAllVirtualMachinesParamSet (Default)</span></span>
```
Get-AzVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9b1a-106">ListVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="d9b1a-106">ListVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d9b1a-107">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="d9b1a-107">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9b1a-108">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="d9b1a-108">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9b1a-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9b1a-109">DESCRIPTION</span></span>
<span data-ttu-id="d9b1a-110">Das Cmdlet " **Get-AzVM** " Ruft die Modellansicht und die Instanzen Ansicht eines Azure Virtual Machine ab.</span><span class="sxs-lookup"><span data-stu-id="d9b1a-110">The **Get-AzVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="d9b1a-111">Die Modellansicht ist die benutzerdefinierten Eigenschaften des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="d9b1a-111">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="d9b1a-112">Bei der Instanzansicht handelt es sich um den Status der Instanzebene des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="d9b1a-112">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="d9b1a-113">Geben Sie den Parameter *Status* an, um nur die Instanzen Ansicht eines virtuellen Computers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d9b1a-113">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="d9b1a-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d9b1a-114">EXAMPLES</span></span>

### <span data-ttu-id="d9b1a-115">Beispiel 1: Abrufen von Modell-und Instanzen Ansichtseigenschaften</span><span class="sxs-lookup"><span data-stu-id="d9b1a-115">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="d9b1a-116">Mit diesem Befehl werden die Eigenschaften Modellansicht und Instanzen Ansicht des virtuellen Computers mit dem Namen VirtualMachine07 abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d9b1a-116">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="d9b1a-117">Beispiel 2: Abrufen von Instanzen Ansichtseigenschaften</span><span class="sxs-lookup"><span data-stu-id="d9b1a-117">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

<span data-ttu-id="d9b1a-118">Dieser Befehl ruft Eigenschaften des virtuellen Computers mit dem Namen VirtualMachine07 ab.</span><span class="sxs-lookup"><span data-stu-id="d9b1a-118">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="d9b1a-119">Mit diesem Befehl wird der *Status* -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="d9b1a-119">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="d9b1a-120">Daher ruft der Befehl nur die Eigenschaften der Instanzen Ansicht ab.</span><span class="sxs-lookup"><span data-stu-id="d9b1a-120">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="d9b1a-121">Beispiel 3: Abrufen von Eigenschaften für alle virtuellen Computer in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="d9b1a-121">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="d9b1a-122">Dieser Befehl ruft Eigenschaften für alle virtuellen Computer in der Ressourcengruppe mit dem Namen ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="d9b1a-122">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="d9b1a-123">Beispiel 4: Abrufen aller virtuellen Computer in Ihrem Abonnement</span><span class="sxs-lookup"><span data-stu-id="d9b1a-123">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzVM
```

<span data-ttu-id="d9b1a-124">Dieser Befehl ruft alle virtuellen Computer in Ihrem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="d9b1a-124">This command gets all the virtual machines in your subscription.</span></span>

## <span data-ttu-id="d9b1a-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9b1a-125">PARAMETERS</span></span>

### <span data-ttu-id="d9b1a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9b1a-126">-DefaultProfile</span></span>
<span data-ttu-id="d9b1a-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d9b1a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9b1a-128">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="d9b1a-128">-DisplayHint</span></span>
<span data-ttu-id="d9b1a-129">Bestimmt, wie das Objekt des virtuellen Computers angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d9b1a-129">Determines how the virtual machine object is displayed.</span></span>

<span data-ttu-id="d9b1a-130">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="d9b1a-130">Valid values are:</span></span>

<span data-ttu-id="d9b1a-131">– Kompakt: zeigt nur Eigenschaften der obersten Ebene an.</span><span class="sxs-lookup"><span data-stu-id="d9b1a-131">-- Compact: displays only top level properties</span></span>

<span data-ttu-id="d9b1a-132">--Expand: zeigt alle Eigenschaften auf allen Ebenen an</span><span class="sxs-lookup"><span data-stu-id="d9b1a-132">-- Expand: displays all properties in all levels</span></span>
```yaml
Type: DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: 
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9b1a-133">-Name</span><span class="sxs-lookup"><span data-stu-id="d9b1a-133">-Name</span></span>
<span data-ttu-id="d9b1a-134">Gibt den Namen des abzurufenden virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="d9b1a-134">Specifies the name of the virtual machine to get.</span></span>

```yaml
Type: String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9b1a-135">-Nextlink</span><span class="sxs-lookup"><span data-stu-id="d9b1a-135">-NextLink</span></span>
<span data-ttu-id="d9b1a-136">Gibt den nächsten Link an.</span><span class="sxs-lookup"><span data-stu-id="d9b1a-136">Specifies the next link.</span></span>

```yaml
Type: Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9b1a-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9b1a-137">-ResourceGroupName</span></span>
<span data-ttu-id="d9b1a-138">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="d9b1a-138">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ListVirtualMachineInResourceGroupParamSet, GetVirtualMachineInResourceGroupParamSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9b1a-139">-Status</span><span class="sxs-lookup"><span data-stu-id="d9b1a-139">-Status</span></span>
<span data-ttu-id="d9b1a-140">Gibt an, dass dieses Cmdlet nur die Instanzen Ansicht des virtuellen Computers abruft.</span><span class="sxs-lookup"><span data-stu-id="d9b1a-140">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9b1a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9b1a-141">CommonParameters</span></span>
<span data-ttu-id="d9b1a-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9b1a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9b1a-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9b1a-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9b1a-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d9b1a-144">INPUTS</span></span>

### <span data-ttu-id="d9b1a-145">Keine</span><span class="sxs-lookup"><span data-stu-id="d9b1a-145">None</span></span>
<span data-ttu-id="d9b1a-146">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="d9b1a-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d9b1a-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d9b1a-147">OUTPUTS</span></span>

### <span data-ttu-id="d9b1a-148">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d9b1a-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="d9b1a-149">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="d9b1a-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="d9b1a-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="d9b1a-150">NOTES</span></span>

## <span data-ttu-id="d9b1a-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d9b1a-151">RELATED LINKS</span></span>

[<span data-ttu-id="d9b1a-152">Neu – AzVM</span><span class="sxs-lookup"><span data-stu-id="d9b1a-152">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="d9b1a-153">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="d9b1a-153">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="d9b1a-154">Neustart-AzVM</span><span class="sxs-lookup"><span data-stu-id="d9b1a-154">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="d9b1a-155">Anfang-AzVM</span><span class="sxs-lookup"><span data-stu-id="d9b1a-155">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="d9b1a-156">Stopp-AzVM</span><span class="sxs-lookup"><span data-stu-id="d9b1a-156">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="d9b1a-157">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="d9b1a-157">Update-AzVM</span></span>](./Update-AzVM.md)


