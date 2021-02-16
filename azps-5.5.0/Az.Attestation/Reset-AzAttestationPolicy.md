---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/reset-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
ms.openlocfilehash: f4bf651fd6e5b84714ddb4511365bc0c17c49470
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168468"
---
# <span data-ttu-id="243bf-101">Reset-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="243bf-101">Reset-AzAttestationPolicy</span></span>

## <span data-ttu-id="243bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="243bf-102">SYNOPSIS</span></span>
<span data-ttu-id="243bf-103">Setzt die Richtlinie eines Mandanten in Azure Attestationn.} zurück.</span><span class="sxs-lookup"><span data-stu-id="243bf-103">Resets the policy from a tenant in Azure Attestationn.}</span></span>

## <span data-ttu-id="243bf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="243bf-104">SYNTAX</span></span>

### <span data-ttu-id="243bf-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="243bf-105">NameParameterSet</span></span>
```
Reset-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> [-Policy <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="243bf-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="243bf-106">ResourceIdParameterSet</span></span>
```
Reset-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-Policy <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="243bf-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="243bf-107">DESCRIPTION</span></span>
<span data-ttu-id="243bf-108">Das Reset-AzAttestationPolicy cmdlet setzt die benutzerdefinierte Nachweisrichtlinie von einem Mandanten in Azure Attestation zurück.</span><span class="sxs-lookup"><span data-stu-id="243bf-108">The Reset-AzAttestationPolicy cmdlet resets the user defined attestation policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="243bf-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="243bf-109">EXAMPLES</span></span>

### <span data-ttu-id="243bf-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="243bf-110">Example 1</span></span>
```powershell
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave
```

<span data-ttu-id="243bf-111">Setzen Sie die Richtlinie auf die Standardeinstellung für den *Nachweisanbieter-Pshtest* für Tee vom Typ *"SgxEnsche" zurück.*</span><span class="sxs-lookup"><span data-stu-id="243bf-111">Reset the policy to the default for the Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

### <span data-ttu-id="243bf-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="243bf-112">Example 2</span></span>
```powershell
PS C:\> $resetJwt = Get-Content -Path .\reset.policy.txt.signed.txt
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $resetJwt
```

<span data-ttu-id="243bf-113">Wenn der *Nachweisanbieter-Pshtest* für die Verwendung des isolierten Vertrauensmodells konfiguriert ist, setzen Sie die Richtlinie auf den Standardwert für *"SgxEn uhrse"* zurück, indem Sie eine signierte Richtlinie verwenden.</span><span class="sxs-lookup"><span data-stu-id="243bf-113">If the Attestation Provider *pshtest* is configured to use the isolated trust model, reset the policy to the default for Tee type *SgxEnclave* by including a signed policy.</span></span>

## <span data-ttu-id="243bf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="243bf-114">PARAMETERS</span></span>

### <span data-ttu-id="243bf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="243bf-115">-DefaultProfile</span></span>
<span data-ttu-id="243bf-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="243bf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="243bf-117">-Name</span><span class="sxs-lookup"><span data-stu-id="243bf-117">-Name</span></span>
<span data-ttu-id="243bf-118">Gibt einen Namen des Mandanten an.</span><span class="sxs-lookup"><span data-stu-id="243bf-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="243bf-119">Dieses Cmdlet setzt die Nachweisrichtlinie für den Mandanten zurück, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="243bf-119">This cmdlet resets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="243bf-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="243bf-120">-PassThru</span></span>
<span data-ttu-id="243bf-121">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="243bf-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="243bf-122">Wenn dieser Schalter angegeben ist, wird "true" zurückgegeben, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="243bf-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="243bf-123">-Policy</span><span class="sxs-lookup"><span data-stu-id="243bf-123">-Policy</span></span>
<span data-ttu-id="243bf-124">Gibt das JSON-Webtoken an, das das zurückzusetzende Richtliniendokument beschreibt.</span><span class="sxs-lookup"><span data-stu-id="243bf-124">Specifies the JSON Web Token describing the policy document to reset.</span></span>

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

### <span data-ttu-id="243bf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="243bf-125">-ResourceGroupName</span></span>
<span data-ttu-id="243bf-126">Gibt den Ressourcengruppennamen eines Nachweisanbieters an.</span><span class="sxs-lookup"><span data-stu-id="243bf-126">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="243bf-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="243bf-127">-ResourceId</span></span>
<span data-ttu-id="243bf-128">Gibt die ResourceID eines Nachweisanbieters an.</span><span class="sxs-lookup"><span data-stu-id="243bf-128">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="243bf-129">-Tee</span><span class="sxs-lookup"><span data-stu-id="243bf-129">-Tee</span></span>
<span data-ttu-id="243bf-130">Gibt einen Typ der vertrauenswürdigen Ausführungsumgebung an.</span><span class="sxs-lookup"><span data-stu-id="243bf-130">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="243bf-131">Wir unterstützen vier Umgebungstypen: SgxEncomponene, OpenEnsdatum, CyResComponent und VBSEnsdatume.</span><span class="sxs-lookup"><span data-stu-id="243bf-131">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="243bf-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="243bf-132">-Confirm</span></span>
<span data-ttu-id="243bf-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="243bf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="243bf-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="243bf-134">-WhatIf</span></span>
<span data-ttu-id="243bf-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="243bf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="243bf-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="243bf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="243bf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="243bf-137">CommonParameters</span></span>
<span data-ttu-id="243bf-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="243bf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="243bf-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="243bf-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="243bf-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="243bf-140">INPUTS</span></span>

### <span data-ttu-id="243bf-141">System.String</span><span class="sxs-lookup"><span data-stu-id="243bf-141">System.String</span></span>

## <span data-ttu-id="243bf-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="243bf-142">OUTPUTS</span></span>

### <span data-ttu-id="243bf-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="243bf-143">System.Boolean</span></span>

## <span data-ttu-id="243bf-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="243bf-144">NOTES</span></span>

## <span data-ttu-id="243bf-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="243bf-145">RELATED LINKS</span></span>
