---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestationpolicysigner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestationPolicySigner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestationPolicySigner.md
ms.openlocfilehash: fdd62a78b9d75ef222dc9f41f2c791afadfad9b4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306659"
---
# <span data-ttu-id="a0cc8-101">Remove-AzAttestationPolicySigner</span><span class="sxs-lookup"><span data-stu-id="a0cc8-101">Remove-AzAttestationPolicySigner</span></span>

## <span data-ttu-id="a0cc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0cc8-102">SYNOPSIS</span></span>
<span data-ttu-id="a0cc8-103">Entfernt einen vertrauenswürdigen Richtlinien signierten Benutzer für einen Mandanten in Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="a0cc8-103">Removes a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="a0cc8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0cc8-104">SYNTAX</span></span>

### <span data-ttu-id="a0cc8-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0cc8-105">NameParameterSet</span></span>
```
Remove-AzAttestationPolicySigner [-Name] <String> [-ResourceGroupName] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0cc8-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0cc8-106">ResourceIdParameterSet</span></span>
```
Remove-AzAttestationPolicySigner [-ResourceId] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0cc8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0cc8-107">DESCRIPTION</span></span>
<span data-ttu-id="a0cc8-108">Das Remove-AzAttestationPolicySigner cmdlet entfernt einen vertrauenswürdigen Richtlinien signer für einen Mandanten in Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="a0cc8-108">The Remove-AzAttestationPolicySigner cmdlet removes a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="a0cc8-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a0cc8-109">EXAMPLES</span></span>

### <span data-ttu-id="a0cc8-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a0cc8-110">Example 1</span></span>
```powershell
PS C:\> $trustedSigner = Get-Content -Path .\trusted.signer.txt
PS C:\> Remove-AzAttestationPolicySigner -Name pshtest -ResourceGroupName psh-test-rg -Signer $trustedSigner
```

<span data-ttu-id="a0cc8-111">Entfernen Sie einen vertrauenswürdigen Signer für den Nachweisanbieter namens *"pshtest".*</span><span class="sxs-lookup"><span data-stu-id="a0cc8-111">Remove a trusted signer for the Attestation Provider named *pshtest*.</span></span>

## <span data-ttu-id="a0cc8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0cc8-112">PARAMETERS</span></span>

### <span data-ttu-id="a0cc8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0cc8-113">-DefaultProfile</span></span>
<span data-ttu-id="a0cc8-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0cc8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0cc8-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a0cc8-115">-Name</span></span>
<span data-ttu-id="a0cc8-116">Gibt den Namen eines Nachweisanbieters an.</span><span class="sxs-lookup"><span data-stu-id="a0cc8-116">Specifies the name of an attestation provider.</span></span>

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

### <span data-ttu-id="a0cc8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0cc8-117">-ResourceGroupName</span></span>
<span data-ttu-id="a0cc8-118">Gibt den Ressourcengruppennamen eines Nachweisanbieters an.</span><span class="sxs-lookup"><span data-stu-id="a0cc8-118">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="a0cc8-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0cc8-119">-ResourceId</span></span>
<span data-ttu-id="a0cc8-120">Gibt die ResourceID eines Nachweisanbieters an.</span><span class="sxs-lookup"><span data-stu-id="a0cc8-120">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="a0cc8-121">-Signer</span><span class="sxs-lookup"><span data-stu-id="a0cc8-121">-Signer</span></span>
<span data-ttu-id="a0cc8-122">Gibt das RFC7519-JSON-Webtoken an, das einen Anspruch namens "maa-policyCertificate" enthält, dessen Wert ein RFC7517 JSON-Webschlüssel ist, der einen vertrauenswürdigen Signaturschlüssel enthält, den Sie entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="a0cc8-122">Specifies the RFC7519 JSON Web Token containing a claim named "maa-policyCertificate" whose value is an RFC7517 JSON Web Key which contains a trusted signing key to remove.</span></span>
<span data-ttu-id="a0cc8-123">Das RFC7519-JWT muss mit einem der vorhandenen vertrauenswürdigen Signaturschlüssel signiert sein.</span><span class="sxs-lookup"><span data-stu-id="a0cc8-123">The RFC7519 JWT must be signed with one of the existing trusted signing keys.</span></span>

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

### <span data-ttu-id="a0cc8-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0cc8-124">-Confirm</span></span>
<span data-ttu-id="a0cc8-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a0cc8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0cc8-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a0cc8-126">-WhatIf</span></span>
<span data-ttu-id="a0cc8-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a0cc8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0cc8-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a0cc8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0cc8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0cc8-129">CommonParameters</span></span>
<span data-ttu-id="a0cc8-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0cc8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0cc8-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0cc8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0cc8-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a0cc8-132">INPUTS</span></span>

### <span data-ttu-id="a0cc8-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a0cc8-133">System.String</span></span>

## <span data-ttu-id="a0cc8-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a0cc8-134">OUTPUTS</span></span>

### <span data-ttu-id="a0cc8-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span><span class="sxs-lookup"><span data-stu-id="a0cc8-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="a0cc8-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a0cc8-136">NOTES</span></span>

## <span data-ttu-id="a0cc8-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a0cc8-137">RELATED LINKS</span></span>
