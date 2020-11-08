---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/add-azattestationpolicysigner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Add-AzAttestationPolicySigner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Add-AzAttestationPolicySigner.md
ms.openlocfilehash: df46bc097ce4a1a52c486bb0e418bce656f0f476
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997444"
---
# <span data-ttu-id="00aab-101">Add-AzAttestationPolicySigner</span><span class="sxs-lookup"><span data-stu-id="00aab-101">Add-AzAttestationPolicySigner</span></span>

## <span data-ttu-id="00aab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="00aab-102">SYNOPSIS</span></span>
<span data-ttu-id="00aab-103">Fügt einen vertrauenswürdigen Richtlinien Signaturgeber für einen Mandanten in Azure-Bescheinigung hinzu.</span><span class="sxs-lookup"><span data-stu-id="00aab-103">Adds a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="00aab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="00aab-104">SYNTAX</span></span>

### <span data-ttu-id="00aab-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="00aab-105">NameParameterSet</span></span>
```
Add-AzAttestationPolicySigner [-Name] <String> [-ResourceGroupName] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00aab-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="00aab-106">ResourceIdParameterSet</span></span>
```
Add-AzAttestationPolicySigner [-ResourceId] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00aab-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="00aab-107">DESCRIPTION</span></span>
<span data-ttu-id="00aab-108">Das Add-AzAttestationPolicySigner-Cmdlet fügt einen vertrauenswürdigen Richtlinien Signaturgeber für einen Mandanten in Azure-Bescheinigung hinzu.</span><span class="sxs-lookup"><span data-stu-id="00aab-108">The Add-AzAttestationPolicySigner cmdlet adds a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="00aab-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="00aab-109">EXAMPLES</span></span>

### <span data-ttu-id="00aab-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="00aab-110">Example 1</span></span>
```powershell
PS C:\> $trustedSigner = Get-Content -Path .\trusted.signer.txt
PS C:\> Add-AzAttestationPolicySigner -Name pshtest -ResourceGroupName psh-test-rg -Signer $trustedSigner
```

<span data-ttu-id="00aab-111">Hinzufügen eines vertrauenswürdigen Unterzeichners für den Atteestation-Anbieter mit dem Namen *pshtest*.</span><span class="sxs-lookup"><span data-stu-id="00aab-111">Add a trusted signer for the Atteestation Provider named *pshtest*.</span></span>

## <span data-ttu-id="00aab-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="00aab-112">PARAMETERS</span></span>

### <span data-ttu-id="00aab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00aab-113">-DefaultProfile</span></span>
<span data-ttu-id="00aab-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="00aab-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00aab-115">-Name</span><span class="sxs-lookup"><span data-stu-id="00aab-115">-Name</span></span>
<span data-ttu-id="00aab-116">Gibt den Namen eines Bescheinigungs Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="00aab-116">Specifies the name of an attestation provider.</span></span>

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

### <span data-ttu-id="00aab-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00aab-117">-ResourceGroupName</span></span>
<span data-ttu-id="00aab-118">Gibt den Namen der Ressourcengruppe eines Bescheinigungs Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="00aab-118">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="00aab-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="00aab-119">-ResourceId</span></span>
<span data-ttu-id="00aab-120">Gibt die Resourcen-Nr eines Bescheinigungs Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="00aab-120">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="00aab-121">-Signer</span><span class="sxs-lookup"><span data-stu-id="00aab-121">-Signer</span></span>
<span data-ttu-id="00aab-122">Gibt das RFC7519-JSON-webtoken an, das einen Anspruch mit dem Namen "AAS-policyCertificate" enthält, dessen Wert ein RFC7517 JSON-Webschlüssel mit einem neuen vertrauenswürdigen Signaturschlüssel ist, der hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="00aab-122">Specifies the RFC7519 JSON Web Token containing a claim named "aas-policyCertificate" whose value is an RFC7517 JSON Web Key which contains a new trusted signing key to add.</span></span>
<span data-ttu-id="00aab-123">Das RFC7519-JWT muss mit einem der vorhandenen vertrauenswürdigen Signaturschlüssel signiert sein.</span><span class="sxs-lookup"><span data-stu-id="00aab-123">The RFC7519 JWT must be signed with one of the existing trusted signing keys.</span></span>

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

### <span data-ttu-id="00aab-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="00aab-124">-Confirm</span></span>
<span data-ttu-id="00aab-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="00aab-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00aab-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00aab-126">-WhatIf</span></span>
<span data-ttu-id="00aab-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="00aab-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00aab-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="00aab-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00aab-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00aab-129">CommonParameters</span></span>
<span data-ttu-id="00aab-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00aab-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00aab-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00aab-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00aab-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="00aab-132">INPUTS</span></span>

### <span data-ttu-id="00aab-133">System. String</span><span class="sxs-lookup"><span data-stu-id="00aab-133">System.String</span></span>

## <span data-ttu-id="00aab-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="00aab-134">OUTPUTS</span></span>

### <span data-ttu-id="00aab-135">Microsoft. Azure. Commands. Testat. Models. PSPolicySigners</span><span class="sxs-lookup"><span data-stu-id="00aab-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="00aab-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="00aab-136">NOTES</span></span>

## <span data-ttu-id="00aab-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="00aab-137">RELATED LINKS</span></span>
