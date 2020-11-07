---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/new-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
ms.openlocfilehash: ce21b116ceb41bfdfb26008dd44c914f3198ab39
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658089"
---
# <span data-ttu-id="4643f-101">New-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="4643f-101">New-AzAttestation</span></span>

## <span data-ttu-id="4643f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4643f-102">SYNOPSIS</span></span>
<span data-ttu-id="4643f-103">Erstellt eine Bescheinigung</span><span class="sxs-lookup"><span data-stu-id="4643f-103">Creates an attestation</span></span>

## <span data-ttu-id="4643f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4643f-104">SYNTAX</span></span>

```
New-AzAttestation -Name <String> -ResourceGroupName <String> [-AttestationPolicy <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4643f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4643f-105">DESCRIPTION</span></span>
<span data-ttu-id="4643f-106">Das New-AzAttestation-Cmdlet erstellt eine Bescheinigung in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4643f-106">The New-AzAttestation cmdlet creates an attestation in the specified resource group.</span></span>

## <span data-ttu-id="4643f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4643f-107">EXAMPLES</span></span>

### <span data-ttu-id="4643f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4643f-108">Example 1</span></span>
```powershell
PS C:\> New-AzAttestation -Name example -ResourceGroupName rg1 
Id                  : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/rg1/providers/Microsoft.Attestation/attestationProviders/example
Name                : example
Type                : Microsoft.Attestation/attestationProviders
Status              : Ready
AttesUri            : https://example.us.attest.azure.net
ResoureGroupName    : rg1 
SubscriptionId      : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
```

<span data-ttu-id="4643f-109">Erstellen einer neuen Bescheinigung "Beispiel" im aktuellen Abonnement, Ressourcengruppe "RG1"</span><span class="sxs-lookup"><span data-stu-id="4643f-109">Create a new Attestation "example" in current Subscription, Resource Group "rg1"</span></span>

## <span data-ttu-id="4643f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4643f-110">PARAMETERS</span></span>

### <span data-ttu-id="4643f-111">-AttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="4643f-111">-AttestationPolicy</span></span>
<span data-ttu-id="4643f-112">Gibt die Richtlinie an, die zum Erstellen der Bescheinigung übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="4643f-112">Specifies the attestation policy passed in which to create the attestation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4643f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4643f-113">-DefaultProfile</span></span>
<span data-ttu-id="4643f-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4643f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4643f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4643f-115">-Name</span></span>
<span data-ttu-id="4643f-116">Gibt den Namen der Instanz an, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4643f-116">Specifies a name of the Instance to create.</span></span>
<span data-ttu-id="4643f-117">Der Name kann eine beliebige Kombination aus Buchstaben, Ziffern oder Bindestrichen sein.</span><span class="sxs-lookup"><span data-stu-id="4643f-117">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="4643f-118">Der Name muss mit einem Buchstaben oder einer Ziffer beginnen und enden.</span><span class="sxs-lookup"><span data-stu-id="4643f-118">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="4643f-119">Der Name muss universell eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="4643f-119">The name must be universally unique.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4643f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4643f-120">-ResourceGroupName</span></span>
<span data-ttu-id="4643f-121">Gibt den Namen einer vorhandenen Ressourcengruppe an, in der die Bescheinigung erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4643f-121">Specifies the name of an existing resource group in which to create the attestation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4643f-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4643f-122">-Confirm</span></span>
<span data-ttu-id="4643f-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4643f-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4643f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4643f-124">-WhatIf</span></span>
<span data-ttu-id="4643f-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4643f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4643f-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4643f-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4643f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4643f-127">CommonParameters</span></span>
<span data-ttu-id="4643f-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4643f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4643f-129">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4643f-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4643f-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4643f-130">INPUTS</span></span>

### <span data-ttu-id="4643f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4643f-131">System.String</span></span>

## <span data-ttu-id="4643f-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4643f-132">OUTPUTS</span></span>

### <span data-ttu-id="4643f-133">Microsoft. Azure. Commands. Testat. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="4643f-133">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="4643f-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="4643f-134">NOTES</span></span>

## <span data-ttu-id="4643f-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4643f-135">RELATED LINKS</span></span>
