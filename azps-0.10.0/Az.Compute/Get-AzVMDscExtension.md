---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDscExtension.md
ms.openlocfilehash: 70f06718c2d96e11b46842e4f39af26d3e29c2f9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844603"
---
# <span data-ttu-id="42390-101">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="42390-101">Get-AzVMDscExtension</span></span>

## <span data-ttu-id="42390-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="42390-102">SYNOPSIS</span></span>
<span data-ttu-id="42390-103">Ruft die Einstellungen der DSC-Erweiterung auf einem bestimmten virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="42390-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

## <span data-ttu-id="42390-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="42390-104">SYNTAX</span></span>

```
Get-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42390-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42390-105">DESCRIPTION</span></span>
<span data-ttu-id="42390-106">Das Cmdlet " **Get-AzVMDscExtension** " Ruft die Einstellungen der gewünschten DSC-Erweiterung (State Configuration) auf einem bestimmten virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="42390-106">The **Get-AzVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="42390-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42390-107">EXAMPLES</span></span>

### <span data-ttu-id="42390-108">Beispiel 1: Abrufen der Einstellungen einer DSC-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="42390-108">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="42390-109">Dieser Befehl ruft die Einstellungen der Erweiterung mit dem Namen DSC auf dem virtuellen Computer mit dem Namen VM07 ab.</span><span class="sxs-lookup"><span data-stu-id="42390-109">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="42390-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="42390-110">PARAMETERS</span></span>

### <span data-ttu-id="42390-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42390-111">-DefaultProfile</span></span>
<span data-ttu-id="42390-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="42390-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42390-113">-Name</span><span class="sxs-lookup"><span data-stu-id="42390-113">-Name</span></span>
<span data-ttu-id="42390-114">Gibt den Namen der Azure Resource Manager-Ressource an, die die Erweiterung darstellt.</span><span class="sxs-lookup"><span data-stu-id="42390-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="42390-115">Mit dem Set-AzVMDscExtension-Cmdlet wird dieser Name auf Microsoft. PowerShell. DSC festgelegt, bei dem es sich um denselben Wert handelt, der von **Get-AzVMDscExtension** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="42390-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtension**.</span></span>
<span data-ttu-id="42390-116">Geben Sie diesen Parameter nur an, wenn Sie den Standardnamen im Cmdlet " **Satz-AzVMDscExtension** " geändert oder einen anderen Ressourcennamen in einer Ressourcen-Manager-Vorlage verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="42390-116">Specify this parameter only if you changed the default name in the **Set-AzVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="42390-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42390-117">-ResourceGroupName</span></span>
<span data-ttu-id="42390-118">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="42390-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="42390-119">-Status</span><span class="sxs-lookup"><span data-stu-id="42390-119">-Status</span></span>
<span data-ttu-id="42390-120">Gibt an, dass dieses Cmdlet die Instanzen Ansicht der DSC-Erweiterung abruft.</span><span class="sxs-lookup"><span data-stu-id="42390-120">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

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

### <span data-ttu-id="42390-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="42390-121">-VMName</span></span>
<span data-ttu-id="42390-122">Gibt den Namen eines virtuellen Computers an, für den dieses Cmdlet die DSC-Erweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="42390-122">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

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

### <span data-ttu-id="42390-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42390-123">CommonParameters</span></span>
<span data-ttu-id="42390-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42390-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42390-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42390-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42390-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="42390-126">INPUTS</span></span>

### <span data-ttu-id="42390-127">Keine</span><span class="sxs-lookup"><span data-stu-id="42390-127">None</span></span>
<span data-ttu-id="42390-128">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="42390-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="42390-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="42390-129">OUTPUTS</span></span>

### <span data-ttu-id="42390-130">Microsoft. Azure. Commands. Compute. Extension. DSC. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="42390-130">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="42390-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="42390-131">NOTES</span></span>

## <span data-ttu-id="42390-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="42390-132">RELATED LINKS</span></span>

[<span data-ttu-id="42390-133">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="42390-133">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="42390-134">Satz-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="42390-134">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


