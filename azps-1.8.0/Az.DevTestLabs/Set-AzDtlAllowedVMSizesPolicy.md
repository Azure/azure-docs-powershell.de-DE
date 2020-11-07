---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: AAABDD1D-71BF-409C-B50B-9BE861D84229
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 9d41e3c4c91a61a12ac18becb4b996bfbe52dbb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661152"
---
# <span data-ttu-id="e81bc-101">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="e81bc-101">Set-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="e81bc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e81bc-102">SYNOPSIS</span></span>
<span data-ttu-id="e81bc-103">Legt die zulässige Größen Richtlinie für virtuelle Maschinen einer Übungseinheit in DevTest Labs fest.</span><span class="sxs-lookup"><span data-stu-id="e81bc-103">Sets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="e81bc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e81bc-104">SYNTAX</span></span>

### <span data-ttu-id="e81bc-105">Aktivieren (Standard)</span><span class="sxs-lookup"><span data-stu-id="e81bc-105">Enable (Default)</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e81bc-106">Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="e81bc-106">Disable</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e81bc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e81bc-107">DESCRIPTION</span></span>
<span data-ttu-id="e81bc-108">Das Cmdlet " **Set-AzDtlAllowedVMSizesPolicy** " legt die zulässige Größen Richtlinie für virtuelle Maschinen fest, die eine Liste der in einer Übungseinheit zulässigen virtuellen Computer Größen angibt.</span><span class="sxs-lookup"><span data-stu-id="e81bc-108">The **Set-AzDtlAllowedVMSizesPolicy** cmdlet sets the allowed virtual machine sizes policy, which specifies a list of virtual machine sizes allowed in a lab.</span></span>
<span data-ttu-id="e81bc-109">Das Cmdlet verwendet die angegebene Ressourcengruppe und den Namen der Übungseinheit, um die Richtlinie festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e81bc-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="e81bc-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e81bc-110">EXAMPLES</span></span>

## <span data-ttu-id="e81bc-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e81bc-111">PARAMETERS</span></span>

### <span data-ttu-id="e81bc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e81bc-112">-DefaultProfile</span></span>
<span data-ttu-id="e81bc-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e81bc-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e81bc-114">-Deaktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="e81bc-114">-Disable</span></span>
<span data-ttu-id="e81bc-115">Gibt an, dass dieses Cmdlet die Richtlinie deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e81bc-115">Indicates that this cmdlet disables the policy.</span></span>

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

### <span data-ttu-id="e81bc-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="e81bc-116">-Enable</span></span>
<span data-ttu-id="e81bc-117">Gibt an, dass dieses Cmdlet die Richtlinie aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e81bc-117">Indicates that this cmdlet enables the policy.</span></span>

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

### <span data-ttu-id="e81bc-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="e81bc-118">-LabName</span></span>
<span data-ttu-id="e81bc-119">Gibt den Namen der Übungseinheit an, für die dieses Cmdlet die Richtlinien für virtuelle Computer Größen festlegt.</span><span class="sxs-lookup"><span data-stu-id="e81bc-119">Specifies the name of the lab for which this cmdlet sets the virtual machine sizes policy.</span></span>

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

### <span data-ttu-id="e81bc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e81bc-120">-ResourceGroupName</span></span>
<span data-ttu-id="e81bc-121">Gibt den Namen der Ressourcengruppe an, zu der die Übungseinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="e81bc-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="e81bc-122">-VmSizes</span><span class="sxs-lookup"><span data-stu-id="e81bc-122">-VmSizes</span></span>
<span data-ttu-id="e81bc-123">Gibt als Zeichenfolgenarray die Liste der Größen für virtuelle Maschinen an, die in der Übungseinheit zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="e81bc-123">Specifies, as a string array, the list of virtual machine sizes allowed in the lab.</span></span>

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

### <span data-ttu-id="e81bc-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e81bc-124">-Confirm</span></span>
<span data-ttu-id="e81bc-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e81bc-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e81bc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e81bc-126">-WhatIf</span></span>
<span data-ttu-id="e81bc-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e81bc-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e81bc-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e81bc-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e81bc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e81bc-129">CommonParameters</span></span>
<span data-ttu-id="e81bc-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e81bc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e81bc-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e81bc-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e81bc-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e81bc-132">INPUTS</span></span>

### <span data-ttu-id="e81bc-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e81bc-133">System.String</span></span>

## <span data-ttu-id="e81bc-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e81bc-134">OUTPUTS</span></span>

### <span data-ttu-id="e81bc-135">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="e81bc-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="e81bc-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="e81bc-136">NOTES</span></span>

## <span data-ttu-id="e81bc-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e81bc-137">RELATED LINKS</span></span>

[<span data-ttu-id="e81bc-138">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="e81bc-138">Get-AzDtlAllowedVMSizesPolicy</span></span>](./Get-AzDtlAllowedVMSizesPolicy.md)


