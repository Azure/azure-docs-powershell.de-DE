---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVM.md
ms.openlocfilehash: 8601a7cc6a02211a0264030784485a5ecb4d29fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480478"
---
# <span data-ttu-id="f473b-101">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f473b-101">Get-AzureRmVM</span></span>

## <span data-ttu-id="f473b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f473b-102">SYNOPSIS</span></span>
<span data-ttu-id="f473b-103">Ruft die Eigenschaften eines virtuellen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="f473b-103">Gets the properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f473b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f473b-104">SYNTAX</span></span>

### <span data-ttu-id="f473b-105">ListAllVirtualMachinesParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f473b-105">ListAllVirtualMachinesParamSet (Default)</span></span>
```
Get-AzureRmVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f473b-106">ListVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="f473b-106">ListVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f473b-107">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="f473b-107">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f473b-108">ListLocationVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="f473b-108">ListLocationVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM -Location <String> [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f473b-109">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="f473b-109">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f473b-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f473b-110">DESCRIPTION</span></span>
<span data-ttu-id="f473b-111">Das Cmdlet " **Get-AzureRmVM** " Ruft die Modellansicht und die Instanzen Ansicht eines Azure Virtual Machine ab.</span><span class="sxs-lookup"><span data-stu-id="f473b-111">The **Get-AzureRmVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="f473b-112">Die Modellansicht ist die benutzerdefinierten Eigenschaften des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="f473b-112">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="f473b-113">Bei der Instanzansicht handelt es sich um den Status der Instanzebene des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="f473b-113">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="f473b-114">Geben Sie den Parameter *Status* an, um nur die Instanzen Ansicht eines virtuellen Computers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f473b-114">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="f473b-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f473b-115">EXAMPLES</span></span>

### <span data-ttu-id="f473b-116">Beispiel 1: Abrufen von Modell-und Instanzen Ansichtseigenschaften</span><span class="sxs-lookup"><span data-stu-id="f473b-116">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="f473b-117">Mit diesem Befehl werden die Eigenschaften Modellansicht und Instanzen Ansicht des virtuellen Computers mit dem Namen VirtualMachine07 abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f473b-117">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="f473b-118">Beispiel 2: Abrufen von Instanzen Ansichtseigenschaften</span><span class="sxs-lookup"><span data-stu-id="f473b-118">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

<span data-ttu-id="f473b-119">Dieser Befehl ruft Eigenschaften des virtuellen Computers mit dem Namen VirtualMachine07 ab.</span><span class="sxs-lookup"><span data-stu-id="f473b-119">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="f473b-120">Mit diesem Befehl wird der *Status* -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="f473b-120">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="f473b-121">Daher ruft der Befehl nur die Eigenschaften der Instanzen Ansicht ab.</span><span class="sxs-lookup"><span data-stu-id="f473b-121">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="f473b-122">Beispiel 3: Abrufen von Eigenschaften für alle virtuellen Computer in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f473b-122">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="f473b-123">Dieser Befehl ruft Eigenschaften für alle virtuellen Computer in der Ressourcengruppe mit dem Namen ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="f473b-123">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="f473b-124">Beispiel 4: Abrufen aller virtuellen Computer in Ihrem Abonnement</span><span class="sxs-lookup"><span data-stu-id="f473b-124">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzureRmVM
```

<span data-ttu-id="f473b-125">Dieser Befehl ruft alle virtuellen Computer in Ihrem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="f473b-125">This command gets all the virtual machines in your subscription.</span></span>

### <span data-ttu-id="f473b-126">Beispiel 5: Abrufen aller virtuellen Computer am Standort.</span><span class="sxs-lookup"><span data-stu-id="f473b-126">Example 5: Get all virtual machines in the location.</span></span>
```
PS C:\> Get-AzureRmVM -Location "westus"
```

<span data-ttu-id="f473b-127">Dieser Befehl ruft alle virtuellen Computer in der West US-Region ab.</span><span class="sxs-lookup"><span data-stu-id="f473b-127">This command gets all the virtual machines in West US region.</span></span>

