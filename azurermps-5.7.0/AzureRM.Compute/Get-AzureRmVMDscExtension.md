---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtension.md
ms.openlocfilehash: 0a3c54331b557b6be279ab5ce3f9fafad62b158c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478637"
---
# <span data-ttu-id="91c21-101">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="91c21-101">Get-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="91c21-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="91c21-102">SYNOPSIS</span></span>
<span data-ttu-id="91c21-103">Ruft die Einstellungen der DSC-Erweiterung auf einem bestimmten virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="91c21-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91c21-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="91c21-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="91c21-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91c21-105">DESCRIPTION</span></span>
<span data-ttu-id="91c21-106">Das Cmdlet " **Get-AzureRmVMDscExtension** " Ruft die Einstellungen der gewünschten DSC-Erweiterung (State Configuration) auf einem bestimmten virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="91c21-106">The **Get-AzureRmVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="91c21-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="91c21-107">EXAMPLES</span></span>

### <span data-ttu-id="91c21-108">Beispiel 1: Abrufen der Einstellungen einer DSC-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="91c21-108">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="91c21-109">Dieser Befehl ruft die Einstellungen der Erweiterung mit dem Namen DSC auf dem virtuellen Computer mit dem Namen VM07 ab.</span><span class="sxs-lookup"><span data-stu-id="91c21-109">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="91c21-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="91c21-110">PARAMETERS</span></span>

### <span data-ttu-id="91c21-111">-Name</span><span class="sxs-lookup"><span data-stu-id="91c21-111">-Name</span></span>
<span data-ttu-id="91c21-112">Gibt den Namen der Azure Resource Manager-Ressource an, die die Erweiterung darstellt.</span><span class="sxs-lookup"><span data-stu-id="91c21-112">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="91c21-113">Mit dem Set-AzureRmVMDscExtension-Cmdlet wird dieser Name auf Microsoft. PowerShell. DSC festgelegt, bei dem es sich um denselben Wert handelt, der von **Get-AzureRmVMDscExtension** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="91c21-113">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtension**.</span></span>
<span data-ttu-id="91c21-114">Geben Sie diesen Parameter nur an, wenn Sie den Standardnamen im Cmdlet " **Satz-AzureRmVMDscExtension** " geändert oder einen anderen Ressourcennamen in einer Ressourcen-Manager-Vorlage verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="91c21-114">Specify this parameter only if you changed the default name in the **Set-AzureRmVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91c21-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91c21-115">-ResourceGroupName</span></span>
<span data-ttu-id="91c21-116">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="91c21-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="91c21-117">-Status</span><span class="sxs-lookup"><span data-stu-id="91c21-117">-Status</span></span>
<span data-ttu-id="91c21-118">Gibt an, dass dieses Cmdlet die Instanzen Ansicht der DSC-Erweiterung abruft.</span><span class="sxs-lookup"><span data-stu-id="91c21-118">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91c21-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="91c21-119">-VMName</span></span>
<span data-ttu-id="91c21-120">Gibt den Namen eines virtuellen Computers an, für den dieses Cmdlet die DSC-Erweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="91c21-120">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91c21-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91c21-121">CommonParameters</span></span>
<span data-ttu-id="91c21-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91c21-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91c21-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91c21-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91c21-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="91c21-124">INPUTS</span></span>

### <span data-ttu-id="91c21-125">Keine</span><span class="sxs-lookup"><span data-stu-id="91c21-125">None</span></span>
<span data-ttu-id="91c21-126">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="91c21-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="91c21-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="91c21-127">OUTPUTS</span></span>

### <span data-ttu-id="91c21-128">Microsoft. Azure. Commands. Compute. Extension. DSC. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="91c21-128">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="91c21-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="91c21-129">NOTES</span></span>

## <span data-ttu-id="91c21-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="91c21-130">RELATED LINKS</span></span>

[<span data-ttu-id="91c21-131">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="91c21-131">Remove-AzureRmVMDscExtension</span></span>](./Remove-AzureRmVMDscExtension.md)

[<span data-ttu-id="91c21-132">Satz-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="91c21-132">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


