---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainconsortium
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
ms.openlocfilehash: d34e8257d6946476ff5b6a2356ba9b1b06d8a9f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179767"
---
# <span data-ttu-id="35521-101">Get-AzBlockchainConsortium</span><span class="sxs-lookup"><span data-stu-id="35521-101">Get-AzBlockchainConsortium</span></span>

## <span data-ttu-id="35521-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="35521-102">SYNOPSIS</span></span>
<span data-ttu-id="35521-103">Listet die verfügbaren Konsortien für ein Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="35521-103">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="35521-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="35521-104">SYNTAX</span></span>

```
Get-AzBlockchainConsortium -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="35521-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="35521-105">DESCRIPTION</span></span>
<span data-ttu-id="35521-106">Listet die verfügbaren Konsortien für ein Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="35521-106">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="35521-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="35521-107">EXAMPLES</span></span>

### <span data-ttu-id="35521-108">Beispiel 1: Abrufen von Blockchain-Konsortien.</span><span class="sxs-lookup"><span data-stu-id="35521-108">Example 1: Get Blockchain consortiums.</span></span>
```powershell
PS C:\> Get-AzBlockchainConsortium -Location eastus

```

<span data-ttu-id="35521-109">Dieser Befehl listet die Konsortien unter einem Abonnement für einen bestimmten Standort auf.</span><span class="sxs-lookup"><span data-stu-id="35521-109">This command lists the consortiums under a subscription for a specific location.</span></span>

## <span data-ttu-id="35521-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="35521-110">PARAMETERS</span></span>

### <span data-ttu-id="35521-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35521-111">-DefaultProfile</span></span>
<span data-ttu-id="35521-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="35521-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35521-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="35521-113">-Location</span></span>
<span data-ttu-id="35521-114">Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="35521-114">Location Name.</span></span>

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

### <span data-ttu-id="35521-115">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="35521-115">-SubscriptionId</span></span>
<span data-ttu-id="35521-116">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="35521-116">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="35521-117">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="35521-117">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35521-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="35521-118">-Confirm</span></span>
<span data-ttu-id="35521-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="35521-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35521-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35521-120">-WhatIf</span></span>
<span data-ttu-id="35521-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="35521-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35521-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="35521-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35521-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35521-123">CommonParameters</span></span>
<span data-ttu-id="35521-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35521-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35521-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35521-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35521-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="35521-126">INPUTS</span></span>

## <span data-ttu-id="35521-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="35521-127">OUTPUTS</span></span>

### <span data-ttu-id="35521-128">Microsoft. Azure. PowerShell. Cmdlets. Blockchain. Models. Api20180601Preview. IConsortium</span><span class="sxs-lookup"><span data-stu-id="35521-128">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortium</span></span>

## <span data-ttu-id="35521-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="35521-129">NOTES</span></span>

<span data-ttu-id="35521-130">Aliase</span><span class="sxs-lookup"><span data-stu-id="35521-130">ALIASES</span></span>

## <span data-ttu-id="35521-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="35521-131">RELATED LINKS</span></span>

