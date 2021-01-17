---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/add-azattestationpolicysigner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Add-AzAttestationPolicySigner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Add-AzAttestationPolicySigner.md
ms.openlocfilehash: 5a1c4638d75a916f77ee4cb526eab7a8e3c126bf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381197"
---
# <span data-ttu-id="0dd77-101">Add-AzAttestationPolicySigner</span><span class="sxs-lookup"><span data-stu-id="0dd77-101">Add-AzAttestationPolicySigner</span></span>

## <span data-ttu-id="0dd77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0dd77-102">SYNOPSIS</span></span>
<span data-ttu-id="0dd77-103">Fügt einen vertrauenswürdigen Richtlinien signierten Mandanten in Azure Attestation hinzu.</span><span class="sxs-lookup"><span data-stu-id="0dd77-103">Adds a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="0dd77-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0dd77-104">SYNTAX</span></span>

### <span data-ttu-id="0dd77-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dd77-105">NameParameterSet</span></span>
```
Add-AzAttestationPolicySigner [-Name] <String> [-ResourceGroupName] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dd77-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dd77-106">ResourceIdParameterSet</span></span>
```
Add-AzAttestationPolicySigner [-ResourceId] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0dd77-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0dd77-107">DESCRIPTION</span></span>
<span data-ttu-id="0dd77-108">Das Add-AzAttestationPolicySigner cmdlet fügt einen vertrauenswürdigen Richtlinien signer für einen Mandanten in Azure Attestation hinzu.</span><span class="sxs-lookup"><span data-stu-id="0dd77-108">The Add-AzAttestationPolicySigner cmdlet adds a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="0dd77-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0dd77-109">EXAMPLES</span></span>

### <span data-ttu-id="0dd77-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0dd77-110">Example 1</span></span>
```powershell
PS C:\> $trustedSigner = Get-Content -Path .\trusted.signer.txt
PS C:\> Add-AzAttestationPolicySigner -Name pshtest -ResourceGroupName psh-test-rg -Signer $trustedSigner
```

<span data-ttu-id="0dd77-111">Fügen Sie einen vertrauenswürdigen Signer für den Atteestation-Anbieter namens *"pshtest" hinzu.*</span><span class="sxs-lookup"><span data-stu-id="0dd77-111">Add a trusted signer for the Atteestation Provider named *pshtest*.</span></span>

## <span data-ttu-id="0dd77-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0dd77-112">PARAMETERS</span></span>

### <span data-ttu-id="0dd77-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dd77-113">-DefaultProfile</span></span>
<span data-ttu-id="0dd77-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0dd77-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0dd77-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0dd77-115">-Name</span></span>
<span data-ttu-id="0dd77-116">Gibt den Namen eines Nachweisanbieters an.</span><span class="sxs-lookup"><span data-stu-id="0dd77-116">Specifies the name of an attestation provider.</span></span>

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

### <span data-ttu-id="0dd77-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dd77-117">-ResourceGroupName</span></span>
<span data-ttu-id="0dd77-118">Gibt den Ressourcengruppennamen eines Nachweisanbieters an.</span><span class="sxs-lookup"><span data-stu-id="0dd77-118">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="0dd77-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0dd77-119">-ResourceId</span></span>
<span data-ttu-id="0dd77-120">Gibt die ResourceID eines Nachweisanbieters an.</span><span class="sxs-lookup"><span data-stu-id="0dd77-120">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="0dd77-121">-Signer</span><span class="sxs-lookup"><span data-stu-id="0dd77-121">-Signer</span></span>
<span data-ttu-id="0dd77-122">Gibt das RFC7519-JSON-Webtoken an, das einen Anspruch namens "maa-policyCertificate" enthält, dessen Wert ein RFC7517 JSON-Webschlüssel ist, der einen neuen vertrauenswürdigen Signaturschlüssel enthält, den Sie hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="0dd77-122">Specifies the RFC7519 JSON Web Token containing a claim named "maa-policyCertificate" whose value is an RFC7517 JSON Web Key which contains a new trusted signing key to add.</span></span>
<span data-ttu-id="0dd77-123">Das RFC7519-JWT muss mit einem der vorhandenen vertrauenswürdigen Signaturschlüssel signiert sein.</span><span class="sxs-lookup"><span data-stu-id="0dd77-123">The RFC7519 JWT must be signed with one of the existing trusted signing keys.</span></span>

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

### <span data-ttu-id="0dd77-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0dd77-124">-Confirm</span></span>
<span data-ttu-id="0dd77-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0dd77-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0dd77-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0dd77-126">-WhatIf</span></span>
<span data-ttu-id="0dd77-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0dd77-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0dd77-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0dd77-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0dd77-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dd77-129">CommonParameters</span></span>
<span data-ttu-id="0dd77-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dd77-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dd77-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0dd77-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dd77-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0dd77-132">INPUTS</span></span>

### <span data-ttu-id="0dd77-133">System.String</span><span class="sxs-lookup"><span data-stu-id="0dd77-133">System.String</span></span>

## <span data-ttu-id="0dd77-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0dd77-134">OUTPUTS</span></span>

### <span data-ttu-id="0dd77-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span><span class="sxs-lookup"><span data-stu-id="0dd77-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="0dd77-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0dd77-136">NOTES</span></span>

## <span data-ttu-id="0dd77-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0dd77-137">RELATED LINKS</span></span>
