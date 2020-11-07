---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDscExtension.md
ms.openlocfilehash: 69eff38068c379dadc4f3a061cfba4f9cb6539e3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844368"
---
# <span data-ttu-id="6225f-101">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="6225f-101">Remove-AzVMDscExtension</span></span>

## <span data-ttu-id="6225f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6225f-102">SYNOPSIS</span></span>
<span data-ttu-id="6225f-103">Entfernt einen DSC-Erweiterungshandler von einem virtuellen Computer in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6225f-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="6225f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6225f-104">SYNTAX</span></span>

```
Remove-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6225f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6225f-105">DESCRIPTION</span></span>
<span data-ttu-id="6225f-106">Mit dem Cmdlet **Remove-AzVMDscExtension** wird der Erweiterungshandler für die gewünschte Zustands Konfiguration (DSC) von einem virtuellen Computer in einer Ressourcengruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="6225f-106">The **Remove-AzVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="6225f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6225f-107">EXAMPLES</span></span>

### <span data-ttu-id="6225f-108">Beispiel 1: Entfernen einer DSC-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="6225f-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="6225f-109">Dieser Befehl entfernt die Erweiterung mit dem Namen DSC auf dem virtuellen Computer mit dem Namen VM07.</span><span class="sxs-lookup"><span data-stu-id="6225f-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="6225f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6225f-110">PARAMETERS</span></span>

### <span data-ttu-id="6225f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6225f-111">-DefaultProfile</span></span>
<span data-ttu-id="6225f-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6225f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6225f-113">-Name</span><span class="sxs-lookup"><span data-stu-id="6225f-113">-Name</span></span>
<span data-ttu-id="6225f-114">Gibt den Namen der DSC-Erweiterung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="6225f-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="6225f-115">Mit dem Set-AzVMDscExtension-Cmdlet wird dieser Name auf Microsoft. PowerShell. DSC festgelegt, bei dem es sich um den Standardwert handelt, der von **Remove-AzVMDscExtension** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6225f-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzVMDscExtension**.</span></span>

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

### <span data-ttu-id="6225f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6225f-116">-ResourceGroupName</span></span>
<span data-ttu-id="6225f-117">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="6225f-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="6225f-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="6225f-118">-VMName</span></span>
<span data-ttu-id="6225f-119">Gibt den Namen eines virtuellen Computers an, von dem dieses Cmdlet die DSC-Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="6225f-119">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

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

### <span data-ttu-id="6225f-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6225f-120">-Confirm</span></span>
<span data-ttu-id="6225f-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6225f-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6225f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6225f-122">-WhatIf</span></span>
<span data-ttu-id="6225f-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6225f-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="6225f-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6225f-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6225f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6225f-125">CommonParameters</span></span>
<span data-ttu-id="6225f-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6225f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6225f-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6225f-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6225f-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6225f-128">INPUTS</span></span>

### <span data-ttu-id="6225f-129">Keine</span><span class="sxs-lookup"><span data-stu-id="6225f-129">None</span></span>
<span data-ttu-id="6225f-130">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="6225f-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6225f-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6225f-131">OUTPUTS</span></span>

### <span data-ttu-id="6225f-132">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6225f-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="6225f-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="6225f-133">NOTES</span></span>

## <span data-ttu-id="6225f-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6225f-134">RELATED LINKS</span></span>

[<span data-ttu-id="6225f-135">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="6225f-135">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="6225f-136">Satz-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="6225f-136">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


