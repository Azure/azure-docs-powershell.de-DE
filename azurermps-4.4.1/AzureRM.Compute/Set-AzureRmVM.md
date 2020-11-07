---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVM.md
ms.openlocfilehash: 6fa67a039599ab066b82ad923f5a2f896b0db519
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664284"
---
# <span data-ttu-id="bf7cd-101">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="bf7cd-101">Set-AzureRmVM</span></span>

## <span data-ttu-id="bf7cd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bf7cd-102">SYNOPSIS</span></span>
<span data-ttu-id="bf7cd-103">Kennzeichnet einen virtuellen Computer als generalisiert.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-103">Marks a virtual machine as generalized.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf7cd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf7cd-104">SYNTAX</span></span>

### <span data-ttu-id="bf7cd-105">GeneralizeResourceGroupNameParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="bf7cd-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf7cd-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="bf7cd-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf7cd-107">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="bf7cd-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Generalized] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bf7cd-108">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="bf7cd-108">RedeployIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Redeploy] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bf7cd-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf7cd-109">DESCRIPTION</span></span>
<span data-ttu-id="bf7cd-110">Das Cmdlet " **Satz-AzureRmVM** " kennzeichnet einen virtuellen Computer als generalisiert.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-110">The **Set-AzureRmVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="bf7cd-111">Bevor Sie dieses Cmdlet ausführen, melden Sie sich beim virtuellen Computer an, und verwenden Sie Sysprep zum Vorbereiten der Festplatte.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="bf7cd-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bf7cd-112">EXAMPLES</span></span>

### <span data-ttu-id="bf7cd-113">Beispiel 1: Kennzeichnen eines virtuellen Computers als generalisiert</span><span class="sxs-lookup"><span data-stu-id="bf7cd-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="bf7cd-114">Dieser Befehl kennzeichnet den virtuellen Computer mit dem Namen "VirtualMachine07" als "generalisiert".</span><span class="sxs-lookup"><span data-stu-id="bf7cd-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="bf7cd-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf7cd-115">PARAMETERS</span></span>

### <span data-ttu-id="bf7cd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf7cd-116">-DefaultProfile</span></span>
<span data-ttu-id="bf7cd-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf7cd-118">-Generalisiert</span><span class="sxs-lookup"><span data-stu-id="bf7cd-118">-Generalized</span></span>
<span data-ttu-id="bf7cd-119">Gibt an, dass dieses Cmdlet einen virtuellen Computer als generalisiert kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-119">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, GeneralizeIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf7cd-120">-ID</span><span class="sxs-lookup"><span data-stu-id="bf7cd-120">-Id</span></span>
<span data-ttu-id="bf7cd-121">Gibt die Ressourcen-ID des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-121">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="bf7cd-122">-Name</span><span class="sxs-lookup"><span data-stu-id="bf7cd-122">-Name</span></span>
<span data-ttu-id="bf7cd-123">Gibt den Namen des virtuellen Computers an, auf dem dieses Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-123">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="bf7cd-124">– Erneute Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="bf7cd-124">-Redeploy</span></span>
<span data-ttu-id="bf7cd-125">Gibt an, dass dieses Cmdlet den virtuellen Computer manuell auf einem anderen Azure-Host erneut bereitstellt, um Probleme zu beheben.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-125">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>

<span data-ttu-id="bf7cd-126">Wenn Sie einen virtuellen Computer erneut bereitstellen, wird er neu gestartet, was zum Verlust ephemerer Laufwerk Daten führt.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-126">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf7cd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf7cd-127">-ResourceGroupName</span></span>
<span data-ttu-id="bf7cd-128">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-128">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="bf7cd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf7cd-129">CommonParameters</span></span>
<span data-ttu-id="bf7cd-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf7cd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf7cd-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf7cd-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf7cd-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bf7cd-132">INPUTS</span></span>

## <span data-ttu-id="bf7cd-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bf7cd-133">OUTPUTS</span></span>

## <span data-ttu-id="bf7cd-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="bf7cd-134">NOTES</span></span>

## <span data-ttu-id="bf7cd-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bf7cd-135">RELATED LINKS</span></span>

[<span data-ttu-id="bf7cd-136">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="bf7cd-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


