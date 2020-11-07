---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
ms.openlocfilehash: d054cb84ccd4e77ca47caf653c5a3d9322691929
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820600"
---
# <span data-ttu-id="61655-101">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="61655-101">Remove-AzVMDscExtension</span></span>

## <span data-ttu-id="61655-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="61655-102">SYNOPSIS</span></span>
<span data-ttu-id="61655-103">Entfernt einen DSC-Erweiterungshandler von einem virtuellen Computer in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="61655-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="61655-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="61655-104">SYNTAX</span></span>

```
Remove-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61655-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61655-105">DESCRIPTION</span></span>
<span data-ttu-id="61655-106">Mit dem Cmdlet **Remove-AzVMDscExtension** wird der Erweiterungshandler für die gewünschte Zustands Konfiguration (DSC) von einem virtuellen Computer in einer Ressourcengruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="61655-106">The **Remove-AzVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="61655-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="61655-107">EXAMPLES</span></span>

### <span data-ttu-id="61655-108">Beispiel 1: Entfernen einer DSC-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="61655-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="61655-109">Dieser Befehl entfernt die Erweiterung mit dem Namen DSC auf dem virtuellen Computer mit dem Namen VM07.</span><span class="sxs-lookup"><span data-stu-id="61655-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="61655-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="61655-110">PARAMETERS</span></span>

### <span data-ttu-id="61655-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61655-111">-DefaultProfile</span></span>
<span data-ttu-id="61655-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="61655-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61655-113">-Name</span><span class="sxs-lookup"><span data-stu-id="61655-113">-Name</span></span>
<span data-ttu-id="61655-114">Gibt den Namen der DSC-Erweiterung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="61655-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="61655-115">Mit dem Set-AzVMDscExtension-Cmdlet wird dieser Name auf Microsoft. PowerShell. DSC festgelegt, bei dem es sich um den Standardwert handelt, der von **Remove-AzVMDscExtension** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="61655-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzVMDscExtension**.</span></span>

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

### <span data-ttu-id="61655-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61655-116">-ResourceGroupName</span></span>
<span data-ttu-id="61655-117">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="61655-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="61655-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="61655-118">-VMName</span></span>
<span data-ttu-id="61655-119">Gibt den Namen eines virtuellen Computers an, von dem dieses Cmdlet die DSC-Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="61655-119">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

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

### <span data-ttu-id="61655-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="61655-120">-Confirm</span></span>
<span data-ttu-id="61655-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="61655-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61655-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61655-122">-WhatIf</span></span>
<span data-ttu-id="61655-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="61655-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61655-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="61655-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61655-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61655-125">CommonParameters</span></span>
<span data-ttu-id="61655-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61655-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61655-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61655-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61655-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="61655-128">INPUTS</span></span>

### <span data-ttu-id="61655-129">System. String</span><span class="sxs-lookup"><span data-stu-id="61655-129">System.String</span></span>

## <span data-ttu-id="61655-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="61655-130">OUTPUTS</span></span>

### <span data-ttu-id="61655-131">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="61655-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="61655-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="61655-132">NOTES</span></span>

## <span data-ttu-id="61655-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="61655-133">RELATED LINKS</span></span>

[<span data-ttu-id="61655-134">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="61655-134">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="61655-135">Satz-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="61655-135">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


