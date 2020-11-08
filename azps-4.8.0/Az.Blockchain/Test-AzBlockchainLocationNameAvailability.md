---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/test-azblockchainlocationnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
ms.openlocfilehash: 42bd50dd96d235db823ec12498388f78d5ec641c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173903"
---
# <span data-ttu-id="f85aa-101">Test-AzBlockchainLocationNameAvailability</span><span class="sxs-lookup"><span data-stu-id="f85aa-101">Test-AzBlockchainLocationNameAvailability</span></span>

## <span data-ttu-id="f85aa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f85aa-102">SYNOPSIS</span></span>
<span data-ttu-id="f85aa-103">So überprüfen Sie, ob ein Ressourcenname verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f85aa-103">To check whether a resource name is available.</span></span>

## <span data-ttu-id="f85aa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f85aa-104">SYNTAX</span></span>

```
Test-AzBlockchainLocationNameAvailability -Location <String> [-SubscriptionId <String>] [-Name <String>]
 [-Type <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f85aa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f85aa-105">DESCRIPTION</span></span>
<span data-ttu-id="f85aa-106">So überprüfen Sie, ob ein Ressourcenname verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f85aa-106">To check whether a resource name is available.</span></span>

## <span data-ttu-id="f85aa-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f85aa-107">EXAMPLES</span></span>

### <span data-ttu-id="f85aa-108">Beispiel 1: überprüfen, ob ein Ressourcenname verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="f85aa-108">Example 1: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name erw123 -type Microsoft.Blockchain/blockchainMembers

Message NameAvailable Reason
------- ------------- ------
        True          NotSpecified
```

<span data-ttu-id="f85aa-109">Der Befehl überprüft, ob ein Ressourcenname verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f85aa-109">The command checks whether a resource name is available.</span></span>

### <span data-ttu-id="f85aa-110">Beispiel 2: überprüfen, ob ein Ressourcenname verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="f85aa-110">Example 2: Check whether a resource name is available</span></span>
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name 123 -Type Microsoft.Blockchain/blockchainMembers

Message                                                                                                                                                                             NameAvailable Reason
-------                                                                                                                                                                             ------------- ------
The blockchain member name is invalid. It can contain only lowercase letters and numbers. The first character must be a letter. The value must be between 2 and 20 characters long. False         Invalid
```

<span data-ttu-id="f85aa-111">Der Befehl überprüft, ob ein Ressourcenname verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f85aa-111">The command checks whether a resource name is available.</span></span>

## <span data-ttu-id="f85aa-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f85aa-112">PARAMETERS</span></span>

### <span data-ttu-id="f85aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f85aa-113">-DefaultProfile</span></span>
<span data-ttu-id="f85aa-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f85aa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f85aa-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="f85aa-115">-Location</span></span>
<span data-ttu-id="f85aa-116">Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="f85aa-116">Location Name.</span></span>

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

### <span data-ttu-id="f85aa-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f85aa-117">-Name</span></span>
<span data-ttu-id="f85aa-118">Ruft den zu überprüfenden Namen ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="f85aa-118">Gets or sets the name to check.</span></span>

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

### <span data-ttu-id="f85aa-119">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="f85aa-119">-SubscriptionId</span></span>
<span data-ttu-id="f85aa-120">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f85aa-120">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="f85aa-121">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="f85aa-121">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f85aa-122">-Typ</span><span class="sxs-lookup"><span data-stu-id="f85aa-122">-Type</span></span>
<span data-ttu-id="f85aa-123">Ruft den Typ der zu überprüfenden Ressource ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="f85aa-123">Gets or sets the type of the resource to check.</span></span>

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

### <span data-ttu-id="f85aa-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f85aa-124">-Confirm</span></span>
<span data-ttu-id="f85aa-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f85aa-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f85aa-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f85aa-126">-WhatIf</span></span>
<span data-ttu-id="f85aa-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f85aa-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f85aa-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f85aa-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f85aa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f85aa-129">CommonParameters</span></span>
<span data-ttu-id="f85aa-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f85aa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f85aa-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f85aa-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f85aa-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f85aa-132">INPUTS</span></span>

## <span data-ttu-id="f85aa-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f85aa-133">OUTPUTS</span></span>

### <span data-ttu-id="f85aa-134">Microsoft. Azure. PowerShell. Cmdlets. Blockchain. Models. Api20180601Preview. INameAvailability</span><span class="sxs-lookup"><span data-stu-id="f85aa-134">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.INameAvailability</span></span>

## <span data-ttu-id="f85aa-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="f85aa-135">NOTES</span></span>

<span data-ttu-id="f85aa-136">Aliase</span><span class="sxs-lookup"><span data-stu-id="f85aa-136">ALIASES</span></span>

## <span data-ttu-id="f85aa-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f85aa-137">RELATED LINKS</span></span>

