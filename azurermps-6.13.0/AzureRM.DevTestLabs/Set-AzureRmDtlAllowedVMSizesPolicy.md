---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: AAABDD1D-71BF-409C-B50B-9BE861D84229
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/set-azurermdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 5d5ca3f06ec76f45a8bb33aa5d4b810283ffce97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482482"
---
# <span data-ttu-id="143f7-101">Set-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="143f7-101">Set-AzureRmDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="143f7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="143f7-102">SYNOPSIS</span></span>
<span data-ttu-id="143f7-103">Legt die zulässige Größen Richtlinie für virtuelle Maschinen einer Übungseinheit in DevTest Labs fest.</span><span class="sxs-lookup"><span data-stu-id="143f7-103">Sets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="143f7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="143f7-104">SYNTAX</span></span>

### <span data-ttu-id="143f7-105">Aktivieren (Standard)</span><span class="sxs-lookup"><span data-stu-id="143f7-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="143f7-106">Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="143f7-106">Disable</span></span>
```
Set-AzureRmDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="143f7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="143f7-107">DESCRIPTION</span></span>
<span data-ttu-id="143f7-108">Das Cmdlet " **Set-AzureRmDtlAllowedVMSizesPolicy** " legt die zulässige Größen Richtlinie für virtuelle Maschinen fest, die eine Liste der in einer Übungseinheit zulässigen virtuellen Computer Größen angibt.</span><span class="sxs-lookup"><span data-stu-id="143f7-108">The **Set-AzureRmDtlAllowedVMSizesPolicy** cmdlet sets the allowed virtual machine sizes policy, which specifies a list of virtual machine sizes allowed in a lab.</span></span>
<span data-ttu-id="143f7-109">Das Cmdlet verwendet die angegebene Ressourcengruppe und den Namen der Übungseinheit, um die Richtlinie festzulegen.</span><span class="sxs-lookup"><span data-stu-id="143f7-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="143f7-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="143f7-110">EXAMPLES</span></span>

## <span data-ttu-id="143f7-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="143f7-111">PARAMETERS</span></span>

### <span data-ttu-id="143f7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="143f7-112">-DefaultProfile</span></span>
<span data-ttu-id="143f7-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="143f7-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="143f7-114">-Deaktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="143f7-114">-Disable</span></span>
<span data-ttu-id="143f7-115">Gibt an, dass dieses Cmdlet die Richtlinie deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="143f7-115">Indicates that this cmdlet disables the policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="143f7-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="143f7-116">-Enable</span></span>
<span data-ttu-id="143f7-117">Gibt an, dass dieses Cmdlet die Richtlinie aktiviert.</span><span class="sxs-lookup"><span data-stu-id="143f7-117">Indicates that this cmdlet enables the policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Enable
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="143f7-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="143f7-118">-LabName</span></span>
<span data-ttu-id="143f7-119">Gibt den Namen der Übungseinheit an, für die dieses Cmdlet die Richtlinien für virtuelle Computer Größen festlegt.</span><span class="sxs-lookup"><span data-stu-id="143f7-119">Specifies the name of the lab for which this cmdlet sets the virtual machine sizes policy.</span></span>

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

### <span data-ttu-id="143f7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="143f7-120">-ResourceGroupName</span></span>
<span data-ttu-id="143f7-121">Gibt den Namen der Ressourcengruppe an, zu der die Übungseinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="143f7-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="143f7-122">-VmSizes</span><span class="sxs-lookup"><span data-stu-id="143f7-122">-VmSizes</span></span>
<span data-ttu-id="143f7-123">Gibt als Zeichenfolgenarray die Liste der Größen für virtuelle Maschinen an, die in der Übungseinheit zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="143f7-123">Specifies, as a string array, the list of virtual machine sizes allowed in the lab.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="143f7-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="143f7-124">-Confirm</span></span>
<span data-ttu-id="143f7-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="143f7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="143f7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="143f7-126">-WhatIf</span></span>
<span data-ttu-id="143f7-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="143f7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="143f7-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="143f7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="143f7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="143f7-129">CommonParameters</span></span>
<span data-ttu-id="143f7-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="143f7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="143f7-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="143f7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="143f7-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="143f7-132">INPUTS</span></span>

### <span data-ttu-id="143f7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="143f7-133">System.String</span></span>

## <span data-ttu-id="143f7-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="143f7-134">OUTPUTS</span></span>

### <span data-ttu-id="143f7-135">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="143f7-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="143f7-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="143f7-136">NOTES</span></span>

## <span data-ttu-id="143f7-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="143f7-137">RELATED LINKS</span></span>

[<span data-ttu-id="143f7-138">Get-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="143f7-138">Get-AzureRmDtlAllowedVMSizesPolicy</span></span>](./Get-AzureRmDtlAllowedVMSizesPolicy.md)


