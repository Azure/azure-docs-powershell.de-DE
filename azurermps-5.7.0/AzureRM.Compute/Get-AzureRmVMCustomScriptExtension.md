---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: 1f348a7cddc31a2a3d3d255aa6b4fe80d1808f36
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483122"
---
# <span data-ttu-id="020b7-101">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="020b7-101">Get-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="020b7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="020b7-102">SYNOPSIS</span></span>
<span data-ttu-id="020b7-103">Ruft Informationen zu einer benutzerdefinierten Skripterweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="020b7-103">Gets information about a custom script extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="020b7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="020b7-104">SYNTAX</span></span>

```
Get-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="020b7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="020b7-105">DESCRIPTION</span></span>
<span data-ttu-id="020b7-106">Das Cmdlet " **Get-AzureRmVMCustomScriptExtension** " Ruft Informationen zu einer benutzerdefinierten Virtual Machine-Skripterweiterung auf einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="020b7-106">The **Get-AzureRmVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="020b7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="020b7-107">EXAMPLES</span></span>

### <span data-ttu-id="020b7-108">Beispiel 1: Abrufen einer benutzerdefinierten Skripterweiterung</span><span class="sxs-lookup"><span data-stu-id="020b7-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="020b7-109">Dieser Befehl ruft die benutzerdefinierte Skripterweiterung mit dem Namen ContosoCustomScript für den virtuellen Computer mit dem Namen VirtualMachine07 ab.</span><span class="sxs-lookup"><span data-stu-id="020b7-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="020b7-110">Beispiel 2: Abrufen der Instanzen Ansicht einer benutzerdefinierten Skripterweiterung</span><span class="sxs-lookup"><span data-stu-id="020b7-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="020b7-111">Dieser Befehl ruft die Instanzen Ansicht der benutzerdefinierten Skripterweiterung mit dem Namen ContosoCustomScript für den virtuellen Computer mit dem Namen VirtualMachine07 ab.</span><span class="sxs-lookup"><span data-stu-id="020b7-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="020b7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="020b7-112">PARAMETERS</span></span>

### <span data-ttu-id="020b7-113">-Name</span><span class="sxs-lookup"><span data-stu-id="020b7-113">-Name</span></span>
<span data-ttu-id="020b7-114">Gibt den Namen der benutzerdefinierten Skripterweiterung an, über die dieses Cmdlet Informationen erhält.</span><span class="sxs-lookup"><span data-stu-id="020b7-114">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="020b7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="020b7-115">-ResourceGroupName</span></span>
<span data-ttu-id="020b7-116">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="020b7-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="020b7-117">-Status</span><span class="sxs-lookup"><span data-stu-id="020b7-117">-Status</span></span>
<span data-ttu-id="020b7-118">Gibt an, dass dieses Cmdlet die Instanzen Ansicht der benutzerdefinierten Skripterweiterung abruft.</span><span class="sxs-lookup"><span data-stu-id="020b7-118">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

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

### <span data-ttu-id="020b7-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="020b7-119">-VMName</span></span>
<span data-ttu-id="020b7-120">Gibt den Namen eines virtuellen Computers an, für den dieses Cmdlet die benutzerdefinierte Skripterweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="020b7-120">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

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

### <span data-ttu-id="020b7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="020b7-121">CommonParameters</span></span>
<span data-ttu-id="020b7-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="020b7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="020b7-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="020b7-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="020b7-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="020b7-124">INPUTS</span></span>

### <span data-ttu-id="020b7-125">Keine</span><span class="sxs-lookup"><span data-stu-id="020b7-125">None</span></span>
<span data-ttu-id="020b7-126">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="020b7-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="020b7-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="020b7-127">OUTPUTS</span></span>

## <span data-ttu-id="020b7-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="020b7-128">NOTES</span></span>

## <span data-ttu-id="020b7-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="020b7-129">RELATED LINKS</span></span>

[<span data-ttu-id="020b7-130">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="020b7-130">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="020b7-131">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="020b7-131">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="020b7-132">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="020b7-132">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


