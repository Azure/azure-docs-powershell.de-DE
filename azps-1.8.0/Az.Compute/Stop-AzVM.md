---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: 393f2a75217b95b6c1c5366326735ac0f78ac294
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820504"
---
# <span data-ttu-id="7995c-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="7995c-101">Stop-AzVM</span></span>

## <span data-ttu-id="7995c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7995c-102">SYNOPSIS</span></span>
<span data-ttu-id="7995c-103">Beendet einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="7995c-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="7995c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7995c-104">SYNTAX</span></span>

### <span data-ttu-id="7995c-105">ResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7995c-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7995c-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="7995c-106">IdParameterSetName</span></span>
```
Stop-AzVM [[-Name] <String>] [-Force] [-StayProvisioned] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7995c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7995c-107">DESCRIPTION</span></span>
<span data-ttu-id="7995c-108">Das Cmdlet **Stop-AzVM** beendet einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="7995c-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="7995c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7995c-109">EXAMPLES</span></span>

### <span data-ttu-id="7995c-110">Beispiel 1: Beenden eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="7995c-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="7995c-111">Dieser Befehl beendet den virtuellen Computer mit dem Namen VirtualMachine07 in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="7995c-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="7995c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7995c-112">PARAMETERS</span></span>

### <span data-ttu-id="7995c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7995c-113">-AsJob</span></span>
<span data-ttu-id="7995c-114">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="7995c-114">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7995c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7995c-115">-DefaultProfile</span></span>
<span data-ttu-id="7995c-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7995c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7995c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7995c-117">-Force</span></span>
<span data-ttu-id="7995c-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="7995c-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7995c-119">-ID</span><span class="sxs-lookup"><span data-stu-id="7995c-119">-Id</span></span>
<span data-ttu-id="7995c-120">Die ID des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="7995c-120">The ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7995c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7995c-121">-Name</span></span>
<span data-ttu-id="7995c-122">Der Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="7995c-122">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7995c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7995c-123">-ResourceGroupName</span></span>
<span data-ttu-id="7995c-124">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="7995c-124">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7995c-125">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="7995c-125">-StayProvisioned</span></span>
<span data-ttu-id="7995c-126">Das Cmdlet beendet alle virtuellen Computer innerhalb des VMSS, gibt diese jedoch nicht aus.</span><span class="sxs-lookup"><span data-stu-id="7995c-126">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="7995c-127">Das Konto wird für die angehalten virtuellen Computer berechnet.</span><span class="sxs-lookup"><span data-stu-id="7995c-127">The account is charged for the stopped virtual machines.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7995c-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7995c-128">-Confirm</span></span>
<span data-ttu-id="7995c-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7995c-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7995c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7995c-130">-WhatIf</span></span>
<span data-ttu-id="7995c-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7995c-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7995c-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7995c-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7995c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7995c-133">CommonParameters</span></span>
<span data-ttu-id="7995c-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7995c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7995c-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7995c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7995c-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7995c-136">INPUTS</span></span>

### <span data-ttu-id="7995c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7995c-137">System.String</span></span>

## <span data-ttu-id="7995c-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7995c-138">OUTPUTS</span></span>

### <span data-ttu-id="7995c-139">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="7995c-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="7995c-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="7995c-140">NOTES</span></span>

## <span data-ttu-id="7995c-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7995c-141">RELATED LINKS</span></span>

[<span data-ttu-id="7995c-142">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="7995c-142">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="7995c-143">Neu – AzVM</span><span class="sxs-lookup"><span data-stu-id="7995c-143">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="7995c-144">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="7995c-144">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="7995c-145">Neustart-AzVM</span><span class="sxs-lookup"><span data-stu-id="7995c-145">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="7995c-146">Anfang-AzVM</span><span class="sxs-lookup"><span data-stu-id="7995c-146">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="7995c-147">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="7995c-147">Update-AzVM</span></span>](./Update-AzVM.md)


