---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/test-azblockchainlocationnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
ms.openlocfilehash: 42bd50dd96d235db823ec12498388f78d5ec641c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473238"
---
# <span data-ttu-id="ac095-101">Test-AzBlockchainLocationNameAvailability</span><span class="sxs-lookup"><span data-stu-id="ac095-101">Test-AzBlockchainLocationNameAvailability</span></span>

## <span data-ttu-id="ac095-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac095-102">SYNOPSIS</span></span>
<span data-ttu-id="ac095-103">So überprüfen Sie, ob ein Ressourcenname verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ac095-103">To check whether a resource name is available.</span></span>

## <span data-ttu-id="ac095-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ac095-104">SYNTAX</span></span>

```
Test-AzBlockchainLocationNameAvailability -Location <String> [-SubscriptionId <String>] [-Name <String>]
 [-Type <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ac095-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ac095-105">DESCRIPTION</span></span>
<span data-ttu-id="ac095-106">So überprüfen Sie, ob ein Ressourcenname verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ac095-106">To check whether a resource name is available.</span></span>

## <span data-ttu-id="ac095-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ac095-107">EXAMPLES</span></span>

### <span data-ttu-id="ac095-108">Beispiel 1: Überprüfen, ob ein Ressourcenname verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="ac095-108">Example 1: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name erw123 -type Microsoft.Blockchain/blockchainMembers

Message NameAvailable Reason
------- ------------- ------
        True          NotSpecified
```

<span data-ttu-id="ac095-109">Der Befehl überprüft, ob ein Ressourcenname verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ac095-109">The command checks whether a resource name is available.</span></span>

### <span data-ttu-id="ac095-110">Beispiel 2: Überprüfen, ob ein Ressourcenname verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="ac095-110">Example 2: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name 123 -Type Microsoft.Blockchain/blockchainMembers

Message                                                                                                                                                                             NameAvailable Reason
-------                                                                                                                                                                             ------------- ------
The blockchain member name is invalid. It can contain only lowercase letters and numbers. The first character must be a letter. The value must be between 2 and 20 characters long. False         Invalid
```

<span data-ttu-id="ac095-111">Der Befehl überprüft, ob ein Ressourcenname verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ac095-111">The command checks whether a resource name is available.</span></span>

## <span data-ttu-id="ac095-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac095-112">PARAMETERS</span></span>

### <span data-ttu-id="ac095-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac095-113">-DefaultProfile</span></span>
<span data-ttu-id="ac095-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ac095-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac095-115">-Location</span><span class="sxs-lookup"><span data-stu-id="ac095-115">-Location</span></span>
<span data-ttu-id="ac095-116">Standortname.</span><span class="sxs-lookup"><span data-stu-id="ac095-116">Location Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac095-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ac095-117">-Name</span></span>
<span data-ttu-id="ac095-118">Ruft den zu überprüfende Namen ab oder legt den Namen fest.</span><span class="sxs-lookup"><span data-stu-id="ac095-118">Gets or sets the name to check.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac095-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ac095-119">-SubscriptionId</span></span>
<span data-ttu-id="ac095-120">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ac095-120">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ac095-121">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="ac095-121">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac095-122">-Type</span><span class="sxs-lookup"><span data-stu-id="ac095-122">-Type</span></span>
<span data-ttu-id="ac095-123">Ruft den typ der zu überprüfende Ressource ab oder legt diesen typ fest.</span><span class="sxs-lookup"><span data-stu-id="ac095-123">Gets or sets the type of the resource to check.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac095-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac095-124">-Confirm</span></span>
<span data-ttu-id="ac095-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ac095-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac095-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ac095-126">-WhatIf</span></span>
<span data-ttu-id="ac095-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ac095-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac095-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac095-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac095-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac095-129">CommonParameters</span></span>
<span data-ttu-id="ac095-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac095-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac095-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ac095-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac095-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ac095-132">INPUTS</span></span>

## <span data-ttu-id="ac095-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ac095-133">OUTPUTS</span></span>

### <span data-ttu-id="ac095-134">Microsoft.Azure.PowerShell.Cmdlets.Models.Api20180601Preview.INameAvailability</span><span class="sxs-lookup"><span data-stu-id="ac095-134">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.INameAvailability</span></span>

## <span data-ttu-id="ac095-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ac095-135">NOTES</span></span>

<span data-ttu-id="ac095-136">ALIASE</span><span class="sxs-lookup"><span data-stu-id="ac095-136">ALIASES</span></span>

## <span data-ttu-id="ac095-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ac095-137">RELATED LINKS</span></span>

