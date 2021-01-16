---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/reset-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
ms.openlocfilehash: f4bf651fd6e5b84714ddb4511365bc0c17c49470
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306648"
---
# <span data-ttu-id="b1107-101">Reset-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="b1107-101">Reset-AzAttestationPolicy</span></span>

## <span data-ttu-id="b1107-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1107-102">SYNOPSIS</span></span>
<span data-ttu-id="b1107-103">Setzt die Richtlinie eines Mandanten in Azure Attestationn.} zurück.</span><span class="sxs-lookup"><span data-stu-id="b1107-103">Resets the policy from a tenant in Azure Attestationn.}</span></span>

## <span data-ttu-id="b1107-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b1107-104">SYNTAX</span></span>

### <span data-ttu-id="b1107-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1107-105">NameParameterSet</span></span>
```
Reset-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> [-Policy <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1107-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1107-106">ResourceIdParameterSet</span></span>
```
Reset-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-Policy <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1107-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b1107-107">DESCRIPTION</span></span>
<span data-ttu-id="b1107-108">Das Reset-AzAttestationPolicy cmdlet setzt die benutzerdefinierte Nachweisrichtlinie von einem Mandanten in Azure Attestation zurück.</span><span class="sxs-lookup"><span data-stu-id="b1107-108">The Reset-AzAttestationPolicy cmdlet resets the user defined attestation policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="b1107-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b1107-109">EXAMPLES</span></span>

### <span data-ttu-id="b1107-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b1107-110">Example 1</span></span>
```powershell
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave
```

<span data-ttu-id="b1107-111">Setzen Sie die Richtlinie auf die Standardeinstellung für den *Nachweisanbieter-Pshtest* für Teetyp *"SgxEneuropäischen" zurück.*</span><span class="sxs-lookup"><span data-stu-id="b1107-111">Reset the policy to the default for the Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

### <span data-ttu-id="b1107-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b1107-112">Example 2</span></span>
```powershell
PS C:\> $resetJwt = Get-Content -Path .\reset.policy.txt.signed.txt
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $resetJwt
```

<span data-ttu-id="b1107-113">Wenn der *Nachweisanbieter-Pshtest* für die Verwendung des isolierten Vertrauensmodells konfiguriert ist, setzen Sie die Richtlinie auf den Standardwert für *"SgxEn uhrse"* zurück, indem Sie eine signierte Richtlinie verwenden.</span><span class="sxs-lookup"><span data-stu-id="b1107-113">If the Attestation Provider *pshtest* is configured to use the isolated trust model, reset the policy to the default for Tee type *SgxEnclave* by including a signed policy.</span></span>

## <span data-ttu-id="b1107-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1107-114">PARAMETERS</span></span>

### <span data-ttu-id="b1107-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1107-115">-DefaultProfile</span></span>
<span data-ttu-id="b1107-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b1107-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1107-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b1107-117">-Name</span></span>
<span data-ttu-id="b1107-118">Gibt einen Namen des Mandanten an.</span><span class="sxs-lookup"><span data-stu-id="b1107-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="b1107-119">Dieses Cmdlet setzt die Nachweisrichtlinie für den Mandanten zurück, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="b1107-119">This cmdlet resets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="b1107-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1107-120">-PassThru</span></span>
<span data-ttu-id="b1107-121">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="b1107-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="b1107-122">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="b1107-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="b1107-123">-Policy</span><span class="sxs-lookup"><span data-stu-id="b1107-123">-Policy</span></span>
<span data-ttu-id="b1107-124">Gibt das JSON-Webtoken an, das das zurückzusetzende Richtliniendokument beschreibt.</span><span class="sxs-lookup"><span data-stu-id="b1107-124">Specifies the JSON Web Token describing the policy document to reset.</span></span>

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

### <span data-ttu-id="b1107-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1107-125">-ResourceGroupName</span></span>
<span data-ttu-id="b1107-126">Gibt den Ressourcengruppennamen eines Nachweisanbieters an.</span><span class="sxs-lookup"><span data-stu-id="b1107-126">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="b1107-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1107-127">-ResourceId</span></span>
<span data-ttu-id="b1107-128">Gibt die ResourceID eines Nachweisanbieters an.</span><span class="sxs-lookup"><span data-stu-id="b1107-128">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="b1107-129">-Tee</span><span class="sxs-lookup"><span data-stu-id="b1107-129">-Tee</span></span>
<span data-ttu-id="b1107-130">Gibt einen Typ der vertrauenswürdigen Ausführungsumgebung an.</span><span class="sxs-lookup"><span data-stu-id="b1107-130">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="b1107-131">Wir unterstützen vier Umgebungstypen: SgxEncomponene, OpenEnsdatum, CyResComponent und VBSEnsdatume.</span><span class="sxs-lookup"><span data-stu-id="b1107-131">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="b1107-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1107-132">-Confirm</span></span>
<span data-ttu-id="b1107-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b1107-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1107-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b1107-134">-WhatIf</span></span>
<span data-ttu-id="b1107-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b1107-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1107-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b1107-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1107-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1107-137">CommonParameters</span></span>
<span data-ttu-id="b1107-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1107-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1107-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1107-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1107-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b1107-140">INPUTS</span></span>

### <span data-ttu-id="b1107-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b1107-141">System.String</span></span>

## <span data-ttu-id="b1107-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b1107-142">OUTPUTS</span></span>

### <span data-ttu-id="b1107-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b1107-143">System.Boolean</span></span>

## <span data-ttu-id="b1107-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b1107-144">NOTES</span></span>

## <span data-ttu-id="b1107-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b1107-145">RELATED LINKS</span></span>
