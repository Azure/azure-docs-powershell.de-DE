---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: D00E04D9-C91F-4F89-8867-0A026C274F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: 33f60d8246f7235e4be816ad55b69c2ebafe9b0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651302"
---
# <span data-ttu-id="8e3f8-101">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="8e3f8-101">Set-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="8e3f8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8e3f8-102">SYNOPSIS</span></span>
<span data-ttu-id="8e3f8-103">Legt die Richtlinie für virtuelle Computer pro Benutzer einer Übungseinheit in DevTest Labs fest.</span><span class="sxs-lookup"><span data-stu-id="8e3f8-103">Sets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="8e3f8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e3f8-104">SYNTAX</span></span>

### <span data-ttu-id="8e3f8-105">Aktivieren (Standard)</span><span class="sxs-lookup"><span data-stu-id="8e3f8-105">Enable (Default)</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e3f8-106">Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="8e3f8-106">Disable</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e3f8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e3f8-107">DESCRIPTION</span></span>
<span data-ttu-id="8e3f8-108">Mit dem Cmdlet **Set-AzDtlVMsPerUserPolicy** werden die virtuellen Computer pro Benutzerrichtlinie einer Übungseinheit festgelegt, wodurch die maximale Anzahl der pro Benutzer zulässigen virtuellen Computer festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8e3f8-108">The **Set-AzDtlVMsPerUserPolicy** cmdlet sets the virtual machines per user policy of a lab, which sets the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="8e3f8-109">Das Cmdlet verwendet die angegebene Ressourcengruppe und den Namen der Übungseinheit, um die Richtlinie festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8e3f8-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="8e3f8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8e3f8-110">EXAMPLES</span></span>

## <span data-ttu-id="8e3f8-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e3f8-111">PARAMETERS</span></span>

### <span data-ttu-id="8e3f8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e3f8-112">-DefaultProfile</span></span>
<span data-ttu-id="8e3f8-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8e3f8-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e3f8-114">-Deaktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="8e3f8-114">-Disable</span></span>
<span data-ttu-id="8e3f8-115">Gibt an, dass dieses Cmdlet die Richtlinie für die Übungseinheit deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8e3f8-115">Indicates that this cmdlet disables the policy for the lab.</span></span>

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

### <span data-ttu-id="8e3f8-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="8e3f8-116">-Enable</span></span>
<span data-ttu-id="8e3f8-117">Gibt an, dass dieses Cmdlet die Richtlinie für die Übungseinheit aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8e3f8-117">Indicates that this cmdlet enables the policy for the lab.</span></span>

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

### <span data-ttu-id="8e3f8-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="8e3f8-118">-LabName</span></span>
<span data-ttu-id="8e3f8-119">Gibt den Namen der Übungseinheit an, für die dieses Cmdlet die virtuellen Computer pro Benutzerrichtlinie festlegt.</span><span class="sxs-lookup"><span data-stu-id="8e3f8-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per user policy.</span></span>

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

### <span data-ttu-id="8e3f8-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="8e3f8-120">-MaxVMs</span></span>
<span data-ttu-id="8e3f8-121">Gibt die maximale Anzahl virtueller Computer an, die in der Übungseinheit erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="8e3f8-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

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

### <span data-ttu-id="8e3f8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e3f8-122">-ResourceGroupName</span></span>
<span data-ttu-id="8e3f8-123">Gibt den Namen der Ressourcengruppe an, zu der die Übungseinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="8e3f8-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="8e3f8-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8e3f8-124">-Confirm</span></span>
<span data-ttu-id="8e3f8-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8e3f8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e3f8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e3f8-126">-WhatIf</span></span>
<span data-ttu-id="8e3f8-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8e3f8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e3f8-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8e3f8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e3f8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e3f8-129">CommonParameters</span></span>
<span data-ttu-id="8e3f8-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e3f8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e3f8-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e3f8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e3f8-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8e3f8-132">INPUTS</span></span>

### <span data-ttu-id="8e3f8-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8e3f8-133">System.String</span></span>

## <span data-ttu-id="8e3f8-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8e3f8-134">OUTPUTS</span></span>

### <span data-ttu-id="8e3f8-135">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="8e3f8-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="8e3f8-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="8e3f8-136">NOTES</span></span>

## <span data-ttu-id="8e3f8-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8e3f8-137">RELATED LINKS</span></span>

[<span data-ttu-id="8e3f8-138">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="8e3f8-138">Get-AzDtlVMsPerUserPolicy</span></span>](./Get-AzDtlVMsPerUserPolicy.md)


