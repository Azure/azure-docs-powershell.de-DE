---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/new-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
ms.openlocfilehash: 1fbb3c5d1a82261f5c25bd4351aabcb838355bda
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942728"
---
# <span data-ttu-id="b4849-101">New-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="b4849-101">New-AzAttestation</span></span>

## <span data-ttu-id="b4849-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4849-102">SYNOPSIS</span></span>
<span data-ttu-id="b4849-103">Erstellt eine Bestätigung</span><span class="sxs-lookup"><span data-stu-id="b4849-103">Creates an attestation</span></span>

## <span data-ttu-id="b4849-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4849-104">SYNTAX</span></span>

```
New-AzAttestation -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-PolicySignersCertificateFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b4849-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b4849-105">DESCRIPTION</span></span>
<span data-ttu-id="b4849-106">Das New-AzAttestation-Cmdlet erstellt eine Bestätigung in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b4849-106">The New-AzAttestation cmdlet creates an attestation in the specified resource group.</span></span>

## <span data-ttu-id="b4849-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b4849-107">EXAMPLES</span></span>

### <span data-ttu-id="b4849-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b4849-108">Example 1</span></span>
```powershell
PS C:\> New-AzAttestation -Name pshtest4 -ResourceGroupName psh-test-rg -Location "East US" -Tags @{Test="true";CreationYear="2020"}                                                                                                                                                                                         
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest4
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest4
Status            : Ready
TrustModel        : AAD
AttestUri         : https://pshtest4.us.attest.azure.net
Tags              : {CreationYear, Test}
TagsTable         :
                    Name          Value
                    ============  =====
                    CreationYear  2020
                    Test          true
```

<span data-ttu-id="b4849-109">Erstellen Sie eine neue Instanz eines Nachweisanbieters namens *pshtest4* mit mehreren Tags und verwenden Sie die AAD-Vertrauensstellung zum Mastern der TEE-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="b4849-109">Create a new instance of an Attestation Provider named *pshtest4* with a couple tags and using AAD trust for mastering TEE policy.</span></span>

### <span data-ttu-id="b4849-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b4849-110">Example 2</span></span>
```powershell
PS C:\> New-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg -Location "East US" -PolicySignersCertificateFile .\cert1.pem                                                                                                                                                
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest3
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest3
Status            : Ready
TrustModel        : Isolated
AttestUri         : https://pshtest3.us.attest.azure.net
Tags              :
TagsTable         :
```

<span data-ttu-id="b4849-111">Erstellen Sie eine neue Instanz eines Bestätigungsanbieters namens *pshtest3*', der isoladed trust zum Mastering von TEE-Richtlinien verwendet, indem Sie eine Gruppe vertrauenswürdiger Signaturschlüssel über eine PEM-Datei angeben.</span><span class="sxs-lookup"><span data-stu-id="b4849-111">Create a new instance of an Attestation Provider named *pshtest3*\` that uses Isoladed trust for mastering TEE policy via specifying a set of trusted signing keys via a PEM file.</span></span>

## <span data-ttu-id="b4849-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b4849-112">PARAMETERS</span></span>

### <span data-ttu-id="b4849-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4849-113">-DefaultProfile</span></span>
<span data-ttu-id="b4849-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b4849-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4849-115">-Location</span><span class="sxs-lookup"><span data-stu-id="b4849-115">-Location</span></span>
<span data-ttu-id="b4849-116">Gibt die Azure-Region an, in der der Bescheinigungsanbieter erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b4849-116">Specifies the Azure region in which to create the attestation provider.</span></span> <span data-ttu-id="b4849-117">Verwenden Sie den Befehl Get-AzResourceProvider mit dem Parameter ProviderNamespace, um Ihre Auswahlmöglichkeiten zu sehen.</span><span class="sxs-lookup"><span data-stu-id="b4849-117">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4849-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b4849-118">-Name</span></span>
<span data-ttu-id="b4849-119">Gibt einen Namen der zu erstellenden Instanz an.</span><span class="sxs-lookup"><span data-stu-id="b4849-119">Specifies a name of the Instance to create.</span></span>
<span data-ttu-id="b4849-120">Der Name kann eine beliebige Kombination aus Buchstaben, Ziffern oder Bindestrichen sein.</span><span class="sxs-lookup"><span data-stu-id="b4849-120">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="b4849-121">Der Name muss mit einem Buchstaben oder einer Ziffer beginnen und enden.</span><span class="sxs-lookup"><span data-stu-id="b4849-121">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="b4849-122">Der Name muss universell eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="b4849-122">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4849-123">-PolicySignersCertificateFile</span><span class="sxs-lookup"><span data-stu-id="b4849-123">-PolicySignersCertificateFile</span></span>
<span data-ttu-id="b4849-124">Gibt den Satz der vertrauenswürdigen Signaturschlüssel für die Ausgaberichtlinie in einer einzelnen Zertifikatdatei an.</span><span class="sxs-lookup"><span data-stu-id="b4849-124">Specifies the set of trusted signing keys for issuance policy in a single certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4849-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4849-125">-ResourceGroupName</span></span>
<span data-ttu-id="b4849-126">Gibt den Namen einer vorhandenen Ressourcengruppe an, in der das Attest erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b4849-126">Specifies the name of an existing resource group in which to create the attestation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4849-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="b4849-127">-Tag</span></span>
<span data-ttu-id="b4849-128">Eine Hashtabelle, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="b4849-128">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4849-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b4849-129">-Confirm</span></span>
<span data-ttu-id="b4849-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b4849-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4849-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4849-131">-WhatIf</span></span>
<span data-ttu-id="b4849-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b4849-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4849-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b4849-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4849-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4849-134">CommonParameters</span></span>
<span data-ttu-id="b4849-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4849-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4849-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4849-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4849-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b4849-137">INPUTS</span></span>

### <span data-ttu-id="b4849-138">System.String</span><span class="sxs-lookup"><span data-stu-id="b4849-138">System.String</span></span>

### <span data-ttu-id="b4849-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b4849-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b4849-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b4849-140">OUTPUTS</span></span>

### <span data-ttu-id="b4849-141">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span><span class="sxs-lookup"><span data-stu-id="b4849-141">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="b4849-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b4849-142">NOTES</span></span>

## <span data-ttu-id="b4849-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b4849-143">RELATED LINKS</span></span>
