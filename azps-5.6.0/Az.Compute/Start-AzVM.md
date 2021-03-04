---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: daf1a9c738e6e4d0d97a22eedc8355750d15ec72
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945286"
---
# <span data-ttu-id="99b8d-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="99b8d-101">Start-AzVM</span></span>

## <span data-ttu-id="99b8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99b8d-102">SYNOPSIS</span></span>
<span data-ttu-id="99b8d-103">Startet einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="99b8d-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="99b8d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99b8d-104">SYNTAX</span></span>

### <span data-ttu-id="99b8d-105">ResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="99b8d-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99b8d-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="99b8d-106">IdParameterSetName</span></span>
```
Start-AzVM [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="99b8d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="99b8d-107">DESCRIPTION</span></span>
<span data-ttu-id="99b8d-108">Das **Cmdlet Start-AzVM** startet einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="99b8d-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="99b8d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="99b8d-109">EXAMPLES</span></span>

### <span data-ttu-id="99b8d-110">Beispiel 1: Starten eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="99b8d-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="99b8d-111">Mit diesem Befehl wird der virtuelle Computer "VirtualMachine07" in ResourceGroup11 gestartet.</span><span class="sxs-lookup"><span data-stu-id="99b8d-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="99b8d-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="99b8d-112">PARAMETERS</span></span>

### <span data-ttu-id="99b8d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99b8d-113">-AsJob</span></span>
<span data-ttu-id="99b8d-114">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="99b8d-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="99b8d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99b8d-115">-DefaultProfile</span></span>
<span data-ttu-id="99b8d-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="99b8d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99b8d-117">-ID</span><span class="sxs-lookup"><span data-stu-id="99b8d-117">-Id</span></span>
<span data-ttu-id="99b8d-118">Die ID des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="99b8d-118">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="99b8d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="99b8d-119">-Name</span></span>
<span data-ttu-id="99b8d-120">Der Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="99b8d-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="99b8d-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="99b8d-121">-NoWait</span></span>
<span data-ttu-id="99b8d-122">Startet den Vorgang und gibt sofort zurück, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="99b8d-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="99b8d-123">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="99b8d-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="99b8d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99b8d-124">-ResourceGroupName</span></span>
<span data-ttu-id="99b8d-125">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="99b8d-125">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="99b8d-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="99b8d-126">-Confirm</span></span>
<span data-ttu-id="99b8d-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="99b8d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99b8d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99b8d-128">-WhatIf</span></span>
<span data-ttu-id="99b8d-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="99b8d-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="99b8d-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="99b8d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99b8d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99b8d-131">CommonParameters</span></span>
<span data-ttu-id="99b8d-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99b8d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99b8d-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99b8d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99b8d-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="99b8d-134">INPUTS</span></span>

### <span data-ttu-id="99b8d-135">System.String</span><span class="sxs-lookup"><span data-stu-id="99b8d-135">System.String</span></span>

## <span data-ttu-id="99b8d-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="99b8d-136">OUTPUTS</span></span>

### <span data-ttu-id="99b8d-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="99b8d-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="99b8d-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="99b8d-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="99b8d-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="99b8d-139">NOTES</span></span>

## <span data-ttu-id="99b8d-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="99b8d-140">RELATED LINKS</span></span>

[<span data-ttu-id="99b8d-141">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="99b8d-141">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="99b8d-142">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="99b8d-142">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="99b8d-143">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="99b8d-143">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="99b8d-144">Neustart-AzVM</span><span class="sxs-lookup"><span data-stu-id="99b8d-144">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="99b8d-145">Stopp-AzVM</span><span class="sxs-lookup"><span data-stu-id="99b8d-145">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="99b8d-146">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="99b8d-146">Update-AzVM</span></span>](./Update-AzVM.md)


