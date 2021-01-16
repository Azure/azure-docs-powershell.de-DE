---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/set-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
ms.openlocfilehash: c5659dc2234e6305f07de0a2990c76cbc9cd183a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306640"
---
# <span data-ttu-id="ca052-101">Set-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="ca052-101">Set-AzAttestationPolicy</span></span>

## <span data-ttu-id="ca052-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca052-102">SYNOPSIS</span></span>
<span data-ttu-id="ca052-103">Legt die Richtlinie eines Mandanten in Azure Attestationn fest.</span><span class="sxs-lookup"><span data-stu-id="ca052-103">Sets the policy from a tenant in Azure Attestationn.</span></span>

## <span data-ttu-id="ca052-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca052-104">SYNTAX</span></span>

### <span data-ttu-id="ca052-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca052-105">NameParameterSet</span></span>
```
Set-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> -Policy <String>
 [-PolicyFormat <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca052-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca052-106">ResourceIdParameterSet</span></span>
```
Set-AzAttestationPolicy [-ResourceId] <String> -Tee <String> -Policy <String> [-PolicyFormat <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca052-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ca052-107">DESCRIPTION</span></span>
<span data-ttu-id="ca052-108">Das Set-AzAttestationPolicy cmdlet legt die Richtlinie von einem Mandanten in Azure Attestation fest.</span><span class="sxs-lookup"><span data-stu-id="ca052-108">The Set-AzAttestationPolicy cmdlet sets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="ca052-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ca052-109">EXAMPLES</span></span>

### <span data-ttu-id="ca052-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ca052-110">Example 1</span></span>
```powershell
PS C:\> $policy = Get-Content -Path .\custom.sgx.policy.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policy
```

<span data-ttu-id="ca052-111">Legt die benutzerdefinierte Richtlinie für den TEE-Typ *"SgxEnzente* for Attestation Provider *pshtest"* mit einem Textrichtlinienformat (Standard) fest.</span><span class="sxs-lookup"><span data-stu-id="ca052-111">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a text policy format (default).</span></span>

### <span data-ttu-id="ca052-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ca052-112">Example 2</span></span>
```powershell
PS C:\> $policyjwt = Get-Content -Path .\custom.sgx.policy.jwt.format.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policyjwt -PolicyFormat JWT
```

<span data-ttu-id="ca052-113">Legt die benutzerdefinierte Richtlinie für den TEE-Typ *"SgxEnffee* for Attestation Provider *pshtest"* mithilfe eines JWT-Richtlinienformats fest.</span><span class="sxs-lookup"><span data-stu-id="ca052-113">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a JWT policy format.</span></span>

## <span data-ttu-id="ca052-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca052-114">PARAMETERS</span></span>

### <span data-ttu-id="ca052-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca052-115">-DefaultProfile</span></span>
<span data-ttu-id="ca052-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ca052-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca052-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ca052-117">-Name</span></span>
<span data-ttu-id="ca052-118">Gibt einen Namen des Mandanten an.</span><span class="sxs-lookup"><span data-stu-id="ca052-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="ca052-119">Dieses Cmdlet legt die Nachweisrichtlinie für den Mandanten fest, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ca052-119">This cmdlet sets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="ca052-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca052-120">-PassThru</span></span>
<span data-ttu-id="ca052-121">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="ca052-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="ca052-122">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="ca052-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="ca052-123">-Policy</span><span class="sxs-lookup"><span data-stu-id="ca052-123">-Policy</span></span>
<span data-ttu-id="ca052-124">Gibt das fest zu setzende Richtliniendokument an.</span><span class="sxs-lookup"><span data-stu-id="ca052-124">Specifies the policy document to set.</span></span>  <span data-ttu-id="ca052-125">Das Richtlinienformat kann Text oder JSON Web Token (JWT) sein.</span><span class="sxs-lookup"><span data-stu-id="ca052-125">The policy format can be either Text or JSON Web Token (JWT).</span></span>

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

### <span data-ttu-id="ca052-126">-PolicyFormat</span><span class="sxs-lookup"><span data-stu-id="ca052-126">-PolicyFormat</span></span>
<span data-ttu-id="ca052-127">Gibt das Format für die Richtlinie an, entweder Text oder JWT (JSON-Webtoken).</span><span class="sxs-lookup"><span data-stu-id="ca052-127">Specifies the format for the policy, either Text or JWT (JSON Web Token).</span></span>  <span data-ttu-id="ca052-128">Das Standardrichtlinienformat ist "Text".</span><span class="sxs-lookup"><span data-stu-id="ca052-128">The default policy format is Text.</span></span>

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

### <span data-ttu-id="ca052-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca052-129">-ResourceGroupName</span></span>
<span data-ttu-id="ca052-130">Gibt den Ressourcengruppennamen eines Nachweisanbieters an.</span><span class="sxs-lookup"><span data-stu-id="ca052-130">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="ca052-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca052-131">-ResourceId</span></span>
<span data-ttu-id="ca052-132">Gibt die ResourceID eines Nachweisanbieters an.</span><span class="sxs-lookup"><span data-stu-id="ca052-132">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="ca052-133">-Tee</span><span class="sxs-lookup"><span data-stu-id="ca052-133">-Tee</span></span>
<span data-ttu-id="ca052-134">Gibt einen Typ der vertrauenswürdigen Ausführungsumgebung an.</span><span class="sxs-lookup"><span data-stu-id="ca052-134">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="ca052-135">Es werden vier Umgebungstypen unterstützt: SgxEncomponene, OpenEnsdatum, CyResComponent und VBSEnsdatume.</span><span class="sxs-lookup"><span data-stu-id="ca052-135">Four types of environment are supported: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="ca052-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca052-136">-Confirm</span></span>
<span data-ttu-id="ca052-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ca052-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca052-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ca052-138">-WhatIf</span></span>
<span data-ttu-id="ca052-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ca052-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca052-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ca052-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca052-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca052-141">CommonParameters</span></span>
<span data-ttu-id="ca052-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca052-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca052-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca052-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca052-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ca052-144">INPUTS</span></span>

### <span data-ttu-id="ca052-145">System.String</span><span class="sxs-lookup"><span data-stu-id="ca052-145">System.String</span></span>

## <span data-ttu-id="ca052-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ca052-146">OUTPUTS</span></span>

### <span data-ttu-id="ca052-147">System.String</span><span class="sxs-lookup"><span data-stu-id="ca052-147">System.String</span></span>

## <span data-ttu-id="ca052-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ca052-148">NOTES</span></span>

## <span data-ttu-id="ca052-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ca052-149">RELATED LINKS</span></span>
