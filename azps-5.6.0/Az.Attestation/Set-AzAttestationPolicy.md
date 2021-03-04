---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/set-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
ms.openlocfilehash: c32a9e2fd474578c8526c8352e8649cb84d8b016
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926008"
---
# <span data-ttu-id="75b59-101">Set-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="75b59-101">Set-AzAttestationPolicy</span></span>

## <span data-ttu-id="75b59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75b59-102">SYNOPSIS</span></span>
<span data-ttu-id="75b59-103">Legt die Richtlinie aus einem Mandanten in Azure Attestationn fest.</span><span class="sxs-lookup"><span data-stu-id="75b59-103">Sets the policy from a tenant in Azure Attestationn.</span></span>

## <span data-ttu-id="75b59-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75b59-104">SYNTAX</span></span>

### <span data-ttu-id="75b59-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="75b59-105">NameParameterSet</span></span>
```
Set-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> -Policy <String>
 [-PolicyFormat <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75b59-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75b59-106">ResourceIdParameterSet</span></span>
```
Set-AzAttestationPolicy [-ResourceId] <String> -Tee <String> -Policy <String> [-PolicyFormat <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75b59-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="75b59-107">DESCRIPTION</span></span>
<span data-ttu-id="75b59-108">Das Set-AzAttestationPolicy-Cmdlet legt die Richtlinie von einem Mandanten in Azure Attestation fest.</span><span class="sxs-lookup"><span data-stu-id="75b59-108">The Set-AzAttestationPolicy cmdlet sets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="75b59-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="75b59-109">EXAMPLES</span></span>

### <span data-ttu-id="75b59-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="75b59-110">Example 1</span></span>
```powershell
PS C:\> $policy = Get-Content -Path .\custom.sgx.policy.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policy
```

<span data-ttu-id="75b59-111">Legt die benutzerdefinierte Richtlinie für den TEE-Typ *SgxEnclave* für Attestation Provider *pshtest* mithilfe eines Textrichtlinienformats (Standard) fest.</span><span class="sxs-lookup"><span data-stu-id="75b59-111">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a text policy format (default).</span></span>

### <span data-ttu-id="75b59-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="75b59-112">Example 2</span></span>
```powershell
PS C:\> $policyjwt = Get-Content -Path .\custom.sgx.policy.jwt.format.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policyjwt -PolicyFormat JWT
```

<span data-ttu-id="75b59-113">Legt die benutzerdefinierte Richtlinie für den TEE-Typ *SgxEnclave* für Attestation Provider *pshtest* mithilfe eines JWT-Richtlinienformats fest.</span><span class="sxs-lookup"><span data-stu-id="75b59-113">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a JWT policy format.</span></span>

## <span data-ttu-id="75b59-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="75b59-114">PARAMETERS</span></span>

### <span data-ttu-id="75b59-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75b59-115">-DefaultProfile</span></span>
<span data-ttu-id="75b59-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="75b59-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75b59-117">-Name</span><span class="sxs-lookup"><span data-stu-id="75b59-117">-Name</span></span>
<span data-ttu-id="75b59-118">Gibt einen Namen des Mandanten an.</span><span class="sxs-lookup"><span data-stu-id="75b59-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="75b59-119">Dieses Cmdlet legt die Bestätigungsrichtlinie für den Mandanten fest, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="75b59-119">This cmdlet sets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="75b59-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75b59-120">-PassThru</span></span>
<span data-ttu-id="75b59-121">Dieses Cmdlet gibt standardmäßig kein -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="75b59-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="75b59-122">Wenn dieser Schalter angegeben ist, gibt er "true" zurück, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="75b59-122">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b59-123">-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="75b59-123">-Policy</span></span>
<span data-ttu-id="75b59-124">Gibt das zu erstellende Richtliniendokument an.</span><span class="sxs-lookup"><span data-stu-id="75b59-124">Specifies the policy document to set.</span></span>  <span data-ttu-id="75b59-125">Das Richtlinienformat kann entweder Text oder JSON Web Token (JWT) sein.</span><span class="sxs-lookup"><span data-stu-id="75b59-125">The policy format can be either Text or JSON Web Token (JWT).</span></span>

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

### <span data-ttu-id="75b59-126">-PolicyFormat</span><span class="sxs-lookup"><span data-stu-id="75b59-126">-PolicyFormat</span></span>
<span data-ttu-id="75b59-127">Gibt das Format für die Richtlinie an, entweder Text oder JWT (JSON Web Token).</span><span class="sxs-lookup"><span data-stu-id="75b59-127">Specifies the format for the policy, either Text or JWT (JSON Web Token).</span></span>  <span data-ttu-id="75b59-128">Das Standardrichtlinienformat ist Text.</span><span class="sxs-lookup"><span data-stu-id="75b59-128">The default policy format is Text.</span></span>

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

### <span data-ttu-id="75b59-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75b59-129">-ResourceGroupName</span></span>
<span data-ttu-id="75b59-130">Gibt den Ressourcengruppennamen eines Bescheinigungsanbieters an.</span><span class="sxs-lookup"><span data-stu-id="75b59-130">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="75b59-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75b59-131">-ResourceId</span></span>
<span data-ttu-id="75b59-132">Gibt die ResourceID eines Bescheinigungsanbieters an.</span><span class="sxs-lookup"><span data-stu-id="75b59-132">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="75b59-133">-Tee</span><span class="sxs-lookup"><span data-stu-id="75b59-133">-Tee</span></span>
<span data-ttu-id="75b59-134">Gibt einen Typ der vertrauenswürdigen Ausführungsumgebung an.</span><span class="sxs-lookup"><span data-stu-id="75b59-134">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="75b59-135">Vier Arten von Umgebung werden unterstützt: SgxEnclave, OpenEnclave, CyResComponent und VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="75b59-135">Four types of environment are supported: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="75b59-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="75b59-136">-Confirm</span></span>
<span data-ttu-id="75b59-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="75b59-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75b59-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75b59-138">-WhatIf</span></span>
<span data-ttu-id="75b59-139">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="75b59-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75b59-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="75b59-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75b59-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75b59-141">CommonParameters</span></span>
<span data-ttu-id="75b59-142">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75b59-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75b59-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75b59-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75b59-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="75b59-144">INPUTS</span></span>

### <span data-ttu-id="75b59-145">System.String</span><span class="sxs-lookup"><span data-stu-id="75b59-145">System.String</span></span>

## <span data-ttu-id="75b59-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="75b59-146">OUTPUTS</span></span>

### <span data-ttu-id="75b59-147">System.String</span><span class="sxs-lookup"><span data-stu-id="75b59-147">System.String</span></span>

## <span data-ttu-id="75b59-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="75b59-148">NOTES</span></span>

## <span data-ttu-id="75b59-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="75b59-149">RELATED LINKS</span></span>
