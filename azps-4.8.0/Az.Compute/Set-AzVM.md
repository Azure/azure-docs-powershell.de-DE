---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: 34c49bdd798e23e9c5d151ed3de577136fad5b03
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173294"
---
# <span data-ttu-id="72338-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="72338-101">Set-AzVM</span></span>

## <span data-ttu-id="72338-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="72338-102">SYNOPSIS</span></span>
<span data-ttu-id="72338-103">Kennzeichnet einen virtuellen Computer als generalisiert.</span><span class="sxs-lookup"><span data-stu-id="72338-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="72338-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="72338-104">SYNTAX</span></span>

### <span data-ttu-id="72338-105">GeneralizeResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="72338-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72338-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="72338-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72338-107">ReapplyResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="72338-107">ReapplyResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Reapply] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72338-108">SimulateEvictionResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="72338-108">SimulateEvictionResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-SimulateEviction] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72338-109">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="72338-109">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72338-110">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="72338-110">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Redeploy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="72338-111">ReapplyIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="72338-111">ReapplyIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Reapply] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="72338-112">SimulateEvictionIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="72338-112">SimulateEvictionIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-SimulateEviction] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="72338-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72338-113">DESCRIPTION</span></span>
<span data-ttu-id="72338-114">Das Cmdlet " **Satz-AzVM** " kennzeichnet einen virtuellen Computer als generalisiert.</span><span class="sxs-lookup"><span data-stu-id="72338-114">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="72338-115">Bevor Sie dieses Cmdlet ausführen, melden Sie sich beim virtuellen Computer an, und verwenden Sie Sysprep zum Vorbereiten der Festplatte.</span><span class="sxs-lookup"><span data-stu-id="72338-115">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="72338-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="72338-116">EXAMPLES</span></span>

### <span data-ttu-id="72338-117">Beispiel 1: Kennzeichnen eines virtuellen Computers als generalisiert</span><span class="sxs-lookup"><span data-stu-id="72338-117">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="72338-118">Dieser Befehl kennzeichnet den virtuellen Computer mit dem Namen "VirtualMachine07" als "generalisiert".</span><span class="sxs-lookup"><span data-stu-id="72338-118">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="72338-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="72338-119">PARAMETERS</span></span>

### <span data-ttu-id="72338-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="72338-120">-AsJob</span></span>
<span data-ttu-id="72338-121">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="72338-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="72338-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72338-122">-DefaultProfile</span></span>
<span data-ttu-id="72338-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="72338-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72338-124">-Generalisiert</span><span class="sxs-lookup"><span data-stu-id="72338-124">-Generalized</span></span>
<span data-ttu-id="72338-125">Gibt an, dass dieses Cmdlet einen virtuellen Computer als generalisiert kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="72338-125">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, GeneralizeIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72338-126">-ID</span><span class="sxs-lookup"><span data-stu-id="72338-126">-Id</span></span>
<span data-ttu-id="72338-127">Gibt die Ressourcen-ID des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="72338-127">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName, ReapplyIdParameterSetName, SimulateEvictionIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72338-128">-Name</span><span class="sxs-lookup"><span data-stu-id="72338-128">-Name</span></span>
<span data-ttu-id="72338-129">Gibt den Namen des virtuellen Computers an, auf dem dieses Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="72338-129">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName, SimulateEvictionResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72338-130">-Nowait</span><span class="sxs-lookup"><span data-stu-id="72338-130">-NoWait</span></span>
<span data-ttu-id="72338-131">Startet den Vorgang und gibt unmittelbar vor dem Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="72338-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="72338-132">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="72338-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName, RedeployIdParameterSetName, ReapplyIdParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72338-133">-Erneute Anwendung</span><span class="sxs-lookup"><span data-stu-id="72338-133">-Reapply</span></span>
<span data-ttu-id="72338-134">So wenden Sie den virtuellen Computer erneut an.</span><span class="sxs-lookup"><span data-stu-id="72338-134">To reapply virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReapplyResourceGroupNameParameterSetName, ReapplyIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72338-135">– Erneute Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="72338-135">-Redeploy</span></span>
<span data-ttu-id="72338-136">Gibt an, dass dieses Cmdlet den virtuellen Computer manuell auf einem anderen Azure-Host erneut bereitstellt, um Probleme zu beheben.</span><span class="sxs-lookup"><span data-stu-id="72338-136">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="72338-137">Wenn Sie einen virtuellen Computer erneut bereitstellen, wird er neu gestartet, was zum Verlust ephemerer Laufwerk Daten führt.</span><span class="sxs-lookup"><span data-stu-id="72338-137">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72338-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72338-138">-ResourceGroupName</span></span>
<span data-ttu-id="72338-139">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="72338-139">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName, SimulateEvictionResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72338-140">-SimulateEviction</span><span class="sxs-lookup"><span data-stu-id="72338-140">-SimulateEviction</span></span>
<span data-ttu-id="72338-141">Gibt an, dass dieses Cmdlet die Entfernung von Spot Virtual Machine simuliert.</span><span class="sxs-lookup"><span data-stu-id="72338-141">Indicates that this cmdlet simulates the eviction of spot virtual machine.</span></span>
<span data-ttu-id="72338-142">Die Räumung erfolgt innerhalb von 30 Minuten nach dem Aufruf der API.</span><span class="sxs-lookup"><span data-stu-id="72338-142">The eviction will occur within 30 minutes of calling the API.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimulateEvictionResourceGroupNameParameterSetName, SimulateEvictionIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72338-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72338-143">CommonParameters</span></span>
<span data-ttu-id="72338-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72338-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72338-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72338-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72338-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="72338-146">INPUTS</span></span>

### <span data-ttu-id="72338-147">System. String</span><span class="sxs-lookup"><span data-stu-id="72338-147">System.String</span></span>

## <span data-ttu-id="72338-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="72338-148">OUTPUTS</span></span>

### <span data-ttu-id="72338-149">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="72338-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="72338-150">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="72338-150">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="72338-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="72338-151">NOTES</span></span>

## <span data-ttu-id="72338-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="72338-152">RELATED LINKS</span></span>

[<span data-ttu-id="72338-153">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="72338-153">Get-AzVM</span></span>](./Get-AzVM.md)


