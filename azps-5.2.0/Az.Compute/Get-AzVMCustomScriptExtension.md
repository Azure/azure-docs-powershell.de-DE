---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
ms.openlocfilehash: 1d1ccb7f8e47ce34b798124d54fdd85aa18c7d69
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307032"
---
# <span data-ttu-id="9ad52-101">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="9ad52-101">Get-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="9ad52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ad52-102">SYNOPSIS</span></span>
<span data-ttu-id="9ad52-103">Ruft Informationen über eine benutzerdefinierte Skripterweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="9ad52-103">Gets information about a custom script extension.</span></span>

## <span data-ttu-id="9ad52-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ad52-104">SYNTAX</span></span>

```
Get-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ad52-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9ad52-105">DESCRIPTION</span></span>
<span data-ttu-id="9ad52-106">Das **Cmdlet "Get-AzVMCustomScriptExtension"** ruft Informationen über das benutzerdefinierte Skript "Virtual Machine Extension" auf einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="9ad52-106">The **Get-AzVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="9ad52-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9ad52-107">EXAMPLES</span></span>

### <span data-ttu-id="9ad52-108">Beispiel 1: Erhalten einer benutzerdefinierten Skripterweiterung</span><span class="sxs-lookup"><span data-stu-id="9ad52-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="9ad52-109">Dieser Befehl ruft die benutzerdefinierte Skripterweiterung "ContosoCustomScript" für den virtuellen Computer "VirtualMachine07" ab.</span><span class="sxs-lookup"><span data-stu-id="9ad52-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="9ad52-110">Beispiel 2: Anzeigen der Instanzansicht einer benutzerdefinierten Skripterweiterung</span><span class="sxs-lookup"><span data-stu-id="9ad52-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="9ad52-111">Dieser Befehl ruft die Instanzansicht der benutzerdefinierten Skripterweiterung "ContosoCustomScript" für den virtuellen Computer namens "VirtualMachine07" ab.</span><span class="sxs-lookup"><span data-stu-id="9ad52-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="9ad52-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ad52-112">PARAMETERS</span></span>

### <span data-ttu-id="9ad52-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ad52-113">-DefaultProfile</span></span>
<span data-ttu-id="9ad52-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ad52-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ad52-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9ad52-115">-Name</span></span>
<span data-ttu-id="9ad52-116">Gibt den Namen der benutzerdefinierten Skripterweiterung an, über die dieses Cmdlet Informationen erhält.</span><span class="sxs-lookup"><span data-stu-id="9ad52-116">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="9ad52-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ad52-117">-ResourceGroupName</span></span>
<span data-ttu-id="9ad52-118">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="9ad52-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9ad52-119">-Status</span><span class="sxs-lookup"><span data-stu-id="9ad52-119">-Status</span></span>
<span data-ttu-id="9ad52-120">Gibt an, dass dieses Cmdlet die Instanzansicht der benutzerdefinierten Skripterweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="9ad52-120">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

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

### <span data-ttu-id="9ad52-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="9ad52-121">-VMName</span></span>
<span data-ttu-id="9ad52-122">Gibt den Namen eines virtuellen Computers an, für den dieses Cmdlet die benutzerdefinierte Skripterweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="9ad52-122">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

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

### <span data-ttu-id="9ad52-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ad52-123">CommonParameters</span></span>
<span data-ttu-id="9ad52-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ad52-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ad52-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ad52-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ad52-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9ad52-126">INPUTS</span></span>

### <span data-ttu-id="9ad52-127">System.String</span><span class="sxs-lookup"><span data-stu-id="9ad52-127">System.String</span></span>

### <span data-ttu-id="9ad52-128">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9ad52-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9ad52-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9ad52-129">OUTPUTS</span></span>

### <span data-ttu-id="9ad52-130">Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext</span><span class="sxs-lookup"><span data-stu-id="9ad52-130">Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext</span></span>

## <span data-ttu-id="9ad52-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9ad52-131">NOTES</span></span>

## <span data-ttu-id="9ad52-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9ad52-132">RELATED LINKS</span></span>

[<span data-ttu-id="9ad52-133">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="9ad52-133">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="9ad52-134">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="9ad52-134">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="9ad52-135">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="9ad52-135">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


