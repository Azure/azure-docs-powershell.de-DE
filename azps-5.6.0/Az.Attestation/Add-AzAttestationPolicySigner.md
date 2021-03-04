---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/add-azattestationpolicysigner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Add-AzAttestationPolicySigner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Add-AzAttestationPolicySigner.md
ms.openlocfilehash: d4f04c47c37446b6521c122b7551263809bb1c49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928731"
---
# <span data-ttu-id="f3656-101">Add-AzAttestationPolicySigner</span><span class="sxs-lookup"><span data-stu-id="f3656-101">Add-AzAttestationPolicySigner</span></span>

## <span data-ttu-id="f3656-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3656-102">SYNOPSIS</span></span>
<span data-ttu-id="f3656-103">Fügt einen vertrauenswürdigen Richtlinien signer für einen Mandanten in Azure Attestation hinzu.</span><span class="sxs-lookup"><span data-stu-id="f3656-103">Adds a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="f3656-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f3656-104">SYNTAX</span></span>

### <span data-ttu-id="f3656-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3656-105">NameParameterSet</span></span>
```
Add-AzAttestationPolicySigner [-Name] <String> [-ResourceGroupName] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3656-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3656-106">ResourceIdParameterSet</span></span>
```
Add-AzAttestationPolicySigner [-ResourceId] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3656-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f3656-107">DESCRIPTION</span></span>
<span data-ttu-id="f3656-108">Das Add-AzAttestationPolicySigner-Cmdlet fügt einen vertrauenswürdigen Richtlinien signer für einen Mandanten in Azure Attestation hinzu.</span><span class="sxs-lookup"><span data-stu-id="f3656-108">The Add-AzAttestationPolicySigner cmdlet adds a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="f3656-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f3656-109">EXAMPLES</span></span>

### <span data-ttu-id="f3656-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f3656-110">Example 1</span></span>
```powershell
PS C:\> $trustedSigner = Get-Content -Path .\trusted.signer.txt
PS C:\> Add-AzAttestationPolicySigner -Name pshtest -ResourceGroupName psh-test-rg -Signer $trustedSigner
```

<span data-ttu-id="f3656-111">Fügen Sie einen vertrauenswürdigen Signer für den Atteestation-Anbieter namens *pshtest hinzu.*</span><span class="sxs-lookup"><span data-stu-id="f3656-111">Add a trusted signer for the Atteestation Provider named *pshtest*.</span></span>

## <span data-ttu-id="f3656-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f3656-112">PARAMETERS</span></span>

### <span data-ttu-id="f3656-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3656-113">-DefaultProfile</span></span>
<span data-ttu-id="f3656-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3656-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3656-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f3656-115">-Name</span></span>
<span data-ttu-id="f3656-116">Gibt den Namen eines Bescheinigungsanbieters an.</span><span class="sxs-lookup"><span data-stu-id="f3656-116">Specifies the name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3656-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3656-117">-ResourceGroupName</span></span>
<span data-ttu-id="f3656-118">Gibt den Ressourcengruppennamen eines Bescheinigungsanbieters an.</span><span class="sxs-lookup"><span data-stu-id="f3656-118">Specifies the resource group name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3656-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3656-119">-ResourceId</span></span>
<span data-ttu-id="f3656-120">Gibt die ResourceID eines Bescheinigungsanbieters an.</span><span class="sxs-lookup"><span data-stu-id="f3656-120">Specifies the ResourceID of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3656-121">-Signer</span><span class="sxs-lookup"><span data-stu-id="f3656-121">-Signer</span></span>
<span data-ttu-id="f3656-122">Gibt das RFC7519-JSON-Webtoken an, das einen Anspruch mit dem Namen "maa-policyCertificate" enthält, dessen Wert ein RFC7517-JSON-Webschlüssel ist, der einen neuen vertrauenswürdigen Signaturschlüssel enthält, der hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f3656-122">Specifies the RFC7519 JSON Web Token containing a claim named "maa-policyCertificate" whose value is an RFC7517 JSON Web Key which contains a new trusted signing key to add.</span></span>
<span data-ttu-id="f3656-123">Das RFC7519-JWT muss mit einem der vorhandenen vertrauenswürdigen Signaturschlüssel signiert sein.</span><span class="sxs-lookup"><span data-stu-id="f3656-123">The RFC7519 JWT must be signed with one of the existing trusted signing keys.</span></span>

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

### <span data-ttu-id="f3656-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f3656-124">-Confirm</span></span>
<span data-ttu-id="f3656-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f3656-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3656-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3656-126">-WhatIf</span></span>
<span data-ttu-id="f3656-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f3656-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3656-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f3656-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3656-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3656-129">CommonParameters</span></span>
<span data-ttu-id="f3656-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3656-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3656-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3656-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3656-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f3656-132">INPUTS</span></span>

### <span data-ttu-id="f3656-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f3656-133">System.String</span></span>

## <span data-ttu-id="f3656-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f3656-134">OUTPUTS</span></span>

### <span data-ttu-id="f3656-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span><span class="sxs-lookup"><span data-stu-id="f3656-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="f3656-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f3656-136">NOTES</span></span>

## <span data-ttu-id="f3656-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f3656-137">RELATED LINKS</span></span>
