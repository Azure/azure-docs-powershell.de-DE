---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestationpolicysigner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestationPolicySigner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestationPolicySigner.md
ms.openlocfilehash: fdd62a78b9d75ef222dc9f41f2c791afadfad9b4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008724"
---
# <span data-ttu-id="f13db-101">Remove-AzAttestationPolicySigner</span><span class="sxs-lookup"><span data-stu-id="f13db-101">Remove-AzAttestationPolicySigner</span></span>

## <span data-ttu-id="f13db-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f13db-102">SYNOPSIS</span></span>
<span data-ttu-id="f13db-103">Entfernt einen vertrauenswürdigen Richtlinien Signaturgeber für einen Mandanten in Azure-Bescheinigung.</span><span class="sxs-lookup"><span data-stu-id="f13db-103">Removes a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="f13db-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f13db-104">SYNTAX</span></span>

### <span data-ttu-id="f13db-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f13db-105">NameParameterSet</span></span>
```
Remove-AzAttestationPolicySigner [-Name] <String> [-ResourceGroupName] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f13db-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f13db-106">ResourceIdParameterSet</span></span>
```
Remove-AzAttestationPolicySigner [-ResourceId] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f13db-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f13db-107">DESCRIPTION</span></span>
<span data-ttu-id="f13db-108">Das Remove-AzAttestationPolicySigner-Cmdlet entfernt einen vertrauenswürdigen Richtlinien Signaturgeber für einen Mandanten in Azure-Bescheinigung.</span><span class="sxs-lookup"><span data-stu-id="f13db-108">The Remove-AzAttestationPolicySigner cmdlet removes a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="f13db-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f13db-109">EXAMPLES</span></span>

### <span data-ttu-id="f13db-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f13db-110">Example 1</span></span>
```powershell
PS C:\> $trustedSigner = Get-Content -Path .\trusted.signer.txt
PS C:\> Remove-AzAttestationPolicySigner -Name pshtest -ResourceGroupName psh-test-rg -Signer $trustedSigner
```

<span data-ttu-id="f13db-111">Entfernen Sie einen vertrauenswürdigen Unterzeichner für den Bescheinigungs Anbieternamens *pshtest*.</span><span class="sxs-lookup"><span data-stu-id="f13db-111">Remove a trusted signer for the Attestation Provider named *pshtest*.</span></span>

## <span data-ttu-id="f13db-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f13db-112">PARAMETERS</span></span>

### <span data-ttu-id="f13db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f13db-113">-DefaultProfile</span></span>
<span data-ttu-id="f13db-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f13db-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f13db-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f13db-115">-Name</span></span>
<span data-ttu-id="f13db-116">Gibt den Namen eines Bescheinigungs Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="f13db-116">Specifies the name of an attestation provider.</span></span>

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

### <span data-ttu-id="f13db-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f13db-117">-ResourceGroupName</span></span>
<span data-ttu-id="f13db-118">Gibt den Namen der Ressourcengruppe eines Bescheinigungs Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="f13db-118">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="f13db-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f13db-119">-ResourceId</span></span>
<span data-ttu-id="f13db-120">Gibt die Resourcen-Nr eines Bescheinigungs Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="f13db-120">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="f13db-121">-Signer</span><span class="sxs-lookup"><span data-stu-id="f13db-121">-Signer</span></span>
<span data-ttu-id="f13db-122">Gibt das RFC7519-JSON-webtoken an, das einen Anspruch mit dem Namen "Maa-policyCertificate" enthält, dessen Wert ein RFC7517 JSON-Webschlüssel mit einem vertrauenswürdigen Signaturschlüssel ist, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f13db-122">Specifies the RFC7519 JSON Web Token containing a claim named "maa-policyCertificate" whose value is an RFC7517 JSON Web Key which contains a trusted signing key to remove.</span></span>
<span data-ttu-id="f13db-123">Das RFC7519-JWT muss mit einem der vorhandenen vertrauenswürdigen Signaturschlüssel signiert sein.</span><span class="sxs-lookup"><span data-stu-id="f13db-123">The RFC7519 JWT must be signed with one of the existing trusted signing keys.</span></span>

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

### <span data-ttu-id="f13db-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f13db-124">-Confirm</span></span>
<span data-ttu-id="f13db-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f13db-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f13db-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f13db-126">-WhatIf</span></span>
<span data-ttu-id="f13db-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f13db-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f13db-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f13db-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f13db-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f13db-129">CommonParameters</span></span>
<span data-ttu-id="f13db-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f13db-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f13db-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f13db-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f13db-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f13db-132">INPUTS</span></span>

### <span data-ttu-id="f13db-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f13db-133">System.String</span></span>

## <span data-ttu-id="f13db-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f13db-134">OUTPUTS</span></span>

### <span data-ttu-id="f13db-135">Microsoft. Azure. Commands. Testat. Models. PSPolicySigners</span><span class="sxs-lookup"><span data-stu-id="f13db-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="f13db-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="f13db-136">NOTES</span></span>

## <span data-ttu-id="f13db-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f13db-137">RELATED LINKS</span></span>
