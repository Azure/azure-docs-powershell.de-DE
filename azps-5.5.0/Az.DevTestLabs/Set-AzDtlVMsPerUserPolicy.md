---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: D00E04D9-C91F-4F89-8867-0A026C274F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: 48f9e2a91923fa123b54b5ebf09abbb7cd64a1dd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163660"
---
# <span data-ttu-id="0a676-101">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="0a676-101">Set-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="0a676-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a676-102">SYNOPSIS</span></span>
<span data-ttu-id="0a676-103">Legt die virtuellen Computer pro Benutzerrichtlinie einer Übungseinheit in DevTest Labs fest.</span><span class="sxs-lookup"><span data-stu-id="0a676-103">Sets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="0a676-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0a676-104">SYNTAX</span></span>

### <span data-ttu-id="0a676-105">Aktivieren (Standard)</span><span class="sxs-lookup"><span data-stu-id="0a676-105">Enable (Default)</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a676-106">Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="0a676-106">Disable</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a676-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0a676-107">DESCRIPTION</span></span>
<span data-ttu-id="0a676-108">Das **Cmdlet "Set-AzDtlVMsPerUserPolicy"** legt die virtuellen Computer pro Benutzerrichtlinie einer Übungseinheit fest, mit der die maximal zulässige Anzahl virtueller Computer pro Benutzer festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="0a676-108">The **Set-AzDtlVMsPerUserPolicy** cmdlet sets the virtual machines per user policy of a lab, which sets the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="0a676-109">Das Cmdlet verwendet die angegebene Ressourcengruppe und den Namen der Übungseinheit zum Festlegen der Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="0a676-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="0a676-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0a676-110">EXAMPLES</span></span>

## <span data-ttu-id="0a676-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a676-111">PARAMETERS</span></span>

### <span data-ttu-id="0a676-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a676-112">-DefaultProfile</span></span>
<span data-ttu-id="0a676-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0a676-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a676-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="0a676-114">-Disable</span></span>
<span data-ttu-id="0a676-115">Gibt an, dass mit diesem Cmdlet die Richtlinie für die Übungseinheit deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="0a676-115">Indicates that this cmdlet disables the policy for the lab.</span></span>

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

### <span data-ttu-id="0a676-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="0a676-116">-Enable</span></span>
<span data-ttu-id="0a676-117">Gibt an, dass dieses Cmdlet die Richtlinie für die Übungseinheit aktiviert.</span><span class="sxs-lookup"><span data-stu-id="0a676-117">Indicates that this cmdlet enables the policy for the lab.</span></span>

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

### <span data-ttu-id="0a676-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="0a676-118">-LabName</span></span>
<span data-ttu-id="0a676-119">Gibt den Namen der Übung an, für die dieses Cmdlet die virtuellen Computer pro Benutzerrichtlinie festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0a676-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per user policy.</span></span>

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

### <span data-ttu-id="0a676-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="0a676-120">-MaxVMs</span></span>
<span data-ttu-id="0a676-121">Gibt die maximale Anzahl virtueller Computer an, die in der Übung erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="0a676-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a676-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a676-122">-ResourceGroupName</span></span>
<span data-ttu-id="0a676-123">Gibt den Namen der Ressourcengruppe an, zu der die Übungseinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="0a676-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="0a676-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a676-124">-Confirm</span></span>
<span data-ttu-id="0a676-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0a676-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a676-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0a676-126">-WhatIf</span></span>
<span data-ttu-id="0a676-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0a676-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a676-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0a676-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a676-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a676-129">CommonParameters</span></span>
<span data-ttu-id="0a676-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a676-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a676-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a676-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a676-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0a676-132">INPUTS</span></span>

### <span data-ttu-id="0a676-133">System.String</span><span class="sxs-lookup"><span data-stu-id="0a676-133">System.String</span></span>

## <span data-ttu-id="0a676-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0a676-134">OUTPUTS</span></span>

### <span data-ttu-id="0a676-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="0a676-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="0a676-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0a676-136">NOTES</span></span>

## <span data-ttu-id="0a676-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0a676-137">RELATED LINKS</span></span>

[<span data-ttu-id="0a676-138">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="0a676-138">Get-AzDtlVMsPerUserPolicy</span></span>](./Get-AzDtlVMsPerUserPolicy.md)


