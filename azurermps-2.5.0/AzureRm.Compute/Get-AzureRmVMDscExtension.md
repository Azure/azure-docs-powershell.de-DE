---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdscextension
schema: 2.0.0
ms.openlocfilehash: 0954bcb395cf4a0dcf64dac178b1168ee1abd59b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849403"
---
# <span data-ttu-id="ee26c-101">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ee26c-101">Get-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="ee26c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ee26c-102">SYNOPSIS</span></span>
<span data-ttu-id="ee26c-103">Ruft die Einstellungen der DSC-Erweiterung auf einem bestimmten virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="ee26c-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee26c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee26c-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee26c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee26c-105">DESCRIPTION</span></span>
<span data-ttu-id="ee26c-106">Das Cmdlet " **Get-AzureRmVMDscExtension** " Ruft die Einstellungen der gewünschten DSC-Erweiterung (State Configuration) auf einem bestimmten virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="ee26c-106">The **Get-AzureRmVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="ee26c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ee26c-107">EXAMPLES</span></span>

### <span data-ttu-id="ee26c-108">Beispiel 1: Abrufen der Einstellungen einer DSC-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="ee26c-108">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="ee26c-109">Dieser Befehl ruft die Einstellungen der Erweiterung mit dem Namen DSC auf dem virtuellen Computer mit dem Namen VM07 ab.</span><span class="sxs-lookup"><span data-stu-id="ee26c-109">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="ee26c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee26c-110">PARAMETERS</span></span>

### <span data-ttu-id="ee26c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee26c-111">-DefaultProfile</span></span>
<span data-ttu-id="ee26c-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ee26c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee26c-113">-Name</span><span class="sxs-lookup"><span data-stu-id="ee26c-113">-Name</span></span>
<span data-ttu-id="ee26c-114">Gibt den Namen der Azure Resource Manager-Ressource an, die die Erweiterung darstellt.</span><span class="sxs-lookup"><span data-stu-id="ee26c-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="ee26c-115">Mit dem Set-AzureRmVMDscExtension-Cmdlet wird dieser Name auf Microsoft. PowerShell. DSC festgelegt, bei dem es sich um denselben Wert handelt, der von **Get-AzureRmVMDscExtension** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ee26c-115">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtension**.</span></span>
<span data-ttu-id="ee26c-116">Geben Sie diesen Parameter nur an, wenn Sie den Standardnamen im Cmdlet " **Satz-AzureRmVMDscExtension** " geändert oder einen anderen Ressourcennamen in einer Ressourcen-Manager-Vorlage verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="ee26c-116">Specify this parameter only if you changed the default name in the **Set-AzureRmVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="ee26c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee26c-117">-ResourceGroupName</span></span>
<span data-ttu-id="ee26c-118">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="ee26c-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ee26c-119">-Status</span><span class="sxs-lookup"><span data-stu-id="ee26c-119">-Status</span></span>
<span data-ttu-id="ee26c-120">Gibt an, dass dieses Cmdlet die Instanzen Ansicht der DSC-Erweiterung abruft.</span><span class="sxs-lookup"><span data-stu-id="ee26c-120">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

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

### <span data-ttu-id="ee26c-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="ee26c-121">-VMName</span></span>
<span data-ttu-id="ee26c-122">Gibt den Namen eines virtuellen Computers an, für den dieses Cmdlet die DSC-Erweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="ee26c-122">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

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

### <span data-ttu-id="ee26c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee26c-123">CommonParameters</span></span>
<span data-ttu-id="ee26c-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee26c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee26c-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee26c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee26c-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ee26c-126">INPUTS</span></span>

### <span data-ttu-id="ee26c-127">Keine</span><span class="sxs-lookup"><span data-stu-id="ee26c-127">None</span></span>
<span data-ttu-id="ee26c-128">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="ee26c-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ee26c-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ee26c-129">OUTPUTS</span></span>

### <span data-ttu-id="ee26c-130">Microsoft. Azure. Commands. Compute. Extension. DSC. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="ee26c-130">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="ee26c-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="ee26c-131">NOTES</span></span>

## <span data-ttu-id="ee26c-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ee26c-132">RELATED LINKS</span></span>

[<span data-ttu-id="ee26c-133">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ee26c-133">Remove-AzureRmVMDscExtension</span></span>](./Remove-AzureRmVMDscExtension.md)

[<span data-ttu-id="ee26c-134">Satz-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ee26c-134">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


