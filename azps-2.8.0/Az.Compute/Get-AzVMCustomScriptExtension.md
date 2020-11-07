---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
ms.openlocfilehash: add3437794430e0d5e41ab9330072db4ac3e1616
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652153"
---
# <span data-ttu-id="6a122-101">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="6a122-101">Get-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="6a122-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6a122-102">SYNOPSIS</span></span>
<span data-ttu-id="6a122-103">Ruft Informationen zu einer benutzerdefinierten Skripterweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="6a122-103">Gets information about a custom script extension.</span></span>

## <span data-ttu-id="6a122-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a122-104">SYNTAX</span></span>

```
Get-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a122-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6a122-105">DESCRIPTION</span></span>
<span data-ttu-id="6a122-106">Das Cmdlet " **Get-AzVMCustomScriptExtension** " Ruft Informationen zu einer benutzerdefinierten Virtual Machine-Skripterweiterung auf einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="6a122-106">The **Get-AzVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="6a122-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6a122-107">EXAMPLES</span></span>

### <span data-ttu-id="6a122-108">Beispiel 1: Abrufen einer benutzerdefinierten Skripterweiterung</span><span class="sxs-lookup"><span data-stu-id="6a122-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="6a122-109">Dieser Befehl ruft die benutzerdefinierte Skripterweiterung mit dem Namen ContosoCustomScript für den virtuellen Computer mit dem Namen VirtualMachine07 ab.</span><span class="sxs-lookup"><span data-stu-id="6a122-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="6a122-110">Beispiel 2: Abrufen der Instanzen Ansicht einer benutzerdefinierten Skripterweiterung</span><span class="sxs-lookup"><span data-stu-id="6a122-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="6a122-111">Dieser Befehl ruft die Instanzen Ansicht der benutzerdefinierten Skripterweiterung mit dem Namen ContosoCustomScript für den virtuellen Computer mit dem Namen VirtualMachine07 ab.</span><span class="sxs-lookup"><span data-stu-id="6a122-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="6a122-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a122-112">PARAMETERS</span></span>

### <span data-ttu-id="6a122-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a122-113">-DefaultProfile</span></span>
<span data-ttu-id="6a122-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6a122-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a122-115">-Name</span><span class="sxs-lookup"><span data-stu-id="6a122-115">-Name</span></span>
<span data-ttu-id="6a122-116">Gibt den Namen der benutzerdefinierten Skripterweiterung an, über die dieses Cmdlet Informationen erhält.</span><span class="sxs-lookup"><span data-stu-id="6a122-116">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="6a122-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a122-117">-ResourceGroupName</span></span>
<span data-ttu-id="6a122-118">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="6a122-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="6a122-119">-Status</span><span class="sxs-lookup"><span data-stu-id="6a122-119">-Status</span></span>
<span data-ttu-id="6a122-120">Gibt an, dass dieses Cmdlet die Instanzen Ansicht der benutzerdefinierten Skripterweiterung abruft.</span><span class="sxs-lookup"><span data-stu-id="6a122-120">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

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

### <span data-ttu-id="6a122-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="6a122-121">-VMName</span></span>
<span data-ttu-id="6a122-122">Gibt den Namen eines virtuellen Computers an, für den dieses Cmdlet die benutzerdefinierte Skripterweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="6a122-122">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

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

### <span data-ttu-id="6a122-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a122-123">CommonParameters</span></span>
<span data-ttu-id="6a122-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a122-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a122-125">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a122-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a122-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6a122-126">INPUTS</span></span>

### <span data-ttu-id="6a122-127">System. String</span><span class="sxs-lookup"><span data-stu-id="6a122-127">System.String</span></span>

### <span data-ttu-id="6a122-128">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="6a122-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6a122-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6a122-129">OUTPUTS</span></span>

### <span data-ttu-id="6a122-130">Microsoft. Azure. Commands. Compute. Models. VirtualMachineCustomScriptExtensionContext</span><span class="sxs-lookup"><span data-stu-id="6a122-130">Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext</span></span>

## <span data-ttu-id="6a122-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="6a122-131">NOTES</span></span>

## <span data-ttu-id="6a122-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6a122-132">RELATED LINKS</span></span>

[<span data-ttu-id="6a122-133">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="6a122-133">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="6a122-134">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="6a122-134">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="6a122-135">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="6a122-135">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


