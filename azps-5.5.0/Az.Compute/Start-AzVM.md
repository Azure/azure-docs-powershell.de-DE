---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: 32e633d1f9fea877ef81b6c6e7ef5e8bb09da81a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167889"
---
# <span data-ttu-id="69b6a-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="69b6a-101">Start-AzVM</span></span>

## <span data-ttu-id="69b6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69b6a-102">SYNOPSIS</span></span>
<span data-ttu-id="69b6a-103">Startet einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="69b6a-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="69b6a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69b6a-104">SYNTAX</span></span>

### <span data-ttu-id="69b6a-105">ResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="69b6a-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69b6a-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="69b6a-106">IdParameterSetName</span></span>
```
Start-AzVM [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="69b6a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="69b6a-107">DESCRIPTION</span></span>
<span data-ttu-id="69b6a-108">Das **Start-AzVM-Cmdlet** startet einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="69b6a-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="69b6a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="69b6a-109">EXAMPLES</span></span>

### <span data-ttu-id="69b6a-110">Beispiel 1: Starten eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="69b6a-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="69b6a-111">Dieser Befehl startet den virtuellen Computer "VirtualMachine07" in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="69b6a-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="69b6a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69b6a-112">PARAMETERS</span></span>

### <span data-ttu-id="69b6a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69b6a-113">-AsJob</span></span>
<span data-ttu-id="69b6a-114">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="69b6a-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="69b6a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69b6a-115">-DefaultProfile</span></span>
<span data-ttu-id="69b6a-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="69b6a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69b6a-117">-ID</span><span class="sxs-lookup"><span data-stu-id="69b6a-117">-Id</span></span>
<span data-ttu-id="69b6a-118">Die ID des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="69b6a-118">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="69b6a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="69b6a-119">-Name</span></span>
<span data-ttu-id="69b6a-120">Der Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="69b6a-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="69b6a-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="69b6a-121">-NoWait</span></span>
<span data-ttu-id="69b6a-122">Der Vorgang wird gestartet und unmittelbar vor Abschluss des Vorgangs beendet.</span><span class="sxs-lookup"><span data-stu-id="69b6a-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="69b6a-123">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="69b6a-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="69b6a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69b6a-124">-ResourceGroupName</span></span>
<span data-ttu-id="69b6a-125">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="69b6a-125">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="69b6a-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69b6a-126">-Confirm</span></span>
<span data-ttu-id="69b6a-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="69b6a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69b6a-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="69b6a-128">-WhatIf</span></span>
<span data-ttu-id="69b6a-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="69b6a-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="69b6a-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="69b6a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69b6a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69b6a-131">CommonParameters</span></span>
<span data-ttu-id="69b6a-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69b6a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69b6a-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69b6a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69b6a-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="69b6a-134">INPUTS</span></span>

### <span data-ttu-id="69b6a-135">System.String</span><span class="sxs-lookup"><span data-stu-id="69b6a-135">System.String</span></span>

## <span data-ttu-id="69b6a-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="69b6a-136">OUTPUTS</span></span>

### <span data-ttu-id="69b6a-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="69b6a-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="69b6a-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="69b6a-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="69b6a-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="69b6a-139">NOTES</span></span>

## <span data-ttu-id="69b6a-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="69b6a-140">RELATED LINKS</span></span>

[<span data-ttu-id="69b6a-141">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="69b6a-141">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="69b6a-142">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="69b6a-142">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="69b6a-143">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="69b6a-143">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="69b6a-144">Neustart-AzVM</span><span class="sxs-lookup"><span data-stu-id="69b6a-144">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="69b6a-145">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="69b6a-145">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="69b6a-146">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="69b6a-146">Update-AzVM</span></span>](./Update-AzVM.md)


