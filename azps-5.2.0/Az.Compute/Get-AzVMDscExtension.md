---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
ms.openlocfilehash: ba4ac8d48c72ffac164e447777670c48f529f68f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292294"
---
# <span data-ttu-id="1d42e-101">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="1d42e-101">Get-AzVMDscExtension</span></span>

## <span data-ttu-id="1d42e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d42e-102">SYNOPSIS</span></span>
<span data-ttu-id="1d42e-103">Ruft die Einstellungen der ERWEITERUNG DSC auf einem bestimmten virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="1d42e-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

## <span data-ttu-id="1d42e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1d42e-104">SYNTAX</span></span>

```
Get-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d42e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1d42e-105">DESCRIPTION</span></span>
<span data-ttu-id="1d42e-106">Das **Cmdlet "Get-AzVMDscExtension"** ruft die Einstellungen der Erweiterung "Desired State Configuration (DSC)" auf einem bestimmten virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="1d42e-106">The **Get-AzVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="1d42e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1d42e-107">EXAMPLES</span></span>

### <span data-ttu-id="1d42e-108">Beispiel 1: Erhalten der Einstellungen einer DSC-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="1d42e-108">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="1d42e-109">Dieser Befehl ruft die Einstellungen der Erweiterung "DSC" auf dem virtuellen Computer "VM07" ab.</span><span class="sxs-lookup"><span data-stu-id="1d42e-109">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="1d42e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d42e-110">PARAMETERS</span></span>

### <span data-ttu-id="1d42e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d42e-111">-DefaultProfile</span></span>
<span data-ttu-id="1d42e-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1d42e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d42e-113">-Name</span><span class="sxs-lookup"><span data-stu-id="1d42e-113">-Name</span></span>
<span data-ttu-id="1d42e-114">Gibt den Namen der Azure Resource Manager-Ressource an, die die Erweiterung darstellt.</span><span class="sxs-lookup"><span data-stu-id="1d42e-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="1d42e-115">Das Set-AzVMDscExtension-Cmdlet legt diesen Namen auf "Microsoft.Powershell.DSC" fest. Dies ist derselbe Wert, der von **"Get-AzVMDscExtension" verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="1d42e-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtension**.</span></span>
<span data-ttu-id="1d42e-116">Geben Sie diesen Parameter nur an, wenn Sie den Standardnamen im **Cmdlet "Set-AzVMDscExtension"** geändert oder einen anderen Ressourcennamen in einer Ressourcen-Manager-Vorlage verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="1d42e-116">Specify this parameter only if you changed the default name in the **Set-AzVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d42e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d42e-117">-ResourceGroupName</span></span>
<span data-ttu-id="1d42e-118">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="1d42e-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1d42e-119">-Status</span><span class="sxs-lookup"><span data-stu-id="1d42e-119">-Status</span></span>
<span data-ttu-id="1d42e-120">Gibt an, dass dieses Cmdlet die Instanzansicht der ERWEITERUNG DSC erhält.</span><span class="sxs-lookup"><span data-stu-id="1d42e-120">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

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

### <span data-ttu-id="1d42e-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="1d42e-121">-VMName</span></span>
<span data-ttu-id="1d42e-122">Gibt den Namen eines virtuellen Computers an, für den dieses Cmdlet die DSC-Erweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="1d42e-122">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d42e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d42e-123">CommonParameters</span></span>
<span data-ttu-id="1d42e-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d42e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d42e-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d42e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d42e-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1d42e-126">INPUTS</span></span>

### <span data-ttu-id="1d42e-127">System.String</span><span class="sxs-lookup"><span data-stu-id="1d42e-127">System.String</span></span>

### <span data-ttu-id="1d42e-128">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1d42e-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1d42e-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1d42e-129">OUTPUTS</span></span>

### <span data-ttu-id="1d42e-130">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="1d42e-130">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="1d42e-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1d42e-131">NOTES</span></span>

## <span data-ttu-id="1d42e-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1d42e-132">RELATED LINKS</span></span>

[<span data-ttu-id="1d42e-133">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="1d42e-133">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="1d42e-134">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="1d42e-134">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


