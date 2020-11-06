---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvm
schema: 2.0.0
ms.openlocfilehash: d17d01295d118c3927c127a367747cfde428ccfd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476933"
---
# <span data-ttu-id="3646e-101">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3646e-101">Set-AzureRmVM</span></span>

## <span data-ttu-id="3646e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3646e-102">SYNOPSIS</span></span>
<span data-ttu-id="3646e-103">Kennzeichnet einen virtuellen Computer als generalisiert.</span><span class="sxs-lookup"><span data-stu-id="3646e-103">Marks a virtual machine as generalized.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3646e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3646e-104">SYNTAX</span></span>

### <span data-ttu-id="3646e-105">GeneralizeResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="3646e-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3646e-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="3646e-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3646e-107">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="3646e-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3646e-108">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="3646e-108">RedeployIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Redeploy] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3646e-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3646e-109">DESCRIPTION</span></span>
<span data-ttu-id="3646e-110">Das Cmdlet " **Satz-AzureRmVM** " kennzeichnet einen virtuellen Computer als generalisiert.</span><span class="sxs-lookup"><span data-stu-id="3646e-110">The **Set-AzureRmVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="3646e-111">Bevor Sie dieses Cmdlet ausführen, melden Sie sich beim virtuellen Computer an, und verwenden Sie Sysprep zum Vorbereiten der Festplatte.</span><span class="sxs-lookup"><span data-stu-id="3646e-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="3646e-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3646e-112">EXAMPLES</span></span>

### <span data-ttu-id="3646e-113">Beispiel 1: Kennzeichnen eines virtuellen Computers als generalisiert</span><span class="sxs-lookup"><span data-stu-id="3646e-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="3646e-114">Dieser Befehl kennzeichnet den virtuellen Computer mit dem Namen "VirtualMachine07" als "generalisiert".</span><span class="sxs-lookup"><span data-stu-id="3646e-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="3646e-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="3646e-115">PARAMETERS</span></span>

### <span data-ttu-id="3646e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3646e-116">-AsJob</span></span>
<span data-ttu-id="3646e-117">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="3646e-117">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3646e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3646e-118">-DefaultProfile</span></span>
<span data-ttu-id="3646e-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3646e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3646e-120">-Generalisiert</span><span class="sxs-lookup"><span data-stu-id="3646e-120">-Generalized</span></span>
<span data-ttu-id="3646e-121">Gibt an, dass dieses Cmdlet einen virtuellen Computer als generalisiert kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="3646e-121">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, GeneralizeIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3646e-122">-ID</span><span class="sxs-lookup"><span data-stu-id="3646e-122">-Id</span></span>
<span data-ttu-id="3646e-123">Gibt die Ressourcen-ID des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="3646e-123">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3646e-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3646e-124">-Name</span></span>
<span data-ttu-id="3646e-125">Gibt den Namen des virtuellen Computers an, auf dem dieses Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3646e-125">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3646e-126">– Erneute Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="3646e-126">-Redeploy</span></span>
<span data-ttu-id="3646e-127">Gibt an, dass dieses Cmdlet den virtuellen Computer manuell auf einem anderen Azure-Host erneut bereitstellt, um Probleme zu beheben.</span><span class="sxs-lookup"><span data-stu-id="3646e-127">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>

<span data-ttu-id="3646e-128">Wenn Sie einen virtuellen Computer erneut bereitstellen, wird er neu gestartet, was zum Verlust ephemerer Laufwerk Daten führt.</span><span class="sxs-lookup"><span data-stu-id="3646e-128">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3646e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3646e-129">-ResourceGroupName</span></span>
<span data-ttu-id="3646e-130">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="3646e-130">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3646e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3646e-131">CommonParameters</span></span>
<span data-ttu-id="3646e-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3646e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3646e-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3646e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3646e-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3646e-134">INPUTS</span></span>

### <span data-ttu-id="3646e-135">Keine</span><span class="sxs-lookup"><span data-stu-id="3646e-135">None</span></span>
<span data-ttu-id="3646e-136">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="3646e-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3646e-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3646e-137">OUTPUTS</span></span>

### <span data-ttu-id="3646e-138">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="3646e-138">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="3646e-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="3646e-139">NOTES</span></span>

## <span data-ttu-id="3646e-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3646e-140">RELATED LINKS</span></span>

[<span data-ttu-id="3646e-141">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3646e-141">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


