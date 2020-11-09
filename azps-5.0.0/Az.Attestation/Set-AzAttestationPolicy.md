---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/set-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
ms.openlocfilehash: c5659dc2234e6305f07de0a2990c76cbc9cd183a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299829"
---
# <span data-ttu-id="08545-101">Set-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="08545-101">Set-AzAttestationPolicy</span></span>

## <span data-ttu-id="08545-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="08545-102">SYNOPSIS</span></span>
<span data-ttu-id="08545-103">Legt die Richtlinie von einem Mandanten in Azure Attestationn.</span><span class="sxs-lookup"><span data-stu-id="08545-103">Sets the policy from a tenant in Azure Attestationn.</span></span>

## <span data-ttu-id="08545-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="08545-104">SYNTAX</span></span>

### <span data-ttu-id="08545-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="08545-105">NameParameterSet</span></span>
```
Set-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> -Policy <String>
 [-PolicyFormat <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="08545-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="08545-106">ResourceIdParameterSet</span></span>
```
Set-AzAttestationPolicy [-ResourceId] <String> -Tee <String> -Policy <String> [-PolicyFormat <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08545-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08545-107">DESCRIPTION</span></span>
<span data-ttu-id="08545-108">Das Set-AzAttestationPolicy-Cmdlet legt die Richtlinie von einem Mandanten in Azure-Bescheinigung fest.</span><span class="sxs-lookup"><span data-stu-id="08545-108">The Set-AzAttestationPolicy cmdlet sets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="08545-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08545-109">EXAMPLES</span></span>

### <span data-ttu-id="08545-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="08545-110">Example 1</span></span>
```powershell
PS C:\> $policy = Get-Content -Path .\custom.sgx.policy.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policy
```

<span data-ttu-id="08545-111">Legt die benutzerdefinierte Richtlinie für Tee-Typ *SgxEnclave* für Bescheinigungs Anbieter- *pshtest* mithilfe eines Text Richtlinien Formats fest (Standard).</span><span class="sxs-lookup"><span data-stu-id="08545-111">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a text policy format (default).</span></span>

### <span data-ttu-id="08545-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="08545-112">Example 2</span></span>
```powershell
PS C:\> $policyjwt = Get-Content -Path .\custom.sgx.policy.jwt.format.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policyjwt -PolicyFormat JWT
```

<span data-ttu-id="08545-113">Legt die benutzerdefinierte Richtlinie für Tee-Typ *SgxEnclave* für Bescheinigungs Anbieter- *pshtest* mit einem JWT-Richtlinienformat fest.</span><span class="sxs-lookup"><span data-stu-id="08545-113">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a JWT policy format.</span></span>

## <span data-ttu-id="08545-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="08545-114">PARAMETERS</span></span>

### <span data-ttu-id="08545-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08545-115">-DefaultProfile</span></span>
<span data-ttu-id="08545-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="08545-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08545-117">-Name</span><span class="sxs-lookup"><span data-stu-id="08545-117">-Name</span></span>
<span data-ttu-id="08545-118">Gibt den Namen des Mandanten an.</span><span class="sxs-lookup"><span data-stu-id="08545-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="08545-119">Dieses Cmdlet legt die Richtlinie für den Mandanten fest, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="08545-119">This cmdlet sets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="08545-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08545-120">-PassThru</span></span>
<span data-ttu-id="08545-121">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="08545-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="08545-122">Wenn dieser Schalter angegeben wird, wird true zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="08545-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="08545-123">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="08545-123">-Policy</span></span>
<span data-ttu-id="08545-124">Gibt das festzulegende Richtliniendokument an.</span><span class="sxs-lookup"><span data-stu-id="08545-124">Specifies the policy document to set.</span></span>  <span data-ttu-id="08545-125">Das Richtlinienformat kann entweder Text oder JSON Web Token (JWT) sein.</span><span class="sxs-lookup"><span data-stu-id="08545-125">The policy format can be either Text or JSON Web Token (JWT).</span></span>

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

### <span data-ttu-id="08545-126">-PolicyFormat</span><span class="sxs-lookup"><span data-stu-id="08545-126">-PolicyFormat</span></span>
<span data-ttu-id="08545-127">Gibt das Format für die Richtlinie an, entweder Text oder JWT (JSON Web Token).</span><span class="sxs-lookup"><span data-stu-id="08545-127">Specifies the format for the policy, either Text or JWT (JSON Web Token).</span></span>  <span data-ttu-id="08545-128">Das standardmäßige Richtlinienformat ist "Text".</span><span class="sxs-lookup"><span data-stu-id="08545-128">The default policy format is Text.</span></span>

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

### <span data-ttu-id="08545-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08545-129">-ResourceGroupName</span></span>
<span data-ttu-id="08545-130">Gibt den Namen der Ressourcengruppe eines Bescheinigungs Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="08545-130">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="08545-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="08545-131">-ResourceId</span></span>
<span data-ttu-id="08545-132">Gibt die Resourcen-Nr eines Bescheinigungs Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="08545-132">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="08545-133">-Tee</span><span class="sxs-lookup"><span data-stu-id="08545-133">-Tee</span></span>
<span data-ttu-id="08545-134">Gibt einen Typ einer vertrauenswürdigen Ausführungsumgebung an.</span><span class="sxs-lookup"><span data-stu-id="08545-134">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="08545-135">Es werden vier Arten von Umgebungen unterstützt: SgxEnclave, openenklave, CyResComponent und VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="08545-135">Four types of environment are supported: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="08545-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="08545-136">-Confirm</span></span>
<span data-ttu-id="08545-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="08545-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08545-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08545-138">-WhatIf</span></span>
<span data-ttu-id="08545-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="08545-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08545-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="08545-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08545-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08545-141">CommonParameters</span></span>
<span data-ttu-id="08545-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08545-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08545-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08545-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08545-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="08545-144">INPUTS</span></span>

### <span data-ttu-id="08545-145">System. String</span><span class="sxs-lookup"><span data-stu-id="08545-145">System.String</span></span>

## <span data-ttu-id="08545-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="08545-146">OUTPUTS</span></span>

### <span data-ttu-id="08545-147">System. String</span><span class="sxs-lookup"><span data-stu-id="08545-147">System.String</span></span>

## <span data-ttu-id="08545-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="08545-148">NOTES</span></span>

## <span data-ttu-id="08545-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="08545-149">RELATED LINKS</span></span>
