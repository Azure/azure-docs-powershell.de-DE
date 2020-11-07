---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
ms.openlocfilehash: 9256828a338678cb1da12e14cb6e450ee4030ebb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652012"
---
# <span data-ttu-id="01bd6-101">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="01bd6-101">Remove-AzVM</span></span>

## <span data-ttu-id="01bd6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="01bd6-102">SYNOPSIS</span></span>
<span data-ttu-id="01bd6-103">Entfernt einen virtuellen Computer aus Azure.</span><span class="sxs-lookup"><span data-stu-id="01bd6-103">Removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="01bd6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="01bd6-104">SYNTAX</span></span>

### <span data-ttu-id="01bd6-105">ResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="01bd6-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01bd6-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="01bd6-106">IdParameterSetName</span></span>
```
Remove-AzVM [-Force] [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01bd6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="01bd6-107">DESCRIPTION</span></span>
<span data-ttu-id="01bd6-108">Das Cmdlet **Remove-AzVM** entfernt einen virtuellen Computer aus Azure.</span><span class="sxs-lookup"><span data-stu-id="01bd6-108">The **Remove-AzVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="01bd6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="01bd6-109">EXAMPLES</span></span>

### <span data-ttu-id="01bd6-110">Beispiel 1: Entfernen eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="01bd6-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="01bd6-111">Dieser Befehl entfernt den virtuellen Computer mit dem Namen VirtualMachine07 in der Ressourcengruppe ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="01bd6-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="01bd6-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="01bd6-112">PARAMETERS</span></span>

### <span data-ttu-id="01bd6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01bd6-113">-AsJob</span></span>
<span data-ttu-id="01bd6-114">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="01bd6-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="01bd6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01bd6-115">-DefaultProfile</span></span>
<span data-ttu-id="01bd6-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="01bd6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01bd6-117">-Force</span><span class="sxs-lookup"><span data-stu-id="01bd6-117">-Force</span></span>
<span data-ttu-id="01bd6-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="01bd6-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01bd6-119">-ID</span><span class="sxs-lookup"><span data-stu-id="01bd6-119">-Id</span></span>
<span data-ttu-id="01bd6-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="01bd6-120">The resource group name.</span></span>

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

### <span data-ttu-id="01bd6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="01bd6-121">-Name</span></span>
<span data-ttu-id="01bd6-122">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="01bd6-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01bd6-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="01bd6-123">-NoWait</span></span>
<span data-ttu-id="01bd6-124">Startet den Vorgang und gibt unmittelbar vor dem Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="01bd6-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="01bd6-125">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="01bd6-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="01bd6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01bd6-126">-ResourceGroupName</span></span>
<span data-ttu-id="01bd6-127">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="01bd6-127">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="01bd6-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="01bd6-128">-Confirm</span></span>
<span data-ttu-id="01bd6-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="01bd6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01bd6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01bd6-130">-WhatIf</span></span>
<span data-ttu-id="01bd6-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="01bd6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01bd6-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="01bd6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01bd6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01bd6-133">CommonParameters</span></span>
<span data-ttu-id="01bd6-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01bd6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01bd6-135">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01bd6-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01bd6-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="01bd6-136">INPUTS</span></span>

### <span data-ttu-id="01bd6-137">System. String</span><span class="sxs-lookup"><span data-stu-id="01bd6-137">System.String</span></span>

## <span data-ttu-id="01bd6-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="01bd6-138">OUTPUTS</span></span>

### <span data-ttu-id="01bd6-139">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="01bd6-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="01bd6-140">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="01bd6-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="01bd6-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="01bd6-141">NOTES</span></span>

## <span data-ttu-id="01bd6-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="01bd6-142">RELATED LINKS</span></span>

[<span data-ttu-id="01bd6-143">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="01bd6-143">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="01bd6-144">Neu – AzVM</span><span class="sxs-lookup"><span data-stu-id="01bd6-144">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="01bd6-145">Neustart-AzVM</span><span class="sxs-lookup"><span data-stu-id="01bd6-145">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="01bd6-146">Anfang-AzVM</span><span class="sxs-lookup"><span data-stu-id="01bd6-146">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="01bd6-147">Stopp-AzVM</span><span class="sxs-lookup"><span data-stu-id="01bd6-147">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="01bd6-148">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="01bd6-148">Update-AzVM</span></span>](./Update-AzVM.md)


