---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: b3e060680ee5df25708f153b239ec6c13b4e8a35
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651936"
---
# <span data-ttu-id="2cdb3-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="2cdb3-101">Set-AzVM</span></span>

## <span data-ttu-id="2cdb3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2cdb3-102">SYNOPSIS</span></span>
<span data-ttu-id="2cdb3-103">Kennzeichnet einen virtuellen Computer als generalisiert.</span><span class="sxs-lookup"><span data-stu-id="2cdb3-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="2cdb3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2cdb3-104">SYNTAX</span></span>

### <span data-ttu-id="2cdb3-105">GeneralizeResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="2cdb3-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cdb3-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="2cdb3-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cdb3-107">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="2cdb3-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cdb3-108">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="2cdb3-108">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Redeploy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2cdb3-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2cdb3-109">DESCRIPTION</span></span>
<span data-ttu-id="2cdb3-110">Das Cmdlet " **Satz-AzVM** " kennzeichnet einen virtuellen Computer als generalisiert.</span><span class="sxs-lookup"><span data-stu-id="2cdb3-110">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="2cdb3-111">Bevor Sie dieses Cmdlet ausführen, melden Sie sich beim virtuellen Computer an, und verwenden Sie Sysprep zum Vorbereiten der Festplatte.</span><span class="sxs-lookup"><span data-stu-id="2cdb3-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="2cdb3-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2cdb3-112">EXAMPLES</span></span>

### <span data-ttu-id="2cdb3-113">Beispiel 1: Kennzeichnen eines virtuellen Computers als generalisiert</span><span class="sxs-lookup"><span data-stu-id="2cdb3-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="2cdb3-114">Dieser Befehl kennzeichnet den virtuellen Computer mit dem Namen "VirtualMachine07" als "generalisiert".</span><span class="sxs-lookup"><span data-stu-id="2cdb3-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="2cdb3-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="2cdb3-115">PARAMETERS</span></span>

### <span data-ttu-id="2cdb3-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2cdb3-116">-AsJob</span></span>
<span data-ttu-id="2cdb3-117">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="2cdb3-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="2cdb3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cdb3-118">-DefaultProfile</span></span>
<span data-ttu-id="2cdb3-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2cdb3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cdb3-120">-Generalisiert</span><span class="sxs-lookup"><span data-stu-id="2cdb3-120">-Generalized</span></span>
<span data-ttu-id="2cdb3-121">Gibt an, dass dieses Cmdlet einen virtuellen Computer als generalisiert kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2cdb3-121">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

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

### <span data-ttu-id="2cdb3-122">-ID</span><span class="sxs-lookup"><span data-stu-id="2cdb3-122">-Id</span></span>
<span data-ttu-id="2cdb3-123">Gibt die Ressourcen-ID des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="2cdb3-123">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cdb3-124">-Name</span><span class="sxs-lookup"><span data-stu-id="2cdb3-124">-Name</span></span>
<span data-ttu-id="2cdb3-125">Gibt den Namen des virtuellen Computers an, auf dem dieses Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2cdb3-125">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cdb3-126">-Nowait</span><span class="sxs-lookup"><span data-stu-id="2cdb3-126">-NoWait</span></span>
<span data-ttu-id="2cdb3-127">Startet den Vorgang und gibt unmittelbar vor dem Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="2cdb3-127">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="2cdb3-128">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="2cdb3-128">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cdb3-129">– Erneute Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="2cdb3-129">-Redeploy</span></span>
<span data-ttu-id="2cdb3-130">Gibt an, dass dieses Cmdlet den virtuellen Computer manuell auf einem anderen Azure-Host erneut bereitstellt, um Probleme zu beheben.</span><span class="sxs-lookup"><span data-stu-id="2cdb3-130">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="2cdb3-131">Wenn Sie einen virtuellen Computer erneut bereitstellen, wird er neu gestartet, was zum Verlust ephemerer Laufwerk Daten führt.</span><span class="sxs-lookup"><span data-stu-id="2cdb3-131">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

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

### <span data-ttu-id="2cdb3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cdb3-132">-ResourceGroupName</span></span>
<span data-ttu-id="2cdb3-133">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="2cdb3-133">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cdb3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cdb3-134">CommonParameters</span></span>
<span data-ttu-id="2cdb3-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cdb3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cdb3-136">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2cdb3-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cdb3-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2cdb3-137">INPUTS</span></span>

### <span data-ttu-id="2cdb3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2cdb3-138">System.String</span></span>

## <span data-ttu-id="2cdb3-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2cdb3-139">OUTPUTS</span></span>

### <span data-ttu-id="2cdb3-140">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="2cdb3-140">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="2cdb3-141">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2cdb3-141">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2cdb3-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="2cdb3-142">NOTES</span></span>

## <span data-ttu-id="2cdb3-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2cdb3-143">RELATED LINKS</span></span>

[<span data-ttu-id="2cdb3-144">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="2cdb3-144">Get-AzVM</span></span>](./Get-AzVM.md)


