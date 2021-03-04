---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/remove-azattestationpolicysigner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestationPolicySigner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestationPolicySigner.md
ms.openlocfilehash: e0b86a1cd7c3e1355cfc760fecc257b3cde87561
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926019"
---
# <span data-ttu-id="a57e5-101">Remove-AzAttestationPolicySigner</span><span class="sxs-lookup"><span data-stu-id="a57e5-101">Remove-AzAttestationPolicySigner</span></span>

## <span data-ttu-id="a57e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a57e5-102">SYNOPSIS</span></span>
<span data-ttu-id="a57e5-103">Entfernt einen vertrauenswürdigen Richtlinien signer für einen Mandanten in Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="a57e5-103">Removes a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="a57e5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a57e5-104">SYNTAX</span></span>

### <span data-ttu-id="a57e5-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a57e5-105">NameParameterSet</span></span>
```
Remove-AzAttestationPolicySigner [-Name] <String> [-ResourceGroupName] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a57e5-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a57e5-106">ResourceIdParameterSet</span></span>
```
Remove-AzAttestationPolicySigner [-ResourceId] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a57e5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a57e5-107">DESCRIPTION</span></span>
<span data-ttu-id="a57e5-108">Das Remove-AzAttestationPolicySigner cmdlet entfernt einen vertrauenswürdigen Richtlinien signer für einen Mandanten in Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="a57e5-108">The Remove-AzAttestationPolicySigner cmdlet removes a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="a57e5-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a57e5-109">EXAMPLES</span></span>

### <span data-ttu-id="a57e5-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a57e5-110">Example 1</span></span>
```powershell
PS C:\> $trustedSigner = Get-Content -Path .\trusted.signer.txt
PS C:\> Remove-AzAttestationPolicySigner -Name pshtest -ResourceGroupName psh-test-rg -Signer $trustedSigner
```

<span data-ttu-id="a57e5-111">Entfernen Sie einen vertrauenswürdigen Signer für den Zertifizierungsanbieter mit dem Namen *pshtest*.</span><span class="sxs-lookup"><span data-stu-id="a57e5-111">Remove a trusted signer for the Attestation Provider named *pshtest*.</span></span>

## <span data-ttu-id="a57e5-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a57e5-112">PARAMETERS</span></span>

### <span data-ttu-id="a57e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a57e5-113">-DefaultProfile</span></span>
<span data-ttu-id="a57e5-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a57e5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a57e5-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a57e5-115">-Name</span></span>
<span data-ttu-id="a57e5-116">Gibt den Namen eines Bescheinigungsanbieters an.</span><span class="sxs-lookup"><span data-stu-id="a57e5-116">Specifies the name of an attestation provider.</span></span>

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

### <span data-ttu-id="a57e5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a57e5-117">-ResourceGroupName</span></span>
<span data-ttu-id="a57e5-118">Gibt den Ressourcengruppennamen eines Bescheinigungsanbieters an.</span><span class="sxs-lookup"><span data-stu-id="a57e5-118">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="a57e5-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a57e5-119">-ResourceId</span></span>
<span data-ttu-id="a57e5-120">Gibt die ResourceID eines Bescheinigungsanbieters an.</span><span class="sxs-lookup"><span data-stu-id="a57e5-120">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="a57e5-121">-Signer</span><span class="sxs-lookup"><span data-stu-id="a57e5-121">-Signer</span></span>
<span data-ttu-id="a57e5-122">Gibt das RFC7519-JSON-Webtoken an, das einen Anspruch mit dem Namen "maa-policyCertificate" enthält, dessen Wert ein RFC7517-JSON-Webschlüssel ist, der einen zu entfernenden vertrauenswürdigen Signaturschlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="a57e5-122">Specifies the RFC7519 JSON Web Token containing a claim named "maa-policyCertificate" whose value is an RFC7517 JSON Web Key which contains a trusted signing key to remove.</span></span>
<span data-ttu-id="a57e5-123">Das RFC7519-JWT muss mit einem der vorhandenen vertrauenswürdigen Signaturschlüssel signiert sein.</span><span class="sxs-lookup"><span data-stu-id="a57e5-123">The RFC7519 JWT must be signed with one of the existing trusted signing keys.</span></span>

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

### <span data-ttu-id="a57e5-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a57e5-124">-Confirm</span></span>
<span data-ttu-id="a57e5-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a57e5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a57e5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a57e5-126">-WhatIf</span></span>
<span data-ttu-id="a57e5-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a57e5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a57e5-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a57e5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a57e5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a57e5-129">CommonParameters</span></span>
<span data-ttu-id="a57e5-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a57e5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a57e5-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a57e5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a57e5-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a57e5-132">INPUTS</span></span>

### <span data-ttu-id="a57e5-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a57e5-133">System.String</span></span>

## <span data-ttu-id="a57e5-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a57e5-134">OUTPUTS</span></span>

### <span data-ttu-id="a57e5-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span><span class="sxs-lookup"><span data-stu-id="a57e5-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="a57e5-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a57e5-136">NOTES</span></span>

## <span data-ttu-id="a57e5-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a57e5-137">RELATED LINKS</span></span>