## <span data-ttu-id="f473b-128">Parameter</span><span class="sxs-lookup"><span data-stu-id="f473b-128">PARAMETERS</span></span>

### <span data-ttu-id="f473b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f473b-129">-DefaultProfile</span></span>
<span data-ttu-id="f473b-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f473b-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f473b-131">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="f473b-131">-DisplayHint</span></span>
<span data-ttu-id="f473b-132">Bestimmt, wie das Objekt des virtuellen Computers angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f473b-132">Determines how the virtual machine object is displayed.</span></span>
<span data-ttu-id="f473b-133">Gültige Werte sind:--Compact: zeigt nur Eigenschaften der obersten Ebene an--Expand: zeigt alle Eigenschaften auf allen Ebenen an.</span><span class="sxs-lookup"><span data-stu-id="f473b-133">Valid values are: -- Compact: displays only top level properties -- Expand: displays all properties in all levels</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases:
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f473b-134">-Standort</span><span class="sxs-lookup"><span data-stu-id="f473b-134">-Location</span></span>
<span data-ttu-id="f473b-135">Gibt einen Speicherort für die Liste der virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="f473b-135">Specifies a location for the virtual machines to list.</span></span>

```yaml
Type: System.String
Parameter Sets: ListLocationVirtualMachinesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f473b-136">-Name</span><span class="sxs-lookup"><span data-stu-id="f473b-136">-Name</span></span>
<span data-ttu-id="f473b-137">Gibt den Namen des abzurufenden virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="f473b-137">Specifies the name of the virtual machine to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f473b-138">-Nextlink</span><span class="sxs-lookup"><span data-stu-id="f473b-138">-NextLink</span></span>
<span data-ttu-id="f473b-139">Gibt den nächsten Link an.</span><span class="sxs-lookup"><span data-stu-id="f473b-139">Specifies the next link.</span></span>

```yaml
Type: System.Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f473b-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f473b-140">-ResourceGroupName</span></span>
<span data-ttu-id="f473b-141">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="f473b-141">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVirtualMachineInResourceGroupParamSet, GetVirtualMachineInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f473b-142">-Status</span><span class="sxs-lookup"><span data-stu-id="f473b-142">-Status</span></span>
<span data-ttu-id="f473b-143">Gibt an, dass dieses Cmdlet nur die Instanzen Ansicht des virtuellen Computers abruft.</span><span class="sxs-lookup"><span data-stu-id="f473b-143">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f473b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f473b-144">CommonParameters</span></span>
<span data-ttu-id="f473b-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f473b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f473b-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f473b-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f473b-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f473b-147">INPUTS</span></span>

### <span data-ttu-id="f473b-148">System. String</span><span class="sxs-lookup"><span data-stu-id="f473b-148">System.String</span></span>

### <span data-ttu-id="f473b-149">System. Uri</span><span class="sxs-lookup"><span data-stu-id="f473b-149">System.Uri</span></span>

### <span data-ttu-id="f473b-150">Microsoft. Azure. Commands. Compute. Models. DisplayHintType</span><span class="sxs-lookup"><span data-stu-id="f473b-150">Microsoft.Azure.Commands.Compute.Models.DisplayHintType</span></span>

## <span data-ttu-id="f473b-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f473b-151">OUTPUTS</span></span>

### <span data-ttu-id="f473b-152">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f473b-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="f473b-153">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="f473b-153">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="f473b-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="f473b-154">NOTES</span></span>

## <span data-ttu-id="f473b-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f473b-155">RELATED LINKS</span></span>

[<span data-ttu-id="f473b-156">Neu – AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f473b-156">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="f473b-157">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f473b-157">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="f473b-158">Neustart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f473b-158">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="f473b-159">Anfang-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f473b-159">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="f473b-160">Stopp-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f473b-160">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="f473b-161">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f473b-161">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


