---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMDscExtension.md
ms.openlocfilehash: b25b65e9c42cd388d685320802690c6538122e94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477885"
---
# <span data-ttu-id="38965-101">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="38965-101">Remove-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="38965-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="38965-102">SYNOPSIS</span></span>
<span data-ttu-id="38965-103">Entfernt einen DSC-Erweiterungshandler von einem virtuellen Computer in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="38965-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38965-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="38965-104">SYNTAX</span></span>

```
Remove-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38965-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="38965-105">DESCRIPTION</span></span>
<span data-ttu-id="38965-106">Mit dem Cmdlet **Remove-AzureRmVMDscExtension** wird der Erweiterungshandler für die gewünschte Zustands Konfiguration (DSC) von einem virtuellen Computer in einer Ressourcengruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="38965-106">The **Remove-AzureRmVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="38965-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="38965-107">EXAMPLES</span></span>

### <span data-ttu-id="38965-108">Beispiel 1: Entfernen einer DSC-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="38965-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="38965-109">Dieser Befehl entfernt die Erweiterung mit dem Namen DSC auf dem virtuellen Computer mit dem Namen VM07.</span><span class="sxs-lookup"><span data-stu-id="38965-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="38965-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="38965-110">PARAMETERS</span></span>

### <span data-ttu-id="38965-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38965-111">-DefaultProfile</span></span>
<span data-ttu-id="38965-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="38965-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38965-113">-Name</span><span class="sxs-lookup"><span data-stu-id="38965-113">-Name</span></span>
<span data-ttu-id="38965-114">Gibt den Namen der DSC-Erweiterung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="38965-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="38965-115">Mit dem Set-AzureRmVMDscExtension-Cmdlet wird dieser Name auf Microsoft. PowerShell. DSC festgelegt, bei dem es sich um den Standardwert handelt, der von **Remove-AzureRmVMDscExtension** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="38965-115">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzureRmVMDscExtension**.</span></span>

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

### <span data-ttu-id="38965-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38965-116">-ResourceGroupName</span></span>
<span data-ttu-id="38965-117">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="38965-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="38965-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="38965-118">-VMName</span></span>
<span data-ttu-id="38965-119">Gibt den Namen eines virtuellen Computers an, von dem dieses Cmdlet die DSC-Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="38965-119">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

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

### <span data-ttu-id="38965-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="38965-120">-Confirm</span></span>
<span data-ttu-id="38965-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="38965-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38965-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38965-122">-WhatIf</span></span>
<span data-ttu-id="38965-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="38965-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38965-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="38965-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38965-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38965-125">CommonParameters</span></span>
<span data-ttu-id="38965-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38965-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38965-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38965-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38965-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="38965-128">INPUTS</span></span>

### <span data-ttu-id="38965-129">System. String</span><span class="sxs-lookup"><span data-stu-id="38965-129">System.String</span></span>

## <span data-ttu-id="38965-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="38965-130">OUTPUTS</span></span>

### <span data-ttu-id="38965-131">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="38965-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="38965-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="38965-132">NOTES</span></span>

## <span data-ttu-id="38965-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="38965-133">RELATED LINKS</span></span>

[<span data-ttu-id="38965-134">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="38965-134">Get-AzureRmVMDscExtension</span></span>](./Get-AzureRmVMDscExtension.md)

[<span data-ttu-id="38965-135">Satz-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="38965-135">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


