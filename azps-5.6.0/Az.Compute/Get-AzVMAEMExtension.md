---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
ms.openlocfilehash: ed5f79763d8e9786f0a502f404474eeef2f641f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922112"
---
# <span data-ttu-id="3804b-101">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="3804b-101">Get-AzVMAEMExtension</span></span>

## <span data-ttu-id="3804b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3804b-102">SYNOPSIS</span></span>
<span data-ttu-id="3804b-103">Ruft Informationen zur Erweiterung AEM ab.</span><span class="sxs-lookup"><span data-stu-id="3804b-103">Gets information about the AEM extension.</span></span>

## <span data-ttu-id="3804b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3804b-104">SYNTAX</span></span>

```
Get-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3804b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3804b-105">DESCRIPTION</span></span>
<span data-ttu-id="3804b-106">Das **Cmdlet Get-AzVMAEMExtension** ruft Informationen zur Azure Enhanced Monitoring (AEM)-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="3804b-106">The **Get-AzVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="3804b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3804b-107">EXAMPLES</span></span>

### <span data-ttu-id="3804b-108">Beispiel 1: Erhalten der Erweiterung AEM</span><span class="sxs-lookup"><span data-stu-id="3804b-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="3804b-109">Dieser Befehl ruft Informationen zur AEM-Erweiterung für den virtuellen Computer mit dem Namen contoso-server ab.</span><span class="sxs-lookup"><span data-stu-id="3804b-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="3804b-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3804b-110">PARAMETERS</span></span>

### <span data-ttu-id="3804b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3804b-111">-DefaultProfile</span></span>
<span data-ttu-id="3804b-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3804b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3804b-113">-Name</span><span class="sxs-lookup"><span data-stu-id="3804b-113">-Name</span></span>
<span data-ttu-id="3804b-114">Gibt den Namen eines virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="3804b-114">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="3804b-115">Dieses Cmdlet ruft Informationen zur AEM-Erweiterung auf dem virtuellen Computer ab, die dieses Cmdlet angibt.</span><span class="sxs-lookup"><span data-stu-id="3804b-115">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3804b-116">-OSType</span><span class="sxs-lookup"><span data-stu-id="3804b-116">-OSType</span></span>
<span data-ttu-id="3804b-117">Gibt den Typ des Betriebssystems des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="3804b-117">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="3804b-118">Wenn der Betriebssystemdatenträger keinen Typ hat, müssen Sie diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="3804b-118">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="3804b-119">Die zulässigen Werte für diesen Parameter sind: Windows und Linux.</span><span class="sxs-lookup"><span data-stu-id="3804b-119">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3804b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3804b-120">-ResourceGroupName</span></span>
<span data-ttu-id="3804b-121">Gibt den Namen der Ressourcengruppe eines virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="3804b-121">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="3804b-122">Dieses Cmdlet ruft Informationen zur Erweiterung AEM auf diesem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="3804b-122">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="3804b-123">-Status</span><span class="sxs-lookup"><span data-stu-id="3804b-123">-Status</span></span>
<span data-ttu-id="3804b-124">Gibt an, dass dieses Cmdlet nur die Instanzansicht der AEM-Erweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="3804b-124">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

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

### <span data-ttu-id="3804b-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="3804b-125">-VMName</span></span>
<span data-ttu-id="3804b-126">Gibt den Namen eines virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="3804b-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="3804b-127">Dieses Cmdlet ruft Informationen zur AEM-Erweiterung für den virtuellen Computer ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="3804b-127">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="3804b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3804b-128">CommonParameters</span></span>
<span data-ttu-id="3804b-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3804b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3804b-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3804b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3804b-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3804b-131">INPUTS</span></span>

### <span data-ttu-id="3804b-132">System.String</span><span class="sxs-lookup"><span data-stu-id="3804b-132">System.String</span></span>

### <span data-ttu-id="3804b-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3804b-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3804b-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3804b-134">OUTPUTS</span></span>

### <span data-ttu-id="3804b-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="3804b-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="3804b-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3804b-136">NOTES</span></span>

## <span data-ttu-id="3804b-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3804b-137">RELATED LINKS</span></span>

[<span data-ttu-id="3804b-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="3804b-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="3804b-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="3804b-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="3804b-140">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="3804b-140">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


