---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
ms.openlocfilehash: e487e86c26ec09d1335ee34dab56292b564169b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166553"
---
# <span data-ttu-id="e007c-101">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="e007c-101">Get-AzVMDscExtension</span></span>

## <span data-ttu-id="e007c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e007c-102">SYNOPSIS</span></span>
<span data-ttu-id="e007c-103">Ruft die Einstellungen der ERWEITERUNG DSC auf einem bestimmten virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="e007c-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

## <span data-ttu-id="e007c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e007c-104">SYNTAX</span></span>

### <span data-ttu-id="e007c-105">GetDscExtension (Standard)</span><span class="sxs-lookup"><span data-stu-id="e007c-105">GetDscExtension (Default)</span></span>
```
Get-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e007c-106">VMParameterSet</span><span class="sxs-lookup"><span data-stu-id="e007c-106">VMParameterSet</span></span>
```
Get-AzVMDscExtension [-Status] [-VM <PSVirtualMachine>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e007c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e007c-107">DESCRIPTION</span></span>
<span data-ttu-id="e007c-108">Das **Cmdlet "Get-AzVMDscExtension"** ruft die Einstellungen der Erweiterung "Desired State Configuration (DSC)" auf einem bestimmten virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="e007c-108">The **Get-AzVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="e007c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e007c-109">EXAMPLES</span></span>

### <span data-ttu-id="e007c-110">Beispiel 1: Erhalten der Einstellungen einer DSC-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="e007c-110">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="e007c-111">Dieser Befehl ruft die Einstellungen der Erweiterung "DSC" auf dem virtuellen Computer "VM07" ab.</span><span class="sxs-lookup"><span data-stu-id="e007c-111">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="e007c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e007c-112">PARAMETERS</span></span>

### <span data-ttu-id="e007c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e007c-113">-DefaultProfile</span></span>
<span data-ttu-id="e007c-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e007c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e007c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e007c-115">-Name</span></span>
<span data-ttu-id="e007c-116">Gibt den Namen der Azure Resource Manager-Ressource an, die die Erweiterung darstellt.</span><span class="sxs-lookup"><span data-stu-id="e007c-116">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="e007c-117">Das Set-AzVMDscExtension-Cmdlet legt diesen Namen auf "Microsoft.Powershell.DSC" fest. Dies ist derselbe Wert, der von **"Get-AzVMDscExtension" verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="e007c-117">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtension**.</span></span>
<span data-ttu-id="e007c-118">Geben Sie diesen Parameter nur an, wenn Sie den Standardnamen im **Cmdlet "Set-AzVMDscExtension"** geändert oder einen anderen Ressourcennamen in einer Ressourcen-Manager-Vorlage verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="e007c-118">Specify this parameter only if you changed the default name in the **Set-AzVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e007c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e007c-119">-ResourceGroupName</span></span>
<span data-ttu-id="e007c-120">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="e007c-120">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e007c-121">-Status</span><span class="sxs-lookup"><span data-stu-id="e007c-121">-Status</span></span>
<span data-ttu-id="e007c-122">Gibt an, dass dieses Cmdlet die Instanzansicht der ERWEITERUNG DSC erhält.</span><span class="sxs-lookup"><span data-stu-id="e007c-122">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e007c-123">-VM</span><span class="sxs-lookup"><span data-stu-id="e007c-123">-VM</span></span>
<span data-ttu-id="e007c-124">Gibt das Objekt des virtuellen Computers an, auf dem sich die Erweiterung befindet.</span><span class="sxs-lookup"><span data-stu-id="e007c-124">Specifies the virtual machine object the extension is on.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e007c-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="e007c-125">-VMName</span></span>
<span data-ttu-id="e007c-126">Gibt den Namen eines virtuellen Computers an, für den dieses Cmdlet die DSC-Erweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="e007c-126">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e007c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e007c-127">CommonParameters</span></span>
<span data-ttu-id="e007c-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e007c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e007c-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e007c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e007c-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e007c-130">INPUTS</span></span>

### <span data-ttu-id="e007c-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e007c-131">System.String</span></span>

### <span data-ttu-id="e007c-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e007c-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e007c-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e007c-133">OUTPUTS</span></span>

### <span data-ttu-id="e007c-134">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="e007c-134">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="e007c-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e007c-135">NOTES</span></span>

## <span data-ttu-id="e007c-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e007c-136">RELATED LINKS</span></span>

[<span data-ttu-id="e007c-137">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="e007c-137">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="e007c-138">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="e007c-138">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


